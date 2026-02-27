---
layout: default
title: 技术博客
permalink: /blog/
---

# 技术博客

在这里我分享关于深度学习、生成式AI和工程实践的心得体会。

<div class="blog-list">
{% for post in site.posts %}
  <article style="margin-bottom: 40px; padding-bottom: 20px; border-bottom: 1px solid #eee;">
    <h2 style="margin-bottom: 10px;">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <p style="color: #888; font-size: 14px; margin-bottom: 10px;">
      <time>{{ post.date | date: "%Y年%m月%d日" }}</time>
      {% if post.categories %}
      <span style="margin-left: 10px;">
        {% for category in post.categories %}
          <span class="category-tag" style="background: #f0f0f0; padding: 2px 8px; border-radius: 3px; margin-right: 5px;">{{ category }}</span>
        {% endfor %}
      </span>
      {% endif %}
    </p>
    <div style="margin-bottom: 15px;">
      {{ post.excerpt | strip_html | truncate: 200 }}
    </div>
    <a href="{{ post.url | relative_url }}" style="color: #0366d6; text-decoration: none;">
      阅读全文 →
    </a>
  </article>
{% endfor %}
</div>

{% if site.posts.size == 0 %}
<p style="color: #888; font-style: italic; text-align: center; margin-top: 50px;">
  博客文章筹备中,敬请期待...
</p>
{% endif %}