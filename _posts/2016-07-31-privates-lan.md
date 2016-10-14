---
ID: 38
post_title: Privates-LAN am TP-LINK WR842ND v2
author: enno0815de
post_date: 2016-07-31 23:08:48
post_excerpt: ""
layout: post
permalink: https://blog.soapbubbles.de/archive/38
published: true
---
Um an Freifunk-Router WR842ND die LAN-Buchsen auf das eigene Netzwerk umzulegen muss folgendes ausgeführt werden:

&nbsp;
<ol>
 	<li>per SSH auf den Router verbinden</li>
 	<li>folgendes in der Konsole enigeben:</li>
</ol>
<pre class="toolbar-overlay:false lang:default decode:true " title="Privates-LAN">uci set network.client.ifname=bat0
uci set network.wan.ifname='eth0 eth1'
uci commit
reboot</pre>
&nbsp;
