---
layout: home
title: Welcome to Barnsley Gymnastics Club
---

<!-- Services -->
  <section class="page-section" id="services">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">Services</h2>
          <h3 class="section-subheading text-muted">Lorem ipsum dolor sit amet consectetur.</h3>
        </div>
      </div>
      <div class="row text-center">
        {% for service in site.services %}
        <div class="col-md-4">
            <span class="fa-stack fa-4x">
                <i class="fas fa-circle fa-stack-2x text-primary"></i>
                <i class="fas fa-{{ service.fa_icon }} fa-stack-1x fa-inverse"></i>
            </span>
            <h4 class="service-heading">{{ service.heading}}</h4>
            <p class="text-muted">
                    {{ service.content }}
            </p>
        </div>
        {% endfor %}
      </div>
    </div>
  </section>
