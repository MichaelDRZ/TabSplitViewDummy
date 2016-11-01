# TabSplitViewDummy
Simple NSSplitViewController inside an NSTabViewController

I made this very simple dummy project to illustrate my problem (using Xcode 8.1 on 10.12.1).
It has a storyboard with an NSTabViewController with 2 tabs, one of which is an NSSplitViewController.
Although everything seems to work perfectly, I see the following warning at runtime:

"TabSplitViewDummy[3615:89221] [Layout] Detected missing constraints for <_NSSplitViewItemViewWrapper: 0x6000001a0d20>.
It cannot be placed because there are not enough constraints to fully define the size and origin.
Add the missing constraints, or set translatesAutoresizingMaskIntoConstraints=YES and constraints will be generated for you.
If this view is laid out manually on macOS 10.12 and later, you may choose to not call [super layout] from your override.
Set a breakpoint on DETECTED_MISSING_CONSTRAINTS to debug. This error will only be logged once."

I've tried to set translatesAutoresizingMaskIntoConstraints=YES for all views as well as setting constraints - nothing worked.
So far I only found out 3 things:

1. when I change the order of the tabs so that the split view is invisible at launch, there is no warning message
2. when I remove the tab view an make the split view content of the window, there is no warning message
3. when I set a symbolic break point on DETECTED_MISSING_CONSTRAINTS, it gets hit 6 times, so I guess there are 6 missing constraints

I've already lost days with this, what am I missing here?

Any help or inputs will be much appreciated!
