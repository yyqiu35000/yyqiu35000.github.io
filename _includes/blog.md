<!-- <h2 id="blog" style="margin: 2px 0px -15px;">Blog Posts</h2>

<div class="publications" style="margin-top: 20px;">

{% if site.posts.size > 0 %}
  <ul style="list-style-type: none; padding: 0;">
  {% for post in site.posts limit:3 %}
    <li style="margin-bottom: 25px;">
      <div class="pub-row">
        <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
          <div class="title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
          <div class="author" style="color: #888; font-size: 14px; margin-top: 5px;">
            {{ post.date | date: "%Y年%m月%d日" }}
            {% if post.categories %}
              | {% for category in post.categories %}{{ category }}{% unless forloop.last %}, {% endunless %}{% endfor %}
            {% endif %}
          </div>
          <div style="margin-top: 10px;">
            <p style="font-size: 14px; color: #666;">
              {{ post.excerpt | strip_html | truncate: 120 }}
            </p>
          </div>
          <div class="links" style="margin-top: 10px;">
            <a href="{{ post.url | relative_url }}" class="btn btn-sm z-depth-0" role="button" style="font-size:12px;">阅读全文</a>
          </div>
        </div>
      </div>
    </li>
  {% endfor %}
  </ul>
  
  <div style="text-align: center; margin-top: 20px;">
    <a href="/blog/" class="btn btn-sm z-depth-0" role="button" style="font-size:14px;">查看所有博客 →</a>
  </div>

{% else %}
  <p style="color: #888; font-style: italic;">技术博客筹备中,敬请期待...</p>
{% endif %}

</div> -->

<h2 id="blog" style="margin: 2px 0px -15px;">Blog Posts</h2>

<div class="publications" style="margin-top: 20px;">

<!-- 调试信息 -->
<p>博客文章数量: {{ site.posts.size }}</p>

{% if site.posts.size > 0 %}
  <p style="color: green;">✓ 检测到博客文章</p>
  <ul style="list-style-type: none; padding: 0;">
  {% for post in site.posts limit:3 %}
    <li style="margin-bottom: 20px;">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p style="color: #888;">{{ post.date | date: "%Y年%m月%d日" }}</p>
      <p>{{ post.excerpt | strip_html | truncate: 100 }}</p>
      <a href="{{ post.url | relative_url }}">阅读全文 →</a>
    </li>
  {% endfor %}
  </ul>
  
  <div style="text-align: center; margin-top: 20px;">
    <a href="/blog/">查看所有博客 →</a>
  </div>

{% else %}
  <p style="color: #888; font-style: italic;">技术博客筹备中,敬请期待...</p>
  <p style="color: red;">⚠️ 当前没有检测到博客文章</p>
{% endif %}

</div>