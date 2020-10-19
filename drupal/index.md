---
layout: page
title: Drupal
excerpt: "Drupal es un gestor de contenidos CMS que nos permite desarrollar webs en base a artículos, páginas, imágenes y archivos."
image:
  feature: covers/gota.jpg
  credit: Mayank Dhanawade
  creditlink: https://unsplash.com/@mayank_dhanawade
search_omit: true
---

{% assign categoria = site.data.categories | where:"title","drupal" %}
{{ categoria[0].description }}

<ul class="post-list">
{% for post in site.categories.drupal %}
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{% include date-es.html date=post.date %}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
