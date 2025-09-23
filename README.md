# decidim-shared-actions

This repository holds the actions that [PokeCode](https://pokecode.net) uses throughout the different decidim applications and modules.

## List of actions

- Upgrade instance
  This action upgrades the gem dependencies of the application in a conservative manner. After that it generates a PR. It should be used in the application with a scheduled action, that way you can update the application on a weekly basis. The upgrade will only apply for patches, so there shouldn't be any problem with braking changes and so on. Always take into account to also have actions to test and build the application.
- Run brakeman
  This action runs the brakeman gem to generate a report to see the security vulnerabilities of the application. It won't make the action fail if there are warnings, as we are limited to the release process of Decidim, but it will give us information on how we are doing related the security best practices
