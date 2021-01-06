# adpush-library
RoyalMobi Media offers AdPushLibrary SDK, just integrate in simple steps and start showing our ad repository in your app and start earning from today.

# How to implement -
Add the JitPack repository to your build file, add it in your root build.gradle at the end of repositories:

    allprojects {
        repositories {
          ...
          maven { url 'https://jitpack.io' }
        }
      }
  
Add the dependency in app build.gradle:

    dependencies {
              implementation 'com.github.royalmobimedia:adpush-library:1.0'
      }

In project menifest file add -

    <application
      ...
      android:usesCleartextTraffic="true">
      <uses-library  android:name="org.apache.http.legacy"  android:required="false"/>
      ...
    </application>

In your main xml activity use an ImageView, keep the banner alignment as per your requirements -

    <ImageView
      android:id="@+id/banner_ad" 
      android:layout_width="300dp" 
      android:layout_height="40dp" 
      android:clickable="true"/>
  

In MainActivity.java -

    //Declaration ImageView banner_ad;
    PushAds  pads; //The  ad  library  class
    //Inside  onCreate()  function
    banner_ad = findViewByid(R.id.banner_ad);
    pads = new PushAds();
    pads.displayAds(MainActivity.this, banner_ad);


That's it, now your ads will start serving.

Thank you.
