---
layout: page
title: Research
permalink: /research/
---

Research notes and technical write-ups organized by research area.

{% assign sorted_categories = site.categories | sort %}

{% for category in sorted_categories %}
  {% assign category_name = category[0] %}

  {% if category_name != "research" and category_name != "activities" %}

## {{ category_name | replace: "-", " " }}

{% for post in category[1] %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}

  {% endif %}
{% endfor %}
