---
layout: home
title: Arsa raksti
---

{% for post in site.posts limit:10 %}
<div class="post-summary">
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p class="post-excerpt">
    {{ post.excerpt }}

    <p>
        {% assign months = "janvāris,februāris,marts,aprīlis,maijs,jūnijs,jūlijs,augusts,septembris,oktobris,novembris,decembris" | split: "," %}
        {% assign month = post.date | date: "%-m" | minus: 1 %}
        {{ post.date | date: "%-d." }} {{ months[month] }} {{ post.date | date: "%Y" }}. gads
        <a href="{{ post.url | relative_url }}">Lasīt tālāk ...</a>
    </p>
  </p>
</div>
<hr>
{% endfor %}
