---
layout: default
lesson-example: "https://carpentries.github.io/lesson-example/"
title: "Learning how to build websites with Jekyll"
---

## Description
{{ site.description }}

{%  assign lead = site.team_members | where:"role", "project lead" | first %}
The project is led by {{ lead.name }}. [See our full team](about#team).

If you want to know more, you can check [the about page](about).

See some [examples of our work]({{ page.lesson-example }}).

## Blog Posts

{% for post in site.posts % | sort: "author" %}
- {{ post.date | date_to_string }}: [{{ post.title }}]({{ post.url }}) by {{ post.author }}
{% endfor %}
