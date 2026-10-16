---
layout: page
title: "Top artists | Joe Taggart"
permalink: /artists/
---

<p>Your most-listened artists on Last.fm:</p>

{% assign artists = site.data.lastfm.topartists.artist %}
{% if artists and artists.size > 0 %}
<ol>
  {% for artist in artists %}
    <li>
      <a href="{{ artist.url }}" target="_blank" rel="noreferrer">{{ artist.name }}</a>
      — {{ artist.playcount }} plays
    </li>
  {% endfor %}
</ol>
{% else %}
<p>The artist list has not been refreshed yet. Run the <strong>Update Last.fm artists</strong> workflow from the Actions tab.</p>
{% endif %}
