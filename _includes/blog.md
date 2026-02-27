<h2 id="blog" style="margin: 2px 0px -15px;">Blog Posts</h2>

<div class="publications">
<ul style="list-style-type: none; padding: 0;">

{% for post in site.posts limit:5 %}
<li style="margin-bottom: 20px;">
  <div class="pub-row">
    <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </div>
      <div class="author" style="color: #888;">
        {{ post.date | date: "%Y年%m月%d日" }}
      </div>
      <div style="margin-top: 10px;">
        <p style="font-size: 14px;">{{ post.excerpt | strip_html | truncate: 150 }}</p>
      </div>
      <div class="links">
        <a href="{{ post.url | relative_url }}" class="btn btn-sm z-depth-0" role="button" style="font-size:12px;">阅读全文</a>
      </div>
    </div>
  </div>
</li>
{% endfor %}

</ul>
</div>

<div style="text-align: center; margin-top: 20px;">
  <a href="/blog/" class="btn btn-sm z-depth-0" role="button" style="font-size:14px;">查看所有博客文章 →</a>
</div>