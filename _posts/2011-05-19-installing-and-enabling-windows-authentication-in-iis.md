---
layout: post
title:  "Installing and Enabling Windows Authentication in IIS 7.5"
description: "A post to remind Owen HTF to do this."
date:   2011-05-19 04:25:27
---
This post is intended to be one of a series of info dumps so I don&#8217;t forget any fiddly work-arounds, and may even be useful for anyone else facing similar issues.

I recently needed to build and run a web app on my Win7 dev box that required IIS to be configured to use integrated Windows Authentication.  IIS 7.5 (bundled with Windows 7) has a substantially different UI from versions 5 and 6, which I&#8217;m familiar with from Windows XP and Server 2003. On older versions, this feature is a simple check box, which has been removed in 7.5.  
<!-- more -->

According to my first rounds of googling, enabling Windows Auth <em>should</em> have simply been a matter of selecting it from an appropriate list and clicking &#8220;Enable". My problem was that it wasn&#8217;t on that list in the first place.
Cue much head scratching.

In the end I found the right combination of google terms and found this <a href="http://blog.hoegaerden.be/2010/02/14/iis-7-5-and-windows-authentication/">invaluable post</a> which includes sage advice for all of us:

>And like any decent developer, I didn’t waste my time reading all the text on the error page and started investigating the issue
> <cite>&mdash; Me</cite>

Well obviously!

The ultimate solution was to go to the Windows Features tool, drill down into the IIS feature lists and tick the box labelled, unsurprisingly &#8220;Windows Authentication". Windows Auth should now appear in the appropriate list in IIS.
And now I can get on with actual development rather than config headaches!