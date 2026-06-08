---
layout: none
permalink: /publications.bib
---
{% assign pubs = site.data.publications | sort: "year" | reverse -%}
{% for p in pubs -%}
{% if p.title and p.title != "" -%}
{% assign fa = p.authors | split: "," | first | strip | split: " " | last -%}
{% assign tw = p.title | replace: "*","" | strip | split: " " | first | replace: ":","" | replace: ",","" -%}
{% assign citekey = fa | append: p.year | append: tw -%}
{% include bibtex.html p=p key=citekey %}
{% endif -%}
{% endfor -%}
