---
menu_item: true
menu_title: Parent
layout: default
child_category: child
order: 5
---

{% assign child_pages = site.pages | where: "category", page.child_category %}
{% for apage in child_pages %}
- [{{apage.menu_title}}]({{baseurl}}{{apage.url}})
{% endfor %}