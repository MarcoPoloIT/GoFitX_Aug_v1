GoFit X Geylang — website + member guides
=========================================

CONTENTS
  index.html                                the site (menu items 01–09)
  mobile-app-tutorial.html                  09 › GOFIT APP TUTORIAL
  guest-registration-tutorial.html          09 › TRIAL REGISTRATION
  plus-upgrade-tutorial.html                09 › UPGRADE TO PLUS
  voucher-new-membership-activation.html    09 › NEW TERM MEMBERSHIP REGISTRATION
  voucher-membership-renewal.html           09 › TERM MEMBERSHIP RENEWAL
  lazada-new-membership-activation.html     09 › LAZADA PURCHASED TERM REGISTRATION
  lazada-membership-renewal.html            09 › LAZADA PURCHASED TERM RENEWAL

  Every file is self-contained — all photos and screenshots are embedded.
  No external image hosts. Nothing depends on Wix.

DEPLOY
  Drag this folder onto netlify.com/drop, or connect it to Cloudflare
  Pages. No build step. Keep all eight files in the same folder.

HOW THE LINKS WORK
  Site  → guide   the 09 list links to each guide by filename
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
  reachable from menu 09 if a member goes looking.

EDITING
  index.html   MENU, GUIDES, MEMBERSHIPS, PASSES, PT, FLOORS, CLASSES,
               FAQS, TCS — all near the top of the script
  guides       GUIDE (title, intro, time) and STEPS — same place
