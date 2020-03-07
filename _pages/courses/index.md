---
layout: default
title: Courses
permalink: /courses/
order: 2
menu: true
---
All our courses are highly interactive, with plenty of time to reflect on what you're learning.

{% assign courses = site.pages | sort: 'order' | where_exp: "item" , "item.path contains 'courses'" %}
{% for item in courses %}
{% if item.title != "Courses" %}
                                
<h3><a href="{{ item.permalink }}">{{ item.title }} {{ item.abbrev }}</a></h3>

<p>{{ item.summary }}</p>
<p>{{ item.summary2 }}</p>

<p>Length: {{ item.length }}</p>

                                
                            
                            {% endif %}
                            {% endfor %}

