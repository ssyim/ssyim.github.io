---
layout: page
title: research
permalink: /research/
description: towards programmable microbiome | under construction
---

Sung's research interest lies broadly in multi-scale characterization and engineering of biological systems towards developing useful solutions to real-world problems.

To this end, Sung develops and utilizes a diverse set of systems/synthetic biology tools including high-throughput DNA synthesis and sequencing technologies, massively parallel reporter assays, directed evolution strategies, DNA-based cellular recording systems, and cell-free expression systems to study and engineer diverse microbes and their communities.

Several technological innovations that Sung has contributed to in the field include,
* temporal recording of biological/digital information into the genomes of living cells
* multiplex characterizations of gene regulatory elements across diverse microbes
* expanding bacterial carbon substrate range towards raw biomass for biomanufacturing

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
