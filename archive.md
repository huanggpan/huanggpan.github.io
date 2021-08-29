---
layout: page
title: "Archive"
description: "文章归档"
header-img: "img/green.jpg"
---


<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <h3 class="listing-seperator">{{ y }}</h3>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}"><u style="color:blue">{{ post.title }}</u></a>
  </li>
{% endfor %}
</ul>
