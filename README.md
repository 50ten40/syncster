# rsyncster
__CMS -> Static site generation using standard cli utilities. Philosophy is seven second rule. Avoid tl;dr. User experience is fast, clean, simple. Mobile optimized. Accessibility is important. Screen reader friendly.__

Dependencies
* Perl
* Wget
* Rsync
* Sed
* Cron

Backend environment 
* Haproxy
* Nginx
* Apache2
* Syncthing

CMS assumptions
* Simplified one-page interface. Bootstrap theme.
* Mobile emphasis. No menus, mobile users can't see, don't use.
* No ajax or sliding features etc.
* Deep functionality and ui complexity available with login.
* Public facing assets are obsessively lean and easily consumed.

Basic Drupal Workflow
* Change top level dns record. eg domain.tld -> subdomain.domain.tld
* Update $base_url in settings.php
* Edit site according to CMS assumptions above. eg Strip out everything that is unneccessary.
* Turn off database logging (optional)
* Verify custom logos and favicon. Set in theme and global settings.(optional)
* Run scripts as needed
* Enjoy your new peace of mind.
