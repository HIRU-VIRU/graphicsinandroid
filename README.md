
# Ex.No:12 Design an application that draws basic graphical primitives on the screen.


## AIM

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED

Android Studio(Latest Version)

## ALGORITHM
```
Step 1: Open Android Stdio and then click on File -> New -> New project.
Step 2: Then type the Application name as “graphical″ and click Next. 
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml.
Step 6: Draw basic object details give in MainActivity file.
Step 7: Save and run the application.
```
## PROGRAM
```
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed by: HIRUTHIK SUDHAKAR
Registeration Number : 212223240054
```
## In acitivity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <ImageView
        android:id="@+id/imageView1"
        android:layout_width="413dp"
        android:layout_height="736dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

## In MainActivity.java
```java
package com.example.graphical;
import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.graphics.drawable.BitmapDrawable;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.ImageView;
import java.nio.file.Path;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        //Creating a Bitmap
        Bitmap bg = Bitmap.createBitmap(720, 1280,Bitmap.Config.ARGB_8888);
        //Setting the Bitmap as background for the ImageView
        ImageView i = (ImageView) findViewById(R.id.imageView1);
        i.setBackgroundDrawable(new BitmapDrawable(bg));
        //Creating the Canvas Object
        Canvas canvas = new Canvas(bg);
        //Creating the Paint Object and set its color & TextSize
        Paint paint = new Paint();
        paint.setColor(Color.GREEN);
        paint.setTextSize(50);
        //To draw a Circle
        canvas.drawText("Circle", 120, 150, paint);
        canvas.drawCircle(200, 350, 150, paint);
        //To draw a Rectangle
        canvas.drawText("Rectangle", 420, 150, paint);
        canvas.drawRect(400, 200, 650, 700, paint);
        //To draw a Square
        canvas.drawText("Square", 120, 800, paint);
        canvas.drawRect(50, 850, 350, 1150, paint);
        //To draw a Line
        canvas.drawText("Line", 500, 800, paint);
        canvas.drawLine(520, 850, 520, 1150, paint);
    }
}
```

## OUTPUT
![image](https://github.com/SudharsanamRK/graphicsinandroid/assets/115523484/6cd88673-28aa-48f3-8998-ee34c49b7f62)


## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
