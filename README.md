# SLP Requirements Document
#Alzheimer's Association, Central & Western VA Chapter

**Nonprofit overview:** To eliminate Alzheimer's disease through the advancement of research; to
provide and enhance care and support for all affected; and to reduce the risk of dementia through
the promotion of brain health.

**Contact:** Mary Sandridge, msandridge@alz.org, 973 6122 x 106

**Website:** [http://www.alz.org/cwva](http://www.alz.org/cwva)

System summary: A system that will help manage the 1,000 volunteers, as well as keep all their
data in a single place. Also, a volunteer portal where volunteers can sign up for various events.

**Development notes:** The http://www.alz.org website is managed by the national organization,
and installing software on there for this chapter is likely not going to be allowed; so a separate
hosting site will be necessary. The customer is aware that this may incure a nominal hosting
charge. The current website is hosted on “Red Dot”, which is apparently a content management
system. This is what the national organization provides, and some aspects (such as the look and
feel, or the top navigation bar) cannot be changed. However, the chapter is able to insert links,
so they could insert a link to a site such as “cvillealzheimersportal.org”, or similar.

**Confidentiality notes:** The information in this system deals with the volunteers, not those who
have Alzheimer's. Thus, no medical information will be kept in the system. It is thus considered
slightly confidential, and an NDA may be necessary. A sample NDA is included as an
attachment.

##Description
The chapter serves central and western Virginia, and includes 37 counties in that area.
The Charlottesville office has 10 staff members, and is one of 4 offices in the chapter. It is the
head office of the chapter, and thus the largest of the chapter offices. There are about 1,000
volunteers throughout the chapter's area. Most, but not all, have Internet access and email
(probably 95% are online, 5% are not). 

The volunteers for the chapter sign up for various events – a race, staffing a booth, etc. Some volunteer for many different events throughout the year, and some only volunteer for one event (say, the 5k race each year). Currently, they keep track of their volunteers through a series of Excel files that are inconsistent as to what data fields they record; also, some data may only exist in hard copy form. The chapter uses Raiser's Edge to manage their fund raising. There is  minimal overlap between the volunteers (that this system will handle) and donors (that Raiser's Edge will handle); any overlap will require duplicate data entry (into both systems), and this is
acceptable.

The purpose of this project is to build a volunteer management system that will keep
track, in a single database, of all the volunteers, managing volunteer scheudling, and keeping
track of the events that they volunteer for. One-time conversions of the Excel data sets into the
system will be necessary. A volunteer portal is also part of this project. The portal only has a
few features included, as much of the system is the volunteer management that is only seen by
the staff.

##Features
* A volunteer registration form. This would, presumably, both create an account and
complete the form at the same time. They could then update their profile. And
configurable email updates about this sent to some/all of the staff.
 * The current (hard-copy) volunteer registration form is included as an attachment.
 * It may be that the form needs to be configurable (it's a lot more work to make it so,
thus if it does not need to be configurable, then that extra time can be spent on other
system development).
* Database of volunteers (and their profiles)
 * Queries based on many criteria, including geographic location
 * Ability for volunteers to update their profile via the volunteer portal (described
below)
 * Volunteers should have an inactive flag (if they move out of town, if they were a
temporary intern, etc.); this will eliminate them from most (but not necessarily all)
search results.
 * Obtain an email list for selected volunteers so they can send an email. The results
would beb ased on various criteria. The result would be a mailto: link that has all
their addresses, and the customer would then send the email from their regular email
program (likely Outlook).
* The volunteer portal aspect implies users and user levels: volunteer, staff, admins
* Social media integration: one of the facebook links that allows posting “I volunteered for alzheimers” to their feed; similar for twitter and others. There are numerous libraries that provide this (and many websites that have it – Lou's List, as one example).
* The staff should be able to create volunteer opportunity events, which will then be displayed, in the volunteer portal, to those logging in. These events will have categories so that volunteers can filter the possible opportunities that way. Events will likely have a maximum number of participants, and should have a configurable means to send emails when somebody signs up. Staff will also have to be able to sign up volunteers (andotherwise manage who is signed up), in particular for those volunteers who do not have Internet access. Events will have an hours field (how many hours that event took, per volunteer), which will be useful for the report generation.
* Volunteer portal
 * The ability to update profile and reset password
 * Browse and search the schedule of volunteer opportunities, and sign up for them
 * Links to other parts of the chapter website: home page, sign up for their newsletter, etc
 * Portal should be mobile friendly (both tablets and mobile phones)

* Report generation: staff should be able to pull up reports (who volunteered for this, how
many hours that volunteer did, unique volunteers this year, listing of volunteers who did a
lot for volunteer recognition, etc.)
 * Further details about the report generation, and the specific reports to be generated,
will be provided by the customer throughout the year.
* Export data to CSV

## Requirements: Minimum
* Creation of DB to hold the data, with MVC components
* Initial volunteer portal
* Transfer of some of the existing data into the system (this can be dummy data instead)
* Basic searches and report generation

## Requirements: Desired
* Fully featured volunteer management: full search capability, full report generation, create
mailto: links, etc.
* Fully featured volunteer portal: ability to search for events, sign up for them,
implementation of event participant cap, etc.
* Configurable emails to the staff when things happen in the system
* A nice UI that works with mobile devices; the look-and-feel should match their current
website
* Import of all existing data; system data exportable to CSV
* Social media integration

## Requirements: Optional
* Additional features for the volunteer portal: uploading of pictures, a full calendar-based
scheduling system, etc. These features will be determined by the customer if the project
gets that far.

##Notes
There as a company called RedDot that, in 2006, was acquired by OpenText
(http://www.opentext.com/) – this may be the content management system that they use.
