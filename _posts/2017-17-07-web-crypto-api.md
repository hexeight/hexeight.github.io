---
layout: post
title: "Cryptographic Identities for the World Wide Web"
date: 2017-12-31
excerpt: "Centrally controlled logical identities put control in hands of web services. Users need to maintain full control of their identities, especially those that affect their social and economic credibility. Cryptographic identities can help regain this control."
tags: [web 3.0, zero rating, free internet, blockchain]
comments: true
---

## Overview
Proof of Identity is a primary problem for any network protocol and the World Wide Web (HTTP) is no different. Introduction of the state management RFC in 1997<sup><a href="https://tools.ietf.org/html/rfc2109" target="_blank">[1]</a></sup> led to use common use of Cookie headers to maintain a state of identity in HTTP sessions. These identities have been dominantly powered by logical authentication mechanisms. The world wide web has progressed far ahead in its adoption of identities that are authenticated by trusted delegates. These identities still aren't universal over the world wide web. A central authority is required to act as a delegate and authenticate a user. While these identities inter-operate, there's isn't a single central authority that controls these identities. To remain aligned with the philosophy of the open web, there shouldn't be such a centralized entity. Here we discuss the possibility of extending cryptographic identities in the way they are being used in Distributed Ledger Technologies (popularly known as Blockchains), while keeping in mind the expected operational simplicity for an Internet user. Such identities would consistently keep the user in control and can be utilized by modern age applications to extend services with end-to-end encryption.

 Centrally controlled logical identities put control in hands of web services. Users need to maintain full control of their identities, especially those that affect their social and economic credibility. Cryptographic identities can help regain this control.

Delegated authentication protocols such as OAuth while being of tremendous utility, escalate the problem of identities being centrally controlled by a select few service providers.

## Cryptographic signatures for the Web
As opposed to conventional authentication that relies on username and password combinations, cryptographic authentication for the web can rely on messages signed by users with their secrets[2]. The signing mechanism needs to fullfil the following two requirements.

1. Allow users to sign challenges posed by webpages to prove their identity.
2. Allow users to sign HTTP transactions that may occur through forms or XHR requests as a proof of authenticity.

### Approach
1. Users will first have to generate their keys using standardized algorithms asymmetric cryptography.
2. Web pages can challenge the user to sign a message with their secret/private key.
3. Web services receive the signed challenge, and parse the signature for a public key, and verify the signature against the same public key.

Challenges can be used by web pages for registertion, login or even transactions. Public keys can be substituted as usernames for services that do not require user friendly naming conventions. Services like social platforms can map usernames with public keys for a friendly authentication experience.

### Browser based interface
The standard HTML input field can be used as a base to build the signature component.

```
<input type="signature" />
```
On user action, the field generates a signature based on the form inputs filled by the user.

### Verification by services


### Third-party authentication

## Security measures

## Conclusion

## References
1. [HTTP State Management Mechanism (rfc2109)](https://tools.ietf.org/html/rfc2109)