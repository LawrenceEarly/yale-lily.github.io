---
layout: page
title: Internal
permalink: /internal/
---


  <header class="post-header">
    <h2 class="post-title">Internal Information</h2>
  </header> 
{% for term in site.data.internal.presentations %}
<div class ="row">

<div style="text-align:center">
<h3>{{term.term}}</h3>
<h3>{{term.place}}</h3>
</div>
</div>

<table class="table table-striped table-hover">
<tr>
    <th> Time </th> <th> Title </th> <th> Presenter</th> 
</tr>
{% for presentation in term.presentations %}
    <tr>
        <td> {{ presentation.time }}  </td>
        <td> 
        </td>
        <td> 
           {{presentation.presenter}}
        </td>
    </tr>
{% endfor %}
</table>
{% endfor %}

<style>
#pubTable_filter{
    display:none;
}
</style>

<table id="pubTable" class="table table-hover"></table>



{% for term in site.data.internal.meetings %}
<div class ="row">

<div style="text-align:center">
<h3>
{{term.term}}
{{term.place}}
</h3>
</div>
</div>

<table class="table table-striped table-hover">
<tr>
    <th> Date</th> <th> Meeting</th> <th> Location </th>
</tr>
{% for event in term.events %}
    <tr>
        <td> {{ event.date }}  </td>
        <td> 
           {{event.type}}
        </td>
        <td> {{event.location}} </td>
    </tr>
{% endfor %}
</table>
{% endfor %}

<style>
#pubTable_filter{
    display:none;
}
</style>

<table id="pubTable" class="table table-hover"></table>



