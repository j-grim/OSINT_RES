# OSINT RESOURCES

### Quick OSINT Guide to OSINT resources, tools, and techniques for independent journalists and techno-sleuths.

###### This is intended for those who are just getting started in OSINT, those who are new to investigative journalism, and established independent journalists who want to expand their research techniques in a meaningful way.

# The Basics of OSINT

OSINT stands for "Open Source Intelligence". This means: intelligence that can be sourced about a given target from public records and data. In the intelligence community, OSINT has a more specific designation. In the security community, it broadly refers to any type of data that can be sourced without resorting to unauthorized access methods.

The typical OSINT researcher will use a very wide variety of sources and tactics, some of which require more advanced knowledge of networks and the ability to "roll your own" code to access or interpret specific data streams. I will address (for the sake of the target audience) provide simple guides to using a variety of resources (both programatic ones and websites).

I will include some technical instruction via command line for those running Mac or Linux, but I will indicate it with a "technical warning".


### How Does One Conduct OSINT Research?

OSINT research is conducted a number of ways, but the most basic, preliminary methodology is as follows:

1. Determine your target. Without a goal to focus on, your research is useless. If you are researching multiple people, say, in the capacity of a company or an organization, then target them one by one. But, always keep your focus on one target at a time.
2. Organize the information you already have. Examples include: Full name, university attended, place of birth or upbringing, parents names, email addresses, current addresses, phone numbers, etc. Whatever you have at your disposal, this is what you will use to build your body of knowledge on the target. 
3. Using a variety of methods, some low-tech, some very high-tech, and most being somewhere in between, you begin accumulating more and more information about the target, via public resources. 
4. OSINT, as definied by the security community (rather than the intelligence community) comes with the goal of never snapping a branch: that is, you never send a packet in the direction of the subject of your research, and the undertaking of such research is never known by the target.

This all sounds simple, and in theory, it is. You would be shocked at how much information you can learn about an individual. 

As one delves further into OSINT, the tactics become more technical. This guide will not be concerned with such things, as the assumption is that the audience using this paper are researchers and journalists, not technical types.


# Getting Started: An example

Bob is the purportedly unscrupulous owner of a night club. It is told that his business functions, underneath as a business of ill repute. Bob has decided to run for town mayor. He is well-liked, has power, money, and influence. You want to dig in deeper to see whether Bob would make a good mayor, or use his political power to do not-so-good things. Where do you begin?

*The easiest way to get started is to Google Bob.* Sounds ridiculously easy, and it is. Give him a google. Use various search functions to narrow him down. Say Bob lives in Dallas, TX. Run a search query like so:

"Bob Whatshisname" "Dallas"

Pop it into Google, and start hunting for breadcrumbs.

Don't assume anything particularly salacious is going to pop up in Google (although, you'd be shocked to find that it frequently does). Just collect whatever information you can. You are on a mission to scavenge for any data you can pick up. This includes, but is not limited to: names of pets, assets owned, addresses lived at, middle names, parents, wives and childrens' names, what kind of vehicle he drives, what his hobbies are. Remember, anything you can learn about Bob will help you create a greater scope of investigation.

Make sure to collect any images you can find of him, or taken by him. Collect the usernames of any social media accounts you come across.

Once you exhaust google, visit yandex.com. It has more fine-tuned search. The search operators for yandex are explained here: https://yandex.com/support/search/how-to-search/search-operators.html 
They are very powerful, and the search engine is very, very useful. Google also has search operators, though there are fewer. It is important to canvas the search engines to the best of your ability.
Search terms you should be concerned with are meant to include any keywords that you feel may be useful, given what you already know about Bob. Be creative. If nothing turns up, no harm no foul.

Once search engine leads have dried up, it is time to move on to greener pastures: social media accounts. You can learn a ton by adding your target on social media using a honeypot account, or a spoof account. This steps *somewhat* outside of the realm of traditional OSINT, because it puts the researcher in a position to have their IP address recorded. If you are not able to successfully obsfuscate your identity via vpn, burner phones, and email addresses obtained under anonymous conditions, skip this step. Otherwise, if you have the means and desire, continue. Find out who Bob knows, or what Bob's weaknesses are. If he likes beautiful women, make an account that is sure to draw him in. Once you have internal access to social media accounts, there is a trove of information waiting for you.

Now, if Bob is smart, he will do his best to maintain a formal presence online. (This is the case for many high-profile people, so if that is who you are after, go into social media sleuthing with the knowledge that you may not score heavy duty data this way.) What social media profiles (especially ones with photos in them) can offer you, however, is the potential for metadata.

Using image meta data, you can piece together lots of information about the individual who took the picture: where they were when they took it, what kind of device they used to take it, the date they took it, etc. This can be extraordinarily helpful. 

This can also be done for other types of media, like videos and voice or music clips. 

Beyond using social media to target him directly, depending on what you were able to obtain from your prior searches, you can start looking at his social circles in his social media accounts, doing the same thing for his associates as you have done for him.

If you are able to obtain a mix of: business records, articles, personal data, friendship data, meta data, etc, you can begin to piece together a picture of who Bob is, and where your research should go next.

