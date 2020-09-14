
# Laravel & Lando

Looking at how to configure Lando (a local dev environment built on docker) to support Laravel development.

#### Usage: 
- Copy the folder `.lando/*` into laravel project.
- Copy the file `.lando.yml` into laravel project.
- Run `lando start`.
- Done!

##### Support Files (.lando/*):
- cron.txt - typical cronfile for laravel.
- docker-php-entrypoint.sh - ensures cron starts.
- laravel-worker.conf - typical supervisor setup with paths/user adapted for lando.
- php.ini - Overcame the issue with memory limits from default Lando config for php.ini
- **Note:** If any of the above is changed, rebuild with `lando rebuild -y`

##### A few phrases I tried to search when figuring this out:
- Lando Laravel Supervisor
- Configure Lando for Laravel
- Configure Laravel Cron on Lando