# Android Link Previewer
Link Preview Library for Android

#### Gradle setup

Step 1: Add it in your root build.gradle at the end of repositories:

~~~
gradle
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
~~~

Step 2: Add the dependency
~~~
gradle
dependencies {
	        implementation 'com.github.OverflowArchives:AndroidLinkPreviewer:0.01'
	}
~~~

Step 3: Usage
~~~
val linkPreview: LinkPreview = LinkPreview(
        responseListener = object : ResponseListener {
            override fun onData(previewMetaData: PreviewMetaData) {
                // on loaded metadata
            }

            override fun onError(e: Throwable?) {
                // error to load metadata
            }
        })
~~~
