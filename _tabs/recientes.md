---
title: Actualizado recientemente
icon: fas fa-history
order: 7
---
<!-- Sección de Actualizado Recientemente -->
<div class="mt-4">
  <ul class="list-unstyled">
    {% assign updated_posts = site.posts | sort: "last_modified_at" | reverse %}
    {% for post in updated_posts %}
      <li class="py-1">
        <a href="{{ post.url | relative_url }}" class="text-muted">
          [{{post.last_modified_at | default: post.date}}] {{ post.title }}
        </a>
      </li>
    {% endfor %}
  </ul>
</div>
