---
layout: page
title: Photography
permalink: /photography/
collection: pages
---

Here is my photo.

<div class="photo-grid">
{% for file in site.static_files %}
  {% if file.path contains "images/photography/" %}
    <a href="{{ site.baseurl }}{{ file.path }}" data-lightbox="gallery">
      <img src="{{ site.baseurl }}{{ file.path }}" alt="" loading="lazy">
    </a>
  {% endif %}
{% endfor %}
</div>

<style>
.photo-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 14px;
}

.photo-grid img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 4px;
}
</style>

