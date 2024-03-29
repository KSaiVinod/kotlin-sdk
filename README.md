## Overview
![Fyno: Fire your notifications](https://fynodev.s3.ap-south-1.amazonaws.com/others/Fyno_Banner.jpeg)
Fyno Android SDK allows you to track your notification delivery
<div style="display: flex;gap:10px"><img src="https://app.dev.fyno.io/images/fyno-logo.svg" width="50"><h1> Fyno - Android SDK</h1></div>

Fyno Android SDK allows you to track your notification delivery
#### Prerequisites
1. Setup Firebase/OneSignal 

2. Configure Providers in [Fyno App](https://app.fyno.io/)

3. Project Gradle
```kotlin
// place the below snippet in your project gradle file
allprojects {
    repositories {
        google()
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```
4. App gradle 
```kotlin
// place the below snippet in your app gradle file. 
implementation 'com.github.fynoio:kotlin-sdk:1.0.0'
```
<sup>[check the latest version here](https://jitpack.io/#fynoio/kotlin-sdk)</sup>

5. add the following in your ```MainActivity```.
```kotlin
//Initilize
FynoSdk.initialize(context, workspace_id)

//for enabling mi push
FynoSdk.setMiRegion(PushRegion.Global)
FynoSdk.registerMiPush(APP_ID, APP_KEY)
```


