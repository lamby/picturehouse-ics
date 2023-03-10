---
layout: default
---

<a href="https://www.picturehouses.com/">
    <img src="assets/logo.png?{{ site.github.build_revision }}" height="100">
</a>

<body>

<h1>ICS files for Picturehouse Cinemas</h1>

<ul>
{% for cinema in site.data.cinemas %}
<li>
    <a href="ics/{{ cinema.slug }}.ics?{{ site.github.build_revision }}">{{ cinema.name }}</a>
</li>
{% endfor %}
</ul>
