---
layout: blog
title: Blog
permalink: /blog/
---

## Latest Posts

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%b %d, %Y" }}
{% endfor %}
