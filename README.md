### 第一章  js数据类型

* js里数据类型分为两大类：
1. 基本数据类型
2. 引用数据类型

* 基本数据类型包含五中数据类型：
1. Number 数字
2. String 字符串
3. Boolean 布尔
4. Undefined 未定义
5. Null    空
* 引用数据类型包含1种数据类型： Object 对象
* Object分为5类
1. Object 对象
2. Array  数组
3. Function 函数
4. Date   时间
5. RegExp 正则表达式

下面我们来研究每种具体数据类型里的知识点：

### Number
```
掌握Numbere类型，我们必须记入Number类里的几个函数
1.Number(x)  把参数x转换成Number类型   Number(true)==1  Number(false)==0
2.parseInt(x) 提取x中的整数部分        parseInt(12.56)==12
3.parseFloat(x)提取x中的整数和小数部分  parseFloat('12.56abc')==12.56
3.isNaN(x)     检查x是不是NaN         isNaN(true)==false     
Number 类型数据分为3种： 整数、小数、NaN
NaN:以上（1，2，3）方法将X转换成Number类型，转换失败得到NaN.  如：Number('abc')结果就是NaN
NaN也是Number类型：如下用typeof 方法检查NaN 结果为 ‘number’
typeof NaN == number

```
### String
```
掌握String类型，我们必须知道以下几个知识点：
1.字符串有长度属性    ‘abc’.length==3
2.字符串可以通过下标来获取指定字符    ‘abcd’[0]=='a'   'abcd'[1]=='b'
2.字符串必须用引号包裹  ‘123’ “abc”  'true' "你好"
3.字符串最外层单引号，双引号没有区别，但是同种引号不可以嵌套使用，例如：  
   错误：  “胖平说：“我是唐山黑肥子””
   正确：  '胖平说：“我是唐山黑肥子”'
4.String(x) 把其他数据类型转换层字符串类型   String(100)=='100' String(true)=='true'

```
### Boolean

