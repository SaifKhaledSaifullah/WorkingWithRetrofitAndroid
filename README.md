## To Install java in Linux(Ubuntu)
To install this version, first update the package index:</br>
`$ sudo apt update`</br>
Next, check if Java is already installed:</br>
`java -version`</br>
If Java is not currently installed, you’ll see the following output:</br>

```
Command 'java' not found, but can be installed with:

apt install default-jre
apt install openjdk-11-jre-headless
apt install openjdk-8-jre-headless
```
Execute the following command to install the default Java Runtime Environment (JRE), which will install the JRE from OpenJDK 11:</br>
`$ sudo apt install default-jre`</br>
Verify the installation with:</br>
`java -version`</br>
Youill see the output like this:
```
openjdk version "11.0.7" 2020-04-14
OpenJDK Runtime Environment (build 11.0.7+10-post-Ubuntu-2ubuntu218.04)
OpenJDK 64-Bit Server VM (build 11.0.7+10-post-Ubuntu-2ubuntu218.04, mixed mode, sharing)
```

## To build and install apk file from source code
1. Download the source code file 
2. Go inside the source code folder
3. Click on mouse right button and open terminal
4. execute the folowing command
   * `gradlew assembleDebug`
   (This will create the debug apk file)
5. Then execute the following command (You must need to connect your device with your PC/Laptop)
   * `gradlew installDebug` </br>

This will install the app into your mobile device. Then open the app and explore it
