---
title: "Podcasts"
permalink: "/podcasts.html"
---

{% assign posts = site.posts | where_exp: "item", "item.categories contains 'Podcast'" %}

<ol class="list-featured">
  {% for post in posts %}
  <li class="mb-4">
    <span>
      <h6 class="font-weight-bold">
        <p class="text-dark">{{ post.title }}</p>
      </h6>
      <audio controls preload="metadata">
        <source src="{{site.baseurl}}/{{ post.audio }}" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <p class="text-muted">{{ post.date | date: '%b %d, %Y' }}</p>
    </span>
  </li>
  {% endfor %}
</ol>