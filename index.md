---
layout: default
title: Introduction
---

{% for post in site.posts %}
<div class="mod post">
  <h2>{{ post.title }}</h2>
  <p class="quiet"><image src="/images/clock.png" />  {{ post.date | date_to_string }} </p>
  <p>{{ post.content }}</p>
</div>
{% endfor %}
