<div style="width:1000px; height: 320px; text-align: center; background-color: #FC4C4C; border-radius:20px;">
	<a href="https://RealityScript.io"><img src="https://realityscript.io/images/rs_logo_large.png" width="320" height="320" alt="RealityScript" title="RealityScript" /></a>
</div>

<p align="center">
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/github/license/ProjectDent/ARKit-CoreLocation.svg" alt="MIT License"></a>
</p>


## Intro: 

<strong>The RealityScript project</strong>

An open-source Web Component (Reality-Tag: <reality>) and Javascript Library (Reality.js) for embedding native Augmented Reality on the mobile web - unifying Apple's 'AR Quick Look' method and Google's 'Model-Viewer/Scene-Viewer' method under one shared code method. 

- Example (short-tag method): <a href="https://realityscript.io/example-short.html" target="_blank">Demo</a>

- Example (full-tag method): <a href="https://realityscript.io/example-full.html" target="_blank">Demo</a>


## Description 

The goal of RealityScript is to unify the intersection of common features, shared by both Apple’s ARKit web API, ‘AR Quick Look’, and Google’s ARCore web API, ‘Model-Viewer/Scene-Viewer’ under one code protocol instead of using two separate components and two different sets of attribute rules. 

RealityScript introduces the ‘Reality-Tag’ web component, as a single cross-platform solution for using both the native iOS and native Android, Augmented Reality frameworks on the mobile web. 

The Reality.js Javascript Library interprets the Reality-Tag attributes and automatically handles the different iOS and Android components and attribute rules, required by both iOS and Android with respect to detecting the device and OS of the user. 


## The Reality-Tag web component 

Web components are a set of custom HTML tags that are used to expand upon standard web platform features. 
A web component behaves like a standard HTML element but has a unique tag convention, with properties and methods used to fire and respond to events, most often then not, with a set of JavaScript functions, methods and classes. 

There are two ways you can use the Reality-Tag web component:   

A short-tag method for embedding Augmented Reality in your HTML with one line of code. 
This is good for quick and simple usage and assumes a specific folder & file layout convention, called the ‘asset group shortcut’, for pathing the separate asset files with relevancy to each other. 

And a full-tag method with attributes for customisation. 
This makes use of the intersection of common features available from both iOS and Android, Web AR frameworks. 


## Usage: Reality-Tag - Short-tag method 

The quickest way to get up and running with RealityScript is to use the 'one line' short-tag method. 

This method assumes a specific folder & file layout convention, called the ‘asset group shortcut’, for pathing the separate asset files with relevancy to each other. See the 'Asset group shortcut' section below for the specific folder & file layout convention. 

Once you have uploaded your asset files, you only then need to include the the 'asset group shortcut' URL for the Reality-Tag's 'src' attribute to implement RealityScript with the minimum usage. 

Example: <a href="https://realityscript.io/example-short.html" target="_blank">Demo</a>

```html
<reality src="https://realitymaker.io/test/robot"></reality>
```

Reality.js will generate the full asset paths from the 'asset group shortcut' URL. 

Note: To use this method, you must only provide the following file formats in the asset group: .jpg for the image, .usdz for the iOS model and .gltf for the Android model. 

Support for .jpeg, .png, .reality and .glb is planned for a future release however you can use these file formats now if you implement the 'full-tag method' instead of the 'short-tag method'. 


## Usage: Reality-Tag - Full-tag method 

The full-tag method uses attributes for customisation and layout. The following example lists each of the current attributes available. 

Example: <a href="https://realityscript.io/example-full.html" target="_blank">Demo</a>

```html
<reality title="Robot" 
	 image="https://realityscript.io/examples/robot/image/robot.jpg"
	 model-ios="https://realityscript.io/examples/robot/ios/robot.usdz" 
	 model-android="https://realityscript.io/examples/robot/android/robot.gltf"
	 display-image="yes" 
	 display-instructions="yes"
	 display-editorial="yes"
	 box-width="400"
	 box-height="400"
	 box-radius="40" 
	 box-margin="20"
	 box-background-color="#CF2F33"
	 box-size="" >
</reality>
```

- The Reality-Tag's 'title' attribute is assigned to the 'alt' and 'title' attribute of the preview image when used. 
It is also on display in Model-Viewer's UI. 

- The Reality-Tag's 'image' attribute is the path URL for the preview image when used. 

- The Reality-Tag's 'model-ios' attribute is the path URL for the 3D model required for iOS and AR Quick Look. 

- The Reality-Tag's 'model-android' attribute is the path URL for the 3D model required for Android and Model-Viewer/Scene-Viewer. 

- The Reality-Tag's 'display-image' attribute can be set to 'yes' or 'no'. This will determine whether or not the preview image will be displayed when viewed in any way other than AR Quick Look (AR Quick Look currently requires an image preview).

- The Reality-Tag's 'display-instructions' attribute can be set to 'yes' or 'no'. This will determine whether or not some end-user instructions will be displayed on top of the preview box. 

- The Reality-Tag's 'box-width' attribute can be set to any number correlating with the number of pixels you would like to use for the width of the preview box. 

- The Reality-Tag's 'box-height' attribute can be set to any number correlating with the number of pixels you would like to use for the height of the preview box. 

- The Reality-Tag's 'box-radius' attribute can be set to any number correlating with the number of pixels you would like to use for the corner radius of the preview box. 

