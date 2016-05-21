FloatingActionButton 
====================
Yet another library for drawing [Material Design promoted actions](http://www.google.com/design/spec/patterns/promoted-actions.html).

just fork from  [futuresimple](https://github.com/futuresimple/android-floating-action-button) 

[![Release](https://jitpack.io/v/jitpack/maven-simple.svg)](https://jitpack.io/#ddqd/android-floating-action-button)

Features
========
* Support for normal `56dp` and mini `40dp` buttons.

  ![Demo](screenshots/buttons.png)

* Customizable background colors for normal and pressed states and icon drawable.

  ![Demo](screenshots/custom.png)

* Convenience `AddFloatingActionButton` class with plus icon drawn in code.
* `FloatingActionsMenu` which can be expanded/collapsed to reveal multiple actions.

  ![Demo](screenshots/menu.gif)

* Optional labels for buttons in `FloatingActionsMenu`.

  ![Demo](screenshots/labels.png)

Usage
=====

**Step 1.** Add the JitPack repository to your build file

Add it in your root `build.gradle` at the end of repositories:

```groovy
allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}
```

**Step 2.** Add the dependency

```groovy
dependencies {
	compile 'com.github.ddqd:android-floating-action-button:1.10.2'
}
```
To see how the buttons are added to your xml layouts, check the sample project.

Caveats
=======
The API is **extremely** limited at the moment. It solves few select use cases in the app I'm working on.

Unlike some other FloatingActionButton libraries this library doesn't implement "quick return" pattern, i.e. hiding the button on scrolling down and showing it on scrolling up. That's intentional, I think that should be responsibility of another component, not the button itself.

This library is `minSdkVersion=14` and if that changes, the version number will be increased, not decreased. It means that Honeycomb, Gingerbread or - gods forbid - Froyo, won't ever be supported. I won't even consider merging pull requests fully implementing support for older versions. We need to move on as Android community and focus on delivering value for 95% of users of modern Android OS instead of jumping through burning hoops to support ancient devices with ancient OS.

If you **really** require support for older Android versions, [str4d](https://github.com/str4d) maintains [a version of this library with `minSdkVersion=4`](https://github.com/str4d/android-floating-action-button).

Credits
=======
I used [FloatingActionButton](https://github.com/makovkastar/FloatingActionButton) library by [Oleksandr Melnykov](https://github.com/makovkastar) as a base for development.

License
=======

    Copyright (C) 2014 Jerzy Chalupski

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

         http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
