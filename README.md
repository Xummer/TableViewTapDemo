##UITapGesture 和 UITablviewCell 点击冲突解决

```objc
return ![NSStringFromClass([touch.view class]) isEqualToString:@"UITableViewCellContentView"];
```

[stackoverflow传送门](http://stackoverflow.com/questions/8192480/uitapgesturerecognizer-breaks-uitableview-didselectrowatindexpath)