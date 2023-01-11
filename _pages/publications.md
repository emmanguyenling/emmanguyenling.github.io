---
layout: page
permalink: /publications/
title: publications
description: Below is a list of selected places where my research has seen the light of day categorized by date. I have included the citations and any downloadable documents (subject to availability). Please check out my CV for more citations!
years: [2021, 2019, 2018, 2017, 2016, 2015]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
