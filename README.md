# SpamAssassin for docker

This is an image for running [SpamAssassin](http://spamassassin.apache.org/). This image is based on the lightweight [Alpine Linux](https://alpinelinux.org/).

## Usage

To run spamd
```
docker run -v /var/lib/spamassassin:/var/lib/spamassassin -v /etc/spamassassin/user_prefs:/etc/mail/spamassassin/user_prefs:ro waldher/spamassassin spamd -i 0.0.0.0:40001
```

To retrieve updates
```
docker run -v /var/lib/spamassassin:/var/lib/spamassassin waldher/spamassassin sa-update
```
