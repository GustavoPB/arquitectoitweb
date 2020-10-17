---
layout: page
title: Apache
excerpt: "Artículos relativos al servidor Apache y cómo poder sacarle el máximo partido a sus configuraciones para tener un servidor web optimizado"
image:
  feature: covers/pluma.jpg
  credit: Alexander Sinn
  creditlink: https://unsplash.com/@swimstaralex
search_omit: true
---

{% assign categoria = site.data.categories | where:"title","apache" %}
{{ categoria[0].description }}

<ul class="post-list">
{% for post in site.categories.apache %}
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{% include date-es.html date=post.date %}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
