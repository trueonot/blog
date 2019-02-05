---
layout: page
title: About
permalink: /about/
---
{% assign my = site.my %}
<div class="row" id="about">
    <header id="title">
        <img src="/images/trueonot.jpg">
        <h1>{{ my.realName_kr }} | <small>{{ my.jobTitle | upcase }}</small></h1>
    </header>


    <section id="intro">
      
        <h2>Intro</h2>
			<p> * Name : trueonot</p>
			<p>* email : trueonot@gmail.com</p>
			<p>* Steem : http://steemit.com/@trueonot</p>
			<p>* Twitter : @trueonot (Not use)</p>
			<p>* facebook : trueonot (Not use)</p>
    </section>

    <section id="skillsets">
        <h2>SKILLSETS</h2>
        <ul id="frontend">
            <i class="fa fa-tv">front end</i>
            {% for skill in my.skills.frontend %}
            <li>{{ skill }}</li>
            {% endfor %}
        </ul>
        <ul id="backend">
            <i class="fa fa-cog"> backend</i>
            {% for skill in my.skills.backend %}
            <li>{{ skill }}</li>
            {% endfor %}
        </ul>
        <ul id="tools">
            <i class="fa fa-wrench"> tools</i>
            {% for skill in my.skills.tools %}
            <li>{{ skill }}</li>
            {% endfor %}
        </ul>
    </section>

    <section id="findme">
        <h2>FIND ME ON</h2>
        <ul>
            <li><a href="{{ my.contact.github }}"><i class="fa fa-github"></i></a></li>
            <li><a href="{{ my.contact.qzone }}"><i class="fa fa-qq"></i></a></li>
            <li><a href="{{ my.contact.pinterest }}"><i class="fa fa-pinterest"></i></a></li>
        </ul>
    </section>

    <section id="action">
        <h2>MORE</h2>
        <a href="/resume">resume</a>
        <span> / </span>
        <a href="mailto:{{ my.contact.email }}">trueonot@gmail.com</a>
    </section>

</div>