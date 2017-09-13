---
title: Publications
layout: archive
permalink: /publications/
author_profile: true
---

{% capture written_year %}'None'{% endcapture %}

{% for post in site.posts %}
  {% capture year %}{{ post.publication | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
  <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
    {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}