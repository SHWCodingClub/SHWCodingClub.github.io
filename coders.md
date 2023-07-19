---
layout: default
title: Coders at the SHW
permalink: coders
---

{% assign coders = site.data.profiles %}

### Some of our SHW staff who like to contribute:

<table class = "coders">
<th></th>
<th>Coder</th>
<th>Languguages they like using</th>
<th>GitHub profile</th>
{% for coder in coders %}

<tr>
    <td><img width=100 class = "profilepic" src="https://github.com/{{coder.github}}.png?size=100"></td>
    <td>{{coder.name}}</td>
    <td>{{coder.langs}}</td>
    <td><a href="https://github.com/{{coder.github}}">{{coder.github}}</a></td>
</tr>

{% endfor %}

</table>
