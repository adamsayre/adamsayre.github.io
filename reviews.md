---
layout: page
title: Reviews
permalink: /reviews/
---

{% for post in site.categories.reviews %}
<li>
{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
<span class="post-meta">{{ post.date | date: date_format }}</span>
<h3>
    <a class="post-link" href="{{ post.url | relative_url }}">
    {{ post.title | escape }}
    </a>
</h3>
    {{ post.excerpt }}
</li>

{% endfor %}
