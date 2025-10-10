---
layout: default
title: "Blog"
---

<h2>Blog Posts</h2>
<input type="text" id="blog-search-input" placeholder="Search by date or keyword...">

<ul class="blog-post-list">
{% for post in site.posts %}
  <li data-keywords="{{ post.tags | join: ' ' }}">
    <a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date }})
  </li>
{% endfor %}
</ul>

<script src="/assets/js/blog-search.js"></script>