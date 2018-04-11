Supported tags and respective `Dockerfile` links
================================================


What is Dante
-------------

[**Dante**](http://www.inet.no/dante/index.html) consists of a SOCKS server and a SOCKS client, implementing RFC 1928 and related standards. It can in most cases be made transparent to clients, providing functionality somewhat similar to what could be described as a non-transparent Layer 4 router. For customers interested in controlling and monitoring access in or out of their network, the Dante SOCKS server can provide several benefits, including security and TCP/IP termination (no direct contact between hosts inside and outside of the customer network), resource control (bandwidth, sessions), logging (host information, data transferred), and authentication.


Usage example
-------------

    $ docker run -d -p 1080:1080 usureseach/docker-dante


### Client-side set up

Set your browser or application to use SOCKS v4 or v5 proxy `localhost` on port 1080,
like for example:

    $ curl --proxy socks5://localhost:1080 https://example.com
