Order properly for better readability

```Objective-C
self.titleLabel.text = title;
self.titleImage.hidden = YES;
self.titleLabel.hidden = NO;

To -
self.titleLabel.text = title;
self.titleLabel.hidden = NO;
self.titleImage.hidden = YES;
```
