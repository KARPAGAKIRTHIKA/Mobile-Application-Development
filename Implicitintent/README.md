# Ex.No:3 

Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by:KARPAGAKIRTHIKA.V
Registeration Number :212221220025
*/
```
# Activity_main.xml:
```
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

xmlns:app="http://schemas.android.com/apk/res-auto"

xmlns:tools="http://schemas.android.com/tools"

android:layout_width="match_parent"

android:layout_height="match_parent"

tools:context=".MainActivity">

<EditText
    android:id="@+id/urlEditText"
    android:layout_width="292dp"
    android:layout_height="67dp"
    android:layout_marginStart="56dp"
    android:layout_marginTop="108dp"
    android:hint="Enter URL"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

<Button
    android:id="@+id/navigateButton"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_gravity="center"
    android:text="Navigate"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toBottomOf="@+id/urlEditText" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
# MainActivity.java:
```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;

import android.net.Uri;

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.EditText;

public class MainActivity extends AppCompatActivity { EditText editText; Button button;

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    button = findViewById(R.id.navigateButton);
    editText = (EditText) findViewById(R.id.urlEditText);
    button.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View view) {
            String url=editText.getText().toString();
            Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(intent);
        }
    });
}
}
```

# OUTPUT

![image](https://github.com/KARPAGAKIRTHIKA/Mobile-Application-Development/assets/103020162/31ee07f9-cf25-417b-9bfe-f370369d4be8)

![image](https://github.com/KARPAGAKIRTHIKA/Mobile-Application-Development/assets/103020162/0c457b03-5c25-4243-a703-1e96adcee227)

![image](https://github.com/KARPAGAKIRTHIKA/Mobile-Application-Development/assets/103020162/1d73c2c9-d25b-4dde-909b-a0b8020c4598)

![image](https://github.com/KARPAGAKIRTHIKA/Mobile-Application-Development/assets/103020162/c2cb128c-351a-41ad-8466-4d18173d7d80)

# RESULT

Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
