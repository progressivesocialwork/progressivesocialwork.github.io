---
layout: page
title: 专题 
permalink: /tags/
---

<div class="tag">
{% for tag in site.tags %}
  <a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}">{{ tag[0] }}</a>
{% endfor %} 
</div>

{% for tag in site.tags %}
#### {{ tag[0] }}
  {% for post in tag[1] %}
- {{ post.date | date:"%Y-%m-%d" }} [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
  {% endfor %}
{% endfor %} 
