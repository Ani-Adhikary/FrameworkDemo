# FrameworkDemo


<h2> Create Xcframework YT 1</h2>

https://www.youtube.com/watch?v=TCnhvHUcjrY

<h3> Steps </h3>

1. Create framework
2. Add needed classes
3. Build Settings / Build Libraries for Distribution set YES
4. Build Settings / Skip Install set NO
5. Open termnial
6. cd and drag the folder with project
7. run three scripts in turn, which are located at the bottom

(!) Don't forget replace "PROJECTNAME_HERE" & ""FRAMEWORK_NAME" on your project name.

xcodebuild archive -scheme PROJECTNAME_HERE -destination="iOS" -archivePath /tmp/xcf/ios.xcarchive -derivedDataPath /tmp/iphoneos -sdk iphoneos SKIP_INSTALL=NO 


xcodebuild archive -scheme PROJECTNAME_HERE -destination="iOS Simulator" -archivePath /tmp/xcf/iossimulator.xcarchive -derivedDataPath /tmp/iphoneos -sdk iphonesimulator SKIP_INSTALL=NO


xcodebuild -create-xcframework -framework /tmp/xcf/ios.xcarchive/Products/Library/Frameworks/PROJECTNAME_HERE.framework -framework /tmp/xcf/iossimulator.xcarchive/Products/Library/Frameworks/PROJECTNAME_HERE.framework -output FRAMEWORK_NAME.xcframework


<h2> YT 2 </h2>

https://www.youtube.com/watch?v=40EmwraG4-k

![Cmd](https://user-images.githubusercontent.com/33363003/224033047-91405a3e-428c-480e-8b0f-bfe75165db26.png)


<h2> Tutorials </h2>

https://www.appcoda.com/xcframework/

https://www.kodeco.com/17753301-creating-a-framework-for-ios

https://developer.apple.com/videos/play/wwdc2019/416/
