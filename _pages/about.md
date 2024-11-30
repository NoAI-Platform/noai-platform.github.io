---
permalink: /about
layout: page
title: Meet the Team
---
## Core Team

<div class="team-gallery">
  {% for member in site.data.team %}
  <div class="team-member">
    <div class="team-image-container">
      <img src="{{ member.image }}" alt="{{ member.name }}" class="team-image">
    </div>
    <h3>{{ member.name }}</h3>
    <p class="role">{{ member.role }}</p>
    <p class="description">{{ member.description }}</p>
    <a href="{{ member.link }}" class="team-link" target="_blank">Learn more</a>
  </div>
  {% endfor %}
</div>

## Project Team Members

<div class="team-gallery">
  {% for member in site.data.project_team %}
  <div class="team-member">
    <div class="team-image-container">
      <img src="{{ member.image }}" alt="{{ member.name }}" class="team-image">
    </div>
    <h3>{{ member.name }}</h3>
    <p class="role">{{ member.role }}</p>
    <p class="description">{{ member.description }}</p>
    <a href="{{ member.link }}" class="team-link" target="_blank">Learn more</a>
  </div>
  {% endfor %}
</div>

<style>

.team-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  padding: 20px;
  justify-items: center;
}

.team-member {
  text-align: center;
  padding: 15px;
  border: 1px solid #eaeaea;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.team-member:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
}

.team-image-container {
  width: 150px; 
  height: 150px; 
  margin: 0 auto 10px; 
  overflow: hidden;
  border-radius: 50%; 
}

.team-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}

.team-link {
  display: inline-block;
  margin-top: 10px;
  font-size: 0.9em;
  color: #007acc;
  text-decoration: none;
  font-weight: bold;
}

.team-link:hover {
  text-decoration: underline;
  color: #005f99;
}

</style>
