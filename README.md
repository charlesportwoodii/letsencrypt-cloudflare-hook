# CloudFlare hook for letsencrypt.sh ACME client

This a hook for [letsencrypt.sh](https://github.com/lukas2511/letsencrypt.sh) (a [Let's Encrypt](https://letsencrypt.org/) ACME client) that allows you to use [CloudFlare](https://www.cloudflare.com/) DNS records to respond to `dns-01` challenges. Requires Python and your CloudFlare account e-mail and API key being in the environment.

## Setup

```
git clone https://github.com/charlesportwoodii/letsencrypt-cloudflare-hook hooks/cloudflare
cd hooks/cloudflare
chmod a+x hooks/cloudflare/cloudflare.py
ln -s hooks/cloudflare/cloudflare.py /usr/libexec/acme/hooks/cloudflare.py
cp hooks/cloudflare/cloudflare.yml /var/lib/acme/cloudflare.yml

# Install via Python3 (pip3)
pip3 install -r hooks/cloudflare/requirements.txt
pip3 install pyyaml
```

After installing the package, edit ```/var/lib/acme/cloudflare.yml``` with your Cloudflare email address and API key
