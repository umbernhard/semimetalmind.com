---
layout: page
title: Home
id: home
permalink: /
---

<ul>
  {% assign recent_notes = site.notes | sort: "date" | reverse %}

  <!-- { % for note in recent_notes limit: 5 % }-->

  {% for note in recent_notes %}
    <li>
      {{ note.date | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
