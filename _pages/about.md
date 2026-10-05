---
permalink: /
layout: home
title: ""
redirect_from:
  - /about/
  - /about.html
---

<header class="hero">
  <div class="hero__text">
    <h1 class="hero__name">{{ site.author.name }}</h1>
    <p class="hero__role">Ph.D. Student in Data Science</p>
    <div class="hero__meta">
      <span>{% include icon.html name="landmark" %}AML Lab, City University of Hong Kong</span>
      <span>{% include icon.html name="pin" %}{{ site.author.location }}</span>
    </div>
    <div class="bio">
      <p>I am a Ph.D. student in Data Science at City University of Hong Kong, advised by <a href="https://zhaoxyai.github.io/">Prof. Xiangyu Zhao</a> in the <a href="https://aml-cityu.github.io/">Applied Machine Learning Lab</a>. My research interests are human-centered AI and LLM security. Recently, I have been studying persona control in LLM-based user simulation.</p>
      <p>Previously, I received dual B.S. degrees in Electrical Engineering from Zhejiang University and the University of Illinois Urbana-Champaign, where I worked with <a href="https://person.zju.edu.cn/en/houqingchun">Prof. Qingchun Hou</a> on constraint-aware neural networks.</p>
    </div>
    <div class="links">
      <a href="mailto:{{ site.author.email }}">{% include icon.html name="mail" %}Email</a>
      <a href="{{ site.author.googlescholar }}">{% include icon.html name="scholar" %}Google Scholar</a>
      <a href="https://github.com/{{ site.author.github }}">{% include icon.html name="github" %}GitHub</a>
      <a href="https://www.linkedin.com/in/{{ site.author.linkedin }}">{% include icon.html name="linkedin" %}LinkedIn</a>
      <a href="{{ '/files/resume.pdf' | relative_url }}">{% include icon.html name="file" %}CV</a>
    </div>
  </div>
  <img class="hero__photo" src="{{ '/images/profile-portrait.jpg' | relative_url }}" alt="{{ site.author.name }}">
</header>

<section class="section" id="news">
  <h2 class="section__title">{% include icon.html name="news" %}News</h2>
  <ul class="rows">
    <li class="row row--news">
      <span class="row__date">Sep 2026</span>
      <p class="row__main">New preprint on persona control in LLM user simulation, now on <a href="https://arxiv.org/abs/2609.35036">arXiv</a>.</p>
    </li>
    <li class="row row--news">
      <span class="row__date">Aug 2026</span>
      <p class="row__main">Started my Ph.D. at the <a href="https://aml-cityu.github.io/">AML Lab</a>, City University of Hong Kong.</p>
    </li>
    <li class="row row--news">
      <span class="row__date">Mar 2026</span>
      <p class="row__main">T-SKM-Net published in the <a href="https://ojs.aaai.org/index.php/AAAI/article/view/38459">AAAI 2026</a> proceedings.</p>
    </li>
  </ul>
</section>

<section class="section" id="publications">
  <h2 class="section__title">{% include icon.html name="book" %}Publications</h2>
  {% for pub in site.data.publications %}
  <article class="pub">
    <a class="pub__thumb" href="{{ pub.url }}">
      <img src="{{ pub.image | relative_url }}" alt="" loading="lazy">
    </a>
    <div class="pub__body">
      <h3 class="pub__title"><a href="{{ pub.url }}">{{ pub.title }}</a></h3>
      <p class="pub__authors">{{ pub.authors | replace: site.author.name, "<strong>Jiashen Ren</strong>" }}</p>
      <p class="pub__venue"><span class="pub__tag">{{ pub.tag }}</span>{{ pub.venue }}</p>
      <p class="pub__summary">{{ pub.summary }}</p>
      <div class="pub__links">
        {% for link in pub.links %}<a href="{{ link.url }}">{% include icon.html name=link.icon %}{{ link.name }}</a>{% endfor %}
      </div>
    </div>
  </article>
  {% endfor %}
</section>

<section class="section" id="education">
  <h2 class="section__title">{% include icon.html name="scholar" %}Education</h2>
  <ul class="rows">
    <li class="row">
      <p class="row__main">City University of Hong Kong</p>
      <span class="row__date">Aug 2026 – Present</span>
      <p class="row__sub">Ph.D. in Data Science</p>
    </li>
    <li class="row">
      <p class="row__main">Zhejiang University &amp; University of Illinois Urbana-Champaign</p>
      <span class="row__date">Sep 2022 – May 2026</span>
      <p class="row__sub">Dual B.S. in Electrical Engineering</p>
    </li>
  </ul>
</section>

<section class="section" id="experience">
  <h2 class="section__title">{% include icon.html name="flask" %}Research Experience</h2>
  <ul class="rows">
    <li class="row">
      <p class="row__main">Constraint-Oriented Neural Networks for Power-System Optimization</p>
      <span class="row__date">Feb 2025 – Aug 2026</span>
      <p class="row__sub">ZJU-UIUC Institute, with Prof. Qingchun Hou</p>
    </li>
    <li class="row">
      <p class="row__main">DiffSinger-Based Voice Enhancement and Synthesis</p>
      <span class="row__date">Jun 2023 – Aug 2023</span>
      <p class="row__sub">Zhejiang University, with Prof. Zhou Zhao</p>
    </li>
  </ul>
</section>

<section class="section" id="honors">
  <h2 class="section__title">{% include icon.html name="award" %}Honors</h2>
  <ul class="rows">
    <li class="row">
      <p class="row__main">Top Universities Studentship Scheme (TUSS)</p>
      <span class="row__date">2026</span>
      <p class="row__sub">City University of Hong Kong</p>
    </li>
  </ul>
</section>

<section class="section" id="teaching">
  <h2 class="section__title">{% include icon.html name="presentation" %}Teaching</h2>
  <ul class="rows">
    <li class="row">
      <p class="row__main">Teaching Assistant, MATH241 Calculus III</p>
      <span class="row__date">Fall 2025</span>
      <p class="row__sub">University of Illinois Urbana-Champaign</p>
    </li>
    <li class="row">
      <p class="row__main">Teaching Assistant, MATH285 Intro to Differential Equations</p>
      <span class="row__date">Spring 2025</span>
      <p class="row__sub">University of Illinois Urbana-Champaign</p>
    </li>
  </ul>
</section>
