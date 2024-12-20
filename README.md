# zenn-docs-template

## Quick start

Set up env.
To test locally, save to `.env`.
To run on github actions, set them to repository secrets.

```toml
NOTCMS_SECRET_KEY=<your secret key>
NOTCMS_WORKSPACE_ID=<your workspace id>
```

Set up webhook
[reference](https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#create-a-repository-dispatch-event)

```sh
curl -L \
  -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <YOUR-TOKEN>" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/OWNER/REPO/dispatches \
  -d '{"event_type":"sync_zenn"}'
```
