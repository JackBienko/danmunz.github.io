---
layout: page
title: Writing
permalink: /writing/
---

<ul class="post-list">
{% for post in site.posts %}
  <li>
	<span class="post-meta">{{ post.date | date: "%b %-d, %Y" }} / <span class="disqus-comment-count" data-disqus-url="http://localhost:4000{{ post.url | append:'#disqus_thread'}}"></span></span>

    <h2>
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    </h2>

    <p>
    	{% if post.summary %}{{ post.summary }}{% else %}{{ post.excerpt | remove: '<p>' | remove: '</p>' | truncatewords: 50, '…' }}{% endif %}
    </p>
    

    
  </li>
{% endfor %}
</ul>

{% include disqus_comments.html %}