```
掌握Boolean类型，必须掌握以下知识点
1.Boolean类型 只有两个值 true、false
2.Boolean(x) 把其它类型转换成Boolean类型
  经过Boolean(x)函数转换，结果为false的分析如下表：
  
  
    x的数据类型        x的值
<1>  Number           0/NaN
<2>  String           ""
<3>  Undefined        undefined
<4>  Null             null
<5> Boolean           false

如果x不是以上几个特殊值，结果都为true

Boolean()转换引用数据类型 结果都是true
```
### Undefined
```
1. Undefined类型只有一个值 即： undefined
2. 只声明，不赋值，就是undefined   如下代码：
  var a ;
  console.log(a);    // undefined
```
### Null
```
1.Null类型只有一个值 即： null
2.null表示空，一般将来要赋值一个引用数据类型  如：
  var a=null;
  ...
  ...
  a={name:"胖平"}
  
```
# 第二章 运算
```
 ### 一元运算：
    var b=a++: 加号在后面，先把a赋值给b,在对a进行 +1操作
    var a=100;
    var b=a++;// b=a; a=a+1
    console.log(a);//101
    console.log(b);//100


    var b=++a;加号在前面，先对a进行+1操作，再把a赋值给b
    var a=100;
    var b=++a;// a=a+1;  b=a;
    console.log(a);//101
    console.log(b);//101


   ### 算数运算：
    加法：
    1> 字符串加法就是拼接
    2> 如果不是Number 类型参加运算，首先调用Number方法转换成Number再进行运算
    3>任何数于NaN参加运算，结果都是NaN
       console.log(100+"hello"); //"100hello"
    减法：
    1> 如果不是Number 类型参加运算，首先调用Number方法转换成Number再进行运算
    2>任何数于NaN参加运算，结果都是NaN
    console.log("您的年龄是："-20);//NaN
    console.log(true-10);//-9  Number(true)
    console.log(null-false);//0
    console.log(undefined-null);//NaN
    console.log(undefined-"true");//NaN
    console.log(false-"0");//0
    console.log(""-NaN);//NaN
    console.log(null-"false"-NaN);//0-NaN-NaN=NaN
    乘法：
    1> 如果不是Number 类型参加运算，首先调用Number方法转换成Number再进行运算
    2>任何数于NaN参加运算，结果都是NaN
    除法：
    1> 如果不是Number 类型参加运算，首先调用Number方法转换成Number再进行运算
    2>任何数于NaN参加运算，结果都是NaN

    取余：
    1> 如果不是Number 类型参加运算，首先调用Number方法转换成Number再进行运算
    2>任何数于NaN参加运算，结果都是NaN
    var a=100%3;//1   把100除以3的余数赋值给a
    console.log(a)


   ### 关系运算：
    >、<、<=、>=、==、！=、===、！==

    1.两边都是Number ,直接比较大小
    2.有一边不是Number ,则转换成Number再进行比较
    console.log(null==0);//  false null不会调用Number转换
    console.log(null==undefined);//  true
    console.log(NaN==NaN);//  false
    3.两边都是字符串，比较首字符字符编码的大写
    4.任何值与NaN进行比较，都是false

    console.log("1"==1);//  true
    console.log("1"===1);//false
    console.log("1"!==1);//true
    console.log("1"!=1);//false




   ### 逻辑运算：
      逻辑与    条件1 && 条件2   ；  逻辑或：     条件1 || 条件2      逻辑非 ： ！条件

      逻辑与：
      先把第一个值转换成布尔值
    1.	第一个为true，则返回第二个值
    2.	第一个为false,则返回第一个值


    逻辑或：

    先把第一个值转换成布尔值
    1.第一个值为true,返回第一个值
    2.第一个值为false,返回第二个值

    逻辑非：！

      先对非号右边部分进行布尔转换，在取反

    逻辑非非：！！

     非号有边的部分，取反再取反


   ### 赋值运算：

     三元运算（三目运算）

    条件？ 语句1：语句2；
   if(5>4){alert("对")}else {alert("错")}

    5<4?alert("对"):alert("错");


    运算优先级；
     1. 一元运算 ：  ++  --   ！
     2.* / %
     3.+ -
     4.< <= > >=  == != === !==
     5. &&  ||
     6.=
```
# 第三章 语句
###   if判断语句
```
    1.单支判断语句  if（添加）语句；
    var box=100;
    if(box>50) {alert("box大于50")};

     2.双支条件判断语句：
    if(box>50) {alert("box大于50");}else {alert("box不大于50")}

    3.多支条件判断语句：
    var num=75;
    if(num>=90)
    { alert("A级")}
    else if(num>=80)
    {alert("B级")}
    else if(num>=70)
    {alert("C级")}
    else if(num>=60)
    {alert("D级")}
    else {alert("不及格")}
```
### switch判断语句
```
    switch(值){
     case 1:
     语句1；
     break;
     case 2:
     语句2；
     break;
     case 3:
     语句3；
     break;
     default:
     语句4；
    }
```
###  while()循环语句 do...while()循环语句
```
    while循环语句：  先判断，后执行
    while(循环条件){
       循环语句
    }


    先执行，后判断
    do{
    循环语句
    }while(循环条件)

```
### for执行顺序
```
 

   求：  1+2+3+...+100=?
   var sum=0;
   for(var i=1;i<=100;i++){
       sum+=a;
   }
   console.log(sum);  // 1-100的和2525
   console.log(i);   //最后循环后的i是 101
    // 第一步： var i=1;
    //第二步：i<=100；   如果返回false 循环终止
    //第三步：sum+=a;
    //第四步：i++；  跌代语句
    //第五步：重复二到四步

    for循环 写出 56---1024  所有整数的和
    var sum=0;

    for(var a=56;a<=1024;a++){
        sum+=a;
    }
    console.log(sum);
```
# 第三章 数组方法
```
 ### 数组方法
    
      1.push() 数组后面添加一项或者多项   方法返回新数组的长度
               参数：一个或多个
      2.pop() 数组的后面删除一项  ， 方法返回最后一项
               参数：0个
      3.unshift()  数组前面添加一项或多项， 方法返回新数组的长度
              参数：一个或多个
      4.shift()数组前面删除一项， 返回第一项
             参数：0个

       5. sort() 数组排序

           参数：function(a,b){return a-b}
           升序：function(a,b){return a-b}
           降序：function(a,b){return b-a}
           
      var arr=['刘子豪','陈浩然','刘博','李永林']

             arr.sort(function (a,b) {return a-b})
             arr.sort(function (a,b) {return b.localeCompare(a)})
             console.log(arr);
             
      6.reverse() 将数组倒叙排列  方法的返回时反正后的数组
              没有参数

      7.concat() 数组的连接    方法返回拼接后的新数组
             原数组不发生改变

      8.slice（） 从原数组中获取子数组
            方法返回 获取到的子数组     原数组不发生改变
        两个参数：
        参数一：开始获取到的位置
        参数二：结束获取的位置（可以）
        9.splice()   数组的增删改查
        方法的返回：删除的项组成的数组
        一个参数：开始删除的位置   表示删除
        二个参数：
                参数一：开始删除的位置
                参数二：删除的个数
        三个参数：表示替换
              参数一：开始删除的位置
              参数二：删除的个数
              参数三：替换的内容
         三个参数以上都表示替换


         10.join()将数组转换成字符串
                  var arr=['刘子豪','陈浩然','刘博','李永林']
                  var a=arr.join("+");
                  console.log(a,arr);
                  
```
