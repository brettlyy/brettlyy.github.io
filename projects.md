---
layout: page
title: Projects
permalink: /projects/
---

<div class="row" id="project-cards">
{% for project in site.projects %}
  <div class="col-md-6 mb-4">
    <div class="card h-100 project-card">
      {% if project.project-image %}
        <a href="{{ project.url | relative_url }}"><img class="card-img-top" src="{{ project.project-image | relative_url }}" alt="{{ project.title }}"></a>
      {% endif %}
      <div class="card-body">
        <h4 class="card-title"><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h4>
        <p class="card-text">{{ project.excerpt }}</p>
      </div>
      <div class="card-footer">
        <a href="{{ project.url | relative_url }}" class="btn btn-primary">Read More</a>
      </div>
    </div>
  </div>
{% else %}
  <div class="col-12">
    <p>I have no projects here yet. Stay tuned for more!</p>
  </div>
{% endfor %}
</div>
