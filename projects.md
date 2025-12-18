---
layout: guide
title: Projects
description: Projects some of us are involved in or think highly of.
permalink: /projects/
main_nav: true
nav_order: 4
main_classes: -no-top-padding
body_class: theme-projects
image: https://bitcoin.design/assets/images/projects/projects-preview.jpg
---

<!--

Editor's notes

Header illustration source:
https://www.figma.com/file/qzvCvqhSRx3Jq8aywaSjlr/Bitcoin-Design-Guide-Illustrations-CO?node-id=1127%3A7710

-->

<div class="creative-block-hero">
  <div class="creative-block-hero__year">'26</div>
  <div class="creative-block-hero__title">Impact<br>Initiatives</div>
</div>

{% include picture.html
   image = "/assets/images/projects/creative-block--supergraphic.svg"
   alt-text = "Creative block illustration"
   width = 1400
   height = 700
   layout = "full-width"
%}

<section class="intro-text" id="intro-text">
  <p>Explore the high-impact initiatives shaping how Bitcoin will be experienced, understood, and used in the next decade. Each project needs contributors and some need a Directly Responsible Individual to lead the charge.</p>
</section>

{% assign all_categories = site.data.projects.projects | map: "category" | uniq %}
{% assign project_counter = 0 %}
<div class="projects-grid">
  {% for category in all_categories %}
  {% assign category_projects = site.data.projects.projects | where: "category", category %}
  <div class="project-category">
    <div class="project-category__header">
      <span class="project-category__count">{{ category_projects.size }} Projects</span>
      <span class="project-category__name">{{ category }}</span>
    </div>
    <div class="project-category__list">
      {% for project in category_projects %}
      {% assign project_counter = project_counter | plus: 1 %}
      <div class="project-card">
        <div class="project-card__content">
          <span class="project-card__number">{{ project_counter | prepend: '00' | slice: -2, 2 }}</span>
          <div class="project-card__title">{{ project.title }}</div>
          <p class="project-card__desc">{{ project.long_description }}</p>
        </div>
        <div class="project-card__image">
          <img src="/assets/images/projects/guide-icon.svg" alt="">
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
  {% endfor %}
</div>

{% capture community_body %}
<p>Tools and initiatives created by the community to improve Bitcoin experiences.</p>
{% endcapture %}

{% include split-section.html
   class="split-section--reversed"
   graphic_color="#1134F5"
   graphic_bg_image="/assets/images/projects/section--community-project.svg"
   graphic_image="/assets/images/projects/supergraphic--community-projects-grid.svg"
   content_color="#000032"
   label="Community Projects"
   headline="Built by the Community, for Bitcoin"
   body=community_body
   cta_text="View Community Projects"
   cta_url="/community/"
%}

{% capture collabs_body %}
<p>Design collaborations with teams and projects building real-world Bitcoin products.</p>
{% endcapture %}

{% include split-section.html
   class="split-section--reversed split-section--light"
   graphic_color="#9EE6FF"
   graphic_bg_image="/assets/images/projects/section--collaborations.svg"
   content_color="#ffffff"
   label="Collaborations"
   headline="Partnering to Shape Better Bitcoin"
   body=collabs_body
   cta_text="See Collaborations"
   cta_url="/collabs/"
%}

{% capture who_body %}
<ol class="split-section__list">
  <li><strong>Designers</strong> who turn abstract systems into everyday tools</li>
  <li><strong>Artists</strong> who give form to ideas people struggle to name</li>
  <li><strong>Sculptors</strong> who give form to ideas people struggle to name</li>
  <li><strong>Writers & thinkers</strong> who clarify meaning without noise</li>
  <li><strong>Builders</strong> who care how things feel, not just how they function</li>
  <li><strong>Researchers</strong> who ground ambition in lived reality</li>
</ol>
{% endcapture %}

{% include split-section.html
   class="split-section--reversed"
   graphic_color="#9EE6FF"
   graphic_bg_image="/assets/images/projects/creative-block-who--graphic-bg.svg"
   content_color="#001C4E"
   label="Who This Is For"
   headline="We're looking for creatives who can move culture, and make big impressions."
   body=who_body
%}

<section class="ordered-cards-section">
  <div class="ordered-cards-container">
    <div class="ordered-card">
      <div class="ordered-card__square" style="background-color: #81be8c;">
        <img src="/assets/images/projects/ordered-cards/icon--ownership.svg" alt="">
      </div>
      <div class="ordered-card__text">
        <span class="ordered-card__number">01</span>
        <p class="ordered-card__description">Designing how ownership is experienced, not just explained</p>
      </div>
    </div>
    <div class="ordered-card">
      <div class="ordered-card__square" style="background-color: #ffc220;">
        <img src="/assets/images/projects/ordered-cards/icon--designing.svg" alt="">
      </div>
      <div class="ordered-card__text">
        <span class="ordered-card__number">02</span>
        <p class="ordered-card__description">Creating symbols, tools, and standards that travel across the ecosystem</p>
      </div>
    </div>
    <div class="ordered-card">
      <div class="ordered-card__square" style="background-color: #ae66d6;">
        <img src="/assets/images/projects/ordered-cards/icon--high-bar.svg" alt="">
      </div>
      <div class="ordered-card__text">
        <span class="ordered-card__number">03</span>
        <p class="ordered-card__description">Setting a higher bar for clarity, usability, and cultural coherence</p>
      </div>
    </div>
    <div class="ordered-card">
      <div class="ordered-card__square" style="background-color: #015efe;">
        <img src="/assets/images/projects/ordered-cards/icon--resources.svg" alt="">
      </div>
      <div class="ordered-card__text">
        <span class="ordered-card__number">04</span>
        <p class="ordered-card__description">Building shared references others can build on — not one-off artifacts</p>
      </div>
    </div>
  </div>
</section>

---

For more details, see our [Collaboration](https://github.com/BitcoinDesign/Meta/blob/master/Collaboration.md) and [Project](https://github.com/BitcoinDesign/Meta/blob/master/Projects.md) documents. If you are interested in getting involved, reach out in our [Discord]({{ site.discord_invite_url }}).
