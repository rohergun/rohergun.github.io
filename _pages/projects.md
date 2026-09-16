---
layout: page
title: projects
permalink: /projects/
description: A growing collection of your cool projects.
nav: true
nav_order: 1
---

<!-- pages/projects.md -->
<div class="projects-list">
{% assign sorted_projects = site.projects | sort: "importance" %}
{% for project in sorted_projects %}
  <a class="project-list-item" href="{{ project.url | relative_url }}">
    <h2 class="project-list-title">{{ project.title }}</h2>
    <p class="project-list-description">{{ project.description }}</p>
    {% if project.tech_stack %}
      <p class="project-list-tech">
        {% for tech in project.tech_stack %}<span class="tech-badge">{{ tech }}</span>{% endfor %}
      </p>
    {% endif %}
  </a>
{% endfor %}
</div>
