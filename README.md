# rsyncster
CMS -> Static site generation using standard \*nix utilities.

Philosophy is seven second rule. Avoid tl;dr. User experience is fast, clean, simple. Mobile optimized. Accessibility is important. Screen reader friendly. Open source, open cloud, 'cause your content is yours and should not be locked to your cloud provider.

This is very basic sloppy code, please vent your frustrations by fixing and sharing your awesome improvements. :)

__Status:__ 30nov2018 - Works. Calling this release candidate rsyncster_v.001_30nov2018.rc01. This solution is for those who know their web backends. It is not polished.


__Dependencies__
* Perl
* Wget
* Rsync
* Sed
* Cron
* Find

__Backend environment__
* Haproxy
* Nginx
* Apache2

__CMS assumptions__
* Simplified one-page interface. Bootstrap theme.
* Mobile emphasis. No menus, mobile users can't see, don't use.
* No ajax or sliding features etc.
* Deep functionality and ui complexity available with login.
* Public facing assets are obsessively lean and easily consumed.

__Rsyncster Installation__
* - git clone - (Developers can make pull request)
* No documentation yet, you'll just have to read the code.
* Usage: Call cron_get_changes.sh from cron entry. There are helper scripts in ./extras.
* Configure variables for your setup.

__Basic Drupal Workflow__
* Change top level dns record. eg domain.tld -> subdomain.domain.tld
* Update $base_url in settings.php (required)
* Edit site according to CMS assumptions above. eg Strip out everything that is unneccessary.
* Enable anonymous page caching (required)
* Turn off database logging (optional)
* Verify custom logos and favicon. Set in theme and global settings.(optional)
* Update scripts with your subdomain
* Run scripts as needed
* Enjoy your new peace of mind.
