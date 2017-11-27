
# CCAnimationBtn
A simple subclass of UIButton imitates the animation effect of favor button in DouYin App. 

一个UIButton子类，模仿抖音App中点赞按钮的动画效果

---
# CCAnimationBtn
-------------

### 效果:
![image]()

### 示例:  
```oc
CCAnimationBtn *btn = [[CCAnimationBtn alloc] initWithFrame:CGRectMake(60, 60, 150, 150)];
    [btn addTarget:self action:@selector(btnClicked:) forControlEvents:UIControlEventTouchUpInside];
    [self.view addSubview:btn];
    
-(void)btnClicked:(UIButton *)btn{
    btn.selected = !btn.selected;
}
```

### 特性
- 可配置项: 线条数量、线条末端宽度、线条长度相对比例、动画总时长、中心图片相对比例等。

- 需自行替换2种状态的图片 

### 原理说明
绘制放射线，使用CAShapeLayer结合mask绘制多个三角形图层
动画主要使用CABasicAnimation进行缩放，位移，旋转，透明度等属性进行动画

### 使用方法
直接下载工程，拷贝CCAnimationBtn.h与.m文件，(调整参数)即可使用

### 注意事项
- 需自行替换2种状态的图片。
- 含有CASpringAnimation，需要iOS 9.0+

## License
none

