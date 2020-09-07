# dokku-cloudflare-dns

Automatically update outdated and add new DNS records to your Cloudflare zone(s) whenever an app is deployed or an apps domains have been updated.

## Usage

### Installation

```sh-session
$ dokku plugin:install https://github.com/kldzj/dokku-cloudflare-dns.git
```

### Configuration

1. Grab the IPv4 address of your Dokku instance
1. Grab a new and restricted Cloudflare API token; should have permission to edit DNS records for all the zones you want to manage ([Help](https://support.cloudflare.com/hc/en-us/articles/200167836-Managing-API-Tokens-and-Keys))

Run:

```sh-session
$ dokku config:set --global CF_SERVER_IP=YOUR_DOKKU_SERVER_IP \
                          CF_TOKEN=YOUR_CLOUDFLARE_API_TOKEN
```
