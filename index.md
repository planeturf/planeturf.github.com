---
layout: blog
title:  Home
---

<h2>Recent Posts</h2>
<ul role="recent-posts">
  {% for post in site.posts do %}
  <li>
    <a href="{{ post.url }}">{{ post.date | date: '%d-%b-%y') }}: {{ post.title }}</a>
  </li>
  {% endfor %}
</ul>
