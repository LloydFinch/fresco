---
id: index
title: Adding Fresco to your Project
layout: docs
permalink: /docs/index.html
next: getting-started.html
---

Here's how to add Fresco to your Android project.

### Android Studio or Gradle

Edit your `build.gradle` file. You must add the following line to the `dependencies` section:


```groovy
dependencies {
  // your app's other dependencies
  compile 'com.facebook.fresco:fresco:{{site.current_version}}+'
}
```

### Eclipse ADT

Download the [zip file](https://github.com/facebook/fresco/releases/download/v{{site.current_version}}/frescolib-v{{site.current_version}}.zip).

When you expand it, it will create a directory called 'frescolib'. Note the location of this directory.

1. From the File menu, choose Import.
2. Expand Android, select "Existing Android Code into Workspace", and click Next.
3. Click Browse, navigate to the frescolib directory, and click OK.
4. Five projects should be added: drawee, fbcore, fresco, imagepipeline, and imagepipeline-okhttp. Make sure the first four are checked. Click Finish.
5. Right-click (Ctrl-click on Mac) on your project and choose Properties, then click Android.
6. Click the Add button in the bottom right, select Fresco, and click OK, then click OK again.

You should now be able to build your app with Fresco.

If you want to use OkHttp as the network layer, see the [separate instructions](using-other-network-layers.html#_).

If you get a `Jar Mismatch` warning about `android-support-v4.jar`, delete the one in `frescolib/imagepipeline/libs.`