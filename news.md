---
layout: page
title: News
permalink: /news/
"feature-img": img/header-nologo.jpg
published: true
---

# The latest CENTRA events and information

<div>
{% for news in site.news reversed %}
<div class="post-teaser">
	<h2>
	  <a href="{{ news.url | prepend: site.baseurl }}">
		{{ news.title }}
	  </a>
	</h2>
	<p class="meta">
	  {{ news.date | date: "%B %-d, %Y" }}
	</p>
  <div class="excerpt">
	<p>{{ news.excerpt }}</p>
	<a class="btn btn-default" href="{{ news.url | prepend: site.baseurl }}">
	  {{ site.theme.str_continue_reading }}
	</a>
  </div>
</div>
<p>&nbsp;</p>
{% endfor %}
</div>
