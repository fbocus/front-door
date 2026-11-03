THE FRONT DOOR FOR FIAZ AND NANDO
=================================

What it is
  A small page that lives on a place that is always on (GitHub Pages, free). Your main web address
  (www.fiazandnando.nl) shows this page first. It does one of three things:
    - The home computer is awake: it sends the guest straight on to the real website. The language,
      the invitation code and the page the guest asked for are kept, so the QR codes on the postcards
      still work.
    - It is the rest time (22:00 to 06:00 Amsterdam time): it shows your kind notice, when the site
      opens again in the guest's own time, and the clocks of our friends around the world.
    - It is not the rest time but the computer does not answer (a power cut, a restart): it shows a
      softer "we will be back soon" notice, checks again every minute, and sends the guest on as soon
      as the computer answers.
  The page holds nothing private, so it can be in a public repository.

Before you start
  1. The real site must be reachable at its own address, for example https://live.fiazandnando.nl/
     (that is the home computer). If you choose another address, change LIVE in build_frontdoor.py
     and build again, or ask Claude to do it.
  2. The rest hours are also set in build_frontdoor.py (REST), and in the server file .env
     (REST_FROM, REST_TO). Keep the two the same.

Putting it online with GitHub Pages
  1. Make a free GitHub account and turn on two-step login.
  2. Make a new PUBLIC repository, for example "fiazandnando-front". Public is needed for free Pages,
     and this page has nothing private in it. Keep the real website and the guest list in a PRIVATE
     repository, or only on the home computer.
  3. Upload the files index.html, 404.html and CNAME from this folder.
  4. In the repository open Settings, then Pages. Choose "Deploy from a branch", the main branch and
     the root folder. Save.
  5. At the place where you bought the domain, add the records GitHub Pages asks for (a CNAME record
     for www pointing to YOUR-NAME.github.io). Add also the record for live that points to your home
     address. GitHub shows the exact steps on the Pages settings page.
  6. Turn on "Enforce HTTPS" in the Pages settings when it becomes available.

Trying it
  Add ?now=2030-01-15T22:30:00Z to the address to pretend it is 23:30 in Amsterdam (rest time).
  Add ?now=2030-01-15T10:00:00Z to pretend it is 11:00 (awake). Add ?lang=nl to choose Dutch.
  (The ?live= test link only works on your own computer, never on the real address.)

The file robots.txt asks search engines to stay away, and every page also says noindex. Keep both. Name the repository with something plain that does not show the names (for example front-door), because public repositories on GitHub can be searched.
