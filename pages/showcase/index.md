---
layout: cards
title: Showcase
permalink: /showcase/
nocomments: true
---
<div class="container">
<div class="row">
<div class="col">
<div class="card-columns blog">
{% assign sorted = site.showcases | sort:"date" | reverse %}
{% for post in sorted %}
<div class="card hover-shadow mb-3 mb-3">
<a href="{{ post.url }}" title="{{ post.title | escape}}">
<img 
    src="/img{{ post.url }}lqip_{{ post.img }}" 
    data-sizes="auto"
    data-srcset="
        /img{{ post.url }}lqip_{{ post.img }} 25w,
        /img{{ post.url }}low_{{ post.img }} 500w,
        /img{{ post.url }}med_{{ post.img }} 1000w,
        /img{{ post.url }}high_{{ post.img }} 2000w"
    alt="{{ post.caption }}" 
    class="card-img-top lazyload"
>
</a>
<footer class="rounded-bottom">
<a href="/showcase/pattern/{{ post.categories }}" title="Browse other showcases of this pattern">{{ post.categories }}</a> by 
<a href="/showcase/maker/{{ post.author }}" title="Browse other showcases by this maker">{{ post.author }}</a>
</footer>
</div>
{% endfor %}
</div>
</div>
</div>
</div>

