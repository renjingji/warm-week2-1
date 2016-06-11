##视图跳转
####最普通的视图控制器UIViewContoller
* 一个普通的视图控制器一般只有模态跳转的功能，这个方法是所有视图控制器对象都可以用的，而实现这种功能，有两种方法。
    1. 通过方法 - (void)presentViewController:(UIViewController *)viewControllerToPresent animated: (BOOL)flag completion:(void (^)(void))completion跳转。同一个视图控制器，在同一个时间，只能present一个另外的视图控制器。
    2. 通过方法 - (void)performSegueWithIdentifier:(NSString *)identifier sender:(id)sender跳转
    
#### 导航控制器UINavigationController    
1. pushViewController，推出某个视图控制器。返回到控制器的根界面调用popToRootViewController。popViewController弹出当前显示的界面，也就是返回到上个界面。跳转到这个视图控制器的中间的某个界面。popToViewController。
2. performSegueWithIdentifier方法跳转

#### UITabBarController
1. tabbar控制器，一般作为app的根界面视图控制器。UITabBarController的界面跳转其实就是UITabBarController的viewControllers数组中的几个界面切换。只要设置好了UITabBarController的viewControllers数组，切面的切换基本就没我们什么事儿了。