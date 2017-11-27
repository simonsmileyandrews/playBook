# iOS Development Fundamentals

This document contains concepts that are important for iOS development at Outware. iOS has a massive SDK, but these are the areas that we commonly use.

Get comfortable navigating and understanding [Apple’s documentation](https://developer.apple.com/library/ios/navigation/): the guides, frameworks and class documentation.

If you are new to the language then readning [Programming with Objective-C](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1) is a great place to start.

## Fundamentals

These are the concepts that you should master during induction. They are the fundamental building blocks of iOS and need to be correctly understood.

* Cocoa Design Patterns
  * [Basic programming concepts](https://developer.apple.com/library/content/documentation/General/Conceptual/CocoaEncyclopedia/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010810-CH1-SW1)
  * [MVC](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/MVC.html)
  * [MVVM](https://www.objc.io/issues/13-architecture/mvvm/)
  * [Delegation](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Delegation.html)
  * [Target/action](https://developer.apple.com/library/content/documentation/General/Conceptual/Devpedia-CocoaApp/TargetAction.html)
  * Protocols
    * [What are protocols](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Protocol.html)
    * [Working with protocols](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/WorkingwithProtocols/WorkingwithProtocols.html)
  * [Categories](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Category.html)

* Blocks
  * [Getting started](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/Blocks/Articles/bxGettingStarted.html)
  * [A practical guide to blocks](https://developer.apple.com/library/ios/featuredarticles/Short_Practical_Guide_Blocks/index.html#//apple_ref/doc/uid/TP40009758)
  * How can blocks be replaced with delegation?

* View Controllers
  * [About view controllers](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Introduction.html#//apple_ref/doc/uid/TP400)
  * [Various init methods](https://developer.apple.com/library/content/documentation/General/Conceptual/CocoaEncyclopedia/Initialization/Initialization.html)
  * [UIWindow](https://developer.apple.com/documentation/uikit/uiwindow), [UIViewController](https://developer.apple.com/documentation/uikit/uiviewcontroller), [UIView](https://developer.apple.com/documentation/uikit/uiview) and how they work
  * loadView (when not using XIB files)
    * Add subviews here
  * Lifecycle (using XIBs, not using XIBs)
    * init
    * [loadView](https://developer.apple.com/documentation/uikit/uiviewcontroller/1621454-loadview)
    * [awakeFromNib](https://developer.apple.com/documentation/objectivec/nsobject/1402907-awakefromnib)
    * viewDidLoad
    * viewWillAppear. viewDidAppear
    * viewWillDisappear, viewDidDisappear
  * Be wary of [ViewControllers becoming overloaded](http://www.objc.io/issue-1/)

* Create a view using a XIB file
  * initWithCoder
* [UINavigationController](https://developer.apple.com/documentation/uikit/uinavigationcontroller)
* Autolayout
  * [Understanding autolayout](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/index.html)
  * [Using interface builder](https://developer.apple.com/xcode/interface-builder/)
* UITableViewController
  * [About tableViews in iOS](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/TableView_iPhone/AboutTableViewsiPhone/AboutTableViewsiPhone.html)
* Memory Management
  * Manual/pre-ARC (retain/release/autorelease)
    * Examples:
      * ` NSString *string1 = [NSString string];`
      * ` NSString *string2 = [[NSString alloc] init];`
      * ` NSString *string3 = [[NSString stringWithFormat:@"%d",5] retain];`
      * ` NSString *string4 = [[[NSString alloc] init] autorelease];`
      * ` NSString *string5 = [[NSString string] autorelease];`
    * When leaving a method should I ever call release?
    * When leaving a method should I ever call autorelease?
  * [ARC](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AutomaticReferenceCounting.html)
* [Properties](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/DeclaredProperty.html)
  * strong/retain
  * weak/assign
  * copy
  * readwrite
  * readonly
* BDD (Behaviour Drived Design) Testing using Kiwi
  * [Testing guides and articles](https://www.objc.io/issues/15-testing/)


## Advanced Concepts

These are further concepts that you should learn over your time as an iOS developer. You don't need to master these concepts during induction, but you will likely come across them as a developer and might find them interesting points to learn about.

* [Common patterns](https://www.raywenderlich.com/160651/design-patterns-ios-using-swift-part-12)
  * [Singleton](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Singleton.html)
  * Categories
  * Data manager
    * Caching
  * [Synchronous and asynchronous calls](https://medium.com/ios-os-x-development/managing-async-code-in-swift-d7be44cae89f)
    * Completion Blocks
    * [Futures](https://medium.com/@johnsundell/under-the-hood-of-futures-promises-in-swift-69bd6e7ab972) (promises)
  * Paging views
    * Page controls
    * Lazy loading data
    * Vertical or horizontal paging
    * UICollectionViews
* UIKit components
  * UIWebView
  * UISplitViewController
  * UITabBarController
  * UISegmentedControl
  * UIActivityViewController Sheets
    * iOS6 style
    * iOS7 style
  * [MFMailComposer](https://developer.apple.com/documentation/messageui/mfmailcomposeviewcontroller)
  * UISearchDisplayController
* Other Apple APIs
  * ABAddressBook
  * [NSNotificationCenter](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/Notifications/Articles/NotificationCenters.html)
    * Local reminders
  * [Push Notifications](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)
  * [Location](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/LocationAwarenessPG/Introduction/Introduction.html)
    * Location services
      * Find your current location
      * Track your current location as you move
    * Geo coding
    * Reverse geo coding
    * Maps
      * Annotations
      * Region to view
      * Cameras (iOS7)
      * GET/POST data requests
  * [CoreData](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/CoreData/index.html)
    * [MagicalRecord](https://github.com/magicalpanda/MagicalRecord)
    * Versioning of data model
    * Fetched properties
    * Predicates
  * Media playback using
    * [MPMoviePlayer](https://developer.apple.com/documentation/mediaplayer/mpmovieplayercontroller)
    * AVAudioPlayer
  * Multitasking
    * GrandCentralDispatch
    * NSProcess
* Common 3rd Party APIs
  * AFNetworking
  * [RestKit](https://github.com/RestKit/RestKit/wiki)

While working your way through this remember it is not an exhaustive list, it is instead a good foundation on which to build your development knowledge base.
