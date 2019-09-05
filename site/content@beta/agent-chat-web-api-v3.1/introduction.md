---
weight: 10
---

# Introduction

## Versioning

This documentation describes the version **v3.1** of the **Agent Chat Web API**.

## What is Web API
Web API is similar to REST API. Client can send a **request message** that results in getting a **response message**. It's also possible to get webhooks. 

## When to use Web API
If you're wondering which API to use - Agent Chat **RTM API** or **Web API**, keep on reading.

**Web API** allows for building stateless integrations. The communication is done via **XHR requests**. The implementation is easier than with RTM API, but you need to take possible time delays into consideration.

**Not what you're looking for?** Perhaps, you need to use [**Agent Chat RTM API**](../agent-chat-rtm-api-v3.1)<sup>[![LiveChat Link](link.svg)](../agent-chat-rtm-api-v3.1)</sup> instead.


## Authentication

**Agent authentication** is handled by access tokens. Find out how to get an **access token** from [Agent authorization flows](../beta-authorization/#agent-authorization-flows)<sup>[![LiveChat Link](link.svg)](../beta-authorization/#agent-authorization-flows)</sup>. All authorization scopes are listed in the [Scopes](#scopes) section. If a method requires certain scopes, you'll find them included in the method description. Keep in mind that Web API requires authorization every time you make a request.

## Data centers

LiveChat system operates in two data centers: `dal` and `fra`. The default data center is `dal`.

All the LiveChat OAuth2.0 access tokens have a prefix: `dal-` or `fra-`. This prefix indicates the data center they belong to. If you need to specify the data center while making an API call, simply add the `X-Region: <token_prefix>` optional header.

Summing up, if the user token starts with `fra-`, you should add the `X-Region: fra` header. If the token starts with `dal-` you don’t have to specify the header.

## Postman collection

You can find all the requests from the **Agent Chat Web API v3.0** in Postman.

<a href="https://app.getpostman.com/run-collection/c44c78bef060739c9c88" target="_blank"><img src="https://run.pstmn.io/button.svg"></a>