In this example, let us assume that in our search, we found that Bob has several email accounts. Two of them are public (his business email, and the one he uses for general correspondence), but one is a private email that you obtained when your honeypot promised to send racy photos
if you could get an email to send them to. Hubba hubba. You never send said racy pics, because the truth is you aren't a tall, buxom blonde. What you have done, however is trace this email to a WHOIS registrant for a site called "dallasdoesdebbie.com", an escort service. You were able to achieve this by simply typing in "bobssecretemail@gmail.com" "dallas". Magically, a registrant list appeared to you in Google. As Bob is the registrant of this site, you can basically confirm that Bob has gotten into the escort business. Boom. You have hit your target.

It isn't always this simple, but starting small and building is how you get from point A to point B.

Another thing to keep in mind is that you aren't always going to find what you're looking for. Your suspicions won't always be confirmed, but you may wander down another rabbit hole entirely, and find yourself in an alternate universe, staring at something weirder, more grim, and ppossibly more damning, or... you may find that Bob is a lot more scrupulous than you believed... or at least accourding to information publicly available on him.


#Using OSINT Tools: Going Beyond Google

I've selected a handful of tools that are indespensible for low-tech OSINT research. I will include the most popular command-line tool, recon-ng, for those with macs or linux boxes, who are either command-line proficient or willing to go where eagles dare. 
Lets get things under way:


1. OSINTframework.com: Before you go out into the wild forests of the internet, hunting for dirt, you need to lay out the basics. Fortunately, OSINTframework.com does that bit for you. The pillars of OSINT lay at the base of the OSINT framework. While you are sleuthing, you have the option of taking all these avenues in the pursuit of intelligence gathering. It is helpful to run these bases. Expanding the web, by clicking on the circles, will net you heaps of different tools and avenues for researching. This should be every OSINT n00b's first stop.
Some of these are likely going to be unrelated to your journey, so feel free to completely ignore the ones you don't feel apply. Some are more advanced or for people in the field.

2.Browser Plugins: For the low-tech sleuth, browser plugins are an amazing option. While there are GUI applications for windows boxes, most of them are paid, or unmaintained. Browser plugins are relatively platform agnostic, and are often quite useful.

# Useful Tools and Links Short List: 


* OSINTframework.com - A Full interactive chart of Information Domains and tools used regularly in OSINT. Use *this* to assist in organizing your research model.
* An entire list of browser plugins for OSINT https://github.com/IVMachiavelli/OSINT-Browser-Plugins
* yandex.com - Russia's most popular browser. It contains highly customizable search tools not available through google.
* google.com (duh)
* duckduckgo.com 
* Jeffrey's Image Metadata Viewer: http://exif.regex.info/exif.cgi
* FlightRadar24: https://www.flightradar24.com/
* Wikimapia: Reverse engineer location searches: http://wikimapia.org/
* Archives of Websites: https://archive.is/
* Wayback Machine, another website archiver: https://archive.org/
* Wayback Machine downloader: https://websitedownloader.io/wayback-machine-downloader/
* Opencorporates: the biggest open database of companies in the world: https://opencorporates.com



# Full List Of Useful Tools:

* yandex.com
* nerdydata.com
* google.com
* recon-ng (Do a git pull before you run it, every time)
* craigslist.org
* CrowdTangle Link Checker https://chrome.google.com/webstore/detail/crowdtangle-link-checker/klakndphagmmfkpelfkgjbkimjihpmkh/?authuser=1
* Chrome IG Story https://chrome.google.com/webstore/detail/chrome-ig-story/bojgejgifofondahckoaahkilneffhmf
* Toolkit for Facebook https://chrome.google.com/webstore/detail/toolkit-for-facebook/fcachklhcihfinmagjnlomehfdhndhep
* (For Linux Users) Tinfoleak http://www.vicenteaguileradiaz.com/tools/
* (For Linux Users) Copernicus https://github.com/Soroboruo/Copernicus
* Image, video, and audio meta data
* FlightRadar24: https://www.flightradar24.com/
* Wikimapia: Reverse engineer location searches: http://wikimapia.org/
* Archives of Websites: https://archive.is/
* Wayback Machine, another website archiver: https://archive.org/
* Wayback Machine downloader: https://websitedownloader.io/wayback-machine-downloader/
* Opencorporates: the biggest open database of companies in the world: https://opencorporates.com
* ExifTool: Get metadata on images: https://sno.phy.queensu.ca/~phil/exiftool/
* Jeffrey's Image Metadata Viewer: http://exif.regex.info/exif.cgi
* Reverse reddit image search: http://karmadecay.com/
* Reverse Image Search Using an Archive of the internet: http://rootabout.com/
* TinEye: find websites where an image appears: https://www.tineye.com/
* (For Linux Users) Email gathering tool: Infoga - Gather via domain: https://github.com/cys3c/infoga
* (For Linux Users) Scythe - Social Media Account Harvester: https://blog.c22.cc/2012/10/03/scythe-framework/
* (Paid Service) Geofence Social Media monitoring (Monitor the social media coming out of a certain area)  - https://www.echosec.net/
* Cubib Public Records Search: https://cubib.com/
* Little Sis - Government and Business Personnel Database: https://littlesis.org/
* SocialMention- Realtime social media search and analysis: http://socialmention.com/
* WhosTalkin- Social Media Search engine: http://www.whostalkin.com/
* MelissaData - A broad-spectrum public data resource, including campaign contributions: http://www.melissadata.com/lookups/index.htm
* Geocreepy - Geolocation OSINT tool with Windows, OSX, and Source distributions: http://www.geocreepy.com/
* Pastebin search alerts: https://www.andrewmohawk.com/pasteLert/


