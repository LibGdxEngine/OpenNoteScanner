OpenNoteScanner
===============

[![Build Status](https://travis-ci.org/ctodobom/OpenNoteScanner.svg)](https://travis-ci.org/ctodobom/OpenNoteScanner)

This little application provides a way on scanning handwritten notes and printed documents.

It automatically detect the edge of the paper over a contrastant surface.

When using the [printed special page template](https://github.com/ctodobom/OpenNoteScanner/raw/master/Page%20Templates/A4%20with%202%20pages.pdf) it automatically detects the QR Code printed on the bottom right corner and scans the page immediately.

After the page is detected, it compensates any perspective from the image adjusting it to a 90 degree top view and saves it on a folder on the device.

It is also possible to launch the application from any other application that asks for a picture, just make sure that there is no default application associated with this action.

Screenshots
-----------

[![screenshot1](http://i.imgur.com/1MDisD3m.jpg)](http://imgur.com/a/ypytF/embed#0)
[![screenshot1](http://i.imgur.com/ksvmOlym.png)](http://imgur.com/a/ypytF/embed#3)
[![screenshot1](http://i.imgur.com/Ayy8GGgm.jpg)](http://imgur.com/a/ypytF/embed#1)
[![screenshot1](http://i.imgur.com/tzMLas3m.jpg)](http://imgur.com/a/ypytF/embed#2)

Requirements
------------

Because of the version of OpenCV that is used in the project it needs to run on Android 5.0 (lollipop) or newer.

In order to capture and manipulate images Open Note Scanner depends on having the OpenCV Manager application installed. If not installed Open Note Scanner will ask to download it from https://github.com/ctodobom/OpenCV-3.1.0-Android or from Google Play Store.


How to Install
--------------

Binary APK file is available [directly from GitHub in the releases section](https://github.com/LibGdxEngine/OpenNoteScanner/releases) of the project.

Instructions for building
-------------------------

### Android Studio

Import the project from GitHub using File -> New -> Project from Version Control -> GitHub, fill the URL https://github.com/ctodobom/OpenNoteScanner.git

It will ask for a base directory, normally AndroidStudioProjects, you can change it to your preference.

After this the Open Note Scanner can be built.


### Command Line

Go to your base folder and import it using ```git```:

```
$ git clone https://github.com/LibGdxEngine/OpenNoteScanner.git
```

This should import the Open Note Scanner repository in OpenNoteScanner folder

You need to point the environment variable ```ANDROID_HOME``` to your Android SDK folder and run ```gradle``` to build the project:

```
$ cd OpenNoteScanner
$ export ANDROID_HOME=~/android-sdk-linux
$ ./gradlew assembleRelease
```

History
-------

I've started this app on a brazilian holyday "extended weekend" based on the fact that I was unable to find any open source application that does this job. I was mainly inspired on the RocketBook Wave closed source application.

I really do not know if I will extend more the application, but I am writing bellow some objectives to make it better.

Roadmap
-------

* enhance the image gallery of scanned documents
* register a share action in order to obtain documents already pictured through standard camera apps
* implement automatic action based on the RocketBook Wave marking of the page


Thanks
------
### External code

This application wouldn't be possible without the great material produced by the community. I would like to give special thanks to the authors of essencial parts I've got on the internet and used in the code:

* [Android-er / GridView code sample](http://android-er.blogspot.com.br/2012/07/gridview-loading-photos-from-sd-card.html)
* [Android Hive / Full Screen Image pager](http://www.androidhive.info/2013/09/android-fullscreen-image-slider-with-swipe-and-pinch-zoom-gestures/)
* [Adrian Rosebrock from pyimagesearch.com for the excellent tutorial on how to handle the images](http://www.pyimagesearch.com/2014/09/01/build-kick-ass-mobile-document-scanner-just-5-minutes/)
* [Gabriele Mariotti / On how to implement sections in the RecyclerView](https://gist.github.com/gabrielemariotti/e81e126227f8a4bb339c)


License
-------

Copyright 2016 - Ahmed Fathy Zain

Software licensed under the GPL version 3 available in GPLv3.TXT and
online on http://www.gnu.org/licenses/gpl.txt.

Use parts from other developers, sometimes with small changes,
references on autorship and specific licenses are on individual
source files.
