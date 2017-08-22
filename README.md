# 分别用VUE与JQUERY实现TODOMVC来学习

无论学习什么框架，框架的官示示例都有一个todo demo

都说学会做todolist mvc，才算入门

本示例使用bootstrap样式

通过这个示例，学会了vue的【双向绑定】,【v-for】【事件】,【计算】,【自定义指令】等的应用

[查看todos-vue](http://chenliwen.tech/todolist-bs/todos-vue.html)

[查看todos-jquery](http://chenliwen.tech/todolist-bs/todos-jquery.html)

共同使用本地应用缓存

```javascript
var STORAGE_KEY = 'todos-bs';
var todoStorage = {
  fetch: function () {
    var todos = JSON.parse(localStorage.getItem(STORAGE_KEY) || '[]');
    return todos;
  },
  save: function (todos) {
    localStorage.setItem(STORAGE_KEY, JSON.stringify(todos));
  }
};
```

初始化todos的时候，调用fetch()，而每次检测到todos变化的时候，利用watch调用sava()。

体会到vue的数据驱动DOM的变化的好处和便捷

![效果图](https://raw.githubusercontent.com/ch563/todolist-bs/master/todomvc.jpg)