---
layout: page
title: research
permalink: /research/
description: CURRENTLY UNDER CONSTRUCTION
nav: true
nav_order: 2
display_categories: [behavioral, modeling, corpus]
horizontal: false
---

<u>Broadly, my research asks:</u>

What is the role of <b>evidence</b>, or the language input which must be processed to develop language competence, in the acquisition of complex syntactic structures?

*How might we characterize and quantify evidence?

*How does looking at the evidence differently change the way we perceive the learning problem?

Given that there’s cross-linguistic variation and variation in a child’s input, how do children learn <b>which verbs participate</b> in any given complex syntactic structure (e.g. passives, double-object constructions, etc.).

*How can learning the lexical semantics of a verb be informative for children in such a learning task?

<u>Specifically, my research asks:</u>

What can <b>input frequency</b> and <b>lexical semantic features</b> tell us about how children acquire the English verbal passive?

I use a combination of in-depth corpus analysis, computational modeling, behavioral experiments in order to investigate these questions.

Here, you will find research materials that I have made accessible to the public broken down into behavioral experiments, computational modeling, and corpus research. I have also provided the appropriate citations should you wish to make use of this work. If you have any questions, please feel free to contact me.


<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
