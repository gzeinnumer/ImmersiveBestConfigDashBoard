# ImmersiveBestConfigDashBoard

<p align="center">
  <img src="https://github.com/gzeinnumer/ImmersiveBestConfigDashBoard/blob/master/preview/example1.jpg" width="300"/>
</p>
<p align="center">
  <img src="https://github.com/gzeinnumer/ImmersiveBestConfigDashBoard/blob/master/preview/example2.jpg"/>
</p>

```xml
<style name="AppTheme" parent="Theme.MaterialComponents.Light.NoActionBar">
    <item name="colorPrimary">@color/colorPrimary</item>
    <item name="colorPrimaryVariant">@color/colorPrimaryDark</item>
    <item name="colorOnPrimary">@color/white</item>
    <item name="colorSecondary">@color/colorPrimary</item>
    <item name="colorSecondaryVariant">@color/colorPrimaryDark</item>
    <item name="colorOnSecondary">@color/white</item>
    <item name="android:statusBarColor" tools:targetApi="l">@android:color/white</item>
    <item name="android:fitsSystemWindows">false</item>
    <item name="android:navigationBarColor">@color/colorPrimary</item>
</style>
<style name="AppTheme.Dashboard" parent="AppTheme">
    <item name="android:navigationBarColor">@color/white_low</item>
</style>
```

```java
protected void setFullScreen() {
    int decore = 0;

    if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.M) {
        //enable this tho maker icon status bar become black
        decore += View.SYSTEM_UI_FLAG_LIGHT_STATUS_BAR;
    }

    if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.O) {
        //enable this tho maker icon Navigation bar become black
        decore +=  View.SYSTEM_UI_FLAG_LIGHT_NAVIGATION_BAR;
    }

    getWindow().getDecorView().setSystemUiVisibility(decore);
}
```

---

```
Copyright 2021 M. Fadli Zein
```