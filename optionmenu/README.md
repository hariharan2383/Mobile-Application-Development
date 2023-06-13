# Ex.No:10 To create a option menu to display menu items.


## AIM:

To create a option menu to display menu items using Android Studio.

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
<TextView
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Hello World!"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
option.xml :
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">
<item android:title="Item 1" />
<item android:title="Item 2" />
<item android:title="Item 3" />
</menu>
MainActivity.java :
package com.example.menuoption;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuInflater;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
    }
    @Override
    public booleanonCreateOptionsMenu(Menu menu) {
MenuInflater m = getMenuInflater();
m.inflate(R.menu.option,menu);
        return true;
    }
}

/*
Program to print the text “optionmenu”.
Developed by: Srihariharan S A
Registeration Number : 212221040160
*/
```

## OUTPUT

![image](https://github.com/hariharan2383/Mobile-Application-Development/assets/117346668/349ae2f4-9aa9-4120-af90-23b00fbb4e16)
![image](https://github.com/hariharan2383/Mobile-Application-Development/assets/117346668/a361d563-9fad-4367-bb89-5943757eddc1)



## RESULT
Thus a Simple Android Application to create a option menu to display menu items using Android Studio is developed and executed successfully.


