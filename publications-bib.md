---
layout: none
permalink: /publications.bib
---
{% assign pubs = site.data.publications | sort: "year" | reverse -%}
{% for p in pubs -%}
{% if p.bibtex and p.bibtex != "" %}{{ p.bibtex }}

{% endif -%}
{% endfor -%}
