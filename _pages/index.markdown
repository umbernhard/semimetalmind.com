---
layout: page
title: Home
id: home
permalink: /
---

<ul>
  {% assign recent_notes = site.notes | sort: "created" | reverse %}

  <!-- { % for note in recent_notes limit: 5 % }-->

  {% for note in recent_notes %}
    <li>
      {{ note.created | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
