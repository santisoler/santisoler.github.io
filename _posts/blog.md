---
title:  "Blog"
layout: archive
permalink: /blog/
author_profile: true
comments: false
header:
  image: /assets/images/blog/frozen-stream.jpg
---

{% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'"  %}
{% for year in postsByYear %}
  <h2 id="{{ year.name | slugify }}" class="archive__subtitle">{{ year.name }}</h2>
  {% for post in year.items %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
