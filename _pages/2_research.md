---
layout: page
title: research
permalink: /research/
description: towards programmable microbiome | under construction
---

My research interest lies broadly in characterization and engineering of diverse microbes and microbial communities in various environments towards understanding their design principles and transforming them into living sensors, therapeutics, factories, and bioremediation systems.

To this end, I develop and utilize a diverse set of systems and synthetic biology tools including high-throughput DNA synthesis and sequencing technologies, massively parallel reporter assays, directed evolution strategies, DNA-based cellular recording systems, and cell-free systems.

Several technological advances to which I have contributed include,
* temporal recording of biological/digital information into the genomes of living cells
* cell-free characterization of gene regulatory elements across diverse microbes
* synbio toolbox for a food-grade industrial microbe, <i>Corybacterium glutamicum</i>

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
