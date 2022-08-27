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
{%- if module.basename %} [[key](https://github.com/daveminh/Chem456-2022F/raw/main/slides/{{ module.basename }}.key)/{% if module.slides == "ppt" %}[ppt](https://github.com/daveminh/Chem456-2022F/raw/main/slides/{{ module.basename }}.ppt)/{% endif -%}[pdf](https://github.com/daveminh/Chem456-2022F/raw/main/slides/{{ module.basename }}.pdf)]. {% endif %}
{%- if module.lab %} Lab {{ module.lab }}{% endif -%}
{%- if module.notebook %} [[colab](https://colab.research.google.com/github/daveminh/Chem456-2022F/blob/main/labs/{{ module.notebook }}.ipynb)]. {% endif -%}
{%- if module.panopto %} [[Recording](https://iit.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id={{module.panopto}})]{% endif -%}
{%- if module.due %} <u>Due:</u> {{ module.due }}. {% endif %}
{%- if module.quiz %} <u>Quiz:</u> {{ module.quiz }}. {% endif %} |
{% endfor %}
