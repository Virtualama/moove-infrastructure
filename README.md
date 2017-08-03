# moovechallenge-infrastructure

Basic docker-compose setup to run project

* app folder must include app source before building image
* Gemfile is bundled upon building or first start

To start things up

` ./scripts/start.sh `

To stop working

` ./scripts/stop.sh `

To remove generated images & containers

` ./scripts/clean.sh `

To open a user shell within running app

` ./scripts/bash.sh `

To open a root shell within running app

` ./scripts/root_bash.sh `

## In case of modifying Gemfile while container is up:

```
./scripts/root_bash.sh
#(inside root bash)
bundle
exit
./scripts/restart_app.sh
```

## Image rebuild is still necessary:

` ./scripts/rebuild_app.sh `

