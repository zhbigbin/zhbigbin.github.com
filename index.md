---
layout: index
title: 首页
---
{% include JB/setup %}
#<h2>正在阅读 <a href="{{ HOME_PATH }}book" style="font-size:18px">(更多...)</a></h2>
#<div class="row-fluid">
#    <ul class="thumbnails">
#    {% for book in site.categories.book | limit:3 %}
 #       <li class="span3">
  #          <div class="thumbnail"> 
     #           <a href="{{ book.url }}" class="thumbnail"> 
     #               <img style="width: 200px; height: 270px;" class="img-rounded" alt="{{book.title}}" src="book/covers/{{ book.cover }}">
      #          </a>
      #          <div class="caption">
      #              <ul class="tag_box inline">
      #                  {% assign tags_list = book.tags %}
       #                 {% include JB/tags_list %}
       #             </ul>
        #            <h4>作者: {{ book.author }}</h4>
        #            <h4>加入时间: {{ book.date | date: "%Y-%m-%d"}}</h4>
        #            <h4>评星: <span class="allstar{{ book.star }}"></span></h4>
        #            <h4>相关链接: 
        #                {% for link in book.urls %}
        #                <a class="btn btn-primary btn-mini" href="{{ link.url }}">{{ link.text }} </a>
          #              {% endfor %}
        #            </h4> 
        #        </div>
        #    </div>
       # </li>
   # {% endfor %}
  #  </ul>
#</div>
<h2>最新文章 <a href="{{ HOME_PATH }}blog" style="font-size:18px">(更多...)</a></h2>
{% assign blogs_list = site.categories.blog %}
{% assign blogs_limit = 2 %}
{% include custom/blogs_abs %}
