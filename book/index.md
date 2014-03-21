---
layout: book
title: 阅读
group: navigation
---
<h2>我的阅读【{{ site.categories.book | size }}】</h2>
{% for book in site.categories.book %}
<div class="thumbnail row-fluid">
<div class="span3">
<a href="{{ book.url }}"> 
<img style="width: 200px; height: 240px;" class="img-rounded" alt="{{book.title}}" src="/book/covers/{{ book.cover }}">
</a>
</div>
<div class="caption span7">
<h2><a href="{{ book.url }}">{{ book.title }}</a></h2>
<ul class="tag_box inline">
{% assign tags_list = book.tags %}
{% include JB/tags_list %}
</ul>
<h3>作者: {{ book.author }}</h3>
<h3>加入时间: {{ book.date | date: "%Y-%m-%d"}}</h3>
<h3>评星: <span class="allstar{{ book.star }}"></span></h3>
<h3>打卡:</h3>
{% for record in book.records | limit:5 %}
<p> - {{ record.datetime }} : {{ record.content }}</p>
{% endfor %}
</div>
</div>
<br>
{% endfor %}
