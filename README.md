# mbta-lando
Lando recipe for MBTA Drupal/Pantheon site

1. [Install Lando](https://github.com/lando/lando/releases) -- comes with Docker!
  
2. Register with Pantheon (you'll need a Pantheon account for our MBTA site).

3. Clone the mbta/cms repo on your local machine.

4. Place this .lando.yml recipe in that directory

5. run `lando init` inside that directory

6. build/start lando with `lando start`

7. [authenticate with Pantheon](https://dashboard.pantheon.io/login?destination=%2Fuser#account/tokens/create/terminus/) -- prefix command with `lando `

8. get Pantheon Drush aliases for the various environments: `lando terminus aliases`

9. pull the latest code and files using `lando pull` -- may have to do this twice

10. log in to Drupal at http://mbta.lndo.site/
