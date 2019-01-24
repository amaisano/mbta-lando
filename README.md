# mbta-lando
Lando recipe for MBTA Drupal/Pantheon site

1. [Install Lando](https://github.com/lando/lando/releases) -- comes with Docker!
  
1. Clone the [mbta/cms](https://github.com/mbta/cms) repo on your local machine.

1. Place this repo's `.lando.yml` recipe in that directory

1. build/start lando with `lando start`

1. [authenticate with Pantheon](https://dashboard.pantheon.io/login?destination=%2Fuser#account/tokens/create/terminus/) -- prefix command with `lando ` (you should have had Adamo or Gene create you as a Pantheon Team Member)

1. get Pantheon Drush aliases for the various environments: `lando terminus aliases`

1. pull the latest code and files using `lando pull` -- may have to do this twice (first run will download 2GB+ of files)

1. log in to Drupal at http://mbta.lndo.site/

ACTIVITIES
- Switching repo branches to test features -- using `lando drush cim` to update configuration
- Connecting the front-end (http://localhost:4001) to the local lando site via ENV

NOTES
- [Potential NGNIX issue with redirect](https://github.com/mbta/wiki/blob/master/website/content/drupal.md#known-issue-with-kalabox--redirect-module)
