---
title: Fifty Things
summary: |
  The story of DAI told through fifty seperate objects found in staff offices around the globe. 
layout: default
permalink: /fifty-things
--- 
<section class="feature-wrap section">
  <div class="feature container">
    <div class="dai-box">
      <h1 class="title is-size-2">
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
</section>
<section class="section">
  <div class="container fifty-things">
  {%- for card in site.artifacts -%}
  <a href="{{card.url}}">
    <div class="card card-grid">
      <div class="front">
        <div class="card-image">
          <figure class="image is-4by4">
            <img src="{{card.image}}" alt="Placeholder image">
          </figure>
        </div>
      </div>
      <div class="back">
        <div class="card-content">
          <div class="media">
            <div class="media-content">
              <h3 class="title is-4">{{ card.title }}<hr class="bar"></h3>
            </div>
          </div>
          <div class="content">
          {{card.summary | truncate: 200, '...' }}
          </div>
        </div>
      </div>
    </div>
  </a>
  {%- endfor -%}
  </div>
</section>
<script>
$(".card-grid").flip({
          trigger: 'hover'
        });

        $(".flip-btn").click(function(){
          $(this).closest(".card-grid").flip(true);
        });

        $(".unflip-btn").click(function(){
          $(this).closest(".card-grid").flip(false);
        });
</script>