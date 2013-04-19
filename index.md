---
layout: page
title: Weblog
tagline: Catapult's digital diary
---
{% include JB/setup %}

<article class="animated fadeIn">
	{% for post in site.posts limit:1 %}
	<h1><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h1>
	<span>{{ post.date | date_to_string }}</span>
	{{ post.content}}
	{% endfor %}
</article>

## Archive

<ul id="archive" class="posts animated fadeIn">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &middot; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
