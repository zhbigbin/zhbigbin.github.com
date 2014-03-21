---
layout: blog 
title: 博客
group: navigation
---
{% include JB/setup %}
<h2>我的文章【{{ site.categories.blog | size }}】</h2>
{% assign blogs_list = site.categories.blog %}
{% include custom/blogs_abs %}
