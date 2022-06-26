activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
 xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:id="@+id/layout"
 android:background="@drawable/gradient_list"
 tools:context=".MainActivity">
<TextView
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:textSize="22sp"
 android:textStyle="bold"
 android:textColor="#219806"
 android:text="Spread love everywhere you go."

app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintLeft_toLeftOf="parent"
 app:layout_constraintRight_toRightOf="parent"
 app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>


MainActivity.java:
package com.example.livewallpaper;
import androidx.appcompat.app.AppCompatActivity;
import androidx.constraintlayout.widget.ConstraintLayout;
import android.graphics.drawable.AnimationDrawable;
import android.os.Bundle;
public class MainActivity extends AppCompatActivity {
@Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 ConstraintLayout layout = findViewById(R.id.layout);
 //With the help of AnimatedDrawable class, we can set
 //the duration to our background and then call the
 //function start at the end.
 AnimationDrawable animationDrawable = (AnimationDrawable)
 layout.getBackground();
 animationDrawable.setEnterFadeDuration(1500);
 animationDrawable.setExitFadeDuration(3000);
 animationDrawable.start();
 }
}
