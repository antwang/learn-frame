# 项目框架搭建

## 注意的问题

`postcss-preset-env` 是否自动给 `css` 添加前缀以及添加什么前缀，依赖于要支持的浏览器列表。浏览器列表有以下几种配置方式：

1. `package.json` 中的 `browserslist` 字段中配置，也是官方推荐的方式。
2. 在 `.browserslistrc` 或者 `browserslist` 配置文件中配置
3. 在 `BROWSERSLIST` 环境变量中配置

如果没有找到有效的浏览器列表，`postcss-preset-env` 会使用默认值：`> 0.5%, last 2 versions, Firefox ESR, not dead`。表示的浏览器范围是：

1. 市场份额大于 0.5% 的浏览器；
2. 各个厂商最新两个版本的浏览器；
3. Firefox ESR 浏览器；
4. 剔除以上所有的浏览器中 2 年内未更新的浏览器。

在 `package.json` 中添加 `browserslist` 字段:

```
"browserslist": [
    "> 0.5%",
    "last 2 versions"
  ]
```

我们指定的浏览器范围中有一部分浏览器对 `transform` 属性的支持需要添加浏览器厂商前缀，我们可以在构建后访问页面进行验证。
