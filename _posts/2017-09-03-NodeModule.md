---
　　layout: default
　　title: 你好，世界
---

## Node模块化详细讲解

> 前言
>
> > Nodejs是服务端的javascript，它的模块化遵循CommonJs规范，CommonJs规范的主要内容有
> >
> > - 定义全局函数require，通过传入模块标识来引入其他模块，执行的结果即为别的模块暴漏出来的API
> > - 如果被require函数引入的模块中也包含依赖，那么依次加载这些依赖
> > - 如果引入模块失败，那么require函数应该报一个异常
> > - 模块通过变量exports来向往暴漏API，exports只能是一个对象，暴漏的API须作为此对象的属性。

### 初级

 - 使用module.exports或exports来创建模块
 - 使用require(path)来引入模块

​        

```javascript
//mathutil.js，使用exports
exports.add=function(a,b){
  return a+b;
}
exports.sub=function(a,b){
  return a-b;
}
```

```javascript
//index.js
var mathutil=require('./mathutil');
console.log(mathutil.sub(1,2));
console.log(mathutil.add(1,2));
```

这里我们通过给exports添加add和sub属性，向外暴露了求和和求差的方法

```javascript
//mathutil.js，使用module.exports

```

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}



