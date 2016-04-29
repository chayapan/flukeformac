This is Apple's Sandbox Test Case.

App Sandboxing
 - https://developer.apple.com/app-sandboxing/
Checkout the slide
 - http://devstreaming.apple.com/videos/wwdc/2013/710xfx3xn8197k4i9s2rvyb/710/710.pdf




Pre-requisite:

1. set the shebang of setup.py to current python version of your Mac. Possibly this path:

/System/Library/Frameworks/Python.framework/Versions/Current/bin/python2.7

Python 2.7.10 (default, Oct 23 2015, 19:19:21) 
[GCC 4.2.1 Compatible Apple LLVM 7.0.0 (clang-700.0.59.5)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> 

#!/System/Library/Frameworks/Python.framework/Versions/Current/bin/python2.7


2. install dependency from pip (may need sudo)

* appscript
* mutagen

sudo pip install -r requirements.txt


3. build

./setup.py py2app

4. run

open ./dist/Fluke.app

5. failing with following in the log


29/04/2016 5:10:32.826 PM appleeventsd[56]: SecTaskLoadEntitlements failed error=22
29/04/2016 5:10:33.022 PM Fluke[4318]: Fluke Error
29/04/2016 5:10:33.076 PM launchservicesd[82]: SecTaskLoadEntitlements failed error=22
29/04/2016 5:10:33.081 PM launchservicesd[82]: SecTaskLoadEntitlements failed error=22
29/04/2016 5:10:36.018 PM sharedfilelistd[3327]: SecTaskLoadEntitlements failed error=22

