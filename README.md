Glimr Android SDK
==============

Documentation
============

For documentation visit http://developer.glimr.io

Minimum setup steps
============

Add the Glimr SDK dependency in your build.gradle:

    compile 'io.glimr.sdk:glimr-geo:1.8.8'

Also, don't forget to add jcenter to your repositories:

    allprojects {
        repositories {
            jcenter()
        }
    }

The SDK requires these permissions:
	
  	<uses-permission android:name="android.permission.BLUETOOTH"/>
	  <uses-permission android:name="android.permission.BLUETOOTH_ADMIN"/>
	  <uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

At this moment the SDK depends on the gson library, which you can add as a maven 
dependency in gradle (as in the example project) or download the jar and add it as a dependency 
in your own project.

Changelog
==========================

### Version 1.9.0 - 30. September 2016

* Skip reconnecting to GoogleApiClient if permissions are already satisfied
* Update GPS fix using LocationServices.FusedLocationApi.getLastLocation when app comes to foreground
* Use "socket.getClass().getMethod("setHostname", String.class).invoke(socket, host);" fallback for TLS connections for < Android 4.2

