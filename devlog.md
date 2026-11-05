---
layout: default
title: Development Log
permalink: /devlog/
---

<div class="container">
  <section class="page">

    <div class="eyebrow">THE DEVELOPMENT JOURNEY</div>
    <h1>Development <span class="highlight">Log.</span></h1>

    <p class="intro">
      A chronological record of the development process.
      Ideas, experiments, progress, unexpected problems
      and everything learned along the way.
    </p>

    <h2>Latest Entries</h2>

    {% for post in site.posts %}

      <a href="{{ post.url | relative_url }}" class="post-card">
        <div class="post-date">
          {{ post.date | date: "%B %d, %Y" }}
        </div>

        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
        <span class="highlight">READ ENTRY →</span>
      </a>

    {% else %}

      <div class="empty-state">
        <h3>The journey starts here.</h3>
        <p>The first development entries are coming soon.</p>
      </div>

    {% endfor %}

  </section>
</div>
