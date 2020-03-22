---
title: Publications
permalink: /publications 
---

[Google Scholar profile](https://scholar.google.com/citations?user=wWN7-O0AAAAJ&hl=en)

{% for item in site.data.publications %}
  <h3>{{ item.year }}</h3> 
  {% for paper in item.papers %}
   {% if forloop.first %}<ul>{% endif %}
    <li>
    {{ paper.authors | replace:"SOCHOR Jakub","<span class='paper-my-name'>SOCHOR Jakub</span>" | replace:" and ",", and "}}.    
    <span class="paper-title">{{ paper.title }}</span>.
    {{ paper.journal }}. 
    {% if paper.notes %} <span class="paper-notes">{{ paper.notes }}</span>. {% endif %}
    </li>
   {% if forloop.last %}</ul>{% endif %}
  {% endfor %}  
{% endfor %}