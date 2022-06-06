# Ex.No:6 Build a program to create a first display screen of any search engine using Auto Complete Text View.
## AIM:
To develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min.required Artic Fox)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as searchengine and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using AutoComplete TextView in activity_main.xml.

Step 6: Display screen of search engine in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```python
/*
Program to print the text “display screen of any search engine”.
Developed by: DurgaDevi P
Registeration Number : 212220230015
*/
```
## MainActivity.java
```python
package com.example.autocomplete;

import android.graphics.Color;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.ArrayAdapter;
import android.widget.AutoCompleteTextView;

public class MainActivity extends AppCompatActivity {
    String[] fruit ={"Apple","Mango","Orange","Banana","Watermelon","Grapes","Cherry","Pineapple","Kiwi","Strawberry","Litchi","Blueberry","Raspberry","Guava","Custard apple","Pomegranate","Dragon fruit","Gooseberry","Jack fruit","Lime","Peach","Pear","Fig","Muskmelon","Olives","Java Plum","Papaya","Mulberry","Sugarcane"};
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        //Creating the instance of ArrayAdapter containing list of language names
        ArrayAdapter<String> adapter = new ArrayAdapter<String>
                (this,android.R.layout.select_dialog_item,fruit);
        //Getting the instance of AutoCompleteTextView
        AutoCompleteTextView actv =  (AutoCompleteTextView)findViewById(R.id.autoCompleteTextView);
        actv.setThreshold(1);//will start working from first character
        actv.setAdapter(adapter);//setting the adapter data into the AutoCompleteTextView
        actv.setTextColor(Color.RED);
    }
}
```
## activity_main.xml
```python
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="331dp"
        android:layout_height="62dp"
        android:text="What is your favourite fruit?"
        android:textColor="#C5082D"
        android:textSize="25sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintHorizontal_bias="0.662"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.14" />

    <AutoCompleteTextView
        android:id="@+id/autoCompleteTextView"
        android:layout_width="358dp"
        android:layout_height="55dp"
        android:background="#F3AFB9"
        android:text=""
        android:textColor="@color/black"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.49"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.667" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="286dp"
        android:layout_height="200dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.496"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.378"
        app:srcCompat="@drawable/fruit" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT
![o1](https://user-images.githubusercontent.com/75235704/172090744-f3c68bf9-abb0-4707-8fe7-99c936ae39c7.PNG)
![o2](https://user-images.githubusercontent.com/75235704/172090758-994302b8-156d-484e-bb2d-2e24d3ea75ee.PNG)
![o3](https://user-images.githubusercontent.com/75235704/172090771-579e8728-16f7-4311-8f4b-e694b2fb6fcf.PNG)



## RESULT
Thus a Simple Android Application develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio is developed and executed successfully.
