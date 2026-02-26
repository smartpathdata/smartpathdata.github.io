---
layout: default
title: Blog
description: Insights, tips, and practical guidance on Power BI, automation, and working smarter with data.
---

<!-- PAGE HERO -->
<div class="page-hero">
  <div class="page-hero-inner">
    <div class="eyebrow">The SmartPath Blog</div>
    <h1>Practical thinking on <em>data that works</em></h1>
    <p>Insights, tips, and honest guidance on Power BI, automation, and getting more from your data — without the fluff.</p>
  </div>
</div>

<!-- BLOG LIST -->
<section style="padding:80px 5vw 100px;background:#fff;">
  <div class="section-inner">

    {% if site.posts.size == 0 %}
    <div style="text-align:center;padding:4rem 0;">
      <div style="font-size:2.5rem;margin-bottom:1rem;">✍️</div>
      <h3 style="font-family:'DM Serif Display',serif;font-size:1.6rem;color:#0B1F3A;margin-bottom:0.6rem;">Posts coming soon</h3>
      <p style="color:#334E6B;font-size:1rem;font-weight:300;">Check back shortly — practical guides on Power BI, automation, and data workflow design are on the way.</p>
    </div>
    {% else %}

    <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(340px,1fr));gap:2rem;">
      {% for post in site.posts %}
      <a href="{{ post.url }}" style="text-decoration:none;display:block;">
        <article style="border:1.5px solid #E2ECF5;border-radius:12px;padding:2rem;background:#fff;transition:all 0.3s;position:relative;overflow:hidden;height:100%;"
          onmouseover="this.style.transform='translateY(-4px)';this.style.boxShadow='0 8px 32px rgba(11,31,58,0.10)';this.style.borderColor='rgba(30,111,191,0.3)';"
          onmouseout="this.style.transform='';this.style.boxShadow='';this.style.borderColor='#E2ECF5';">
          <!-- Top accent bar -->
          <div style="position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,#1E6FBF,#4AACF0);"></div>

          <!-- Category / date row -->
          <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:1.2rem;margin-top:0.2rem;">
            <span style="font-size:0.75rem;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;color:#1E6FBF;font-family:'DM Sans',sans-serif;">
              {{ post.category | default: "Insight" }}
            </span>
            <span style="font-size:0.8rem;color:#8AA4C0;font-family:'DM Sans',sans-serif;">
              {{ post.date | date: "%b %d, %Y" }}
            </span>
          </div>

          <!-- Title -->
          <h2 style="font-family:'DM Serif Display',serif;font-size:1.3rem;color:#0B1F3A;line-height:1.25;margin-bottom:0.8rem;">
            {{ post.title }}
          </h2>

          <!-- Excerpt -->
          <p style="font-size:0.92rem;color:#334E6B;line-height:1.65;font-weight:300;margin-bottom:1.5rem;">
            {{ post.excerpt | strip_html | truncatewords: 28 }}
          </p>

          <!-- Read more -->
          <div style="display:inline-flex;align-items:center;gap:0.3rem;font-size:0.88rem;font-weight:600;color:#1E6FBF;font-family:'DM Sans',sans-serif;">
            Read article →
          </div>
        </article>
      </a>
      {% endfor %}
    </div>

    {% endif %}
  </div>
</section>

<!-- CTA -->
<section class="cta-strip">
  <h2>Want advice tailored to your situation?</h2>
  <p>I write about what I see working in the real world — and I'm always happy to talk through your specific challenges.</p>
  <a href="/contact" class="btn-white">Book a Free Call →</a>
</section>
