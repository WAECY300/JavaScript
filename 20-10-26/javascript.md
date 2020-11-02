#了解Java Script
<hr/>
html ----结构层 --搭建网页页面主体结构

css  ----表现层 --对页面的主体结构进行样式渲染

js   ----行为层 --页面内出现的事件交互效果等，如按钮被点击。
         发红包 --点击按钮---显示、跳转页面（一块页面结构）。输入数据--点击按钮

<hr/> 
客户端:用户操作的页面

服务端:数据显示（玩）的页面 ---服务器--数据--- mysql   php  node 

javascript 是浏览器解析执行的客户端脚本语言

javascript的学习分为3部分  {核心模块}

    1.js的标准学习 ECMAscript，现在学习的标准为ES5/ES6
    2.BOM Browser Object Moudle 浏览器 对象 模型
    3.DOM Document Object Moudle 文档 对象 模型
    
## javascript的使用

 1.在标签上可以为html标签 添加js的一些事件方法
 2.在script标签内书写js
 3.外部引入js文件

 onclick            单击事件
 onblur             失去焦点事件
 onfocus            获取焦点事件
 onsubmit           数据提交事件 -该方法只能添加到form元素上
 onmouseout         鼠标移出事件    
 onmouseover        鼠标移入事件
 onkeydown          键盘按下事件
 onkeyup            事件会在键盘按键被松开时发生
 ondblclick         事件会在对象被双击时发生
 
国企：A
私企：B
个体：C
群众：

### 特殊字符需要转义符 [转义符:\n,\t,\r,\\,\',\"]

## javascript的输出数据方式
    1.console.log
        控制台输出
    2.alert()
        警告框输出
    3.prompt()
        输入框---需要有变量接收输入框输入的值
    4.confirm()
        确认框---需要有变量接收确认框返回的布尔值
    5.document.write()
        向页面中写入或追加----使用较少
        
## 声明变量

作用域--->{}

    1.var           
            var---声明的变量不会有强制性的作用域
            可重复定义
            值可以改变
            var a;
            a =233;
            console.log(a);//233
    2.const
            const---常量
            常量--不可变更的变量
            常量在定义时，变量名都使用大写
            值不可改变
            var b = 233;
            console.log(b);//233
            b = 100;//ERROR 常量不可更改
    3.let
            let---有作用域范围
            在同一作用域内不可重复定义
            可改变值
            不允许变量重复声明
            let a;
            a = 233;
            console.log(a);
            let a =100; ERROR a已经存在，不可重复定义
            a = 100;
            console.log(a);//100
         
    4.class
    
## 运算符
    一.算数运算符
        算数运算符中，如果遇到字符串类型的数字，可以选择*1来转换为数字
        也可以选择使用：
            1.parseInt()取整数
            2.parseFloat() 取小数
            3.Number() 转换为数字
                a.在一个变量的值中，如果遇到不能转换成数字的，直接转换成NaN
                b.例如：
                c.  let num ='12345.13adc'
                    console.log(Number(num));//NaN
                    console.log(parseInt(num));//12345
                    console.log(parseFloat(num));//12345.23
                    console.log(num*1);//NaN
                    
         保留小数位,可以使用数字方法toFixed(),该方法只能针对数字使用。count表示几位小数
         
        1.+
            加法
        2.-
            减法
        3.*
            乘法
        4./
            除法
        5.%
            取余数（模）
        6.+=
            a+=3<==>a=a+3
        7.-=
        8.*=
        9./=
        10.%=
        11.=
            赋值（将等号右边的值赋值给左边）
    二.比较运算符
        1.>
        2.<
        3.==
            比较等号左右俩边的值是否相等 类型可以不相等
        4.>=
        5.<=
        6.!=
            不等
        7.===
            完全相等
            等号左右俩边的值，必须完全相等，类型也要相等
        8.!==
            不完全相等
      三.NaN
        not a Number(不是一个数)
        NaN和任何数相加都是NaN
        NaN和字符串相加 = 数值拼接
        
      四. isNaN
        is NaN 是  不是一个数
                //isNaN()
                //对一个值判断，是否为数字
                //当判断的值不为数字的时候，返回true;为数字，则返回false
                ----------------
                let b ='132.354.67vc';
                console.log(isNaN(Number(b)));
------------------------------------------------------------
### 前++ 和 前--
    
    #### 实例：
            let a =10;
            let b =++a;//前++运算
            console.log(a,b);//
            a输出为11;b输出为11
            
            前++的运算理论（先进行算术运算，再进行赋值）

### 后++ 和 后--
            
            let c = 10;
            let d = 3;
            console.log(c,d);//9,10
            后++、后--  (先赋值，再运算)
---------------------------------------------------               
### 条件运算符
        > < = >= <= == != === !===
        
### 逻辑运算符
    1.&&
    
        a.逻辑与
        并存的关系，2个以上的条件都必须完全成立
        在逻辑与的关系内，只要有一个条件不成立，则直接返回false
        当逻辑与的条件判断内，所有的条件都成立，则返回true
        不为0的数字 都可以转为true
        不为""的字符串都可以转为true
        
    2.||
    
        b.逻辑或
        值要有一个条件为true，则表达式成立
        当条件中，有条件不成立的时候，则连续判断。当所有条件不成立，则返回false;否则值要有一个条件为true,则成立
    3.!
        c.逻辑非
        取相反的值
        let a =true;
        let b =!a;
        console.log(a);
        console.log(b);
        
### 三目运算符

    由？和：组成
    条件语句 ？ 条件为true执行的代码:条件为false执行的代码
    
    let a =parseInt(Math.radom() * 10);
    console.log(a);
    let b = a>=5 ? '对';'错';
    console.log(b);
    
    let c = b == '张三' ? fun('兴欣',b) :fun('蓝雨',b);
    
    console.log(c);
    function fun(){
        if(temp== '欣欣'){
            console.log('.....');
        }else{
            console.log(',,,,,,');
        }
        return temp+user;//return终止并返回结果。当前范围内的代码会停止向下执行
        console.log('.......')
    }
    
            
        
    