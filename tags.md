---
layout: page
title: 文章標籤
---

<h3>Tags Cloud</h3>
{% assign tags = site.tags | sort %}
<div class="tagsblock">
{% for tag in tags %}
 <span class="site-tag">
    <a href="{{ site.baseurl }}/tags/{{ tag | first | slugify }}/"
        style="font-size: {{ tag | last | size  |  times: 4 | plus: 80  }}%">
            {{ tag[0] | replace:'-', ' ' }} ({{ tag | last | size }})
    </a>
 </span>
{% endfor %}
</div>
