# EasingAnimation

![image](http://images.cnitblog.com/i/607542/201403/141558148063393.gif)

This class is used for Easing animation.

 * Easy to understand
 * You can use it to build your own animation



### How to use

 * Import the header 
 
 and use like this:
```
 // 计算好起始值,结束值
 CGFloat oldValue = 0.f;
 CGFloat newValue = 1.f;
 
 // 关键帧动画
 CAKeyframeAnimation *animation = \
 [CAKeyframeAnimation animationWithKeyPath:@"transform.rotation.z"];
 
 // 设置值
 [animation setValues:[YXEasing calculateFrameFromValue:oldValue
 toValue:newValue
 func:ElasticEaseOut
 frameCount:500]];
 
 // 设置持续时间
 animation.duration  = 0.5f;
 
 // 每秒增加的角度(设定结果值,在提交动画之前执行)
 layer.transform = \
     CATransform3DMakeRotation(newValue, 0.0, 0.0, 1.0);
 
 // 提交动画
 [layer addAnimation:animation forKey:nil];
```
enjoy it :)
