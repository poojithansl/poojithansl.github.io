---
layout: default
title: Archive
permalink: /archive/
---

<ul class="archive-list">
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%B %Y" %}
  {% if currentdate != date %}
    <li><a href="#{{ currentdate }}">{{ currentdate }}</a></li>
    {% assign date = currentdate %} 
  {% endif %}
{% endfor %}
</ul>