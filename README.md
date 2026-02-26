## Unofficial Maven Repository for Android SDK files

Android API Levels: https://apilevels.com/

This repo currently provides stub Android SDKs from versions 2 (Android 1.1) to 36 (Android 16)

Explore the repo contents: https://android-mvn.github.io/repo/

---

Snippets to save you some time in case you want to use this repo for your project:

Replace `API-VERSION` with a valid number

> pom.xml
```xml
<repository>
    <id>android-mvn</id>
    <url>https://android-mvn.github.io/repo/</url>
</repository>

<dependency>
    <groupId>com.android</groupId>
    <artifactId>sdk</artifactId>
    <version>API-VERSION</version>
    <scope>provided</scope>
</dependency>
```

> gradle.build.kts
```kotlin
repositories {
    maven {
        url = uri("https://android-mvn.github.io/repo/")
    }
}

dependencies {
    compileOnly("com.android:sdk:API-VERSION")
}
```

