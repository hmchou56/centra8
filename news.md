---
layout: page
title: News
permalink: /news/
"feature-img": img/header-nologo.jpg
published: true
---

# The latest CENTRA events and information

<div>
{% for news in site.news %}
<div class="post-teaser">
  <header>
	<h1>
	  <a class="post-link" href="{{ news.url | prepend: site.baseurl }}">
		{{ news.title }}
	  </a>
	</h1>
	<p class="meta">
	  {{ news.date | date: "%B %-d, %Y" }}
	</p>
  </header>
  <div class="excerpt">
	{{ news.excerpt }}
	<a class="button" href="{{ post.url | prepend: site.baseurl }}">
	  {{ site.theme.str_continue_reading }}
	</a>
  </div>
</div>
{% endfor %}
</div>
