# mi-graphite

Please refer to <https://github.com/joyent/mibe> for use of this repo.

## About

This will install carbon, whisper and graphite version 0.9.12.
The graphite webapp will be hosted by gunicorn and nginx.

Default configuration files will be deployed with minor changes:

- carbon.conf: <code>WHISPER_FALLOCATE_CREATE = False</code> to prevent file corruptions
- storage-schemas.conf: default retention of 15s:7d,1m:30d,15m:5y

Tested with a base64 13.2.1 image (pkgsrc 2013Q2).