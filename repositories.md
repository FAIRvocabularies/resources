---
layout: repositories
title: Terminology Repositories
permalink: /repositories/
---
{{page}}
XXX<br>
<ul>
    {% assign creator_query = "SELECT ?creator ?firstname WHERE { <https://github.com/FAIRvocabularies/terminology-repositories/LOV> <http://purl.org/dc/terms/creator> ?creator. ?creator <http://xmlns.com/foaf/0.1/firstName> ?firstname . }" %}
    {% assign results = page.rdf | sparql_query: creator_query %}
    {% for item in results %}
        {{ item.creator }} <br/>
        {{ item.firstname }} <br/>
    {% endfor %}

</ul>
XXX<br>

This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](https://jekyllrb.com/)

You can find the source code for Minima at GitHub:
[jekyll][jekyll-organization] /
[minima](https://github.com/jekyll/minima)

You can find the source code for Jekyll at GitHub:
[jekyll][jekyll-organization] /
[jekyll](https://github.com/jekyll/jekyll)


[jekyll-organization]: https://github.com/jekyll
