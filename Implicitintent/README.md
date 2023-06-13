# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
activity_main.xml :
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayoutxmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:background="@color/purple_200"
tools:context=".MainActivity">
<Button
android:id="@+id/button"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginEnd="48dp"
android:text="NAVIGATE"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintVertical_bias="0.219" />
<EditText
android:id="@+id/editTextTextPersonName"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginStart="32dp"
android:ems="10"
android:inputType="textPersonName"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintVertical_bias="0.218" />
</android.support.constraint.ConstraintLayout>
MainActivity.java :
/*
Program to print the text “Implicitintent”.
Developed by: N. SIDDARTHAN
RegistrationNumber: 212221040154
*/
package com.example.intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.content.Intent;
import android.net.Uri;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
    Button button;
EditTexteditText;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
        button = findViewById(R.id.button);
editText = findViewById(R.id.editTextTextPersonName);
button.setOnClickListener(view -> {
            String url=editText.getText().toString();
            Intent intent=new Intent(Intent.ACTION_VIEW, Uri.parse(url));
startActivity(intent);
        });
    }
}

/*
Program to print the text “Implicitintent”.
Developed by: Srihariharan S A
Registeration Number : 212221040160
*/
```

## OUTPUT
![image](https://github.com/hariharan2383/Mobile-Application-Development/assets/117346668/2523ef67-eba3-4fb1-99b3-dc929c0c66a2)
![image](https://github.com/hariharan2383/Mobile-Application-Development/assets/117346668/2a1bcfa2-b93b-40e5-b3d5-9ba138a4de3e)




## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.


