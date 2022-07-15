---
author: Carlos Madrid G
categories:
- R to GIS
date: "2022-07-14"
draft: false
excerpt: Calcular Pendientes
layout: single
subtitle: Usar R como SIG
title: Crear Mapa de Pendientes con tmap, ggplot2 y leaflet
image:
  placement: 1
  caption: 'Your caption here.'
  focal_point: ''
  preview_only: false
---
<script src="/rmarkdown-libs/kePrint/kePrint.js"></script>
<link href="/rmarkdown-libs/lightable/lightable.css" rel="stylesheet" />


Un mapa de pendientes identifica la diferencia del gradiente entre dos formas de relieve. Es decir es una relación entre la distancia horizontal y la altitud entres dos puntos. A continuación, en una serie de pasos mostraré como realizar este tipo de mapas a partir de código en R:

## Paquetes

<table class=" lightable-material-dark table" style='font-family: "Source Sans Pro", helvetica, sans-serif; margin-left: auto; margin-right: auto; width: auto !important; margin-left: auto; margin-right: auto;'>
 <thead>
  <tr>
   <th style="text-align:left;"> Paquetes </th>
   <th style="text-align:left;"> Definición </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> tidyverse </td>
   <td style="text-align:left;"> Conjunto de paquetes (visualización y manipulación de datos): ggplot2, dplyr, purrr,etc. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> raster </td>
   <td style="text-align:left;"> Lectura, escritura, manipulación, análisis y modelado de datos espaciales raster. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> tmap </td>
   <td style="text-align:left;"> Fácil creación de mapas temáticos. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> rgeoboundaries </td>
   <td style="text-align:left;"> Límites administrativos de países. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> elevatr </td>
   <td style="text-align:left;"> Acceso a datos de evación con API de USGS y AWS. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> sp </td>
   <td style="text-align:left;"> Clases y métodos para tratar con datos espaciales </td>
  </tr>
  <tr>
   <td style="text-align:left;"> rgdal </td>
   <td style="text-align:left;"> Funciones para escribir archivos ráster y vectoriales en formatos compatibles. </td>
  </tr>
</tbody>
</table>
