## 代码来自：
### [UIButtonEdgeInsets](https://github.com/CenterY/UIButtonEdgeInsets)
### [MKButtonStyle](https://github.com/mokong/MKButtonStyle)
### [JXButton](https://github.com/dolacmeng/JXButton)

#### 扩大按钮点击区域
```
@implementation ExpandTouchAreaButton
- (BOOL)pointInside:(CGPoint)point withEvent:(UIEvent*)event
{
    CGRect bounds = self.bounds;
    //最小点击区域 50x50
    CGFloat widthDelta = MAX(50.0 - bounds.size.width, 0);
    CGFloat heightDelta = MAX(50.0 - bounds.size.height, 0);
    bounds = CGRectInset(bounds, -0.5 * widthDelta, -0.5 * heightDelta);
    return CGRectContainsPoint(bounds, point);
}
@end
```
