---
title: "Blog: The Dusty Shelf"
---

{% assign latest = site.posts.first %}

<h2>Latest Post</h2>

<div style="margin-bottom: 3em;">
  <h3><a href="{{ latest.url }}">{{ latest.title }}</a></h3>
  <small>{{ latest.date | date: "%B %d, %Y" }}</small>

  <div style="margin-top: 1em;">
    {{ latest.content | truncatewords: 60 }}
  </div>
</div>

<hr>

<h2>Recent Posts</h2>

{% for post in site.posts offset:1 limit:5 %}
<div style="margin-bottom: 1em;">
  <a href="{{ post.url }}">{{ post.title }}</a><br>
  <small>{{ post.date | date: "%B %d, %Y" }}</small>
</div>
{% endfor %}

<hr>

<h2>Archive</h2>

{% for post in site.posts offset:6 %}
<div style="margin-bottom: 0.8em;">
  <a href="{{ post.url }}">{{ post.title }}</a>
</div>
{% endfor %}
