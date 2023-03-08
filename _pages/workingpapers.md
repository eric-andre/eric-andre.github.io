---
layout: page
permalink: /wp/
title: research
description: 
years: [2023, 2022, 2020]
nav: true
nav_order: 2
---
<!-- _pages/workingpapers.md -->
<div class="publications">
<h2>submitted</h2>
{% bibliography -f submitted %}

</div>

<div class="publications">
<h2>work in progress</h2>
{% bibliography -f workinprogress %}

</div>

<div class="publications">
<h2>working papers</h2>
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f workingpapers -q @*[year={{y}}]* %}
{% endfor %}

</div>
