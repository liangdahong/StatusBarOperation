# 状态栏操作总结

## 情况分类和Demo
### 启动界面显示状态栏 + 全部界面显示状态栏
> 不做任何操作，默认即可 [Demo](https://github.com/asiosldh/StatusBarOperation/tree/master/2%E5%90%AF%E5%8A%A8%E6%98%BE%E7%A4%BA/1%E5%90%AF%E5%8A%A8%E6%98%BE%E7%A4%BA-%E5%85%A8%E9%83%A8%E7%95%8C%E9%9D%A2%E6%98%BE%E7%A4%BA)

### 启动界面显示状态栏 + 全部界面隐藏状态栏
> 在Info.plist 加 `View controller-based status bar appearance` 设`YES`
> 
> 全部控制器重写`prefersStatusBarHidden ` 返回`YES` [Demo](https://github.com/asiosldh/StatusBarOperation/tree/master/2%E5%90%AF%E5%8A%A8%E6%98%BE%E7%A4%BA/2%E5%90%AF%E5%8A%A8%E6%98%BE%E7%A4%BA-%E5%85%A8%E9%83%A8%E7%95%8C%E9%9D%A2%E9%9A%90%E8%97%8F(%E5%A5%87%E8%91%A9))

### 启动界面显示状态栏 + 界面自定义状态栏的显示和隐藏
> 在Info.plist 加 `View controller-based status bar appearance` 设`YES`
> 
> 在需要隐藏的控制器重写`prefersStatusBarHidden ` 返回`YES`
> 
> 在需要显示的控制器重写`prefersStatusBarHidden ` 返回`NO`（或者不重写）[Demo](https://github.com/asiosldh/StatusBarOperation/tree/master/2%E5%90%AF%E5%8A%A8%E6%98%BE%E7%A4%BA/3%E5%90%AF%E5%8A%A8%E6%98%BE%E7%A4%BA-%E7%95%8C%E9%9D%A2%E8%87%AA%E5%AE%9A%E4%B9%89)

### 启动界面隐藏状态栏 + 全部界面显示状态栏
>在Info.plist 加 Status bar is initially hidden 设`YES` [Demo](https://github.com/asiosldh/StatusBarOperation/tree/master/1%E5%90%AF%E5%8A%A8%E9%9A%90%E8%97%8F/1%E5%90%AF%E5%8A%A8%E9%9A%90%E8%97%8F-%E5%85%A8%E9%83%A8%E7%95%8C%E9%9D%A2%E6%98%BE%E7%A4%BA)

### 启动界面隐藏状态栏 + 全部界面隐藏状态栏
>在Info.plist 加 Status bar is initially hidden  设`YES`
>
>在Info.plist 加 View controller-based status bar appearance 设 `NO`[Demo](https://github.com/asiosldh/StatusBarOperation/tree/master/1%E5%90%AF%E5%8A%A8%E9%9A%90%E8%97%8F/2%E5%90%AF%E5%8A%A8%E9%9A%90%E8%97%8F-%E5%85%A8%E9%83%A8%E7%95%8C%E9%9D%A2%E9%9A%90%E8%97%8F)

### 启动界面隐藏状态栏 +  界面自定义状态栏的显示和隐藏
>在Info.plist 加 Status bar is initially hidden  设`YES`
>
> 在Info.plist 加 `View controller-based status bar appearance` 设`YES`（或者不加）
> 
> 在需要隐藏的控制器重写`prefersStatusBarHidden ` 返回`YES`
> 
> 在需要显示的控制器重写`prefersStatusBarHidden ` 返回`NO`（或者不重写）
>[Demo](https://github.com/asiosldh/StatusBarOperation/tree/master/1%E5%90%AF%E5%8A%A8%E9%9A%90%E8%97%8F/3%E5%90%AF%E5%8A%A8%E9%9A%90%E8%97%8F-%E7%95%8C%E9%9D%A2%E8%87%AA%E5%AE%9A%E4%B9%89)
