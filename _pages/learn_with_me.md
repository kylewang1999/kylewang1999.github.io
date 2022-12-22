---
layout: archive
title: "Learn With Me"
permalink: /learn_with_me/
author_profile: true
---

{% include base_path %}

Sharing my learning journey with all of you!

Previously I was using OneNote for note-taking. It is easy-to-use but very inconvenient for publishing. I am transitioning 
towards [MarkDown](https://www.markdownguide.org)-based note-taking, and I'll try posting as much of them as possible right here.

{% for post in site.learn_with_me reversed %}
  {% include archive-single.html %}
{% endfor %}


