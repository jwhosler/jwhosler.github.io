---
title: The Dusty Shelf
---

<h1>{{ page.title }}</h1>

{% for post in site.posts %}
<div style="margin-bottom: 1.2em;">
  <a href="{{ post.url }}">{{ post.title }}</a><br>
  <small>{{ post.date | date: "%B %d, %Y" }}</small>
</div>
{% endfor %}
