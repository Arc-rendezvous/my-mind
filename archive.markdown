---
layout: page
title: Archive
permalink: /archive/
---

<ul>
{% for category in site.categories %}
  <li>{{ category | first | upcase}}
    <ul>
    {% for post in category.last %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%Y-%m-%d" }})</li>
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>
