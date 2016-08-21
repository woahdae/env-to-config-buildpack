The World's Simplest Buildpack
--------------------

Google Drive's REST API, and therefore
[google-drive-ruby](https://github.com/gimite/google-drive-ruby), insist
for service account authorization (the simplest auth style, I think) to
be read from the filesystem.

Heroku, of course, insists configuration is done via env vars.

So, this project takes a step back and renders any erb files in
`config` into plain files, allowing you to read environment files into
config files during slug compilation. So then we can use Google Drive's
REST API, and who knows, maybe that'll be useful some other time too.

Probably won't be great to do in a Rails project, but this is just a
tiny toy project I'm using this on, so eh.
