---
title: 
layout: default
permalink: /teaching/
published: true
---


<div class="ProjectContainer">

	<div class="gallery">


  {% for course in site.teaching %}

  {% if course.redirect %}
  <div class="projectTile">
          <a href="{{ course.redirect }}" target="_blank">
          <span>
              <h2>{{ course.title }}</h2>
              <br/>
              <p>{{ course.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="projectTile">
          <a href="{{ course.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ course.title }}</h2>
              <br/>
              <p>{{ course.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
