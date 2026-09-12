<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <title>我的博客</title>
  <style>
  h1, h2, h3, h4, h5, h6 {
    text-align: center;
  }
</style>
</head>
<body>
  <h1>我的文章列表</h1>
  <ul>
    {% for post in site.posts %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span>{{ post.date | date: "%Y-%m-%d" }}</span>
      </li>
    {% endfor %}
  </ul>
</body>
</html>
