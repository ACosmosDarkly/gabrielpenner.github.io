---
layout: default
title: Home
nav: true
cursor-blink: true
permalink: /
---

<h2 class="post-h2">Posts</h2>
<hr>
<ul class="post-list">
  {% assign recent_posts = site.posts | slice: 0, 50 %}
  {% for post in recent_posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%m.%y" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<h2 class="post-h2">Books</h2>
<hr>
<ul class="post-list">
  {% assign recent_books = site.books | where_exp: "book", "book.title != 'Reading'" %}
  {% for book in recent_books %}
    <li>
      <span class="post-date">{{ book.date | date: "%m.%y" }}</span>
      <a href="{{ book.url | relative_url }}">{{ book.title }}</a>
    </li>
  {% endfor %}
</ul>