- The Reality-Tag's 'box-margin' attribute can be set to any number correlating with the number of pixels you would like to use for the margin space surrounding the preview box. This number will have a minus effect on the overall width and height as per the CSS 

- The Reality-Tag's 'box-background-color' attribute can be set to any CSS colour correlating to background colour you would like to use for the preview box. 

- The Reality-Tag's 'size' attribute can be set to 'small', 'medium' or 'large'. This correlates to the size of the preview box and is used instead of the combination of the 'width', 'height', 'box-border-radius', and 'box-margin' attributes.


## Usage: Asset group shortcut 

The 'asset group shortcut' can be used with both the 'shot-tag method' and the 'full-tag method' and provide a simple method for pathing the separate asset files with relevancy to each other using one single 'asset group shortcut' URL. 

Note: To use the 'asset group shortcut', you must only provide the following file formats in the asset group: .jpg for the image, .usdz for the iOS model and .gltf for the Android model. 

The 'asset group shortcut' relies on the following file naming and folder layout convention: 

- Choose a single, shared file name for all three of the asset files e.g. robot.usdz, robot.gltf and robot.jpg  

- The .usdz file must reside inside a folder named 'ios' eg. the path would be: ios/robot.usdz

- The .gltf file must reside inside a folder named 'android' eg. the path would be: android/robot.gltf

- The .jpg file must reside inside a folder named 'image' eg. the path would be: image/robot.jpg 

- All three of the asset folders, 'ios', 'android' and 'image', must together reside inside one parent group folder named whatever you chose as the shared file name e.g. if your shared file name was 'robot', than your group folder would also be named 'robot'. In this case, your the path to your image would be 'robot/image/robot.jpg', the path to your Android model would be 'robot/android/robot.gltf' and the path to your iOS model would be 'robot/ios/robot.usdz'. The 'robot' group folder can then reside on any server, in any directory or sub-directly. 

As long as you provide the full-path to the group folder, Reality.js can obtain the files eg. 'https://realityscript/examples/robot' could be used as an asset group shortcut URL and so could 'https://realityscript/robot' and 'https://realityscript/examples/3dmodels/robot' depending on where the group folder were uploaded to. 

This URL is then set to the 'src' attribute of the Reality-Tag instead of using the attributes.. 'model-ios', 'model-android' and 'image'.


## Compatible asset file formats 

Use the following file formats for your media assets in order for RealityScript to be compatible with both iOS and Android. 

- For iOS, AR Quick Look: .usdz or .reality 

- For Android, Model-Viewer/Scene-Viewer: .gltf or .glb

- For the preview image: .jpg or .png


## End-user requirements 

RealityScript explicitly requires the availability of ARKit or ARCore, respectively on an end-user’s iOS or Android device to work. 

Without an ARKit or ARCore enabled device, RealityScript will not be able to present any AR experience and instead, will display a message to the user suggesting that they re-visit with a compatible device.


## What about non ARKit and ARCore devices 

If you’re an Augmented Reality developer / creator looking to publish AR experiences on the web for users that don’t have ARKit and ARCore compatible devices, your best bet would be to explore development with non-native, open-source libraries such as Three.js and A-Frame. These libraries are widely adopted with a wealth of expanded options and plugins supported by a large online community of web developers. (Three.js even sits within the rendering stack of Model-Viewer itself!*)

The libraries on their own however, when used with standard mobile web browsers, will be missing some of the more recent and powerful features that users have come to expect from AR such as SLAM with 6-degrees of freedom and surface detection.*

There are a few platforms out there however that aim to bridge the gap, combining non-native Web AR with Computer Vision (a sub-category of Artificial Intelligence) to achieve similar results to that of ARKit and ARCore. 

One of these platforms is called BlippBuilder and it’s developed by a company called Blippar.* Blippar were one of the first tech companies on the Augmented Reality scene and were around prior to the ‘ARKit and ARCore’ era.** The BlippBuilder platform also offers AR creators a “no-code” solution for developing Web AR - presenting a full, end-to-end, suite for easy 3D creation and instant publishing.* 

8th Wall are another company providing a platform for non-native Web AR, incorporating instant SLAM with 6-degrees of freedom and surface detection but minus the 3D creative suit.*  A recent and very interesting addition to 8th Wall’s feature-set allows developers to integrate a Microsoft Mixed Reality Capture Studio hologram into an 8th Wall WebAR project.* 

Augmented Reality holograms are something I feel will one day be extremely compelling to consumers and combining them with conversational AI technology is a planned focus area of mine for future projects. 

[* As of 25/04/20]

[** Full disclosure - I’ve been a full-time employee at Blippar previously and continue to collaborate on R&D projects as part of the wider team at-large]


## From here 

There are many more useful and common Web AR features that could be included in RealityScript. This is just the beginning and my hope is that it will develop further as an easy-to-implement, useful and efficient, cross-platform solution for using powerful, native Augmented Reality on the mobile web. 

RealityScript is open-source and released under the MIT license so please do with it as you wish and maybe contribute to improving/developing any part of it for future updates. 

For updates on other projects, including Holograms, Conversational AI and AR Virtual Assistants, give me a little follow on twitter: <a href="https://twitter.com/jasonio_" target="_blank">@Jasonio_</a>