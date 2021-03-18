# Blktrace Wrapper
To build and install the Blktrace wrapper app on your mobile device, you need some prerequisites. Here is a list of things we will go through to install the app on the mobile device
* Install Java
* Install Android sdk
* Install Gradle
* Build and install apk file from source code


## Install java in Linux(Ubuntu)
   To install java, first update the package index:</br>
   `$ sudo apt update`</br>
   then install jdk </br>
   `sudo apt install default-jdk`

## Install android sdk on Linux(Ubuntu)
1. **Create sdk folder**
   ```
   export ANDROID_SDK_ROOT=/usr/lib/android-sdk
   sudo mkdir -p $ANDROID_SDK_ROOT
   ```
2. **Download android sdk**</br>
  Go to [Android Sdk command line tools download](https://developer.android.com/studio/index.html#command-tools) page.Then down to Command line tools only Click on Linux link, accept the agreement and instead of downloading right click and copy link address
   ```
   cd $ANDROID_SDK_ROOT
    wget https://dl.google.com/android/repository/commandlinetools-linux-6858069_latest.zip
    unzip commandlinetools-linux-6858069_latest.zip
   ```
3. **Move folders**</br>
   Rename the unpacked directory from cmdline-tools to tools, and place it under $ANDROID_SDK_ROOT/cmdline-tools, so now it should look like:        $ANDROID_SDK_ROOT/cmdline-tools/tools. And inside it, you should have: NOTICE.txt bin lib source.properties.
4. **Set path** </br>
  `PATH=$PATH:$ANDROID_SDK_ROOT/cmdline-tools/latest/bin:$ANDROID_SDK_ROOT/cmdline-tools/tools/bin`
5. **Browse to sdkmanager**</br>
   `cd $ANDROID_SDK_ROOT/cmdline-tools/tools/bin`
6. **Accept licenses**<br>
   `yes | sdkmanager --licenses`
## Install Gradle
   Our app is build with Gradle version 6.5. Download Gradle 6.5 from [here](https://gradle.org/releases/) and follow the [installation guideline](https://docs.gradle.org/current/userguide/installation.html#installing_manually)
## Build and install apk file from source code
1. Download the source code file 
2. Go inside the source code folder
3. Click on mouse right button and open terminal
4. execute the folowing command
   * `./gradlew assembleDebug`
   (This will create the debug apk file)
5. Then execute the following command (You must need to connect your device with your PC/Laptop)
   * `./gradlew installDebug` </br>

This will install the app into your mobile device. Then open the app and explore it
