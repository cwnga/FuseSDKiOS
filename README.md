# Upsight Ad Mediation SDK

## Current Version

Version: 2.5.4
Released: April 6th, 2016

## Important Notes About iOS 9:
### App Transport Security
This feature is designed to improve the security of connections between apps and web services.
Upsight bundles several third-party ad network SDKs as part of Upsight Ad Mediation SDK, and some ad providers may not be compliant by the time iOS 9 is released. If you are building an app with Xcode 7 that will run on iOS 9 devices, you may need to implement a short-term fix to allow insecure connections.  Please see http://help.upsight.com/api_sdk_reference/ios/upsight-ad-mediation/.

### Bitcode Support
Bitcode is an intermediate representation of a compiled program ( https://developer.apple.com/library/prerelease/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AppThinning/AppThinning.html#//apple_ref/doc/uid/TP40012582-CH35-SW2 ).

Uploading apps containing bitcode to Apple through iTunes Connect allows Apple to re-optimize the application binary in the future without needing a re-submission.  However, enabling bitcode (which is the default setting in Xcode 7), requires all linked frameworks and binaries to have been built with bitcode enabled.  While the Upsight Ad Mediation itself has been built with bitcode enabled, some of the included ad network libraries have not yet enabled bitcode.  This will be fixed over time, but in the meanwhile, you can manually disable bitcode in their application by going to the Build Options in their target's build settings.  Further details can be found at: http://help.upsight.com/api_sdk_reference/ios/upsight-ad-mediation/

### Xcode 7
This version of the Upsight Ad Mediation SDK is built using the iOS 9 SDK under Xcode 7. Using this SDK with previous version of Xcode currently does not function.

## To Download
The Upsight Ad Mediation SDK is an additional SDK that is used in conjunction with the Upsight SDK to enable rewarded and non-rewarded video ads.
The easiest way to obtain the Upsight Ad Mediation SDK is to click the "Download ZIP" button located in the right-hand navigation pane of the Github repository page.

## Getting Started

Please review the [integration instructions](http://help.upsight.com/api_sdk_reference/ios/upsight-ad-mediation/) found here for more information on integrating the Upsight Ad Mediation SDK.

## References

* [Integration Instructions](http://help.upsight.com/api_sdk_reference/ios/upsight-ad-mediation/)

## Need an Account?
Please visit [http://www.upsight.com](http://www.upsight.com) and contact us to get started!

## Release Notes

### 2.5.4
April 6, 2016
* Fix for potential crash on iOS7 with rewarded ads
* Fix for debug logging enabled by default
* Recompile to fix archiving with certain versions of Unity

### 2.5.1
February 29, 2016
* Update all internal advertising partners

### 2.4.5
February 12, 2016
* Initial release of the Upsight Ad Mediation SDK for use with the Upsight SDK

## Legal Requirements
By downloading the Upsight Ad Mediation SDK, you are granted a limited, non-commercial license to use and review the SDK solely for evaluation purposes.  If you wish to integrate the SDK into any commercial applications, you must register an account with [Upsight](https://www.upsight.com) and accept the terms and conditions.

## Contact Us
For more information, please visit [http://www.upsight.com](http://www.upsight.com). For questions or assistance, please email us at [support@upsight.com](mailto:support@upsight.com).
