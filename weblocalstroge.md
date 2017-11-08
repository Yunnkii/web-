## WEB本地存储

web本地存储分为两类：

- 本地存储-------localStorage对象-------长期保存----站内访问
- 会话存储-------sessionStorage对象------临时保存窗口数据----关闭窗口数据消失

关系：操作完全相同，区别在于数据的寿命，与网站所在的域有关，与计算机有关，本地存储一般在5MB以下。

### 存取数据

```
localStorage.setItem(keyname,data);
//举例
localStorage.setItem("user_name","Mike");
//获取数据
localStorage.getItem("user_name");
```

> localStorage 本地存储在服务器下使用

### 删除数据

```
localStorage.removeItem("user_name");
//清空网站在本地保存的会话数据
sessionStorage.clear();
```

### 查找所有数据项

```
for(var i = 0;i<localStorage.length;i++){
	//取得当前位置数据项的键
  var key = localStorage.key(i);
  var item = localStorage.getItem(key);
}
```

### 保存数值和日期

WEB本地存储的数值和日期是以字符串的形式存储的，所以要进行相应的转化，不然计算方面会出现问题。

数值：

```
x = Number(localStorage.getItem("num"));
x = x+10;
```

日期：

