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
<div class="flex flex-wrap mt4">
  <div class="col-12 md-col-5 pr2 mx-auto">
    <img src="{{ item.logo.url }}" class="mb2" style="width: 160px;">
    <h1 class="oswald line-height-2 h1 black caps m0">{{ item.header_title }}</h1>
    <h4 class="line-height-4 h4 my3 regular gray7 mx-auto pl2" style="border-left: 3px solid">{{ item.header_desc }} </h4>
    <div class="black mvp-total px3 py1 mb2">
      <h3 class="black">Order Summary</h3>
      <p>Monthy subscription<span class="p right">${{ item.monthly_fee }}</span></p>
      <p>One-time activation fee<span class="p right">${{ item.activation_fee }}</span></p>
      <div class="hr" style="margin: 1.5rem 0 1.5rem 0;"></div>
      <p class="p bold">Today's Total<span class="p right bold">${{ item.todays_total }}</span></p>
    </div>
  </div>
  <div class="col-12 md-col-6 mx-auto" id="payment">
    <div class="bg-white card-shadow p3">
      <p class="regular black p">Enter your payment details<img src="/images/icons/lock.svg" style="height: 18px; position: relative; top: 2px;" class="pl1"></p>
      <div class="flex flex-wrap">
      <div style="width: 100%; margin: 0 auto;"><div class="card-wrapper mt2 mb3"></div></div>
      <form style="width: 100%;" class="h5 regular black">
        <label class="h6 inline-block py1"><span class="regular black pb1">Credit Card Number</span></label>
        <input class="input" type="text" name="number" placeholder="Enter your card number">
        <label class="h6 inline-block py1"><span class="regular black pb1">Your Name</span></label>
        <input class="input" type="text" name="name" placeholder="First and last name">
        <div class="flex">
          <div class="col-6 mr1">
            <label class="h6 inline-block py1"><span class="regular black pb1">Expiration Date</span></label>
            <input class="input" type="text" name="expiry" placeholder="MM/YY">
          </div>
          <div class="col-6">
          <label class="h6 inline-block py1"><span class="regular black pb1">Security Code</span></label>
            <input class="input" type="text" name="cvc" placeholder="***">
          </div>
        </div>
      </form>
      <script>
    var card = new Card({
        form: 'form',
        container: '.card-wrapper',
        placeholders: {
            number: '**** **** **** ****',
            name: 'Alex Wood',
            expiry: '**/****',
            cvc: '***'
        }
    });
    </script>
</div>
      <div class="center py2">
        <img src="/images/secure-payments.jpg" style="height: 56px;">
        <a href="#" class="white oswald caps center semibold h4  ltr-spacing-2 text-decoration-none" >
      <div class="py2"><img src="https://www.paypalobjects.com/webstatic/en_US/i/buttons/checkout-logo-large.png" alt="Check out with PayPal" /></div>
      </a>
      </div>
      <a href="#" class="white oswald caps center semibold h4  ltr-spacing-2 text-decoration-none" >
      <div class="bg-gray py2">Upgrade to mvp access</div>
      </a>
    </div>
  </div>
</div>
</section>
 
<section class="bg-black py4">
<div class="mx-auto">
<h2 class="white h2 oswald caps center pb2">The three things you need to succeed</h2>
<div class="flex flex-wrap container mx-auto">
{% assign mvpFeatureCard = site.data.posts.mvpFeatureCard | sort: 'sort' %}
{% for item in mvpFeatureCard %}
<div class="text-decoration-none flex flex-wrap items-center px2 pb4 my2 wow fadeInUp" data-wow-delay="0.2s"  style="order:{{ item.order }};">
<div class="col-12 md-col-4 mx-auto mvp-feature">
<img src="{{ item.icon.url }}" style= "width: 44px;">
<h2 class="bold white mb2 line-height-2">{{ item.name }}</h2>
<p class="line-height-4 p pb1 mb3 regular white" style="opacity:.75;">{{ item.desc }}</p>
<p class="mx-auto">
{% include cta.html inverted=true %}
</p>
</div>
<div class="col-12 md-col-7 mx-auto">
<img src="{{ item.image.url }}?fm=png&q=50" style= "width: 100%;" class="right">
</div>
</div>
{% endfor %}
</div>
</div>
<div class="center white pt4 container mx-auto">
<h2 class="bold oswald caps white mb2 line-height-2 h2">Additional Benefits</h2>
<p class="line-height-4 p pb1 mb3 regular white" style="opacity:.75;">Take advantage of our always-improving MVP benefits</p>
</div>
<div class="flex flex-wrap container mx-auto py4">
{% assign mvpFeatureHeading = site.data.posts.mvpFeatureHeading | sort: 'sort' %}
{% for item in mvpFeatureHeading %}
<div class="col-12 md-col-4 mx-auto px2 additional-benefits" style="order:{{ item.order }};">
<img src="{{ item.icon.url }}" style= "width: 44px;">
<h3 class="bold white mb2 line-height-2">{{ item.title }}</h3>
<p class="line-height-4 p pb1 mb3 regular white" style="opacity:.75;">{{ item.desc }}</p>
</div>
{% endfor %}
</div>
</section>

<section class="py4">
<div class="container mx-auto">
{% assign item = site.data.posts.mvpTestimonialHeading[0] %}
<h3 class="black h3 oswald caps center py2">{{ item.title }}</h3>
<div class="flex flex-wrap">
{% assign mvpTestimonial = site.data.posts.mvpTestimonial | sort: 'sort' %}
{% for item in mvpTestimonial %}
<div class="flex-auto md-col-3 mx2 wow fadeInUp card-shadow my2" data-wow-delay="0.3s">
<div class="bg-black col-12 px2 py3 flex-none" style="background-color: #{{ item.hex_color }};">
<h3 class="oswald line-height-4 ltr-spacing-2 h4 m0 regular white">{{ item.quote }}</h3>
</div>
<div class="col-12 bg-white px2 py3 flex-auto">
<div class="flex items-center">
<div class="mr2 flex-none" style="background-image: url({{ item.image.url }}?fm=jpg&q=25); background-size: cover; background-repeat: no-repeat; background-position: center; height: 64px; width: 64px;"></div>
<div class="flex-auto" style="order:{{ item.order }}">
<p class="line-height-1 h5 regular mt0 mb1 black semibold">{{ item.name }}</p>
<p class="line-height-4 h5 regular m0 muted">{{ item.desc }}</p>
</div>
</div>
</div>
</div>
{% endfor %}
<p class="center mx-auto py2">
{% include cta.html inverted=true %}
</p>
</div>
<!-- </section> -->
