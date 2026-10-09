---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

## Junteng Liu

Ph.D. candidate in Computer Science, HKUST NLP Group.

[Email](mailto:jliugi@connect.ust.hk) | [Google Scholar](https://scholar.google.com/citations?hl=en&user=tbK9jl4AAAAJ&view_op=list_works&sortby=pubdate) | [GitHub](https://github.com/Vicent0205) | [X](https://x.com/junteng88716710)

## Education

{% for education in site.data.cv.education %}
- **{{ education.studyType }}{% if education.area != empty %} in {{ education.area }}{% endif %}**, {{ education.institution }}. {{ education.startDate }} - {% if education.endDate == empty %}Present{% else %}{{ education.endDate }}{% endif %}. {{ education.summary }}
{% endfor %}

## Research Experience

{% for work in site.data.cv.work %}
- **{{ work.position }}, {{ work.name }}**. {{ work.startDate }} - {% if work.endDate == empty %}Present{% else %}{{ work.endDate }}{% endif %}. {{ work.summary }}
{% endfor %}

## Skills and Research Expertise

{% for skill in site.data.cv.skills %}
{{ skill.keywords | join: ", " }}.
{% endfor %}

## Publications

{% include personal-publications.html %}

## Honors

{% for award in site.data.cv.awards %}
- **{{ award.title }}**, {{ award.awarder }}.
{% endfor %}
