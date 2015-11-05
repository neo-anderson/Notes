##UI
**Modal**  
A modal view prevents interaction with any other UI until it is dismissed.
A modal view controller is simply a UIViewController class that is presented modally. When the view controller is presented modally it covers whatever the existing view was (using an animation if specified) and the user most somehow dismiss this view before they can return to what they were doing.
To present a view controller in a modal fashion, you can use the method:
```Objective-C
- (void)presentModalViewController:(UIViewController *)modalViewController animated:(BOOL)animated;
```
