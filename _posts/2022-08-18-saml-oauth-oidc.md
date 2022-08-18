---
layout: post
title: "SAML, OAuth and OpenID Connect"
date: 2022-08-18
category: identity
---
> Because I'm lazy, SAML and OAuth refers here to SAML 2.0 and OAuth 2.0.

## SAML
SAML 2.0 is a standard for authentication and authorization from 2005 that made famous federated identity.

It was **designed with server-based web application in mind** and is poorly suited for single-page applications, mobile applications or to protect APIs.

However, it is still widely used and is supported by a lot of applications and technologies.

## OAuth
OAuth is an **authorization** framework. It provides different authorization flows to accomodate all kind of applications.

As OAuth is a *framework*, a lot of details are left to the implementation (e.g. access tokens do not have to be in any particular format).

### Authorization flows
In order to gain authorization, client needs to perform an authorization grant to request the access token (and optionaly, the refresh token).

OAuth defines four grant types:
1. Authorization Code
2. Implicit
3. Resource Owner Password Credentials
4. Client Credentials

It also provides an extension mechanism for defining additional grant types.

Each of these flows has its advantages/disadvantages and the best flow will depend on the application type and the use case.

## OpenID Connect
OpenID Connect (OIDC) is an **authentication** standard that is built on top of OAuth.

The main difference is that an OIDC flows will give an ID token in addition to the access token. This ID token contains claims about the user.

### Demo with Okta
You can set up a demo application using OIDC with the OAuth **authorization code flow**, using Okta as the identity provider.

1. Create an Okta developer account
2. Select [here](https://developer.okta.com/docs/guides/implement-grant-type/authcode/main/#examples) the framework you want to use for the demo application, clone the repo and follow instruction to deploy.
3. Create an application in Okta using default values
4. Log-in to the demo app at `http://localhost:8080/`


## Useful links
- [Understanding SAML](https://developer.okta.com/docs/concepts/saml) - Okta Developer Blog
- [SAML for Web Developers](https://github.com/jch/saml) - Technical post on SSO with SAML
- [OAuth 2.0 and OpenID Connect Overview](https://developer.okta.com/docs/concepts/oauth-openid) - Okta Developer Blog
- [What the Heck is OAuth?](https://developer.okta.com/blog/2017/06/21/what-the-heck-is-oauth) - (deeper dive) Okta Developer Blog
- [OAuth 2 Simplified](https://aaronparecki.com/oauth-2-simplified) - Implementation-oriented guide

