# Underscore.js常用的方法介绍

标签（空格分隔）： Underscore.js

---
###1. 集合相关方法

reduce方法依次对集合的每个成员进行某种操作，然后将操作结果累计在某一个初始值之上，全部操作结束之后，返回累计的值。该方法接受三个参数。第一个参数是被处理的集合，第二个参数是对每个成员进行操作的函数，第三个参数是累计用的变量。
```
     _.reduce([1, 2, 3], function(memo, num){ return memo + num; }, 0);
    // 6
```
reduce方法的第二个参数是操作函数，它本身又接受两个参数，第一个是累计用的变量，第二个是集合每个成员的值。

----------
 
 map方法对集合的每个成员依次进行某种操作，将返回的值依次存入一个新的数组。
 
```
_.map({name:'whynyist',age:123},function(num,key) {
	return key;
});
//["name", "age"]

 _.map([1,2,3],function(num){
	return num + 1;
});
//[2, 3, 4]

_.map({name:'whynyist',age:123},function(num,key) {
	return num;
});		
//["whynyist", 1234]
```

