---
title: Fifty Things
summary: |
  The story of DAI told through fifty seperate objects found in staff offices around the globe. 
layout: default
permalink: /fifty-things-grid
--- 
<section class="hero bold">
  <div class="hero-body artifacts">
    <div class="container">
      <h1 class="title is-size-4-mobile is-size-2-desktop">
        Fifty Things
        <hr class="bar">
      </h1>
        <p>Look around any DAI office, and you’ll see more than computers and cubicles. Over the years, our desks, walls, shelves, and photo albums have accumulated a wide range of…stuff. Far from simple office clutter, these “artifacts” represent 50 years of stories and impact.</p> 
        <p>Maybe it’s the piece of art you picked up on a field visit. The leftover water testing kit from a project that made a difference. The inflatable unicorn you were given as an inside joke from a colleague who inspired you. The 20-year old winning proposal you can’t bring yourself to throw away. </p>
        <p>To celebrate 50 years, we're telling our story through the detail of fifty such artifacts. As the story unfolds below, you'll find that across all of these people, places, and projects one thing has remaind constant: our mission. To help people improve their lives</p>
    </div>
  </div>
</section>
<!-- <section class="feature-wrap section">
  <div class="feature container">
    <div class="dai-box">
      <h1 class="title is-size-4-mobile is-size-2-desktop">
        Fifty Things
        <hr class="bar">
      </h1>
      <div class="feature--detail">
        <p>Look around any DAI office, and you’ll see more than computers and cubicles. Over the years, our desks, walls, shelves, and photo albums have accumulated a wide range of…stuff. Far from simple office clutter, these “artifacts” represent 50 years of stories and impact.</p> 
        <p>Maybe it’s the piece of art you picked up on a field visit. The leftover water testing kit from a project that made a difference. The inflatable unicorn you were given as an inside joke from a colleague who inspired you. The 20-year old winning proposal you can’t bring yourself to throw away. </p>
        <p>To celebrate 50 years, we're telling our story through the detail of fifty such artifacts. As the story unfolds below, you'll find that across all of these people, places, and projects one thing has remaind constant: our mission. To help people improve their lives</p>
      </div>
    </div>
  </div>
</section> -->
<section class="section fifty-section">
  <div class="container fifty-things">
  {%- for card in site.artifacts -%}
    <div class="card card-grid">
      <div class="front">
        <div class="card-image">
          <figure class="image is-4by4">
            <img src="{{card.image}}" alt="Placeholder image">
          </figure>
        </div>
      </div>
      <div class="back">
      <a href="{{card.url}}">
        <div class="card-content">
          <div class="content">
          <h3 class="title is-4">{{ card.title }}<hr class="bar"></h3>
            {{card.summary | truncate:200}}
          </div>
          <div class="media attribution">
            <div class="media-left">
              <figure class="image is-48x48">
                <img src="{{card.person-image}}" alt="person portrait">
              </figure>
            </div>
            <div class="media-content">
              <p class="title is-5">{{card.person}}</p>
              <p class="subtitle is-6">{{card.person-title}}</p>
            </div>
          </div>
        </div>
      </a>
      </div>
    </div>
  {%- endfor -%}
  </div>
</section>
<script>
$(".card-grid").flip({
          trigger: 'click'
        });

        $(".flip-btn").click(function(){
          $(this).closest(".card-grid").flip(true);
        });

        $(".unflip-btn").click(function(){
          $(this).closest(".card-grid").flip(false);
        });
</script>