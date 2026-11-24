---
title: Home
description: Francisco Del Roio's personal website, featuring his résumé, projects, and contact information.
---

<div class="hero">
  <p class="eyebrow">Backend · APIs · Microservices</p>
  <h1>Hi, I'm Francisco Del Roio.</h1>
  <p class="lead">Welcome to my personal website. Here you can explore my professional background, projects, and ways to get in touch.</p>
  <div class="hero-links">
    <a class="button" href="{{ '/resume/' | relative_url }}">View my résumé</a>
    <a class="text-link" href="{{ '/contact/' | relative_url }}">Get in touch</a>
  </div>
</div>

<section aria-labelledby="explore-heading">
  <h2 id="explore-heading">Explore</h2>
  <div class="card-grid">
    <article class="card">
      <h3><a href="{{ '/resume/' | relative_url }}">Résumé</a></h3>
      <p>Read about my professional background.</p>
    </article>
    <article class="card">
      <h3><a href="{{ '/projects/' | relative_url }}">Projects</a></h3>
      <p>Find selected work and projects as they are added.</p>
    </article>
    <article class="card">
      <h3><a href="{{ '/blog/' | relative_url }}">Blog</a></h3>
      <p>Visit a space for future articles and ideas.</p>
    </article>
  </div>
</section>
