# ChoiceFrame  
MVP模式搭建布局框架

# MVP模式  
### Model 逻辑  
Model提供逻辑处理的方法，例如：接口请求、手机号规则验证等功能性的方法  
### View 视图  
View提供视图控制的方法，例如：等待层的开启与关闭、按钮颜色的变换等视图变换的方法  
### Presenter 交互  
Presenter提供交互方案，例如：接口请求需要关闭等待层，这里就需要将View对象传入Model这样就能提供改变视图的方法  
### 使用
充分利用Java的多态和interface的特点，创建接口View，定义改变视图的方法，让Activity实现该接口并重写改变视图的方法  

这样Activity只重写改变视图的方法，View接口只定义视图改变的方法（视图这一层基本就可以搭建好了）  

创建类Model，在这里定义View接口对象并在构造方法里面初始化，那么在这里写的处理逻辑的方式都可以调用View接口改变视图的方法了  

创建类Presenter，在这里定义View接口对象并在构造方法里面初始化，并在这里创建Model对象传入View接口对象  

View[Activity]创建Presenter对象，对Presenter里面的方法进行调用  

# 说明  
将界面和逻辑分开,不再都在activity里面处理了,减轻了activity负担,并且使代码更加的层次话,不再担心改页面的时候不小心改了逻辑,改逻辑时候不小心动了页面  
按照MVP的思想可以看出来大部分的代码都将写入View[Activity]和Model，Presenter承担的代码很少，是不是可以删除  
从代码层面上面时完全可以删除的，但是不建议这么做，View不会直接操作Model，Presenter将View和Model分离得更加彻底，避免View和Model混淆得情况  

# 效果展示  

# APK下载  
