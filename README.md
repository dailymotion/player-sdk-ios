<p float="left">
  <img src="https://corpostatic.dailymotion.com/corporate-cms-upload-assets-prod/uploads/sites/150001/2024/01/Dailymotion-for-Developers.png" width="500" />
</p>

# Dailymotion Native iOS SDK


## Full SDK Documentation
 [https://developers.dailymotion.com/sdk/player-sdk/ios](https://developers.dailymotion.com/sdk/player-sdk/ios)

 <br>

## Sample Apps
[https://github.com/dailymotion/player-sdk-ios-samples/](https://github.com/dailymotion/player-sdk-ios-samples/)

<br>

## Supported versions & requirements:
- Swift 5+
- iOS 14+
- Xcode 14+

<br>

## Features
- Remote Player management
- iOS 16 support
- Google IMA support
- OMSDK support
- Sample player applications & code samples
- Fullscreen playback management
- Fully-featured Player API to access Player events, state and native control

<br>

## Using your own Google IMA version
The `DailymotionPlayerSDK` product embeds Google IMA (3.23.0). If your app already integrates Google IMA through SPM, or needs another IMA version:
- add the `DailymotionPlayerSDKNoIMA` product instead of `DailymotionPlayerSDK`
- add Google's IMA package: [https://github.com/googleads/swift-package-manager-google-interactive-media-ads-ios](https://github.com/googleads/swift-package-manager-google-interactive-media-ads-ios)

Do not add both Dailymotion products, nor `DailymotionPlayerSDK` together with Google's IMA package: the build fails with `Multiple commands produce ... GoogleInteractiveMediaAds.framework`.

Google's IMA package is required with `DailymotionPlayerSDKNoIMA`: without it the app builds, but crashes at launch with `Library not loaded: @rpath/GoogleInteractiveMediaAds.framework/GoogleInteractiveMediaAds`.

Tested IMA versions: 3.23.0 (embedded), 3.31.0.
