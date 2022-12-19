---
layout: index
title: "Notes from the Overground"
subtitle: Rex Ledesma
excerpt: "Some thoughts on the journey so far, and yet to come."
seo:
  type: Blog
---
{% capture numposts %}{{ site.posts | size }}{% endcapture %}
{% if numposts != '0' %}

## Posts by Year

{% for post in site.posts %}{% assign currentyear = post.date | date: "%Y" %}{% if currentyear != prevyear %}

### {{ currentyear }}

{% assign prevyear = currentyear %}{% endif %} - {{ post.date | date: '%B %-d' }}: [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}
{% endif %}
