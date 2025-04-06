## Setup
(Tested on Kubuntu 24.04.2)

__1. Install libpcap__
```
sudo apt-get install libpcap-dev
```
__2. Fix gradle version__

Open the file `gradle/wrapper/gradle-wrapper.properties` and change the _distributionUrl_ to: `https\://services.gradle.org/distributions/gradle-4.5-all.zip`.

__3. Install jnetpcap local repo__

Navigate to the directory `jnetpcap/linux/jnetpcap-1.4.r1425` and run the follwoing command:
```
mvn install:install-file -Dfile=jnetpcap.jar -DgroupId=org.jnetpcap -DartifactId=jnetpcap -Dversion=1.4.1 -Dpackaging=jar
```

## Run
Open the project in IntelliJ IDEA and open a Terminal in the IDE.
```
sudo bash
chmod +x gradlew
./gradlew execute
```

## Build package
Open the project in IntelliJ IDEA and open a Terminal in the IDE
```
./gradlew distZip
```
The zip file will be generated in `build/distributions`
