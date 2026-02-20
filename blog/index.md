---
layout: page
title: Blog
---

# Blog

Insights, tips, and practical guidance on Power BI, automation, and working smarter with data.

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}
