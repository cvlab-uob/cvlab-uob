---
title: "HCVL Lab - Publications"
layout: gridlay
excerpt: "HCVL Lab -- Publications"
sitemap: false
permalink: /publications/
---


# Publications

## Highlights

(For a full list see [below](#full-list) or go to [Google Scholar](https://scholar.google.com/citations?hl=en&user=3TggrEkAAAAJ&view_op=list_works&gmla=AJsN-F4va6EjHhcBtURRNgDyyLaNVakvwCX5JWPJn7uJWOCSFhlJdQPSnnSTDNSzbTBOJI0MiVzGQVjDyzjGsbv2ySzm7kdgpLQTaODhdr3uvpH0747rsZRmcWi6ZLvHDJEUTIxkBUzq))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List

{% for publi in site.data.publist %}

  <strong>{{ publi.title }}</strong> -- <font color='red'>{{publi.booktitle_short}}</font><br />
  <em>{{ publi.authors }} </em><br />
  {{ publi.booktitle_full }} <br />
  [<a href="{{ site.baseurl }}/downloads/{{ publi.link.url_paper_server }}">{{ publi.link.paper_server }}</a>
  <a href="{{ publi.link.url_paper_web }}">{{ publi.link.paper_web }}</a>
  <a href="{{ publi.link.url_video }}">{{ publi.link.video }}</a>
  <a href="{{ publi.link.url_projectpage }}">{{ publi.link.projectpage }}</a>
  <a href="{{ publi.link.url_code }}">{{ publi.link.code }}</a>
  <a href="{{ publi.link.url_dataset }}">{{ publi.link.dataset }}</a>]  
  <a href="{{ site.baseurl }}/downloads/{{ publi.link.url_supplement }}">{{ publi.link.supplement }}</a>
  <a href="{{ publi.link.url_bibtex }}">{{ publi.link.bibtex }}</a>]

{% endfor %}


## Patents

{% for publi_patent in site.data.publist_patent %}

  <strong>{{ publi.title }}</strong> -- <font color='red'>{{publi.booktitle_short}}</font><br />
  <em>{{ publi.authors }} </em><br />
  {{ publi.booktitle_full }} <br />
  [<a href="{{ publi.link.url_display }}">{{ publi.link.display }}</a>
  <a href="{{ site.baseurl }}/downloads/{{ publi.link.url_paper_download }}">{{ publi.link.paper_download }}</a>
  <a href="{{ publi.link.url_paper_web }}">{{ publi.link.paper_web }}</a>
  <a href="{{ publi.link.url_video }}">{{ publi.link.video }}</a>
  <a href="{{ publi.link.url_ProjectPage }}">{{ publi.link.ProjectPage }}</a>
  <a href="{{ publi.link.url_code }}">{{ publi.link.code }}</a>
  <a href="{{ publi.link.url_bibtex }}">{{ publi.link.bibtex }}</a>]

{% endfor %}
