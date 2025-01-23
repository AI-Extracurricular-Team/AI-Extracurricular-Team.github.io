---
layout: page
title: Weekly Challages
---

{% for challage in site.challages %}
  <h3>{{ challage.name }}</h3>
  {% if challage.level == "hard" %}
    <span style="color:#dc3545">Level: Hard</span>
  {% elsif challage.level == "hard" %}
    <span style="color:#fd7e14">Level: Medium</span>
  {% else %}
    <span style="color:#198754">Level: Easy</span>
  {% endif %}
  <p>{{ challage.description | markdownify }}</p>
  <a href="{{ challage.url }}" class="btn btn-primary">View</a>
  <hr/>
{% endfor %}
