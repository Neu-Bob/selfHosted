# Self-hosted Apps

## Infrastructure Services 

### Infrastructure Management
- Ansible

Ansible is a "declarative" configuration manager. You use YAML to describe the state that local or remote systems or configuration files should be in. You periodically run the tool to validate that "everything is as it should be" and take corrective actions if they are not.

### Networkwide Ad and Malware Blocking
- pi-hole
 
Pi-hole is a caching DNS server that, when servicing DNS lookups requested by other devices, will ignore lookups for domains that are known to offer ads and malware. This establishes a largely ad-free experience for all devices on your network. Note that this does not eliminate pre-roll ads from YouTube. There is no known way to avoid them without paying for YouTube Premium or downloading videos with youtube-dl.

### Monitoring and Availability
- Uptime Kuma

Uptime Kuma is an uptime or availability dashboard that offers at-a-glance updates of the current availability of critical resources as defined by you. The tool is also capable of sending down/up alerts via email.

### Workflow automation
- NodeRED

Node-RED is a no-code scripting environment that allows drag-and-drop configuration of high-level capabilities and functions.

### File Services
- OpenMedia Vault

OpenMedia Vault (OMV) is one of several popular Linux distributions designed to convert any computer capable of running Linux into something resembling a much more expensive Network Attached Storage (NAS). OMV makes storing, sharing, and backup of data easy, and allows for easy integration with Docker for running low-impact containers close to the shared storage. Commonly used with Raspberry Pi computers installed in custom computer cases designed to hold  a Pi and several hard disk drives.

### Password Manager
- VaultWarden

VaultWarden (ex BitWarden RS) is a free highly-capable password manager that competes strongly against similar alternatives that charge monthly fees for use. As VaultWarden consists of the Open Source components released with BitWarden, all BitWarden clients are compatible with VaultWarden servers.

## Media Consumption

### News
- FreshRSS
 
FreshRSS is a self-hosted Google Reader clone but without all the tracking. It supports multiple, independently managed logins per server and replicates the configured RSS feeds to local disk for presentation. Articles that are selected for browsing (usually the first paragraph, sometimes the entire article) are not reported back to the original source, thus protecting your privacy. Clicking on an article title will load the article from the original page, thus eliminating any privacy protections you had up to that point.

### eBooks
- Calibre eBook manager

Calibre and Calbire Web is akin to Plex for ebooks. It is a comprehensive ebook library management tool. It not only stores over a dozen data fields per entry, it also offers format conversion, automatic downloading of daily headlines from various sources, and a web-based online reader or download tool.

### Multimedia Library Management
- Servarr

Servarr is a generic term for a series of tools and applications that together offer automated downloading and organization of media of all different types. All the associated apps (the `arrs`) need an external app that helps the managing app identify what is available for download. The supporting tool is called an indexer, and there are different indexers that specialize in each type of download network. See https://wiki.servarr.com/ for more information about the commonly hosted applications.

- Radarr

Radarr is the movie locator and manager component of the Servarr stack. Radarr is able to use an indexer to find movies available via numerous services, including BitTorrent and USENET. If a movie has been marked as being "in the library" but not yet downloaded, radarr is capable of searching indexers for the title until a suitable download can be found. You may also toggle the continuous searching on and off if you wish to wait a while for a good copy of a desired film to become available. Once a copy that matches the selection criteria has been found, Radarr sends a download request to the download tool, described below.

- Sonarr

Sonarr is the TV show and episode locator and manager component of the Servarr stack. It works the same way as radarr in terms of searching indexers for missing episodes and seasons of TV shows and passing the download requests to the download tool when a suitable episoe appears to have been found.

- Spotweb

Spotweb decrypts encrypted data that has been posted to USENET for the purpose of locating any multimedia that has also been posted to USENET. It bootstraps itself, reading USENET for the purpose of determining what has been posted to USENET and is ready for download. Spotweb updates its database of what is available for download hourly, and continuosly replies to search requests arriving from the arr apps. Spotweb also offers its own minimalistic web interface that can be used to locate media and trigger downloads without involving any of the arr apps in the process.

- NZBGet

Arr apps that download from USENET need a tool that is designed to download file parts from USENET and reassemble the parts into the whole original file. NZBGet performs that download and reassembly process, leaving successfully downloaded and reassembled files in a location known to each arr app. The arr app will then pick up the completed file and move it to the proper location in the media library.

