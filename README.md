# todos-bs

学习官方todolist示例，一边学习，一边摸索。

都说学会做todolist mvc，才算入门

通过这个示例，学会了vue的【双向绑定】,【v-for】【事件】,【计算】,【指令】等的应用。

[查看todos-bs](http://chenliwen.tech/todolist-bs/todos-bs.html)

利用本地应用缓存

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

![效果图](https://raw.githubusercontent.com/ch563/todolist-bs/master/todomvc.jpg)