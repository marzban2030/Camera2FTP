# Camera2FTP
Timelapsed capturing Android Camera App - Utilizing Camera2 API and Uploads to FTP Server periodically.

# Build in Colab
Run below commands in Colab:
```
!apt remove java-common
!apt install openjdk-8-jdk
!wget https://dl.google.com/android/repository/commandlinetools-linux-9123335_latest.zip
!mkdir -p sdk
!unzip commandlinetools-linux-9123335_latest.zip -d sdk
!yes | ./sdk/cmdline-tools/bin/sdkmanager --sdk_root=/content/sdk "tools"
```

Then run:
```
!git clone https://github.com/marzban2030/Camera2FTP
!chmod -c 755 /content/Camera2FTP/gradlew
!export ANDROID_HOME=/content/sdk && cd /content/Camera2FTP && ./gradlew assembleDebug
```

Finally run:
```
from google.colab import files
files.download('/content/Camera2FTP/app/build/outputs/apk/debug/app-debug.apk')
```

# Releases

Ver 2.0:

Added timelapsed capturing

# Use

Change "private int delay = 60000;" in "MainActivity.java" file which its value is in milliseconds.
