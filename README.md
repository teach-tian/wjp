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

