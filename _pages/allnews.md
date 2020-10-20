---
title: "News"
layout: textlay
excerpt: "Lanco Lab at Peking University."
sitemap: false
permalink: /allnews.html
---

<!-- # News -->

**Notice**

The laboratory recruits highly-self-motivated undergraduate intern students and visiting graduate students in natural language processing and deep learning. Please e-mail the teacher and attach your resume.

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
{% endfor %}
