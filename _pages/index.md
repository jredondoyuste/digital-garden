---
layout: page
title: Home
id: home
permalink: /
---

take a peek behind the curtain

<strong>recent thoughts</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<span style="font-size: 0.95em; color: #666;">
  I'd love to know what you are thinking about! Feel free to reach out at
  <a href="mailto:your@email.com" style="background: #dfc415ff; color: #222; padding: 0.15em 0.4em; border-radius: 3px; text-decoration: none; font-weight: 500;">
    jaime.redondo.yuste@gmail.com
  </a>
</span>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
