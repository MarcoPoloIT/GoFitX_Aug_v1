GoFit X Geylang — website + member guides
=========================================

CONTENTS
  index.html                                the site (menu items 01–10)
  our-membership-plans.html                 02 › MEMBERSHIPS        (own page, for SEO)
  visitor-passes.html                       03 › VISITOR PASSES     (own page, for SEO)
  our-equipments.html                       04 › WHAT YOU GET       (own page, for SEO)
  personal-training.html                    06 › PERSONAL TRAINING  (own page, for SEO)
  pt-jason.html, pt-amit.html, pt-xin.html  06 › trainer profiles
  mobile-app-tutorial.html                  10 › GOFIT APP TUTORIAL
  guest-registration-tutorial.html          10 › TRIAL REGISTRATION
  plus-upgrade-tutorial.html                10 › UPGRADE TO PLUS
  voucher-new-membership-activation.html    10 › NEW TERM MEMBERSHIP REGISTRATION
  voucher-membership-renewal.html           10 › TERM MEMBERSHIP RENEWAL
  lazada-new-membership-activation.html     10 › LAZADA PURCHASED TERM REGISTRATION
  lazada-membership-renewal.html            10 › LAZADA PURCHASED TERM RENEWAL

  img/                                      all photos, screenshots, logo, icons
  about-us.html, contact-us.html, faq.html, redirects from the old Wix URLs —
  our-classes.html, photo-gallery.html,     keep them so old links and Google
  terms-of-use.html, privacy-policy.html,   rankings carry over. Each one just
  monthly-membership.html,                  forwards to the new page.
  term-memberships.html,
  gym-rules-and-etiquette.html,
  our-personal-trainers.html,
  personal-trainer-*.html
  robots.txt, sitemap.xml, favicon.ico      search engine files — keep at the root

  Photos and screenshots live in img/ (self-hosted, no external image
  hosts). Nothing depends on Wix. Upload img/ together with the pages.
  The PT pages (pt-*.html) still embed their own photos.

DEPLOY
  Drag this folder onto netlify.com/drop, or connect it to Cloudflare
  Pages. No build step. Keep all files in the same folder.

HOW THE LINKS WORK
  Site  → guide   the 10 list links to each guide by filename
  Guide → site    "← GoFit X" (top left) returns to the 09 guides list
  Guide → site    "Finish" on the last step returns to the home menu
  Guide → guide   registration guides end by linking to the app tutorial

  Filenames match the intended public paths, so /mobile-app-tutorial
  will resolve on most hosts without any change.

  If you later serve extensionless URLs, edit these constants:
    index.html          the GUIDES array — the "f:" value on each entry
    each guide          var HOME  and  var APP_GUIDE, near the top of
                        the script, plus the "← GoFit X" link in the markup

GUIDES ARE UNLISTED
  Each guide is noindex,nofollow with a canonical URL set. They do not
  appear in search results — they are meant to be sent by link. They are
  reachable from menu 10 if a member goes looking.

EDITING
  index.html   MENU, GUIDES, CLASSES, PLUS, TCS (Plus only) — near the
               top of the script
  Memberships, visitor passes, personal training and What You Get are
  plain HTML in their own pages — edit prices, plans, T&Cs and photos
  there. Prices also appear in index.html (home ticker, FAQ, menu
  subtitles, JSON-LD) — keep them in step.
               FAQs are plain HTML in the QUESTIONS section (id="faqList").
               When you edit a FAQ, edit the matching Question in the
               JSON-LD in <head> too — the two must say the same thing.
  sitemap.xml  add any new indexable page; update <lastmod> on changes
  guides       GUIDE (title, intro, time) and STEPS — same place
