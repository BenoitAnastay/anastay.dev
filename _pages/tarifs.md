---
title: Tarifs
layout: splash
permalink: /tarifs
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
---

{% for entry in site.data.tarifs %}
<h2>{{ entry.category }}</h2>
  <table>
  {% for prestation in entry.prestations %}
      {% if forloop.first %}
      <tr>
        {% for pair in prestation %}
          <th>{{ pair[0] }}</th>
        {% endfor %}
      </tr>
      {% endif %}

      {% tablerow pair in prestation %}
        {{ pair[1] }}
      {% endtablerow %}
  {% endfor %}
  </table>
{% endfor %}