
---
layout: default
title: Weekly Development Log
permalink: /devlog/
---

<div class="container">
  <section class="page">

    <div class="eyebrow">THE DEVELOPMENT JOURNEY</div>

    <h1>Weekly <span class="highlight">Updates.</span></h1>

    <p class="intro">
      A week-by-week record of the development process.
      Every update captures what I worked on, what I added,
      what worked, what didn't and what comes next.
    </p>

    <h2>Development Timeline</h2>

    {% for post in site.posts %}

      <a href="{{ post.url | relative_url }}" class="post-card">

        <div class="post-date">
          {{ post.week | default: "WEEKLY UPDATE" }}
          · {{ post.period }}
        </div>

        <h3>{{ post.title }}</h3>

        <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>

        <span class="highlight">READ WEEKLY UPDATE →</span>

      </a>

    {% else %}

      <div class="empty-state">
        <h3>The journey starts here.</h3>
        <p>
          The first weekly development update
          will be published soon.
        </p>
      </div>

    {% endfor %}

  </section>
</div>
