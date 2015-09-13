---
layout: page
title: Archive
---

## Blog Posts
<div class="page-archive">
{% for post in site.posts %}
  {% assign post_month_year = post.date | date: "%B %Y" %}
  {% assign newer_post_month_year = post.next.date | date: "%B %Y" %}
  {% if post_month_year != newer_post_month_year %}
    <h3 class="section-header-archive">
      {{ post_month_year }}
    </h3>
  {% endif %}
  <article>
    <a href="{{ post.url | prepend:site.baseurl}}" class="post-title-archive">{{ post.title }}</a>
    <small class="text-muted">{{ post.date | date_to_string }}</small>
	</article>
{% endfor %}
</div>
