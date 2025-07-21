---
layout: page
title: Blog
permalink: /blog/
---

<div class="blog-list">
{% for post in site.posts %}
<div class="blog-item">
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <small>{{ post.date | date: "%b %d, %Y" }}</small>
  <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
</div>
{% endfor %}
</div>

<style>
.blog-list {
  display: grid;
  gap: 1.5rem;
  padding: 1rem;
}
.blog-item {
  padding: 1rem;
  border-bottom: 1px solid var(--border-color);
}
@media (max-width: 600px) {
  .blog-list { gap: 1rem; }
  .blog-item { padding: 0.75rem 0; }
}
</style>
