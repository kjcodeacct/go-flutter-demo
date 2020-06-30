<!-- class: center, middle -->

# Golang & Flutter
![Logo](https://github.com/kjcodeacct/golang_flutter_demo/raw/master/assets/goflutter.png)

---

<!-- class: left, middle -->

# What is this exactly?
This is a great way to develop truly cross platform desktop applications rapidly, and beautifly.

It's an intersection between:
* Flutter's approach to declarative UI.
* Golang's great performant and system level language.


Powered by the [go-flutter project](https://github.com/go-flutter-desktop/go-flutter)

---

<!-- class: left, middle -->

# Who is this for?
This is for anyone who wants to build an application *with* a modern UI.

This could range from any of the following situations:
* You have a mobile app you want to release on desktop.
* Want to release a golang based app *without* electron or html.
* You know golang, and want to get into mobile development or vice-versa.

---
# Why?

## Flutter
* Flutter is a great UI oriented language, for rapidly getting to production across *all* platforms.

* Has a great UI standard that renders natively on everythin from linux to IOS.

* Desktop support for dart/flutter is spotty, and unofficially in beta.


## Golang
* Golang is a great system oriented language, for getting robust and fast (enough) code onto *all* platforms.

* Has no real official UI tooling or even officially recommened UI.

* Has primarily been developed with cli and server based applications in mind.

---
# Quick Comparison
### What else is available

* GTK <https://github.com/gotk3/gotk3>
    * desktop focused
* Nuklear <https://github.com/golang-ui/nuklear>
    * desktop focused
* Fyne <https://github.com/fyne-io/fyne>
    * basic mobile implementation (lacks sensor data, etc)
* QT <https://github.com/therecipe/qt>
    * fairly complete mobile implementation

Please note this is a list of packages I've used *personally*.
For a more exaustive list please go to
<https://github.com/avelino/awesome-go#gui>
---
# Pros & Cons
## *AKA is this too hipster for production*?

---
# Pros & Cons

## Pros
* Great workflow, can build and package a release for any platform (desktop, mobile, embedded) in moments.

* Flutters UI is declaritive and a part of the business logic. No need to fuss with widget declarations, complex callbacks, async threads, etc.

* Can target any desktop specific features with golang, and provide any mobile specific features with flutter/golang-mobile.
    * Can also have 2 seperate UI's for mobile and desktop experiences.

* Flutter has been proven to be a stable platform for many of the large companies seen at <https://flutter.dev/showcase>

---
# Pros & Cons

## Cons
* [go-flutter](https://github.com/go-flutter-desktop/go-flutter) is unofficial.

* Flutter is less popular than kotlin, swift, and react-native, leading to a smaller community (currently)

* Flutter is a new technology. Sometimes that's scary, and a hard sell.

* Google occasionally likes to [kill nice things](https://killedbygoogle.com/)
    * Should be noted Google dog-foods flutter for everything from Google Ads to Stadia.


---

# How it works
### High Level
![High Level Diagram](https://raw.githubusercontent.com/kjcodeacct/golang_flutter_demo/master/assets/high-level-diagram.png)


---
# How it works
### In depth
![In Depth Diagram](https://raw.githubusercontent.com/kjcodeacct/golang_flutter_demo/master/assets/flutter-system.png)
---
# How it works

### Further Reading 

https://flutter.dev/docs/development/platform-integration/c-interop

https://github.com/flutter/flutter/wiki/Custom-Flutter-Engine-Embedders

https://hover.build/blog/one-year-in/

https://github.com/go-flutter-desktop/go-flutter/issues/191#issuecomment-511384007

https://github.com/go-gl/glfw


---

# Is this too hipster for production?

### TLDR; **No**

* Essentially go-flutter at its core is just ~ 200 lines of code to compile to C byte code with GLFW support
    * I.E. this is not complex, at a language level, just fancy tooling
* All API's going to future flutter versions are deprecated but still functional
    * **ANY** currently working features will not break.
    * Go here for more information on flutter API versioning and compatibility policy
        * <https://flutter.dev/docs/resources/compatibility>

---
<!-- class: left, top -->

# Getting Started

* Install go 1.13+
    * instructions can be found at <https://golang.org/doc/install>
* Install flutter
    * instructions can be found at <https://flutter.dev/docs/get-started/install>
* Install go-flutter
    * install hover (flutters unofficial go client)
        * ```GO111MODULE=on go get -u -a github.com/go-flutter-desktop/hover```
* Install dependencies
    * mac - have xcode installed
    * linux - install the following packages 'libgl1-mesa-dev xorg-dev'
    * windows - install gflw for windows <https://www.glfw.org/docs/latest/compile.html#compile_deps>
* Enable desktop builds
    ```
    flutter config --enable-macos-desktop
    flutter config --enable-linux-desktop
    flutter config --enable-windows-desktop
    ```

---
# Demo
---