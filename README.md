
[![Travis](https://api.travis-ci.org/allandequeiroz/cloudflare-ddns.svg)](https://travis-ci.org/allandequeiroz/cloudflare-ddns)

[![](https://images.microbadger.com/badges/version/allandequeiroz/cloudflare-ddns.svg)](https://microbadger.com/images/allandequeiroz/cloudflare-ddns "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/allandequeiroz/cloudflare-ddns.svg)](https://microbadger.com/images/allandequeiroz/cloudflare-ddns "Get your own image badge on microbadger.com")

[![](https://images.microbadger.com/badges/version/allandequeiroz/cloudflare-ddns:amd64.svg)](https://microbadger.com/images/allandequeiroz/cloudflare-ddns:amd64 "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/allandequeiroz/cloudflare-ddns:amd64.svg)](https://microbadger.com/images/allandequeiroz/cloudflare-ddns:amd64 "Get your own image badge on microbadger.com")

# Cloudflare DDNS

Dockerized way to update Cloudflare domain IP address periodically.

## How to set it up

You need to provide 3 pieces of information as environment variables to create a container.

### 1. Cloudflare API key

* Login to the Cloudflare account.
* Go to My Profile.
* Scroll down to API Keys and locate Global API Key.
* Click API Key to see your API identifier.

### 2. Cloudflare e-mail address
### 3. The Domain to be updated

Assuming that you're planning to use [Docker Compose](https://docs.docker.com/compose/), you could simply create a ***.env*** file providing the information above as property values, eg:

```
CLOUDFLARE_API_KEY='your Cloudflare API key'
CLOUDFLARE_API_EMAIL='your Cloudflare e-mail address'
CLOUDFLARE_API_DOMAIN='your domain address'
```    

__* The `.env` file must be at the same level as your `docker-compose.yaml` file unless you have an `env_file` section on your `docker-compose.yaml`__. [The “env_file” configuration option](https://docs.docker.com/compose/environment-variables/#pass-environment-variables-to-containers)

__* You can have a look at [Docker Secrets](https://docs.docker.com/engine/reference/commandline/secret/) if you're looking for an alternative way to provide your details.__

## How to use

From this point, you just need to start your container.

`docker-compose up -d`
