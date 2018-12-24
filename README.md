# wResize
The math behind window anchoring.
-----------------
Example (yes unoptomized)
-----------------
```
#include "mResize.h"
wResize myWindows;

//Only use this line if you created your menu with the neccessary API calls.
//Prior to adding your child windows to the class.
//MyWindows->AddMenuHeight(MainWindow());

//On your window initalizers
HWND hButton1 = GetDlgItem(MainWindow(), IDC_BUTTON1);
myWindows.AddWindow(MainWindow(), hButton1, true, true, true, true); //this example will resize height and width

//On your dialog process callback
case WM_SIZE:		{ return myWindows.ResizeWindows(); }
```
