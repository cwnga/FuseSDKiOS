# Fuse iOS SDK

## Current Version

Version: 2.5.3
March 22nd, 2016

## Important Notes About iOS 9:
### App Transport Security
This feature is designed to improve the security of connections between apps and web services.
Fuse bundles several third-party ad network SDKs as part of AdRally, and some ad providers may not be compliant by the time iOS 9 is released. If you are building an app with Xcode 7 that will run on iOS 9 devices, you may need to implement a short-term fix to allow insecure connections.  Please see https://wiki.fusepowered.com/index.php?title=Support_for_iOS_9 for details on how to disable App Transport Security.

### Bitcode Support
Bitcode is an intermediate representation of a compiled program ( https://developer.apple.com/library/prerelease/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AppThinning/AppThinning.html#//apple_ref/doc/uid/TP40012582-CH35-SW2 ).

Uploading apps containing bitcode to Apple through iTunes Connect allows Apple to re-optimize the application binary in the future without needing a re-submission.  However, enabling bitcode (which is the default setting in Xcode 7), requires all linked frameworks and binaries to have been built with bitcode enabled.  While the FuseSDK itself has been built with bitcode enabled, some of the included ad network libraries have not yet enabled bitcode.  This will be fixed over time, but in the meanwhile, you can manually disable bitcode in their application by going to the Build Options in their target's build settings.  Further details can be found at: https://wiki.fusepowered.com/index.php?title=Support_for_iOS_9

### Xcode 7
This version of the Fuse SDK is built using the iOS 9 SDK under Xcode 7. Using this SDK with previous version of Xcode currently does not function. If you are using FuseSDK 2.3 or higher please build against iOS9 and Xcode 7 or greater.

## To Download
The easiest way to obtain the Fuse SDK is to click the "Download ZIP" button located in the right-hand navigation pane of the Github repository page.

## Getting Started

Please review the [integration instructions](https://wiki.fusepowered.com/index.php?title=IOS) found here for more information on integrating the Fuse SDK.

## References

* [Integration Instructions](http://wiki.fusepowered.com/index.php/IOS)
* [Inline Code Reference](http://fusepowered.github.io/FuseSDKiOS/)
* [Fuse SDK Class Reference](http://fusepowered.github.io/FuseSDKiOS/Docs/html/interface_fuse_s_d_k.html)

## Need an Account?
Please visit [http://www.fusepowered.com](http://www.fusepowered.com) for an account to get started!

## Release Notes

### 2.5.3
March 22nd, 2016
* Fix for debug logging enabled by default

### 2.5.2
March 9th, 2016
* Fix for potential crash on iOS 7 with rewarded ads

### 2.5.1
February 2th, 2016
* Hotfix for IAP validation

### 2.5.0
February 25th, 2016
* Rich media pre and post rolls for cross promotional videos
* Price localization for offers
* Ad provider updates

### 2.4.1
November 17, 2015
* Ad provider stability fixes

### 2.4.0
November 12, 2015
* Ad Provider updates
* VAST Improvements
* Custom End Cards
* Bug Fixes

### 2.3.2
October 14th, 2015
* fix for crash on iOS 7 64-bit devices

### 2.3.1
October 9th, 2015
* fix Issues with iOS 9 only frameworks being linked.
* fix for some video ads in iOS 9

### 2.3.0
September 23rd, 2015
* iOS 9 Support
* Added meta-data for IAP and Virtual Good Offers
* Support for custom call-to-action text (campaign videos)
* Ad Provider Updates
* Bug Fixes

### 2.2.2
September 3rd, 2015
* Ad provider updates
* Added adDidShow callback

### 2.2.0
August 7th, 2015
* New ad providers added
* Added VAST support
* Added rewarded video authentication 
  * Added method +(void) setRewardedVideoUserID:(NSString *) _userID; to identify the user
  * Added itemID in the FuseRewardedObject in the rewardedAdCompleteWithObject callback
* Added startTime and endTime to FuseIAPOfferObject object in the IAPOfferAcceptedWithObject callback
* Added currencyID, virtualGoodID, startTime and endTime to FuseVirtualGoodsOfferObject object in virtualGoodsOfferAcceptedWithObject callback
* Bug fixes

### 2.1.4
June 16th, 2015
* Ad provider bug fixes

### 2.1.3
June 11th, 2015
* Ad provider bug fixes

### 2.1.2
June 10th, 2015
* Ad provider bug fixes

### 2.1.0
May 29th, 2015
* Virtual goods purchase tracking
* Added new segmentation functionality
* Added new gender enums
* Bug fixes
* Ad Provider updates

### 2.0.5
May 11th, 2015
* Fix for mediated ad partner causing iTunes validation to fail

### 2.0.2
April 9th, 2015
* IAP and Virtual Good offers
* Rewarded video enhancements
* Interface updates
* FuseAPI deprecated - please use FuseSDK

### 1.38.3
March 12th, 2015
* Fix for rare orientation issue

### 1.38.2
March 9th, 2015
* fix for crash on 64 bit iOS 7 devices

### 1.38.0
February 6th, 2015
* Ad provider updates and fixes
* Bug fixes

### 1.37.4
January 8th, 2015
* Ad orientation fixes
* Fixed log warnings
* Remove log spam
* Ad animation fixes
* Ad provider updates

### 1.37.3
December 3rd, 2014
* Orientation fixes for iOS 8
* Ad provider updates and fixes

### 1.37.1
November 18th, 2014
* Rotation bug fixes 
* Fixed linker issue with simulator
* Updated ad provider libraries

### 1.37.0
November 10th, 2014
* 3rd party plugin architecture for mediated networks
* Additional V4VC callbacks
* Bug fixes

## Legal Requirements
By downloading the Fuse Powered SDK, you are granted a limited, non-commercial license to use and review the SDK solely for evaluation purposes.  If you wish to integrate the SDK into any commercial applications, you must register an account with [Fuse Powered](https://www.fusepowered.com) and accept the terms and conditions on the Fuse Powered website.

## Contact Us
For more information, please visit [http://www.fusepowered.com](http://www.fusepowered.com). For questions or assistance, please email us at [support@fusepowered.com](mailto:support@fusepowered.com).
