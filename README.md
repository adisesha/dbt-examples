# dbt-examples

# Time sync issue fix

- [See here to read more about this error](https://www.studytonight.com/post/how-to-resolve-amazon-s3-file-upload-error-requesttimetooskewed)

- To fix either manually set the time by running either of below commands
```bash
docker run --privileged --rm entechlog/dbt date -s "$(date -u "+%Y-%m-%d %H:%M:%S")"
docker run --privileged --rm entechlog/dbt date -s "$("2021-04-27 19:34:12")"
```

# Airflow Integration Notes

- Download and run [Docker](https://docs.docker.com/docker-for-mac/install/)
- Download the [Astro CLI](https://github.com/astronomer/astro-cli)
- `cd` into `\docker\astro`
- Start astro by running `astro dev start`
  > Set environment `setx DOCKER_BUILDKIT 0` to fix buildkit not supported by daemon Error
- Stop astro by running `astro dev stop`

packages.txt
libicu-dev

# References
https://www.astronomer.io/blog/airflow-dbt-1
