---
layout: home
---

# NetLogo Resources

A curated list of NetLogo resources: libraries, guides, tools, and more.

---

{% assign categories = site.data.resources | map: "category" | uniq | sort %}
{% for category in categories %}
## {{ category }}

{% assign items = site.data.resources | where: "category", category %}
{% for resource in items %}
### [{{ resource.title }}]({{ resource.url }})

{{ resource.description }}

{% if resource.authors %}
**Authors:** {{ resource.authors | join: "; " }}
{% endif %}

---
{% endfor %}
{% endfor %}
