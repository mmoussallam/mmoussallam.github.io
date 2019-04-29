---
layout: default
title: Publications
---
A supposedly up-to-date list of my publications.

<h1> Journal Articles </h1>
<ul>
{% for item in site.publications %}

    {% if item.type == "journal" %}
        <li> 
            <div class="pubEntry">
                {{item.authors}} <b> {{item.papertitle}}</b> {{item.year}} in <span class="journal"> {{item.journal}} </span>
            
        {%if item.journal_url %} <a href="{{item.journal_url}}">link</a> {% endif %} 
        {%if item.preprint %} <a href="{{item.preprint}}">preprint</a> {% endif %}
        {%if item.github %} <a href="{{item.github}}">source code</a>  {% endif %}
        {%if item.bibtex %} <button onclick="alert('{{item.bibtex}}')">bibtex</button> {% endif %}
        </div> 
        </li>
    {% endif %}

{% endfor %}
</ul>

<h1> Conferences Papers </h1>
<ul>
{% assign items = site.publications | sort: 'year' | reverse%}
{% for item in items %}

    {% if item.type == "conference" %}
        <li> 
            <div class="pubEntry">
                {{item.authors}} <b> {{item.papertitle}}</b> {{item.year}} in <span class="journal"> {{item.conference}} </span>
            
        {%if item.conference_url %} <a href="{{item.conference_url}}">link</a> {% endif %} 
        {%if item.preprint %} <a href="{{item.preprint}}">preprint</a> {% endif %}
        {%if item.github %} <a href="{{item.github}}">source code</a>  {% endif %}
        </div> 
        </li>
    {% endif %}

{% endfor %}
</ul>

<h1> PhD Dissertation </h1>
 "Représentations redondantes et hiérarchiques pour l'archivage et la compression de scènes sonores" Thèse de Telecom ParisTech (French december 2012). <a href="assets/images/manuscrit_final.pdf">pdf</a>