---
title: "Data"
permalink: /data_test/
layout: page
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{https://scholar.google.com/citations?hl=en&user=dGpH9AIAAAAJ&view_op=list_works&sortby=pubdate}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
