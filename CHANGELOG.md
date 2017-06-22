# Change Log
All notable changes to this project will be documented in this file.
`Pageboy` adheres to [Semantic Versioning](http://semver.org/).

#### 1.x Releases
- `1.2.X` Releases - [1.2.0](#120) | [1.2.1](#121)
- `1.1.X` Releases - [1.1.0](#110) | [1.1.1](#111) | [1.1.2](#112)
- `1.0.X` Releases - [1.0.0](#100) | [1.0.1](#101) | [1.0.2](#102) | [1.0.3](#103) | [1.0.4](#104) | [1.0.5](#105) | [1.0.6](#106) | [1.0.7](#107) | [1.0.8](#108) | [1.0.9](#109)

#### 0.x Releases
- `0.4.X` Releases - [0.4.0](#040) | [0.4.1](#041) | [0.4.2](#042) | [0.4.3](#043) | [0.4.4](#044) | [0.4.5](#045) | [0.4.6](#046) | [0.4.7](#047) | [0.4.8](#048) | [0.4.9](#049) | [0.4.10](#0410) | [0.4.11](#0411) | [0.4.12](#0412)

---

## [1.2.1](https://github.com/uias/Pageboy/releases/tag/1.2.1)
Released on 2017-06-19.

#### Updated
- The internal `UIPageViewController` is now inserted at the back of all subviews in the `UIViewController`.
     - The Z-Index will persist when changing `navigationOrientation` and other destructive updates.

## [1.2.0](https://github.com/uias/Pageboy/releases/tag/1.2.0)
Released on 2017-06-18.

#### Added
- [#67](https://github.com/uias/Pageboy/issues/67) Improved support for Right-To-Left languages to `PageboyViewController`.
- `parentPageboyViewController` property to `UIViewController` to provide access to parent `PageboyViewController` from child view controllers within the page view controller.
- [#70](https://github.com/uias/Pageboy/issues/70) Success result to `scrollToPage()` function in `PageboyViewController`.
     - Returns whether the scroll was able to be successfully executed.

#### Fixed
- [#71](https://github.com/uias/Pageboy/pull/71) A potential error during layout with scroll positional updates.
     - By AlexZd.

---

## [1.1.2](https://github.com/uias/Pageboy/releases/tag/1.1.2)
Released on 2017-06-18.

#### Fixed
- Fixed issue with animated transitions when using `.vertical` `navigationOrientation`.
- Add support for `.vertical` `navigationOrientation` to example app.
     - By Charles Molyneux.

## [1.1.1](https://github.com/uias/Pageboy/releases/tag/1.1.1)
Released on 2017-06-12.

#### Updated
- Updated project to use Swift 3.2 and compatibility with Xcode 9

#### Fixed
- Fixed issue where it would be possible to cause an error by setting properties on `PageboyViewController` before the internal `UIPageViewController` was initialised.
- Fixed issue where changing `navigationOrientation` would cause properties on `PageboyViewController` to not persist.

## [1.1.0](https://github.com/uias/Pageboy/releases/tag/1.1.0)
Released on 2017-06-07.

#### Added 
- [#57](https://github.com/uias/Pageboy/issues/57) Added support for custom scroll transitions to `PageboyViewController`.
     - Available via the `.transition` (`PageboyViewController.Transition`) property.

#### Fixed
- [#61](https://github.com/uias/Pageboy/issues/61) Fixed AutoLayout issue with internal `UIPageViewController` when in-call status bar is visible.

---

## [1.0.9](https://github.com/uias/Pageboy/releases/tag/1.0.9)
Released on 2017-05-29.

#### Added 
- Added `delaysContentTouches` property to `PageboyViewController`.

#### Updated
- Minor improvements to example project.
- Minor refactoring to `PageboyViewController` extensions.

## [1.0.8](https://github.com/uias/Pageboy/releases/tag/1.0.8)
Released on 2017-05-17.

#### Updated
- Refactored and restructured internal extensions of `PageboyViewController`.
- A fresh coat of paint.

#### Fixed
- Fixed a few UI issues with example project.

## [1.0.7](https://github.com/uias/Pageboy/releases/tag/1.0.7)
Released on 2017-05-07.

#### Added
- `isTracking` property to `PageboyViewController`.
- Default stub protocol implementations for `PageboyViewControllerDelegate`.

#### Updated
- Updated scroll management to use `isTracking` for interaction detection.

## [1.0.6](https://github.com/uias/Pageboy/releases/tag/1.0.6)
Released on 2017-04-26.

#### Updated
- Moved internal `UIPageViewController` initialisation to `viewDidLoad` from `loadView`.

## [1.0.5](https://github.com/uias/Pageboy/releases/tag/1.0.5)
Released on 2017-04-22.

#### Fixed
- [#44](https://github.com/uias/Pageboy/issues/44) Fix incorrect `scrollToPage` function behaviour when at the end of page ranges with infinite scrolling enabled.
     - `.next` used an incorrect animation when scrolling from the upper range to the lower range.
     - `.previous` failed to scroll to a page when scrolling from the lower range to the upper range.

## [1.0.4](https://github.com/uias/Pageboy/releases/tag/1.0.4)
Released on 2017-04-19.

#### Added
- Added `didReload` function to `PageboyViewControllerDelegate` for updating when the `PageboyViewController` successfully reloads its child view controllers.

## [1.0.3](https://github.com/uias/Pageboy/releases/tag/1.0.3)
Released on 2017-04-16.

#### Updated
- [#42](https://github.com/uias/Pageboy/issues/42) Rename `atIndex(index: Int)` to `at(index: Int)` in `PageboyViewController.PageIndex`.
   - Deprecated `atIndex(index: Int)`.

## [1.0.2](https://github.com/uias/Pageboy/releases/tag/1.0.2)
Released on 2017-04-11.

#### Fixed
- Added support for `preferredStatusBarStyle` in child view controllers.
- Added support for `prefersStatusBarHidden` in child view controllers.
- Added animation for transition of status bar appearance on page change.
- Added missing `addChildViewController` call for internal `UIPageViewController`.

## [1.0.1](https://github.com/uias/Pageboy/releases/tag/1.0.1)
Released on 2017-04-05.

#### Fixed
- [#34](https://github.com/uias/Pageboy/issues/34) Fixed issue in `PageboyAutoScroller` where `.handler` would not be released correctly.

## [1.0.0](https://github.com/uias/Pageboy/releases/tag/1.0.0)
Released on 2017-03-28.

#### Updated
- Just a quick version bump to 1.0.0.