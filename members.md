---
title: members


---
<style>
  table {
    border-collapse: collapse;
    width: 100%;
    max-width: 800px;
    margin: 0 auto;
    text-align: center;
  }

  th, td {
    padding: 8px;
    border: 1px solid #ddd;
  }

  th {
    background-color: #f2f2f2;
    font-weight: bold;
  }

  tr:nth-child(even) {
    background-color: #f2f2f2;
  }
</style>

<table>
  <tr>
    <th>nombre</th>
    <th>apellido</th>
    <th>adiccion</th>
  </tr>
  {% for objeto in site.data.objetos %}
  <tr>
    <td>{{ objeto.nombre }}</td>
    <td>{{ objeto.apellido }}</td>
    <td>{{ objeto.adiccion }}</td>
  </tr>
  {% endfor %}
</table>
