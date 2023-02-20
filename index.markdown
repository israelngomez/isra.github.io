---
title: Index
permalink: /

---




## Welcome to {{site.title}} {{page.title}} 
# Paginacion de posts


<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


![Image](/assets/img/1.jpg)

{% if paginator.total_pages > 1 %}
  <ul class="pagination">
    {% if paginator.previous_page %}
      <li><a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&laquo;</a></li>
    {% else %}
      <li class="disabled"><span>&laquo;</span></li>
    {% endif %}
    {% for page in (1..paginator.total_pages) %}
      {% if page == paginator.page %}
        <li class="active"><span>{{ page }}</span></li>
      {% elsif page == 1 %}
        <li><a href="{{ '/' | prepend: site.baseurl | replace: '//', '/' }}">{{ page }}</a></li>
      {% else %}
        <li><a href="{{ page | prepend: '/page' | prepend: site.baseurl | replace: '//', '/' }}">{{ page }}</a></li>
      {% endif %}
    {% endfor %}
    {% if paginator.next_page %}
      <li><a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">&raquo;</a></li>
    {% else %}
      <li class="disabled"><span>&raquo;</span></li>
    {% endif %}
  </ul>
{% endif %}
