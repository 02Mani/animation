# Ex.No: 11 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.


## AIM:

To develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Design the layout using activity_main.xml

Step 3: Add an ImageView to display the image and add buttons for each animation (Move, Blink, Fade, Clockwise, Zoom, Slide).

Step 4: Import the image into the drawable folder.

Step 5: Create animation XML files under res/anim/ for each animation type such as blink, fade, move, rotate, slide and zoom.

Step 6: Type the Java program in MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: MANIKANDAN M
Registeration Number : 212224040183
*/
```
## main_avtivity.java
```
package com.example.animation;

import android.app.Activity;
import android.os.Bundle;
import android.view.View;
import android.view.animation.Animation;
import android.view.animation.AnimationUtils;
import android.widget.Button;
import android.widget.ImageView;

public class MainActivity extends Activity {

    ImageView imageView;

    Button btnMove;
    Button btnBlink;
    Button btnFade;
    Button btnClockwise;
    Button btnZoom;
    Button btnSlide;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        imageView = findViewById(R.id.imageView);

        btnMove = findViewById(R.id.btnMove);
        btnBlink = findViewById(R.id.btnBlink);
        btnFade = findViewById(R.id.btnFade);
        btnClockwise = findViewById(R.id.btnClockwise);
        btnZoom = findViewById(R.id.btnZoom);
        btnSlide = findViewById(R.id.btnSlide);

        btnMove.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.move);
                imageView.startAnimation(animation);
            }
        });

        btnBlink.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.blink);
                imageView.startAnimation(animation);
            }
        });

        btnFade.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.fade);
                imageView.startAnimation(animation);
            }
        });

        btnClockwise.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.clockwise);
                imageView.startAnimation(animation);
            }
        });

        btnZoom.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.zoom);
                imageView.startAnimation(animation);
            }
        });

        btnSlide.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.slide);
                imageView.startAnimation(animation);
            }
        });
    }
}
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="200dp"
        android:layout_height="200dp"
        android:src="@drawable/photo"
        android:scaleType="centerInside"
        android:contentDescription="Animated Image" />

    <Button
        android:id="@+id/btnMove"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Move" />

    <Button
        android:id="@+id/btnBlink"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Blink" />

    <Button
        android:id="@+id/btnFade"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Fade" />

    <Button
        android:id="@+id/btnClockwise"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Clockwise" />

    <Button
        android:id="@+id/btnZoom"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Zoom" />

    <Button
        android:id="@+id/btnSlide"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Slide" />

</LinearLayout>
```
## MOVE.XML
```
<?xml version="1.0" encoding="utf-8"?>
<translate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromXDelta="0"
    android:toXDelta="300"
    android:fromYDelta="0"
    android:toYDelta="0"
    android:duration="1000" />
```
## BLINK.XML
```
<?xml version="1.0" encoding="utf-8"?>
<alpha xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromAlpha="1.0"
    android:toAlpha="0.0"
    android:duration="500"
    android:repeatMode="reverse"
    android:repeatCount="5" />
```
## FADE.XML
```
<?xml version="1.0" encoding="utf-8"?>
<alpha xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromAlpha="1.0"
    android:toAlpha="0.0"
    android:duration="2000" />
```
## CLOCKWISE.XML
```
<?xml version="1.0" encoding="utf-8"?>
<rotate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromDegrees="0"
    android:toDegrees="360"
    android:pivotX="50%"
    android:pivotY="50%"
    android:duration="1000" />
```
## ZOOM.XML
```
<?xml version="1.0" encoding="utf-8"?>
<scale xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromXScale="1.0"
    android:toXScale="2.0"
    android:fromYScale="1.0"
    android:toYScale="2.0"
    android:pivotX="50%"
    android:pivotY="50%"
    android:duration="1000" />
```
## SLIDE.XML
```
<?xml version="1.0" encoding="utf-8"?>
<translate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromXDelta="-300"
    android:toXDelta="0"
    android:fromYDelta="0"
    android:toYDelta="0"
    android:duration="1000" />
```

## OUTPUT
<img width="1919" height="1079" alt="Screenshot 2026-08-20 094641" src="https://github.com/user-attachments/assets/868e92dc-bd08-4199-b0d9-d11ae6245d5e" />
<img width="1919" height="1079" alt="Screenshot 2026-08-20 094608" src="https://github.com/user-attachments/assets/8e12d7c7-beaf-481c-9cf5-c9e205a611a2" />
<img width="1918" height="1078" alt="Screenshot 2026-08-20 094630" src="https://github.com/user-attachments/assets/4239c285-4b54-4d1c-ad46-bed209a9ffd7" />
<img width="1919" height="1079" alt="Screenshot 2026-08-20 094555" src="https://github.com/user-attachments/assets/50ba790c-f08d-48e9-98f7-6680013b0cd2" />
<img width="1919" height="1079" alt="Screenshot 2026-08-20 094521" src="https://github.com/user-attachments/assets/757e4eff-79c7-475c-a992-4d4dd1a7b67b" />
<img width="1919" height="1078" alt="Screenshot 2026-08-20 094506" src="https://github.com/user-attachments/assets/e485a72c-caf3-4a85-b5c5-94d37d78a8dc" />





## RESULT
Thus,the experiment Implementation of Animation application using android studio executed successfully.

