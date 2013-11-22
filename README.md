##UITapGesture 和 UITablviewCell 点击冲突解决

通过添加`UITapGesture` 的 `delegate` 方法 `- (BOOL)gestureRecognizer:(UIGestureRecognizer *)gestureRecognizer` 来解决。

```objc
- (BOOL)gestureRecognizer:(UIGestureRecognizer *)gestureRecognizer
       shouldReceiveTouch:(UITouch *)touch
{
    return ![NSStringFromClass([touch.view class]) isEqualToString:@"UITableViewCellContentView"];
}
```

[stackoverflow传送门](http://stackoverflow.com/questions/8192480/uitapgesturerecognizer-breaks-uitableview-didselectrowatindexpath)

-以上-