---
layout: page
title: Activities
permalink: /activities/
---

CTFs, conferences, seminars, presentations, and other activities.

{% assign activity_posts = site.categories.activities %}

{% for post in activity_posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: "%Y-%m-%d" }}

{% if post.tags.size > 0 %}
{% for tag in post.tags %}
`#{{ tag }}`
{% endfor %}
{% endif %}

{% endfor %}
