# Bedrock Server Versions

This origional repo is developed by [loksonarius](https://github.com/loksonarius/bedrock-server-versions) so do feel free to go to the origional on his github page. This is just for me as I needed to edit some of the versions for Guardian Bot.

## Caveats

Needless to say, concessions are made with this approach. To be explicit:

- this is not an API, so please keep expectations reasonable
- this is a _cached_ response, not a live fetch -- expect things to be out of
  date
- there is **no validation** done to ensure returned versions are available for
  download from Mojang's servers
- the versions being returned are **server** versions, not client versions

## Updates

The repo is set up to scrape Gamepedia once a week for server versions and
update the `versions.json` file. The last run scrape time for a response will be
stored in the `LastUpdated` field of the struct in `versions.json`.

## Running Locally

The following can be used to run a scrape locally:

```bash
go run main.go
```
