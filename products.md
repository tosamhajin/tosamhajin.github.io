---
title: "제품 정보 모음"
description: "제품 정보 페이지 모음입니다."
layout: single
permalink: /products/
---

{% assign items = site.products | sort: "title" %}

<div class="product-list">
  {% for p in items %}
    <a class="product-card" href="{{ p.url }}">
      <div class="product-card__title">{{ p.title }}</div>
      {% if p.description %}
      <div class="product-card__desc">{{ p.description }}</div>
      {% endif %}
    </a>
  {% endfor %}
</div>
