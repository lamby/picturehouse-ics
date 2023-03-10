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
    {{ cinema.name }} (<a href="{{ site.url }}/ics/{{ cinema.slug }}.ics?{{ site.github.build_revision }}">ICS</a>,
        <a href="https://larrybolt.github.io/online-ics-feed-viewer/#feed={{ site.url|url_encode }}/ics/{{ cinema.slug }}.ics%3F{{ site.github.build_revision }}&cors=false&title={{ cinema.name|url_encode }}">View</a>)
</li>
{% endfor %}
</ul>
