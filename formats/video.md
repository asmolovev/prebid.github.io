---
layout: page_v2
title: Prebid Video
description: Prebid Video
sidebarType: 6
---

# Prebid Video Ads
{:.no_toc}

Video ads are supported by Prebid.js. Prebid Server support is coming soon.

## Prebid.js

### Adops

- [Prebid.js video overview](/prebid-video/video-overview.html)
- [Show video ads in DFP](/dev-docs/show-video-with-a-dfp-video-tag.html)

### Developers

- [Getting started with video](/prebid-video/video-getting-started.html)
- [Outstream video ads](/dev-docs/show-outstream-video-ads.html)

### Prebid.js bid adapters that support video ads

<div id="dynamicTable"></div>

<script type="text/javascript">
var dynamicTableContents=[];

{% assign numVideo = 0 %}
{% assign bidder_pages = site.pages | where: "layout", "bidder" %}
{% for page in bidder_pages %}
{% if page.media_types contains 'video' %}
   dynamicTableContents[{{numVideo}}]={};
   dynamicTableContents[{{numVideo}}].href="/dev-docs/bidders.html#{{page.biddercode}}";
   dynamicTableContents[{{numVideo}}].text="{{page.title}}";
   {% assign numVideo = numVideo | plus: 1 %}
{% endif %}
{% endfor %}
</script>
<script src="/assets/js/dynamicTable.js" type="text/javascript" data-div="dynamicTable" data-array="dynamicTableContents"></script>
