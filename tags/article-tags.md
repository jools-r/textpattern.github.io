---
layout: document
category: Tags
published: true
title: Category: Article tags
description: A list of Textpattern documentation within the category 'Article tags'.
search_omit: true
---

# Category: Article tags

Textpattern documentation within the category 'Article tags':

<div>
    {% for page in site.pages %}
        {% if page.tags contains 'Article tags' %}
            <article>
                <h3>{{page.title}}</h3>
                <p>{{page.description}}</p>
                <p><a href="{{page.url}}">Go to the full documentation...</a></p>
            </article>
        {% endif %}
    {% endfor %}
</div>