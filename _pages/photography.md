---
layout: page
title: Photography
permalink: /photography/
---

A small selection of my photography work.

<div class="photo-gallery">
{% for file in site.static_files %}
  {% if file.path contains "images/photography/" %}
    <a href="{{ site.baseurl }}{{ file.path }}" target="_blank">
      <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-thumb">
    </a>
  {% endif %}
{% endfor %}
</div>

<style>
.photo-gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}
.gallery-thumb {
  width: 260px;
  height: auto;
  object-fit: cover;
  border: 1px solid #ddd;
}
</style>
