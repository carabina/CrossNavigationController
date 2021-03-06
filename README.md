# CrossNavigationcontroller

Move to cross using `UINavigationController`

[![CocoaPods Compatible](http://img.shields.io/cocoapods/v/CrossNavigationcontroller.svg?style=flat)](http://cocoadocs.org/docsets/CrossNavigationcontroller)
[![Swift 3.0](https://img.shields.io/badge/Swift-3.0-orange.svg?style=flat)](https://developer.apple.com/swift/)

<img src="https://github.com/hryk224/CrossNavigationcontroller/wiki/images/sample.gif" width="320" >

<img src="https://github.com/hryk224/CrossNavigationcontroller/wiki/images/sample2.gif" width="320" >

## Requirements
- iOS 9.0+
- Swift 3.0+
- ARC

## install

#### CocoaPods

Adding the following to your `Podfile` and running `pod install`:

```Ruby
use_frameworks!
pod "CrossNavigationcontroller"
```

### import

```Swift
import CrossNavigationcontroller
```

## Usage

 * Change `UINavigationController` to `CrossNavigationcontroller`
 * Change `UIViewController` to `CrossViewController`
 * If want to use Gesture, set `CrossGestureControllable` protocol at CrossViewController subclass

### Move (push, pop)

```Swift
func moveViewController(_ viewController: CrossViewController, direction : Cross.Direction, animated: Bool)
```

`Cross.Direction` => `.up` or `.down` or `.left` or `right`

### Move to root

```Swift
// UINavigationController method
func moveToRootViewController(animated: Bool) -> [UIViewController]?
```

## Customize

#### If change the start coordinates

In `CrossNavigationcontroller` 

```Swift
override func viewDidLoad() {
  super.viewDidLoad()
  setUp(initialCoordinate: (X, Y))
}
```

#### If use custom transition

In `CrossNavigationcontroller` 

```Swift
override func navigationController(_ navigationController: UINavigationController, animationControllerFor operation: UINavigationControllerOperation, from fromVC: UIViewController, to toVC: UIViewController) -> UIViewControllerAnimatedTransitioning? {
  return CustomTransionAnimator()
}
```

## License

This project is made available under the MIT license. See LICENSE file for details.
