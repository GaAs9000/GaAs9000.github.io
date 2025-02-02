---
layout: archive
title: "Photos"
permalink: /photos/
author_profile: true
---

<div class="grid__wrapper">
  {% for photo in site.photos %}
    <div class="grid__item">
      <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
        <div class="archive__item-teaser">
          {% if photo.image %}
            <a href="{{ photo.url | relative_url }}">
              <img src="{{ photo.image | relative_url }}" alt="{{ photo.title }}">
            </a>
          {% endif %}
        </div>
        <h2 class="archive__item-title" itemprop="headline">
          <a href="{{ photo.url | relative_url }}" rel="permalink">{{ photo.title }}</a>
        </h2>
        {% if photo.location %}<p class="archive__item-excerpt" itemprop="location">{{ photo.location }}</p>{% endif %}
        {% if photo.date %}<p class="archive__item-date">{{ photo.date | date: "%B %d, %Y" }}</p>{% endif %}
      </article>
    </div>
  {% endfor %}
</div>
