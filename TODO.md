# Web site


## To add
1. Split "Events" into "DSI Events" and "Other Events." Other are things not co-sponsored by the DSI and/or not occurring in the DSI space. Will need a category for all events added notDSI: true.
1.  Change so that homepage Events pulls from category Events AND Workshop (currently only pulls Events, which creates confusion for the drop-down Events by Category page as that needs category: workshop to appear in correct place).
1. For front page Events, can it be set to pull from any of Category = Events, Workshop, Talk, or Meetup (versus now where it just pulls from Events)? And create new category for Meetup? This would help with the archiving. Currently, anything that we want on the front page goes into the Events for http://dsi.ucdavis.edu/categories.html and I have to manually change it after it occurs for it to go into the correct category (workshops, talk, etc.). Would also be great to have
1. Administration in menus is a very austere word. How about something more inspiring.
1. [now in Events but not great place] add a link to the categories.html page somewhere, maybe just in a sitemap.
1. Add the two visitors from NAIST to our faculty affiliates.
1. Faculty Affiliates
   + Create new page from facultyaffiliates.md and list under the People tab.
   + Reach out to other potential affiliates- advisory group, Raissa D'Souza, Mark Goldman, 
      Some CS folks. Xin Liu, Chen-Nee Chuah, ... see ToDo google doc for linkt to spreadsheet with potential names.
1. Integrate the following content - maybe already linked, but should have centralized place
   + Climate Refuge event.  In 
   + NSFWorkshops - dsi.ucdavis.edu/NSFWorkshops
   + R bootcamp '16 - dsi.ucdavis.edu/BootcampSep2016
   + D3 materials  - dsi.ucdavis.edu/D3materials
   + RFundamentals  - dsi.ucdavis.edu/RFundamentals
1. Get Carl's slides from talk on Text/NLP processing and have a page that links to all the
   materials, recordings, etc.
 1. Get links to Matt's materials from Bayes and add to workshop.
1. Materials from other talks.
1. Get the remaining unseminar talks from Winter and were there any from Fall 2016?
   There were a few from 2015, some of which are in the Past/
