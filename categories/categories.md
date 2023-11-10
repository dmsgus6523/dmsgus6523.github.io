---
layout: category
---
<h3 class="archive__subtitle">카테고리</h3>

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

<div class="col-lg-4 col-md-2">
  <ul>
    {% for category in site.categories %}
      <li>{{category}}</li>    
    {% endfor%}
  </ul>
</div>

{% include paginator.html %}
