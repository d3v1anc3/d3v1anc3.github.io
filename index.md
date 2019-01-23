---
layout: page
title: Welcome
tagline: Proof of Concepts
---
{% include JB/setup %}

Read [Jekyll Quick Start](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)

Complete usage and documentation available at: [Jekyll Bootstrap](http://jekyllbootstrap.com)

    
## Blog Posts
<ul class="posts">
  {% for post in site.posts %}
    {% if post.layout contains 'post' %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

### Recommended
#### Books
<ul class="posts">
  {% for post in site.posts %}
    {% if post.layout contains 'book' %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

#### Visual Studio Extensions
<ul class="posts">
  {% for post in site.posts %}
    {% if post.layout contains 'extension' %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

### Snippets
<ul class="posts">
  {% for post in site.posts %}
    {% if post.layout contains 'note' %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
