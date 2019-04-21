---
layout: default
title: Chains
permalink: /chains/
nav_order: 10
---

List of chains in block format. You can link directly to each section using the header name:

{% for chain in site.chains %}

<h2><a href="/chains/{{ chain.slug }}.json">{{ chain.name }}</a></h2>
<ul>
<li>Short Name: {{ chain.short_name }}</li>
<li>Chain: {{ chain.chain }}</li>
<li>Chain ID: {{ chain.slug }}</li>
<li>Network: {{ chain.network }}</li>
<li>Network ID: {{ chain.network_id }}</li>
</ul>
<hr />
{% endfor %}
