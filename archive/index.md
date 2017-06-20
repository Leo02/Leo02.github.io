---
layout:  page
title: 归档
description: 归档
---
<ul class="postlist">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <h2>{{ y }}</h2>
  {% endif %}
                              <li class="archive-post archive-day" data-date="{{ post.date | date:"%Y%m%d" }}">
                            <a class="archive-post-title" href="{{ post.url }}">{{ post.title }}</a>
                            </li>
{% endfor %}
</ul>
