---
title: "[Stub] Tarifs"
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
          <th>Libellé</th>
          <th>Tarif</th>
          <th>Description</th>
      </tr>
      {% endif %}

      {% tablerow pair in prestation %}
        {{ pair[1] }}
      {% endtablerow %}
  {% endfor %}
  </table>
{% endfor %}

This page is a stub for a futher company, those informations aren't real.

Cette page est une ébauche pour une future entreprise, ces informations sont fausses 