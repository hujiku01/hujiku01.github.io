---
layout: default
title: 前沿科技
category: 前沿科技
---

<div class="main">
  <div class="sidebar">
    当前位置：<a href="{{ '/' | relative_url }}">首页</a> > {{ page.title }}
  </div>

  <div class="az_list" style="width:100%;">
    <div class="az_list_t"><span><em></em>{{ page.title }}</span></div>
    <ul>
      {% for post in site.categories[page.category] %}
      <li>
        <a href="{{ post.url | relative_url }}" title="{{ post.title }}">
          <h2>{{ post.title }}</h2>
          <span>{{ post.date | date: "%Y-%m-%d" }}</span>
          <p>{{ post.excerpt | strip_html | truncate: 100 }}</p>
        </a>
      </li>
      {% else %}
      <li>该分类下暂无文章。</li>
      {% endfor %}
    </ul>
  </div>
</div>
