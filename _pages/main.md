---
layout: default
title: Home
nav: true
cursor-blink: true
permalink: /
---

<ul class="post-list">
  {% assign recent_posts = site.posts | slice: 0, 50 %}
  {% for post in recent_posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%m.%y" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
