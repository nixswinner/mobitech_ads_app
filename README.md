# Mobitech Ads
Implements the mobitech ads

# Steps to add Ads

# Setup.
1.Add gradle dependency on build.gradle (app).
```
  implementation 'com.github.nixswinner:mobitechads:0.3.0'
```
2.Add on build.gradle project under all allprojects repositories.
```
allprojects {
    repositories {
       .....
       .....
        maven { url 'https://www.jitpack.io' }

    }
}

```

3.Android manifect make sure your Internet Permission.

```
  <uses-permission android:name="android.permission.INTERNET" />
```

# Add Banner ads.
1. On your xml layout 
```
<com.ads.mobitechadslib.MobiAdBanner
        android:id="@+id/bannerAd"
        android:layout_gravity="center"
        android:scaleType="fitXY"
        android:layout_width="320dp"
        android:layout_height="50dp"/>
```
2.On your activity logic.
  1.Find the view 
  ```
  MobiAdBanner bannerAd = findViewById(R.id.bannerAd);
  ```
  2.Load ads - specify ads category_id and pass the activity context
  ```
  bannerAd.getBannerAds(this,
                "1");
  ```
  3.Auto Refresh banner - pass refresh rate (in minutes ) as an integer
  ```
   bannerAd3.getBannerAds(this,
                "1", 1); //refresh after 1 minute
  ```
  
  # Add Intertistial ad.
  
  Add the following code snippet on the activity logic
  It takes 2 parameters - context and ads category_id - string
  ```
   MobitechAds.getIntertistialAd(
                MainActivity.this,
                "1");
  ```
