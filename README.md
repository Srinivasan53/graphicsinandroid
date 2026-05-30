
# Ex.No:12 Design an application that draws basic graphical primitives on the screen.


## AIM:

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed by: Srinivasan S
Registeration Number : 212224220105
*/
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
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
```
## MainActivity.java
```
package com.example.graphicsprimitivesapp;



import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        MyView myView = new MyView(this);
        setContentView(myView);
    }
}
```
## MyView.java
```
package com.example.graphicsprimitivesapp;





import android.content.Context;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.view.View;

public class MyView extends View {

    Paint paint;

    public MyView(Context context) {
        super(context);

        paint = new Paint();
        paint.setAntiAlias(true);
    }

    @Override
    protected void onDraw(Canvas canvas) {
        super.onDraw(canvas);

        // Background
        canvas.drawColor(Color.WHITE);

        // Text Paint
        Paint textPaint = new Paint();
        textPaint.setColor(Color.BLACK);
        textPaint.setTextSize(40);
        textPaint.setAntiAlias(true);

        // ---------------- LINE ----------------
        paint.setColor(Color.BLUE);
        paint.setStrokeWidth(8);

        canvas.drawLine(150, 100, 550, 100, paint);
        canvas.drawText("Line", 300, 160, textPaint);

        // ---------------- RECTANGLE ----------------
        paint.setColor(Color.RED);

        canvas.drawRect(150, 220, 550, 420, paint);
        canvas.drawText("Rectangle", 250, 490, textPaint);

        // ---------------- CIRCLE ----------------
        paint.setColor(Color.GREEN);

        canvas.drawCircle(350, 700, 120, paint);
        canvas.drawText("Circle", 285, 870, textPaint);

        // ---------------- OVAL ----------------
        paint.setColor(Color.MAGENTA);

        canvas.drawOval(150, 980, 550, 1150, paint);
        canvas.drawText("Oval", 300, 1230, textPaint);

        // ---------------- TITLE ----------------
        textPaint.setTextSize(50);

        canvas.drawText("Graphical Primitives", 80, 1400, textPaint);
    }
}
```

## OUTPUT
<img width="1804" height="951" alt="image" src="https://github.com/user-attachments/assets/9633a47b-15ca-4578-a1a5-7bfe79fa3702" />





## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
