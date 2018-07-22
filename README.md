
[![Travis](https://api.travis-ci.org/allandequeiroz/cloudflare-ddns.svg)](https://travis-ci.org/allandequeiroz/cloudflare-ddns)

[![](https://images.microbadger.com/badges/version/allandequeiroz/cloudflare-ddns.svg)](https://microbadger.com/images/allandequeiroz/cloudflare-ddns "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/allandequeiroz/cloudflare-ddns.svg)](https://microbadger.com/images/allandequeiroz/cloudflare-ddns "Get your own image badge on microbadger.com")

[![](https://images.microbadger.com/badges/version/allandequeiroz/cloudflare-ddns:amd64.svg)](https://microbadger.com/images/allandequeiroz/cloudflare-ddns:amd64 "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/allandequeiroz/cloudflare-ddns:amd64.svg)](https://microbadger.com/images/allandequeiroz/cloudflare-ddns:amd64 "Get your own image badge on microbadger.com")

# Cloudflare DDNS

Please, help yourself using this Docker image to update your dynamic domain IP address on Cloudflare registries.

## How to use

You need to provide 3 pieces of information as environment variables to create your container.

**Cloudflare API key**

1. Login to the Cloudflare account.
2. Go to My Profile.
3. Scroll down to API Keys and locate Global API Key.
4. Click API Key to see your API identifier.

**Cloudflare e-mail address**

This one you probably know by heart :)

**The Domain to be updated**

I'll assume that you're planning to use [Docker Compose](https://docs.docker.com/compose/). In this case, you could simply replace the existing ***.env*** file with your own one providing the information above, eg:

```
CLOUDFLARE_API_KEY='your Cloudflare API key'
CLOUDFLARE_API_EMAIL='your Cloudflare e-mail address'
CLOUDFLARE_API_DOMAIN='your domain address'
```

You can have a look at [Docker Secrets](https://docs.docker.com/engine/reference/commandline/secret/) if you're looking for an alternative way to keep your information.

Now you just need to start your container.

`docker-compose up -d`
