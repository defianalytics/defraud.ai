---
title: "Podcasts"
permalink: "/podcasts.html"
---

<ol class="list-featured">
    {% for podcast in site.podcasts reversed %}
    <li class="mb-4">
      <span>
        <h6 class="font-weight-bold">
          <p class="text-dark">{{ podcast.title }}</p>
        </h6>
        <audio controls preload="auto">
          <!-- <source src="{{ podcast.ogg }}" type="audio/ogg"> -->
          <source src="{{site.baseurl}}{{ podcast.mp3 }}" type="audio/mpeg">
          Your browser does not support the audio element.
        </audio>
      </span>
    </li>
    {% endfor %}
  </ol>