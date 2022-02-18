---
#
# Here you can change the text shown in the Home page before the Latest Posts section.
#
# Edit cayman-blog's home layout in _layouts instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: default
title: Assignments
ref: assignments
permalink: /assignments.html
---

Posts tagged with `assignment`

<div>
<ul class="post-list">
    {% for post in site.posts %}
    <li>
      {% if post.tags contains 'assignment' %}
        {% assign date_format = site.cayman-blog.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a
            class="post-link"
            href="{{ post.url | absolute_url }}"
            title="{{ post.title }}"
            >{{ post.title | escape }}</a
          >
        </h2>

        {{ post.content }}
      {% endif %}

    </li>
    {% endfor %}

  </ul>
</div>
