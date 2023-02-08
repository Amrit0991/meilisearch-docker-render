# meilisearch-docker-render

Deploy Meilisearch to render.com

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

## Environment Variables

- `MEILI_HTTP_ADDR` -- the address you want your Meilisearch server to run on. (Default = `0.0.0.0:80`)
- `MEILI_MASTER_KEY` -- the master key (Default = `{randomly_generated_key}`)
- `MEILI_DB_PATH` -- where we want to persist the data. Probably don't need to change this, as it's also in the render.yaml (Default = `/meili-data`)
- `MEILI_ENV` -- environemnt level. Options are `development` or `production`. (Default = `development`)

See full list of options you can configure [here](https://docs.meilisearch.com/reference/features/configuration.html#options)

## Run locally

Install Docker Desktop

https://docs.docker.com/get-docker/

Build the image

```bash
docker build -t meilisearch .
```

Launch a container

```bash
docker run --env MEILI_MASTER_KEY=0xIMnKxGoGmSx0u3cBXKCjvhuFDfnul4 -p 7700:7700 -d meilisearch
```
