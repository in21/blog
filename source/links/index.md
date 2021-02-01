---
title: 友情链接
date: 2021-02-01 22:25:36
---

<div id="links">
<div class="links-content">
<div class="link-navigation">
{% for link in site.data.links %}
<div class="card">
  <a href="{{ link.site }}" target="_blank">
  <img class="ava" src="{{ link.avatar }}"/></a>
  <div class="card-header">
  <div><a href="{{ link.site }}" target="_blank">{{ link.name }}</a></div>
  <div class="info" title="{{ link.info }}">{{ link.info }}</div>
  </div>
</div>
{% endfor %}
</div>
</div>
</div>
