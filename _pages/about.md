---
title: "About"
permalink: "/about.html"
layout: post
toc: false
comments: true
---

This page is about page for DLC (deep learning computing). 

This page also show the avatar with differernt super resolution algorithm of `bicubic` and `waifu2x` (deep learning one)where bicubic is commonly used in common VGA chip as default super resolution algorithm. As you can see the deep learning one provide better quality on smaller aliasing and color disnormal.

<body>
    <script src="https://code.jquery.com/jquery-3.3.1.min.js" integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8=" crossorigin="anonymous"></script>

      <script src="{{ site.url }}{{ site.baseurl }}/assets/plugins/jquery.event.move.js"></script>
      <script src="{{ site.url }}{{ site.baseurl }}/assets/plugins/jquery.twentytwenty.js"></script>
      <script>
        $(function()
        {

          $(".twentytwenty-container").eq(0).twentytwenty({default_offset_pct: 0.5,
          before_label: "bicubic",
          after_label: "waifu2x",
          no_overlay: false, 
          move_slider_on_hover: false, 
          move_with_handle_only: true, 
          click_to_move: true 
          });
        });
  </script>
</body>

{% slider2020 %}
  ![lanczos3]({{ site.url }}{{ site.baseurl }}/assets/images/avatar255x287-bicubic.png)
  ![Waifu2x]({{ site.url }}{{ site.baseurl }}/assets/images/avatar255x287-waifu2x_photo.png)
{% endslider2020 %}

<body>
  <div class="container">
  <h4 class="font-weight-bold spanborder"><span>Authors</span></h4>
      <div class="row gap-y listrecent listrecent listauthor">
      {% for author in site.authors %}
          <div class="col-lg-6 mb-4">
              <div class="p-4 border rounded">
              <div class="row">
              <div class="col-md-3 mb-4 mb-md-0"><img alt="{{ author[1].name }}" src="{{site.baseurl}}/{{ author[1].avatar }}" class="rounded-circle" height="80" width="80"></div>
              <div class="col-md-9">
              <a href="{{site.baseurl}}/author-{{ author[1].name | slugify }}.html">
              <h4 class="text-dark mb-0"> {{ author[1].name }} </h4>
              <small class="d-inline-block mt-1 mb-3 font-weight-normal">(View Posts)</small>
              <div class="excerpt">{{ author[1].bio }}</div>
              </a>
              <div class="icon-block mt-3 d-flex justify-content-between">  
              <div>
              <a target="_blank" href="{{ author[1].twitter }}"><i class="fab fa-twitter text-muted" aria-hidden="true"></i></a>  &nbsp;
              <a target="_blank" href="{{ author[1].site }}"><i class="fa fa-globe text-muted" aria-hidden="true"></i></a> &nbsp;
              </div>
              </div>
              </div>
              </div>
              </div>
          </div>
      {% endfor %}
      </div>
  </div>
</body>