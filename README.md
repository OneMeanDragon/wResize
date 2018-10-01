# wResize
The math behind window anchoring.
-----------------
Example
-----------------
```
#include "mResize.h"
wResize myWindows;

//On your window initalizers
HWND hButton1 = GetDlgItem(MainWindow(), IDC_BUTTON1);
myWindows.AddWindow(MainWindow(), hButton1, true, true, true, true); //this example will resize height and width

//On your dialog process callback
case WM_SIZE:		{ return myWindows.Resize(); }
```
