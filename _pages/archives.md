---
layout: page
title: Categories
permalink: /archives
---

<h2>ARCHIVES</h2>

<h3> Category: </h3>
<ul>
{% for category in site.categories %}
  <li>
    <a href="categories/{{ category[0] }}">{{ category[0] }} ({{ category[1].size }})</a>
  </li>
{% endfor %}
</ul>

<h3> Date: </h3>

<ul>
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    <div style="text-decoration:underline; font-weight: bold; margin-top:20px" id="y{{currentdate}}">{{ currentdate }}</div>
    {% assign date = currentdate %}
  {% endif %}
    <li>{{ post.date | date: '%b %d'}} <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}



</ul>


