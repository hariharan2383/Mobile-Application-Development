# Ex.No:8 To create a gallery control using android studio to display images or photos.


## AIM:

To create a gallery control using android studio to display images or photos.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
activity_main.xml :
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayoutxmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">
<ImageView
android:id="@+id/imageView"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginTop="36dp"
app:layout_constraintBottom_toTopOf="@+id/languagesGallery"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.413"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent"
tools:srcCompat="@tools:sample/avatars" />
<Gallery
android:id="@+id/languagesGallery"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_marginTop="171dp"
android:layout_marginBottom="204dp"
android:animationDuration="2000"
android:padding="10dp"
android:spacing="5dp"
android:unselectedAlpha="50"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toBottomOf="@+id/imageView" />
</androidx.constraintlayout.widget.ConstraintLayout>
MainActivity.java :
package com.example.gallerycontrol;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.Gallery;
import android.widget.ImageView;
public class MainActivity extends AppCompatActivity {
    Gallery simpleGallery;
CustomizedGalleryAdaptercustomGalleryAdapter;
ImageViewselectedImageView;
int[] images = {R.drawable.c,R.drawable.c_1,R.drawable.java,R.drawable.python,R.drawable.r,R.drawable.js};
    @Override
    protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
simpleGallery = (Gallery) findViewById(R.id.languagesGallery);
// get the reference of ImageView
selectedImageView = (ImageView) findViewById(R.id.imageView);
// initialize the adapter
customGalleryAdapter = new CustomizedGalleryAdapter(getApplicationContext(), images);
// set the adapter for gallery
simpleGallery.setAdapter(customGalleryAdapter);
// Let us do item click of gallery and image can be identified by its position
simpleGallery.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
// Whichever image is clicked, that is set in the selectedImageView
// position will indicate the location of image
selectedImageView.setImageResource(images[position]);
            }
        });
    }
}
CustomizedGalleryAdapter.java :
package com.example.gallerycontrol;
import android.content.Context;
import android.view.View;
import android.view.ViewGroup;
import android.widget.BaseAdapter;
import android.widget.Gallery;
import android.widget.ImageView;
public class CustomizedGalleryAdapter extends BaseAdapter {
    private Context context;
    private int[] images;
    public CustomizedGalleryAdapter(Context c, int[] images) {
        context = c;
this.images = images;
    }
    // returns the number of images, in our example it is 10
    public int getCount() {
        return images.length;
    }
    // returns the Item of an item, i.e. for our example we can get the image
    public Object getItem(int position) {
        return position;
    }
    // returns the ID of an item
    public long getItemId(int position) {
        return position;
    }
    // returns an ImageView view
    public View getView(int position, View convertView, ViewGroup parent) {
// position argument will indicate the location of image
// create a ImageView programmatically
ImageViewimageView = new ImageView(context);
// set image in ImageView
imageView.setImageResource(images[position]);
// set ImageView param
imageView.setLayoutParams(new Gallery.LayoutParams(200, 200));
        return imageView;
    }    }

/*
Program to print the text “GalleryControl”.
Developed by: Srihariharan S A
Registeration Number : 212221040160
*/
```

## OUTPUT
![image](https://github.com/hariharan2383/Mobile-Application-Development/assets/117346668/b85333a0-4d2d-4ebf-9120-674aa83cabc7)




## RESULT
Thus a Simple Android Application to create a gallery control using android studio to display images or photos is developed and executed successfully.