### Multimedia Playback
- Plex

Plex is a media player that plays movies, TV shows and music either stored locally or available via a selection of streaming services. Plex also integrates with HDHomeRun TV antenna tuners to offer live TV to viewers or (as a paid feature) a DIY DVR capable of recording TV shows or movies on local storage. The DVR feature is unique in that it is able to detect and remove commercials from recorded shows and movies. Finally, Plex integrates with smart speakers such as Alexa, Siri or Hey Google! to allow you to ask your smart speaker to play stored on your server.

- Kodi

Kodi, formerly Xbox Media Center or XBMC, does not necessarily qualify as a self-hosted server. It is a media player app that supports tens of thousands of sources for movies, TV shows, stored music, and streaming audio and video sources. A common use for Kodi is to attach to NFS shares presented by your file storage system on your local network.

## Office and Productivity Applications
### Office Suite

- NextCloud

NextCloud is an Open Source alternative to Lotus Notes or Microsft Office and SharePoint. NextCloud offers email, shared calendars, task management, instant messaging, and shared file storage. The shared file storage feature is compelling because the mobile apps offer configurable automatic uploads to the server. This is especially useful when searching for an automatic photo backup service (like those offered by Apple and Google) but does not send your photos to a Cloud service. All of your data stays local to your server, respecting your privacy.

## Social Media and Communications
### Decentralized Instant Messaging
- Matrix

Matrix is a decentralized Instant Messaging tool that provides fully encrypted person-to-person chat and "rooms" where multiple users can join to have a secure text, audio, or video chat session. The functionality is equivalent to several similar tools including IRC, Discord, SMS text messaging, Apple Facetime, and Google Duo and Meet, except fully encrypted end-to-end without trusting any third parties using closed source software and Cloud servers.

### Federated Social Media (aka Fediverse or ActivityPub)

At the core of all social networking is the act of "updating" others about your "activity". The Fediverse is a term used to describe a collection of services that all communicate with each other (federate) using the ActivityPub protocol. Each application provides a different user experience, but the goal is the same: to enable communication via a preferred approach to interaction. It is important to note that while all ActivityPub applications can share data amongst each other, only Mastodon and similar tools allow viewing of media shared on any other ActivityPub-compatible client. By following all of someone else's ids across all ActivityPub platforms from your Mastodon client, you can view, like, share, and comment on anything posted by anyone on any platform all without leaving your Mastodon client. You can still use the native tools to interact with them (and you must for advanced functionality) but you are not required to for basic interactions.

- Mastodon

Mastodon offers ActivityPub-based federation of "microblogging". Microblogging is a form of writing using short blurbs to make your point. There are many microblogging platforms, but the most popular one by far worldwide is Twitter.

- Bookwyrm (in progress)

Bookwyrm provides an ActivityPub-based alternative to Goodreads by Amazon. Goodreads (and therefore Bookwyrm) enables people to share lists of books, reading targets, book reviews, and other comments that book lovers like to leave for one another.

### Other ActivityPub applications

There are other ActivityPub-enabled social media applications I am considering installing, but have not yet started the process.

- Pixelfed (being considered)

Pixelfed is an Instagram clone. It allows storing photos and publishing them for others to see, like, share, and comment on. I am considering deploying Pixelfed since I am only using the automatic photo backup feature of NextCloud at this time. I would much rather use an application designed for storing, organizing, and sharing photos.

- Lemmy (being considered)

Lemmy is a Reddit clone. I don't need to find an alternative to Reddit right now, but my general interest in ActivityPub and the Fediverse is giving me more than a passing interest in Lemmy. A common complaint I've heard about Lemmy is the extremely low population count, making the Lemmy experience far less useful and effective than Mastodon (which recently passed 8 million users).

## Telemetry and Data Collection

### TeslaMate

### Airplane tracking (for providing position reports to websites and apps)
- ADS-B Hub
- ADS-B Exchange (best known for not honoring any block requests)
- FlightRadar24 (most popular site but blocks aircraft upon request)
- OpenSky
- Planefinder
- FlightAware (best app for road warriors)
- PlaneWatch
- RadarVirtuel
- RadarBox
