# Android_neumorphic
## neumorphic (sof-ui) library for android  
#### based on https://github.com/florent37/ShapeOfView
---
**NOTE**
This is not a free library. But it has been published based on your trust. If you use this library in your software, be sure to pay the price.
- If this library was very useful ... $ 99
- If it only saves you time ... $ 29
---
🔧 Easy Installation 🔧 click here -> 
[![](https://jitpack.io/v/sshadkany/Android_neumorphic.svg)](https://jitpack.io/#sshadkany/Android_neumorphic)
--
## ✔️some exmaples !!
### with 3 basic shape
| <img src="screenshots/1.png" width="250"> | <img src="screenshots/3.gif" width="250"> | <img src="screenshots/button.gif" width="250"> 
|------------|-------------|--------------|
|code in activity_secend.xml |  code in activity_secend.xml | code in activity_secend.xml

### can works nested and make amazing views !!
|<img src="screenshots/2.png" width="250"> |<img src="screenshots/nested.png" width="250"> |
|-----------------|----------------|
|code in activity_main.xml |code in activity_3.xml 

## how to use ?? 👞 by 👞 
### 1.first install library 
### 2.use this code for circle neumorphic view
```xml
    <com.github.sshadkany.shapes.CircleView
        android:id="@+id/btn35"
        android:layout_width="200dp"
        android:layout_height="200dp"
        android:layout_margin="5dp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="parent"
        app:shape_circle_backgroundColor="#ECF0F3"
        app:shape_circle_shadow_type="drop_shadow" />
```
### 3.a better example 
|<img src="screenshots/shadow style.png" width="250">|
|-------------|
|code in activity_style.xml|

### you can play with every paramter!!
|<img src="screenshots/5.png" width="250">|
|-------------|
|code in activity_5.xml|
```xml
        app:shape_circle_shadow_position_y="-30dp"
        app:shape_circle_shadow_position_x="40dp"
        app:shape_circle_dark_color="@color/colorPrimary"
        app:shape_circle_light_color="@color/colorAccent"

        app:shape_circle_borderColor="@color/colorPrimaryDark"
        app:shape_circle_borderWidth="4dp"
```
### how make a button ?? 
|<img src="screenshots/button2.gif" width="250"> |
|----------|
|code in activity_button.xml|

```java
              final neo mybtn = findViewById(R.id.my_button);
        ViewGroup viewGroup = findViewById(R.id.my_button);
        final ImageView imageview = (ImageView) viewGroup.getChildAt(0);
        mybtn.setOnTouchListener(new View.OnTouchListener() {
            @Override
            public boolean onTouch(View v, MotionEvent event) {
                // is shape Contains Point ----> for detect place of Touch is in the shape or not
                if (mybtn.isShapeContainsPoint(event.getX(), event.getY())) {
                    switch (event.getAction()) {
                        case MotionEvent.ACTION_DOWN:
                            // PRESSED
                            mybtn.setStyle(neo.small_inner_shadow);
                            imageview.setScaleX(imageview.getScaleX() * 0.9f);
                            imageview.setScaleY(imageview.getScaleY() * 0.9f);
                            return true; 
                        case MotionEvent.ACTION_UP:
                        case MotionEvent.ACTION_CANCEL:
                            // RELEASED
                            mybtn.setStyle(neo.drop_shadow);
                            imageview.setScaleX(1);
                            imageview.setScaleY(1);
                            return true; 
                    }
                }
                return false;
            }
        });
    }
```
