---
layout: default
title: Arhīvs
---

# Rakstu arhīvs

<ul class="posts">
{% for post in site.posts %}
  <li>
    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    {% assign m = post.date | date: "%-m" %}
    {{ post.date | date: "%-d." }}
    {% case m %}
      {% when '1' %}janvārī
      {% when '2' %}februārī
      {% when '3' %}martā
      {% when '4' %}aprīlī
      {% when '5' %}maijā
      {% when '6' %}jūnijā
      {% when '7' %}jūlijā
      {% when '8' %}augustā
      {% when '9' %}septembrī
      {% when '10' %}oktobrī
      {% when '11' %}novembrī
      {% when '12' %}decembrī
    {% endcase %}
    {{ post.date | date: "%Y." }} gadā
   
  </li>
{% endfor %}
</ul>
