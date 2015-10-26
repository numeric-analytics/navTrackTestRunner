# navTrackTestRunner
Test runner widget for navTrack functionality

## Usage
* Insert html code in page wanting to test to use the test runner
* Insert via proxy (charles) or
* Insert on the actual page template or file

##Attributes
- `data-linkcontainer=""` // lt_region, lt_section, lt_subsection
- `data-tracklinktext=""` // Region, Section, Subsection
- `data-linktrackform=""` // true,false
- `data-linkblocking= ""` // true,false
- `data-tlcrossdomain=""` // true,false
- `data-linktrack="true"` // Identify a link

##Examples
###General
```html
<div data-linkcontainer="lt_region" data-tracklinktext="[Region Name]">
    <div class="" data-linkcontainer="lt_section" data-tracklinktext="[Section Name]">
        <a href="" data-linktrack="true" data-tracklinktext="[link text]">Link Text</a>
        <a href="" data-linktrack="true" data-tracklinktext="[link text]"><img src="/images/linkimage.jpg"></a>
    </div>
</div>
```

###Form
```html
<div class="searchTop" data-linkcontainer="lt_region" data-tracklinktext="top nav">
    <form name="myform" method="get" action="http://search.netsuite.com/socialsearch/query" data-linktrackform="true"  data-tracklinktext="Search Form" data-linkblocking = "true">
        <input type="hidden" name="cc" value="www" />
        <input type="hidden" name="cn" value="netsuite" />
        <input type="text" name="q" maxlength="2033" id="user" class="searchTopBox" value="" />
        <input type="submit" name="submit" value=" " class="searchTopBtn"/>
    </form>
</div>
```

###Cross-domain
```html
<div class="main-menu-holder clearfix" data-linkcontainer="lt_region" data-tracklinktext="main nav">
    <!-- call to action -->
    <a href="https://forms.netsuite.com/app/site/crm/externalleadpage.nl?compid=NLCORP&formid=3718&h=f61a11ac9974fb1093ec&subsidiary=1&ck=QqI6C4TgAdjuoGmU&vid=QqI6C4TgAfTuoNke&cktime=123012" class="btn btn-primary btn-lg call-to-action"  data-linktrack="true" data-tracklinktext="free product tour" data-tlcrossdomain="true">Free Product Tour</a>
</div>
```

###Lightbox / video
```html
<a href="http://www.youtube.com/watch?v=0rST36LBcEg?rel=0" rel="prettyPhoto[youtube]" title="NetSuite Video" class="show_video box" data-linktrack="true" data-tracklinktext="video: global omnichannel" data-linkblocking="true">
    <img class="img-responsive" src="/portal/common/img/video-williams-sonoma-v3.png" alt="Williams Sonoma" />
	<span class="caption simple-caption">
	<h3>Williams-Sonoma at NetSuite SuiteWorld 2013</h3>
	</span>
</a>
```
