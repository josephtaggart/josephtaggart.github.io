---
layout: page
title: "music!"
permalink: /music/
---

<p>My most-listened artists, albums, and tracks of the last 30 days:</p>

<h2>Artists</h2>
{% assign artists = site.data.lastfm.topartists.artist %}
<ol>
  {% for artist in artists %}
    <li>
      <a href="{{ artist.url }}" target="_blank" rel="noreferrer">{{ artist.name }}</a>
      — {{ artist.playcount }} plays
    </li>
  {% endfor %}
</ol>

<h2>Albums</h2>
{% assign albums = site.data.lastfm.topalbums.album %}
<ol>
  {% for album in albums %}
    <li>
      <a href="{{ album.url }}" target="_blank" rel="noreferrer">{{ album.name }}</a>
      by {{ album.artist.name }} — {{ album.playcount }} plays
    </li>
  {% endfor %}
</ol>

<h2>Tracks</h2>
{% assign tracks = site.data.lastfm.toptracks.track %}
<ol>
  {% for track in tracks %}
    <li>
      <a href="{{ track.url }}" target="_blank" rel="noreferrer">{{ track.name }}</a>
      by {{ track.artist.name }} — {{ track.playcount }} plays
    </li>
  {% endfor %}
</ol>

{% include footer.html %}
