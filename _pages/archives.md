---
layout: page
title: Categories
permalink: /archives
---

<h2>ARCHIVES</h2>

<ul>
{% for category in site.categories %}
  <li>
    <a href="categories/{{ category[0] }}">{{ category[0] }} ({{ category[1].size }})</a>
  </li>
{% endfor %}
</ul>



<ul>
    {% for post in site.posts %}
      {% unless post.next %}
        <h3>{{ post.date | date: '%Y' }}</h3>
      {% else %}
        {% capture year %}{{ post.date | date: '%Y %b' }}{% endcapture %}
        {% capture nyear %}{{ post.next.date | date: '%Y %b' }}{% endcapture %}
        {% if year != nyear %}
          <h3>{{ post.date | date: '%Y %b' }}</h3>
        {% endif %}
      {% endunless %}

      <li>{{ post.date | date: '%b %d'}} <a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
