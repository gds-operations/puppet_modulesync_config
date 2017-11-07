# GDS-operations Puppet modulesync configuration

Contains the generic config files for the gds-operations Puppet modules. Upgrades are
made here and then propagated to all the modules using the `modulesync` gem.

## Using modulesync

Install the required gems

    bundle install

If you want to add a new file to existing repos, add the file under
`moduleroot/` and then run `bundle exec msync update --noop` to see what would change.

To add a repo to `modulesync` management insert the name in
`managed_modules.yml` and then run `bundle exec msync update --noop`

Once you're happy with the changes run

    bundle exec msync update -m "Add base scaffolding"

To work on all modules matching a regex

    bundle exec msync update -f duplicate_