1. Add page unseminar.md file (but where?), which describes the format of the un-seminars   
1. Add all DSI workshops to the "Resources" tutorials page: http://dsi.ucdavis.edu/tag/tutorial.html.
1.	Replace the current Courses page (http://dsi.ucdavis.edu/courses.html comes from courses.html file) with the new courses file (UCDcourses.md)

## Appearance
1.	Move "People" tab to be listed after "About".
1.	Under "Events", get rid of "Announcements" (http://dsi.ucdavis.edu/category/recent.html) (or re-direct to the home page) and "Past Events" (http://dsi.ucdavis.edu/category/past.html). Both are incomplete and redundant of content elsewhere on the site.
1. Move Office Hours on homepage to the top left panel, above Opportunities.
1. !! If the window is too small, the menus disappear.
     Remove the @class in <div class="nav-collapse collapse">
	 But then it doesn't collapse, but goes vertical.
	    search for: bootstrap flatly navbar menus disappear
1. [low] Put buttons at top like the ISS
     + Subscribe  News  Events  Give
     + Make these buttons a header on each page.		

# Check
1. Check all links
    + [created - please edit] unseminars.html from index.html
    + .edu/pages/main/Collaboration
1. Workshops links.
1. carousel links - workshops. 
1. Link to propose a workshop form on Workshops page says "you need permission" (links to https://docs.google.com/forms/d/1PJN-ifhOdUsFIX5cGl7y1pSldPsOfnT1MCO4Fat2DWA/formrestricted?edit_requested=true) 
1. Propose a project link on homepage is broken (http://dsi.ucdavis.edu/pages/main/Collaboration.html)

#### Done
1. [done] Fix the news entries that appeared when we added.
    Easy to introduce as a Category: Talk and not Past
	

# New Structured Pages
1. Order the news item by some other criteria.
    + Currently you can set the Category to APriority.
    + exclude items with nonews attribute set to true.
1. Template for workshops, seminars  - XML or Markdown or DCF
    + Figure out how to do group bys in the templates. Or do this in R.
1. [started] Page for current jobs
    + See jobs.html.  Can build a new template file for this and just look at the categories named Jobs and either in
    + Format the resulting HTML page better to separate the current anb previous jobs.
    + [done] Recent or check for expired is defined.
	
#### Done	
1. [done] In the carousel, have the text wrap around the image.
    + See experiment
	+ Sort out the column structure and offset
1. [done] in categories.html (via the template) format the date/time better
   + [done] for jobs, drop the time
   + [done] drop the PST everywhere - see pelicanconf.py's DEFAULT_DATE_FORMAT variable.
   + [no need] can post process the .html with R if we want.
      doc = htmlParse("build/categories.html")
	  getNodeSet(doc, "//time")
1. [done] [index.md] Reformat the first page so the news and events don't dominate and nobody sees the
   material below
     With fewer old events in the Upcoming Events, this will be less of an issue.
	 But perhaps have these three topics also cycle through like the banner at the top.
1. [done] Get rid of the old events in the upcoming events.
1. [fixed] Search doesn't lead to valid link.
      https://github.com/talha131/pelican-elegant/issues/147

# Content
Write or edit/complete
1. Add in all the other events that are not in the .md files, 
   + ie. from earlier. See events.rss from original web site
   + and separate out the unseminar talks into separate files.
1. [index.md] Rewrite/confirm the text on the first page
1. Propose Projects link on home page - what is it supposed to go to? A form or the collaboration page?
1. Person for the FDA project in collaboration.md
1. Add section somewhere on working groups - current and previous.
1. STS job announcement- fill it out when approved.
1. Plan for Academic unit and programs, HIPs.
1. twitter link in the footer.html template.
1. The related page should separate the davis and external  links on different pages.
1. Think about a new front page that represents the hub/graph and allows people to click on
   different aspects.
    So show research, collaboration, software, training, academic programs, affiliates, etc. as nodes.


#### Done
1. [done] FAQ
    + [done] change "rooms"
    + [done] rephrase courses item.
1. [done] !! Image for workshop and also unseminar series for carousel.	

# Seminars
   + Upcoming
   + Past
   + ?? Use jinja/pelican or R?
   
# Workshops
1. Already a page for these that is auto-paginated.
1. Different quarters grouped
1. Decide on format and then programmatically manipulate these into a page.
  
1.  Information (i.e. documents) are in  content/articles/Past

# Calendar
merge all calendars of events.
+ See CalendarSync
+ Get and merge the calendar information from the different  calendars via OAuth2
+ generate events
+ display calendards in 


# Jobs
   + [done] Add to menus under Resources.
   + [done] on front page in "News" or something related
   + list of jobs. See categories.

# @DTL Content Verify
   + Our Research Software from DSI.
      [check] software.md
   + Review (i.e. Read) the collaborations.
   + [done] Unlink the opportunities   


# Affiliates  content/affiliates.md -
   + [low priority] Grid layout? PLR - looks fine as is, I'd leave it as a list.
   + [low priority] Blurb about each person could have a a "read more" to expand inline, or a popup or bring to a different page.
   + [The page is generated statically as are all the pages. So it doesn't look for the files when you visit the page. Otherwise it would get a broken image.  So we show the incognito picture.
	 We need to regenerate the affiliates.md page which is done via the mkAffiliates function in the funs.R file. This is done in the content directory.]
	 Check why photos of Shaun Geer, Ehsan Gholami, Luiz Carlos Irber, Eric Kalosa-Kenyon, Nicholas Ellinwood, Yuefeng Liang, Ryan Peek, Abbie Poppa, Lida Anita To, Nick Ulle, Ken Wang, and Ismail not showing up. (Filenames are ex: ShaunGeer_c.jpg) .
   + get rid of  word "postdoc, " before "Visiting postdoc" - DTL:  Well, he is not our postdoc.
   + [done] Single column layout
   + [done] Automate the page generation.
   + [done] fix the errors.
   + PLR needs to get blurbs and photos from the most newly admitted affiliates (Julie, etc.).
   + Add Alumni section???  <br/>
      DTL: Sounds good.  We'll have to add code to generate that different
      section (not very difficult) or have a separate page.  That separate page could be generated manually.


# Miscellaneous
   + Move People tab to come after the About tab and before the Research tab.  I (DTL) don't agree;
     I moved it from there
	   Doesn't it actually belong under About ?
   + Get images for the remaining affiliates. Nick Ulle, Ken Wang, Lida Anita, Abbie Poppa (check
     name spelling), Ryan Peek, Ismail, Yuefeng, Nick Ellinwood, Eric Kalosa-Kenyon, Ehsan Gholami,
     Shaun Geer; 
   + Add photos for Titus and Andrew to faculty affiliates page
   + In content/pages/affiliates.md, who should they send an email to ask to be added to the private  affiliates channel.  Is this page linked from anywhere ? i.e. will people get to it?
   + Add photos to Admin page for D, N, C, P & M
   + Add YEAR and Quarter to all events on the "Past Posts" Events Page and organize by date (most
      recent on top). Change page name to "Past Announcements"??
   + Set the Category for workshops/tutorials/etc.   See the functions in the R code for checking these.
	+ Add all the missing events that are in the events.rss.   DTL: Ported many over. See events.rss
      in this repository for remaining one.
	+ !!! [done] Add the D-RUG website https://d-rug.github.io/  to page http://dsi.ucdavis.edu/posts/OfficeHours/davis-r-users-group-informal-drop-in-work-session20170820.html. 
        **Whatever you don't add it to the html file. That is autogenerated.**
    + [done see content/proposeProject.md] When you click "propose a project" it takes you to the collaborations page, which is okay but
      it's a bit unclear where to propose on that page. 
	   Yes, a new page needs to be written.
	+ Font all over the entire website is small....
	+ [done] Top of the Office Hours page, get rid of Spring 2017 and instead write: "Below are our typical weekly office hours. If you plan to come, we encourage you to contact us in advance because our hours are subject to change, especially during the summer."
	+ [moved] Workshops tab under Events just takes you to the homepage.
	    [done] Suggest moving it from Research to under Events. - It was in both.
		Need to generate workshop.html page (programmatically).
	+ For the Suggest a Workshop, "this form" link says special permissions are needed. Probably okay, but not sure why if won't let me access it on campus. https://docs.google.com/forms/d/1PJN-ifhOdUsFIX5cGl7y1pSldPsOfnT1MCO4Fat2DWA/formrestricted?edit_requested=true
    + Mark Redican in people.md has a link to dsi.ucdavis.edu. - For now, removed the link.  Mark keeps a very low profile!
    + Change Category for "Talk" to "Un-Seminar" for consistency across the website?
	
#### Done
1. [done] Move "Space" page from under Research to About.
1. [done] fix name Michael Bissell (add L to end)
1. [done - different photo ] Fix the height of Michael Bissell photo   

# Bring from other site
   + Jobs.
   + NSF workshops.
   + [done] Put the events.rss file into this repos.

# BROKEN LINKS
	+ Subscribe for news of events on all pages goes to http://dsi.ucdavis.edu/posts/Office%20Hours/signup.html but is NOT FOUND; it should direct instead to http://dsi.ucdavis.edu/signup.html 
	+ [position not live yet] Jobs: http://dsi.ucdavis.edu/posts/Job/faculty-position-for-data-studies-in-science-and-technology-studies-and-data-science20170901.html
	+ [fixed] People->faculty members->membership page http://www.dsi.ucdavis.edu/About/Membership/  Should be http://dsi.ucdavis.edu/membership.html
	+ [fixed] Clicking on more for the FAQ is the DSI interested in collaborations link is broken, goes here: http://dsi.ucdavis.edu//Collaboration.html
	+ [fixed] Also under FAQ the Here for how to find out about events is broken, goes here: http://dsi.ucdavis.edu//Signup.html
	+ [fixed] Clicking on listserv on the Workshops page is broken, http://dsi.ucdavis.edu//signup.md. Spring 2017 and Winter 2017 are also broken.
	+	RFundamentals: Notes & Outline link is broken
	+	Visualization Principals: Slides is broken (http://dsi.ucdavis.edu/posts/Workshop/Visualizatio20170609.html)
	+	Efficient Code in R: Resources is broken (http://dsi.ucdavis.edu/posts/Workshop/workshop-efficient-code-in-r20170428.html)
	+	Machine learning session 1: The link isn't broken, but needs a parenthesis removed to make the hyperlink functional (http://dsi.ucdavis.edu/posts/Workshop/MachineLearnin20170505.html)
	+	D3 Workshop: Link to Workshop Materials is broken (http://dsi.ucdavis.edu/posts/Workshop/D3DataVisualizatio20160603.html)
	+	Advanced Beginner Python (main link is broken)
	+	Data Visualization Workshop: materials here is broken (http://dsi.ucdavis.edu/posts/Workshop/DataVisualizatio20150425.html)
	+	Web Scraping and Services: Materials here link is broken (http://dsi.ucdavis.edu/posts/Workshop/WebScraping201520150404.html)
	+	Workshop on accessing data from API's: Link to materials is broken (http://dsi.ucdavis.edu/posts/Workshop/WebScraping201420140929.html)

	

