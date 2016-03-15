# @Deprecated
카카오에서 Gradle을 공식 지원하기 때문에 더이상 이 샘플은 사용할 필요가 없습니다.
아래처럼 사용하시면 됩니다.

app/build.gradle
```
compile group: project.KAKAO_SDK_GROUP, name: 'kakaolink', version: project.KAKAO_SDK_VERSION
compile group: project.KAKAO_SDK_GROUP, name: 'kakaotalk', version: project.KAKAO_SDK_VERSION
compile group: project.KAKAO_SDK_GROUP, name: 'usermgmt', version: project.KAKAO_SDK_VERSION

```

gradle.properties
```
KAKAO_SDK_GROUP=com.kakao.sdk
KAKAO_SDK_VERSION=1.1.4

```


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
        release {
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

or
```
    packagingOptions {
        exclude 'META-INF/DEPENDENCIES.txt'
        exclude 'META-INF/LICENSE.txt'
        exclude 'META-INF/NOTICE.txt'
        exclude 'META-INF/NOTICE'
        exclude 'META-INF/LICENSE'
        exclude 'META-INF/DEPENDENCIES'
        exclude 'META-INF/notice.txt'
        exclude 'META-INF/license.txt'
        exclude 'META-INF/dependencies.txt'
        exclude 'META-INF/LGPL2.1'
        exclude 'META-INF/ASL2.0'
    }
    .
    .
    .
    // kakao
    compile('com.kakao.sdk:usermgmt:1.0.46') {
        exclude module: 'support-v4'
    }
    compile('com.kakao.sdk:kakaolink:1.0.46') {
        exclude module: 'support-v4'
        exclude module: 'jackson-core'
        exclude module: 'jackson-databind'
    }
    compile('com.kakao.sdk:kakaostory:1.0.46') {
        exclude module: 'support-v4'
        exclude module: 'jackson-core'
        exclude module: 'jackson-databind'
    }
    compile('com.kakao.sdk:kakaotalk:1.0.46') {
        exclude module: 'support-v4'
        exclude module: 'jackson-core'
        exclude module: 'jackson-databind'
    }
```
## Author

 * 이용범(LeeYongBeom)
 * Mail: [ray@travelking.kr](mailto://ray@travelking.kr)
 * Web: [www.travelking.kr](https://www.travelking.kr)

## License
    Copyright (c) 2016 LeeYongBeom

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
    Come on, don't tell me you read that.
