---
layout: single
title: Board of Directors
type: page
parent_id: '0'
published: true
password: ''
sidebar:
  nav: "menu"
---

{% assign sorted = site.data.board | sort:"name" %}
{% for member in sorted %}
  <p style="margin-top: 1em;"><a href="mailto:{{ member.email }}">
    {{ member.name }}
  </a>
  {% if member.photo %}
  <img class="align-left" src="{{ member.photo }}">
  {% endif %}
  </p>
  <div style="clear: both"></div>
{% endfor %}
