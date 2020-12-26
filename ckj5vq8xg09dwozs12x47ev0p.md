## How To Change App's StatusBar Colour In Android

# Problem: 

I have an activity which I am using to host three fragments connected to a BottomNavigationView, on users touch events I want to change status bar colours to a different color for each of the fragments.

If I use below code in each of the fragment's onViewCreated or onCreateView method it changes activity's status bar colour white or colour light for the fragment using getActivity() method. 


```
getActivity().getWindow.setStatusBarColor(Color.White); 

``` 
using this give code will only work for a white color and this solution does not solve the problem. So after few searches here a solution I have been able to come up with...

# Solution:



```
/**
 * change the status bar color programmatically (and provided the device has Android 
 *  5.0)
 * then you can use Window.setStatusBarColor().
 * It shouldn't make a difference whether the activity is derived from Activity or 
 * ActionBarActivity.
 */
    private fun setStatusBarColor(color: Int) {
        if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.LOLLIPOP) {
            val window: Window = window 
            window.addFlags(WindowManager.LayoutParams.FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS)
            window.statusBarColor = color
        }
    }

``` 


![Screenshot_20201226_161854_com.chydee.statusbarcolortutorial.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1608997380197/McPIT77VM.jpeg)


![Screenshot_20201226_161856_com.chydee.statusbarcolortutorial.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1608997421176/7yE7W4xzz.jpeg)



![Screenshot_20201226_161858_com.chydee.statusbarcolortutorial.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1608997429897/TIbV8hAP9.jpeg)


That's it. Simple Implementation.

Code:  [https://github.com/chydee/StatusBar-Tutorial](https://github.com/chydee/StatusBar-Tutorial)

Happy Coding ;)

 