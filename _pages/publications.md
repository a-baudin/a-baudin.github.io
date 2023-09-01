---
layout: page
permalink: /publications/
title: All publications
description: Publications by categories in reversed chronological order. 
inconf: [2023,2022]
injournal: [2021,2019]
frconf: [2023]
preprint: [2023]
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->

<div class="publications">

<h2>International conferences</h2>

{%- for y in page.inconf %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}} && inconf = true]%}
{% endfor %}

<h2>International journals</h2>

{%- for y in page.injournal %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}} && injournal = true] %}
{% endfor %}

<h2>Preprints</h2>

{%- for y in page.preprint %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}} && preprint = true]%}
{% endfor %}

<h2>French-speaking conferences</h2>

{%- for y in page.frconf %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}} && frconf = true]%}
{% endfor %}

</div>

