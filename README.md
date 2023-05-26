# cpp-ip-polling

A simple server, client (sending) & client (polling) setup for sending IP data.

## Purpose

- I have a device, I need to know how to talk to it
    - This device should routinely send data to a server, probably using CRONJOB
- I have another device, it needs to know how to talk to the other device
    - This second device does not need to share anything
    - This second device must be able to talk to the other device automatically without any (or much) user input
        - This second device may want to know how to SSH into the first device
        - And possibly other things like SFTP and HTTPS
- There also is a server
    - This server must have a static IP and port open to receive and send data
    - This server must be secure and only communicate with clients (receiving and sending)
        - Probably using asymmetric cryptography (Kalyna? never used it before, seems interesting)
        - Every client should have its own set of keys
        - The signature of the keys should be used for identification of what purpose the client has

## Libraries

- OpenSSL
- Some random TCP/IP library