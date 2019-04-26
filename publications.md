---
layout: default
title: publication
---
<h1> Journal Articles </h1>
<ul>
{% for item in site.publications %}

    {% if item.type == "journal" %}
        <li> 
            <div class="pubEntry">
                {{item.authors}} <b> {{item.papertitle}}</b> {{item.year}} in <span class="journal"> {{item.journal}} </span>
            </div> 
        {%if item.journal_url %} <a href="{{item.journal_url}}">link</a> {% endif %} 
        {%if item.preprint %} <a href="{{item.preprint}}">preprint</a> {% endif %}
        {%if item.github %} <a href="{{item.github}}">source code</a>  {% endif %}
        </li>
    {% endif %}

{% endfor %}
</ul>

<h1> Conferences Papers </h1>
<ul>
{% for item in site.publications %}

    {% if item.type == "conference" %}
        <li> 
            <div class="pubEntry">
                {{item.authors}} <b> {{item.papertitle}}</b> {{item.year}} in <span class="journal"> {{item.conference}} </span>
            </div> 
        {%if item.conference_url %} <a href="{{item.conference_url}}">link</a> {% endif %} 
        {%if item.preprint %} <a href="{{item.preprint}}">preprint</a> {% endif %}
        {%if item.github %} <a href="{{item.github}}">source code</a>  {% endif %}
        </li>
    {% endif %}

{% endfor %}
</ul>