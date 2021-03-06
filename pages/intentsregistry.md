---
layout: page
show_meta: false
subheadline: "Intents Registry"
title: "See All Intents"
teaser: "These are all the possibilities to save your time and delegate to other apps."
permalink: "/intentsregistry/"
redirect_from:
  - /en/intentsregistry/
  - /en/intents/
  - /intents/
---
<a href="https://github.com/openintents/openintents.github.io/blob/master/README.md#intent-specification-for-writers">Add a new intent protocol via Github.</a>
<h3>Activity intents</h3>
<ul>
    {% assign ordered_specs = site.intent_specs | where: "component", "activity" | sort: "title" %}
    {% for spec in ordered_specs %}
    <li><a href="{{ site.url }}/action/{{ spec.action | slugify  }}/{{ spec.name }}">{{ spec.title }}</a> <br/><small>({{spec.action}})</small></li>
    {% endfor %}
</ul>
<a href="https://developer.android.com/guide/components/intents-common.html">Read also Google's documentation about common intents.</a>

<h3>Service intents</h3>
<ul>
    {% assign ordered_specs = site.intent_specs | where: "component", "service" | sort: "title" %}
    {% for spec in ordered_specs %}
    <li><a href="{{ site.url }}/service/{{ spec.name | slugify  }}/{{ spec.name }}">{{ spec.title }}</a> <br/><small>({{spec.action}})</small></li>
    {% endfor %}
</ul>

<h3>Broadcast Intents</h3>
<ul>
    {% assign ordered_specs = site.intent_specs | where: "component", "receiver" | sort: "title" %}
    {% for spec in ordered_specs %}
    <li><a href="{{ site.url }}/broadcast/{{ spec.name | slugify  }}/{{ spec.name }}">{{ spec.title }}</a> <br/><small>({{spec.action}})</small></li>
    {% endfor %}
</ul>
