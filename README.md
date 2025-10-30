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

## Installation

### Swift Package Manager

Add the package dependency to your project:

```swift
dependencies: [
    .package(url: "https://github.com/dailymotion/player-sdk-ios", from: "1.0.0")
]
```

### Core SDK (Without Chromecast)

If you **don't need** Chromecast support or want to avoid conflicts with custom casting implementations:

```swift
.target(
    name: "YourApp",
    dependencies: [
        .product(name: "DailymotionPlayerSDK", package: "player-sdk-ios")
    ]
)
```

Then import in your code:
```swift
import DailymotionPlayerSDK
```

### With Chromecast Support (Optional)

If you need Chromecast support, add **both** products:

```swift
.target(
    name: "YourApp",
    dependencies: [
        .product(name: "DailymotionPlayerSDK", package: "player-sdk-ios"),
        .product(name: "DailymotionChromecast", package: "player-sdk-ios")
    ]
)
```

Then import in your code:
```swift
import DailymotionPlayerSDK
import DailymotionChromecast  // Only if you need Chromecast
```

> **Note**: The `DailymotionChromecast` module includes the Google Cast SDK, which uses a singleton pattern. Only import this module if you specifically need Chromecast functionality to avoid conflicts with custom audio casting implementations.
