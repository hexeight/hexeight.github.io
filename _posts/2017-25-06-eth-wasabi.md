---
layout: post
title:  "Wasabi - For starters"
date:   2016-04-06
excerpt: "A minimal command line tool to help me start building Dapps on Ethereum."
project: true
tag:
- 
comments: true
---

*This post is being updated along with the project progress. Last Update (25th June 2017)*

# Wasabi

| Project URL | [https://github.com/hexeight/wasabi](https://github.com/hexeight/wasabi) |
|-------------|--------------------------------------------------------------------------|
| Description | A minimal command-line tool to help start building Dapps for Ethereum    |
| Status      | In progress                                                              |

I've had my share of trouble getting started with building Distributed apps (Dapps) on Ethereum. There are a bunch of frameworks out there like [this](https://truffleframework.com) and [this]( https://github.com/iurimatias/embark-framework) that help get started immediately. But these frameworks did way too much by themselves. I wanted to understand every step involved in deploying contracts, generating their ABIs, and using them in Dapps through JSON RPC.

## Wait, is this another framework?

I wouldn't call it a framework. Wasabi does the following few things.

- Sets up a minimal project structure with directories for contracts, app and config.
- Compiles contracts and provides an estimate of gas consumption provided by the configured RPC node.
- Deploys contracts using transaction signature at node OR on client.
- Creates a JSON file with Contract addresses and ABIs.
- Wasabi also adds a pre-packaged JS file that can read the contracts.json and create Contract objects in javascript global scope for the Dapp to consume.

The pre-packaged Javascript is less than 40 lines of uncompressed code, ensuring that web developers can maintain complete control over their web app. I shamelessly confess that I took the liberty to cherry pick features from the couple frameworks I tried to use.

## What does it not do?

- It does not have testing inbuilt. As far as possible, everything in the `/app` directory is to be owned by the web developer. This provides freedom to use traditional web frameworks of their choice.
- Add heavy Javascript that abstracts interface between your Dapp and Web3. You do your own house-keeping.
- Does not maintain contract compile/migration history.

## Can I start using wasabi for project that I plan to take in to production?

NO. Not yet. I am building wasabi to suit my own selfish needs, and introduce myself to the intricate art of publishing contracts and integrating them in web apps. While I do plan to make this ready for production, but I provide no garauntees and the tool work as expected.

## Can I use it for projects which I don't mind buring down to ashes?

Sure. If you are learning or experimenting with Ethereum, please feel free to use wasabi and hit me with any feedback with how well or how badly it worked for you. I'll be glad to accept feedback in terms of issues, feature request and better yet, pull requests.