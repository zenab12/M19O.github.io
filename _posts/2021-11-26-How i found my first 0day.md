---
published: true
title: How i found my first 0day 
date: 2021-11-26 14:56:00 +0200
categories: [Publications]
tags: Publications SecurityResearching
---



**Title** : All-in-One Video Gallery plugin <= 2.4.9 - Local File Inclusion (LFI) vulnerability
<br>
**Author**: m19o 
<br>
**Software** : Wordpress 5.8.2
<br>
**CVE** : CVE-2021-24970
<br>
**Poc** : https://example/wordpress/wp-admin/admin.php?page=all-in-one-video-gallery&tab=../../../../../poc
<br>

<h1><strong>Statis analysis</strong></h1>
  
```At the beganinng i started to analyze the code to understand how the code works``` 

```while analyzing the dashboard.php file i saw that the developer using require_once at the end of the file, as you can see {$active_tab} gets his value from TAB and TAB value is provided by the user```
  
  
<img src="https://i.ibb.co/hXRcSQp/1123.png" alt="1123" border="0">
<br>
<br>
**```Let's EXPLOIT```**

<iframe src="https://giphy.com/embed/CY3A9zOlZR8uhFbeok" width="480" height="278" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p>

<h1><strong>Exploitation</strong></h1>
<img src="https://i.ibb.co/nCSZcPc/22.png" alt="22" border="0">

**```You can execute any file with php extension because .php is added to any value you provide```**
  
  


