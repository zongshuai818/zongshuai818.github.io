---
title: "Lanco Lab - Team"
layout: gridlay
excerpt: "Lanco Lab: Team members"
sitemap: false
permalink: /team/

# tab or 4 spaces in markdown in code blocks
---

# Group Members

{% for group in site.data.members %}
  <h2>{{ group.group }}</h2>
  
  {% assign number_printed = 0 %}

  {% for member in group.members %}
    {% assign even_odd = number_printed | modulo: 2 %}
    {% if even_odd == 0 %}
<div class="row">
    {% endif %}
    
<div class="col-sm-6 clearfix">
<h4>{{ member.name }}</h4>

  {% if member.info %}
<i>{{ member.info }}</i>
  {% endif %}

<ul style="overflow: hidden">
      {% if member.number_educ == 1 %}
<li> {{ member.education1 }} </li>
      {% endif %}
</ul>
</div>

    {% if even_odd == 1 %}
</div>
    {% endif %}

    {% assign number_printed = number_printed | plus: 1 %}

  {% endfor %}

  {% assign even_odd = number_printed | modulo: 2 %}
  {% if even_odd == 1 %}
</div>
  {% endif %}

{% endfor %}
