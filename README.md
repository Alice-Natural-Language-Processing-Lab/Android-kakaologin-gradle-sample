# Android-kakaologin-gradle-sample
Kakao login Android Studio SDK Sample

<div style="width:100%;">
<img src="https://github.com/yongbeam/Android-kakaologin-gradle-sample/blob/master/kakao_login1.png?raw=true" align="center" height="30%" width="30%" style="margin-left:20px;">
<img src="https://github.com/yongbeam/Android-kakaologin-gradle-sample/blob/master/kakao_login2.png?raw=true" align="center" height="30%" width="30%" style="margin-left:20px;">
</div>

## Build.gradle
```
apply plugin: 'com.android.application'

android {
    compileSdkVersion 21
    buildToolsVersion "21.1.2"

    defaultConfig {
        applicationId "com.test.kakaotest"
        minSdkVersion 14
        targetSdkVersion 21
        versionCode 1
        versionName "1.0"
    }
    buildTypes {
        rehttps://github.com/yongbeam/Android-kakaologin-gradle-sample/edit/master/README.md#lease {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }

    packagingOptions {
        exclude 'META-INF/LICENSE'
        exclude 'META-INF/NOTICE'
        exclude 'META-INF/LICENSE.txt'
        exclude 'META-INF/ASL2.0'
    }
}

dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    compile project(':kakaologinutil')
}
```

## Author

 * 이용범
 * Mail: [top6616@gmail.com](mailto://top6616@gmail.com)
 * Web: [www.i-rooting.com](http://www.i-rooting.com)
 * Service Web: [www.yongcloud.co.kr](http://www.yongcloud.co.kr)
 * Sub repository: [GO](http://d.yongcloud.co.kr:9000/LibrarySample/KakaoLoginSample)

## License
Apache License
