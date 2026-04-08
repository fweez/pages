---
layout: default
title: Pages
---

# Pages

{% assign doc_pages = site.pages | where_exp: "p", "p.dir != '/'" | where_exp: "p", "p.title" | sort: "path" %}
{% assign groups = doc_pages | group_by: "dir" %}

{% for group in groups %}
## {{ group.name | remove_first: "/" | remove: "/" | replace: "-", " " | capitalize }}

{% for p in group.items %}
- [{{ p.title | default: p.name }}]({{ p.url | relative_url }})
{% endfor %}

{% endfor %}
