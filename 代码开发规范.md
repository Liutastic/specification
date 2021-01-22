# 代码开发规范

## 文件命名规范

### 文件夹的命名

(大小驼峰、横线、下划线统一)

### 组件文件命名

(大小驼峰、横线、下划线统一)

组件的命名应该语义化，最起码要知道这是一个有什么作用的组件

~~~
submitButton.vue  # 按钮
~~~



**prop的命名**

在html文件中prop一般以-形式的命名出现，在js文件中一般以小驼峰的形式命名

~~~JavaScript
props: {
    myProps: String
}
~~~

~~~html
<component my-props="2333"></component>
~~~

## JavaScript命名规范

### 变量命名

​		常量使用const声明、变量使用let声明，向es6靠拢

1. 变量

   变量命名使用驼峰命名法，命名需要语义化，比如说使用复数表示数组

   ~~~JavaScript
   let names = []
   // let nameList = [] 可
   let name = 'Liu'
   ~~~

   

2. 常量

   经常被引用的字面量应该定义成常量并且放在某个js文件下，需要使用的时候再引入，方便统一管理，命名可以使用大写字母

   ~~~JavaScript
   const BASEURL = 'https://www.whalecloud.com'
   ~~~

3. 方法、函数的命名

   使用驼峰命名法，方法名也应语义化

   ~~~JavaScript
   getStudentList(){} // √
   setStudent(){}
   func(){} // ×
   ~~~

### 注释

1. 工具方法应该写多行注释，注明方法的作用，作者，变量意义，return值意义

   ~~~javascript
   /**
    * @author
    * @description 验证身份证号码
    * @params
    * @return
    */
   function isIDNo(data) {
     return /^(\d{6})(\d{4})(\d{2})(\d{2})(\d{3})([0-9]|X)$/.test(data)
   }
   ~~~

   

2. 代码段中如果有一些相对复杂的需求也需要写注释

### ES6风格编码

1. 字符串可以使用单引号或者反引号，少按一下shift
2. 获取对象或者数组内的值时可以优先使用解构赋值
3. 需要使用函数表达式的时候可以使用箭头函数代替匿名函数

## css(scss)命名规范

1. css中如果有0值，省略0后单位

   ~~~css
   padding-bottom: 0
   ~~~

2. 类的名字使用-命名

   ~~~html
   <div class="my-class">
       
   </div>
   ~~~
