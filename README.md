# CHIPageControl with SPM Support

CHIPageControl is a set of cool animated page controls to replace boring UIPageControl.
We were inspired by [Jardson Almeida dribbble shot](https://dribbble.com/shots/2578447-Page-Control-Indicator-Transitions-Collection) and implemented a few more page controls.
Fork is created for usage with Swift Package Manager

Made with ❤️ by [Chili Labs](https://chililabs.io).

## Overview

<img src="Images/demo.gif" width="600" height="450">

## Requirements

* iOS 8.0+
* Xcode 8+
* Swift 3

## Installation
- Go to File -> Swift Packages -> Add Package Dependency...
- Then search for https://github.com/iivanu/CHIPageControl.git
- And choose the version you want


## Usage
### 🎨 Storyboards
Just drop UIView and set its class to be one of CHIPageControls.
<img src="Images/ibdesignable.gif" width="800" height="564">
### 💻 Code
``` swift
let pageControl = CHIPageControlAji(frame: CGRect(x: 0, y:0, width: 100, height: 20))
pageControl.numberOfPages = 4
pageControl.radius = 4
pageControl.tintColor = .red
pageControl.currentPageTintColor = .green
pageControl.padding = 6
```

### Adding multiple tintColors
``` swift
// The size of the array needs to match the numberOfPages or it will throw an fatal error
pageControl.tintColors = [UIColor.black, UIColor.yellow, UIColor.black, UIColor.black]

// or

// If it is the first one, it will fill all colors with the selected tintColor and then replace the colors with the desired one
pageControl.insertTintColor(UIColor.yellow, position: 1)
```

### Updating progress
``` swift
//update dynamically
pageControl.progress = 0.5

//set progress with animation
pageControl.set(progress: 2, animated: true)
```

### Touch events

You can hear touch events in any of the page indicators. 
``` swift
pageControl.enableTouchEvents = true
```

### Delegate

Implement the `CHIBasePageControlDelegate` to catch touch events.

```swift
func didTouch(pager: CHIBasePageControl, index: Int)
```

### Page Controls 🌶️🌶️🌶️

<img src="Images/Aji.gif" width="100" height="50"> CHIPageControlAji

<img src="Images/Aleppo.gif" width="100" height="50"> CHIPageControlAleppo

<img src="Images/Chimayo.gif" width="100" height="50"> CHIPageControlChimayo

<img src="Images/Fresno.gif" width="100" height="50"> CHIPageControlFresno

<img src="Images/Jalapeno.gif" width="100" height="50"> CHIPageControlJalapeno

<img src="Images/Jaloro.gif" width="100" height="50"> CHIPageControlJaloro

<img src="Images/Paprika.gif" width="100" height="50"> CHIPageControlPaprika

<img src="Images/Puya.gif" width="100" height="50"> CHIPageControlPuya

## License
CHIPageControl is released under the MIT license. See [LICENSE](./LICENSE) for details.
