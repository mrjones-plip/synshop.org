---
title: Equipment
layout: collection
permalink: /equipment/
collection: equipment
classes: wide
header:
  overlay_image: /assets/images/header_synshop.png
  overlay_color: "#5e616c"
  overlay_filter: 0.5
---

<div class="entries-grid">
{% for equipment in site.data.equipment | sort(by="title", case_sensitive=true) %}

<div class="grid__item">
  <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork">
    <img src="{{equipment.data.image}}" / >
  <h3 class="archive__item-title no_toc" itemprop="headline">
      {% if equipment.data.permalink %}
        <a href="{{ equipment.data.permalink }}">{{ equipment.data.title }}</a> 
      {% endif %}
    {% if equipment.data.blurb %}<p class="archive__item-excerpt" itemprop="description">{{ equipment.data.blurb | markdownify | strip_html | truncate: 160 }}</p>{% endif %}
  </article>
</div>
{% endfor %}
</div>