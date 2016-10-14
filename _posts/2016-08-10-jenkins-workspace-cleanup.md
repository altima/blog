---
ID: 45
post_title: Jenkins workspace cleanup
author: enno0815de
post_date: 2016-08-10 16:52:46
post_excerpt: ""
layout: post
permalink: https://blog.soapbubbles.de/archive/45
published: true
---
To cleanup all workspaces, execute this piece of code in the script console in the settings menu:
<pre class="lang:java decode:true ">import hudson.model.*
// For each project
for(item in Hudson.instance.items) {
  // check that job is not building
  if(!item.isBuilding()) {
    println("Wiping out workspace of job "+item.name)
    item.doDoWipeOutWorkspace()
  }
  else {
    println("Skipping job "+item.name+", currently building")
  }
}</pre>
go <a href="https://wiki.jenkins-ci.org/display/JENKINS/Wipe+out+workspaces+of+all+jobs" target="_blank">here</a> to get more informations about it