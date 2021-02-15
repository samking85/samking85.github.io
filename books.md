---

layout: page
permalink: /books/
title: Books

---
 {% for post in site.categories.books %}

<hr />
<div class="row">
  <div class="span2">
    {% if post.thumbnail %}
	<img src="{{ post.thumbnail }}" align="center" />
	{% else %}
	<img src="/assets/themes/tmtxt-responsive/images/no-thumnail.jpg" align="center" />
	{% endif %}
  </div>
  <div class="span10">
    <p><a href="{{ BASE_PATH }}{{ post.url }}"><h3>{{ post.title }}</h3></a></p>
	<p>{{ post.content | strip_html | truncatewords: 40 }}
	</p>
  </div>
</div>
{% endfor %}


