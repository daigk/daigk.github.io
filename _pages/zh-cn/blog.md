---
page_id: blog
layout: default
permalink: /blog/
title: 博客
blog_name: 学术博客
description: 研究、教学与相关记录
nav: false
pagination:
  enabled: true
  collection: posts
  permalink: /page/:num/
  per_page: 5
  sort_field: date
  sort_reverse: true
  trail:
    before: 1
    after: 3
---

<div class="post">

{% assign blog_name_size = page.blog_name | size %}
{% assign blog_description_size = page.description | size %}

{% if blog_name_size > 0 or blog_description_size > 0 %}
  <div class="header-bar">
    <h1>{{ page.blog_name }}</h1>
    <h2>{{ page.description }}</h2>
  </div>
{% endif %}

{% include latest_posts.liquid %}
</div>
