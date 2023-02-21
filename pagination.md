---
permalink: /pagination

layout: page
---

<div class="posts">
  {% for post in paginator.posts %}
    <article class="post">
      <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
      <div class="entry">
        {{ post.excerpt }}
      </div>
    </article>
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="prev">Anterior</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Siguiente</a>
  {% endif %}
</div>
