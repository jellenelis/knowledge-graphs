# https://jellenelis.github.io/knowledge-graphs/data.ttl

## Output of curl -I https://jellenelis.github.io/knowledge-graphs/data.ttl

HTTP/2 200 
server: GitHub.com
content-type: text/turtle; charset=utf-8
last-modified: Sun, 01 Mar 2026 23:17:36 GMT
access-control-allow-origin: *
etag: "69a4c910-1d1"
expires: Sun, 01 Mar 2026 23:32:20 GMT
cache-control: max-age=600
x-proxy-cache: MISS
x-github-request-id: 3B24:D861F:152B225:155CEE1:69A4CA2B
accept-ranges: bytes
date: Sun, 01 Mar 2026 23:22:49 GMT
via: 1.1 varnish
age: 30
x-served-by: cache-bru1480041-BRU
x-cache: HIT
x-cache-hits: 1
x-timer: S1772407370.930369,VS0,VE1
vary: Accept-Encoding
x-fastly-request-id: 97122383fc82006b41ccc671b61138d6553b589f
content-length: 465

## Content-Type

The content-type that is returned by the server is "text/turtle; charset=utf-8", presumably based on the file suffix.

## CORS

The server indicates that the resource can be requested from all domains, based on the access-control-allow-origin header having the value "*".

## Caching

The server uses both the cache-control header indicating the resource can be cached for 600 seconds or 10 minutes and the etag header allows the client to use the if-none-match header to ask for an updated version. The vary header tells caches to take into account the accept-encoding header while caching.

## Compression

The request headers do not indicate any form of compression, although the vary header mentions accept-encoding. The vary header indicates the server might support compression since it indicates accept-encoding as an additional header to use to distinguish which requests can be answered with cached responses, although using the curl command "curl -i -H "Accept-Encoding: gzip, deflate, br, zstd" https://jellenelis.github.io/knowledge-graphs/data.ttl#" does not result in a compressed response. Most probably, the server is deciding that it makes no sense to compress the response since it is only 465 bytes.
