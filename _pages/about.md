---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi! I am a passionate and self-motivated researcher. Currently, I am working as a research assistant at the [RAPID Lab](http://lab.sysu-robotics.com) of [Sun Yat-sen University](https://www.sysu.edu.cn/). Previously, I was a game developer at [NetEase Games](https://www.neteasegames.com). I received my master degree at Sun Yat-sen University, advised by Prof. [Hui Cheng](https://cse.sysu.edu.cn/content/2504).

### Interests
- 3D Reconstruction
- (Differentiable) Physical Simulation
- Sim-to-Real (Robotics)

My dream is to conduct interesting and valuable research that closes the gap between virtual reality and physical reality.

<font color="red"><b>I am currently seeking research assistant or Ph.D. opportunities for the 2024/2025 academic year.</b></font>

## Publications ##
***Equal contribution †Corresponding author**

{% assign papers = site.data.pub %}
{% for paper in papers %}
  {% assign authors = paper["authors"] %}
  {% assign materials = paper["materials"] %}
  {% assign title = paper["title"] %}
  {% assign venue = paper["venue"] %}
  
  {% if paper.teaser %}
    {% assign paper_teaser = paper["teaser"] %}
    {% assign paper_teaser_type = paper["teaser_type"] %}
  {% else %}
    {% assign paper_teaser = "assets/images/default_teaser320x180.png" %}
    {% assign paper_teaser_type = "img" %}
  {% endif %}
  {% include paper_row.html 
    teaser=paper_teaser
    teaser_type=paper_teaser_type
    paper_title=title
    paper_authors=authors
    paper_venue=venue
    paper_materials=materials
   %}
{% endfor %}