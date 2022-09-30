---
layout: default
title: Schedule
permalink: /schedule/
---

Lecture slides and exercise notebooks should be available below after the class period. If they are not, please let me know.

| ---- | | |
{% for module in site.data.modules -%} |
{%- if module.day %}{{ module.day }}{% endif %} |
{%- if module.date %}{{ module.date }}{% endif %} | <b>{{ module.title }}</b>
{%- if module.description %} {{ module.description }} {% endif -%}
{%- if module.teacher %} ({{ module.teacher }}){% endif -%}
{%- if module.basename %} [[key](https://github.com/daveminh/Chem456-2022F/raw/main/slides/{{ module.basename }}.key)/[ppt](https://github.com/daveminh/Chem456-2022F/raw/main/slides/{{ module.basename }}.ppt)/[pdf](https://github.com/daveminh/Chem456-2022F/raw/main/slides/{{ module.basename }}.pdf)]. {% endif %}
{%- if module.exercise %} Exercise {{ module.exercise }}{% endif -%}
{%- if module.notebook %} [[colab](https://colab.research.google.com/github/daveminh/Chem456-2022F/blob/main/exercises/{{ module.notebook }}.ipynb)]. {% endif -%}
{%- if module.panopto %} [[Recording](https://iit.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id={{module.panopto}})]{% endif -%}
{%- if module.due %} <u>Due:</u> {{ module.due }}. {% endif %}
{%- if module.quiz %} <u>Quiz:</u> {{ module.quiz }}. {% endif %} |
{% endfor %}
