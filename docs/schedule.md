---
layout: default
title: Schedule
permalink: /schedule/
---

| ---- | | |
{% for module in site.data.modules -%} |
{%- if module.day %}{{ module.day }}{% endif %} |
{%- if module.date %}{{ module.date }}{% endif %} | <b>{{ module.title }}</b>
{%- if module.description %} {{ module.description }} {% endif -%}
{%- if module.teacher %} ({{ module.teacher }}){% endif -%}
{%- if module.basename %} [{% if module.slides == "ppt" %}[ppt](https://github.com/CCBatIIT/modelingworkshop/raw/main/slides/{{ module.basename }}.ppt)/{% elsif module.slides == "pdf"%}{% else %}[key](https://github.com/CCBatIIT/modelingworkshop/raw/main/slides/{{ module.basename }}.key)/{% endif -%}[pdf](https://github.com/CCBatIIT/modelingworkshop/raw/main/slides/{{ module.basename }}.pdf)]. {% endif %}
{%- if module.lab %} Lab {{ module.lab }}{% endif -%}
{%- if module.notebook %} [[colab](https://colab.research.google.com/github/CCBatIIT/modelingworkshop/blob/main/labs/{{ module.day }}-{{module.period}}/{{ module.notebook }}.ipynb)]. {% endif -%}
{%- if module.panopto %} [[Recording](https://iit.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id={{module.panopto}})]{% endif -%}
{%- if module.due %} <u>Due:</u> {{ module.due }}. {% endif %}
{%- if module.quiz %} <u>Quiz:</u> {{ module.quiz }}. {% endif %} |
{% endfor %}

<!---
{% for day in (1..5) %} | {{ day }} | {% for period in (1..2) %} {% for module in site.data.modules %} {% if module.day == day %} {% if module.period == period %}{%- if module.bold %}<b>{% endif %}{{ module.title }}{% if module.bold %}</b>{% endif -%}{% if module.teacher %} ({{ module.teacher }}){% endif -%}{% if module.description %}. <i>{{ module.description }}</i> {% endif -%}
{% if module.notebook %} [[colab](https://colab.research.google.com/github/CCBatIIT/modelingworkshop/blob/main/labs/{{ module.day }}-{{module.period}}/{{ module.notebook }}.ipynb)]
{%- endif -%}
{%- if module.panopto %} [[Recording](https://iit.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id={{module.panopto}})]
{%- endif -%}
{% if module.slides %} [{% if module.slides == "ppt" %}[ppt](https://github.com/CCBatIIT/modelingworkshop/raw/main/slides/{{ module.slides }}.ppt)/{% elsif module.slides == "pdf"%}{% else %}[key](https://github.com/CCBatIIT/modelingworkshop/raw/main/slides/{{ module.slides }}.key)/{% endif -%}[pdf](https://github.com/CCBatIIT/modelingworkshop/raw/main/slides/{{ module.slides }}.pdf)]. {% else %}.
{%- endif %} {%- endif %} {% endif %} {% endfor %} | {% endfor %}
{% endfor %}
-->
