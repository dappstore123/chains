---
layout: home
title: Home
nav_order: 1
---

# EVM Networks

A list of EVM networks. Wallets and Web3 middleware providers should be able to use the appropriate Chain ID and Network ID to connect to the correct chain.

This table is also available as a JSON feed at [chains.json](/chains.json). Individual networks are available at <code>/chains/&laquo;chainid&raquo;.json</code>, and you can browse them in block format on the [chains page](/chains/).

## Chain List

<table>
  <tr>
    <th>Chain ID</th>
    <th>Name</th>
    <th>Short Name</th>
    <th>Chain</th>
    <th>Network</th>
    <th>Network ID</th>
  </tr>
{% for chain in site.chains %}{% comment %}<!-- Look up sort format and sort by Chain ID aka slug -->{% endcomment %}
  <tr>
    <td>{{ chain.slug }}</td>
    <td>{{ chain.name }}</td>
    <td>{{ chain.short_name }}</td>
    <td>{{ chain.chain }}</td>
    <td>{{ chain.network }}</td>
    <td>{{ chain.network_id }}</td>
  </tr>
{% endfor %}
</table>