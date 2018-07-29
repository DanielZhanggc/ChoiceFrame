# ChoiceFrame
使用MVP模式搭建的按钮切换布局框架

#MVP模式
mvp模式由三个部分组成:Model层(逻辑处理) View层(视图层) Presenter层(交互层)

利用Java多态属性(父类的引用指向子类的对象) View层里面定义方法在Activity里面实现 在初始化Presenter层的时候将View层对象传入和一些其他必要参数
之后再Presenter层里面初始化model层,并将view层对象传入model层,这样在model层处理逻辑时可以调用view层方法,实现逻辑和界面的交互

#MVP模式的好处
将界面和逻辑分开,不再都在activity里面处理了,减轻了activity负担,并且使代码更加的层次话,不再担心改页面的时候不小心改了逻辑,改逻辑时候不小心动了页面
