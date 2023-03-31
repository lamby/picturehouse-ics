---
layout: default
---

<a href="{{ site.github.repository_url }}"><img decoding="async" loading="lazy" width="149" height="149" src="https://github.blog/wp-content/uploads/2008/12/forkme_right_darkblue_121621.png?resize=149%2C149" class="attachment-full size-full" alt="Fork me on GitHub" data-recalc-dims="1"></a>

<a href="https://www.picturehouses.com/">
    <img src="assets/logo.png?{{ site.github.build_revision }}" height="100">
</a>

<body>

<h1>ICS files for Picturehouse Cinemas</h1>


<ul>
{% for cinema in site.data.cinemas %}
<li>
    {{ cinema.name }} (<a href="ics/{{ cinema.slug }}.ics?{{ site.github.build_revision }}">ICS</a>,
        <a href="https://larrybolt.github.io/online-ics-feed-viewer/#feed={{ site.url|url_encode }}{{ site.baseurl|url_encode }}/ics/{{ cinema.slug }}.ics%3F{{ site.github.build_revision }}&cors=false&title={{ cinema.name|url_encode }}">View</a>)
</li>
{% endfor %}
</ul>

<p><a href="{{ site.github.repository_url }}/commit/{{ site.github.build_revision }}">Last update</a></p>
