---
title: TeamWork Online - MVP Access
layout: default
cta:
  title: "Recruiting Software with over 130,000 success stories built for Sports & Entertainment"
  desc: "Everything you need to attract, source, and hire your top talent at every size organization."
  email: "buffy@teamworkonline.com"
  subject: "Test subject"
---
{% assign item = site.data.posts.mvpHeader[0] %}

<section class="container mx-auto py4 my4">
<div class="flex flex-wrap">
<div class="col-12 md-col-5 pr2 mx-auto">
<h1 class="oswald line-height-3 h2 blacks caps" >{{ item.header_title }}</h1>
<h2 class="line-height-4 h5 pb2 regular blacks mx-auto">{{ item.header_desc }} </h2>
<div class="border-top py2">
<p>Monthy MVP access<span class=" h4 right bold">${{ item.monthly_fee }}</span></p>
<p>One-time activation fee<span class=" h4 right bold">${{ item.activation_fee }}</span></p>
<p class="h3">Today's Total<span class=" h3 right bold">${{ item.todays_total }}</span></p>
</div>
</div>
<div class="col-12 md-col-5 pl2 mx-auto">
<div class="p4 bg-white">
<h2>Payment form placeholder</h2>
<p class="m0">
{% include cta.html inverted=true %}
</p>
</div>
</div>
</div>
</section>
 
<section class="bg-black py4">
<div class="container mx-auto">
<h3 class="white h3 oswald caps center py2">The three things you need to succeed</h3>
<div class="flex flex-wrap center">
{% assign mvpFeatureCard = site.data.posts.mvpFeatureCard | sort: 'sort' %}
{% for item in mvpFeatureCard %}
<div class="text-decoration-none flex flex-column p2 col-12 md-col-4 wow fadeInUp" data-wow-delay="0.2s"  style="order:{{ item.orderOverride }};">
<div class="flex-auto px3 pt3 card-shadow bg-white"  >
<img src="{{ item.image.url }}" style= "width: 44px;">
<h2 class="oswald black mb2">{{ item.name }}</h2>
<p class="line-height-4 p mb3 regular black">{{ item.desc }}</p>
</div>
</div>
{% endfor %}
<p class="center mx-auto py4">
{% include cta.html inverted=true %}
</p>
</div>
</div>
</section>

<section class="py4">
<div class="container mx-auto">
<h3 class="black h3 oswald caps center py2">The three things you need to succeed</h3>
<div class="flex flex-wrap">
{% assign mvpTestimonial = site.data.posts.mvpTestimonial | sort: 'sort' %}
{% for item in mvpTestimonial %}
<div class="flex-auto md-col-3 mx2 wow fadeInUp card-shadow my4" data-wow-delay="0.3s">
<div class="bg-black col-12 px2 py3 flex-none" style="background-color: #002244;">
<h3 class="oswald line-height-4 ltr-spacing-2 h4 m0 regular white">{{ item.quote }}</h3>
</div>
<div class="col-12 bg-white px2 py3 flex-auto">
<div class="flex items-center">
<div class="mr2 flex-none" style="background-image: url({{ item.image.url }}); background-size: cover; background-repeat: no-repeat; background-position: center; height: 64px; width: 64px;"></div>
<div class="flex-auto">
<p class="line-height-1 h5 regular mt0 mb1 black semibold">{{ item.name }}</p>
<p class="line-height-4 h5 regular m0 muted">{{ item.desc }}</p>
</div>
</div>
</div>
</div>
{% endfor %}
<p class="center mx-auto py4">
{% include cta.html inverted=true %}
</p>
</div>
<!-- </section> -->
