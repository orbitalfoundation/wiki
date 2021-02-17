---
layout: post
title:  Persistent Web Agents
category: Philosophy
tags: [PWA]
---

# What do you mean by Persistent Web Agents?

Web developers often use a term "Persistent Web App" to talk about an idea of a rich client application being delivered to the client device and then running locally. Persistence in this phrasing is "stored locally". In this idea a user doesn't have to reload an app again once they fetched it. Often this is seen as a way to have some of the capabilities that App Stores provide, where you download apps, and have a rich high performance client experience, online and offline. An example of a web page that uses local storage heavily is [Figma](https://figma.com).

The web has been somewhat resistant to durable apps on the client - for a variety of reasons it has not taken off yet. There was a FirefoxOS effort which sought to build a web centric desktop, but it didn't succeed. There are also some formalisms around Persistent Web Apps such as in W3C standards but they haven't taken off either and in some cases are being deprecated. As a whole the web has been seen as "good enough" for most of us as is. And if you look around the net you can easily see quite a bit of conversation about the topic - for and against: https://levelup.gitconnected.com/progressive-web-applications-the-trend-of-2020-pros-and-cons-301bab02d673

These conversations however don't entirely reflect new points of view or new capabilities. When we talk about durable persistent execution on the client we mean so much more than merely "a nicer user experience". Here are a few implications, and why we think weaving these ideas into the fundamental fabric of this browser is important.

## 1. High Performance is no longer a barrier

First of all to reiterate, none of what is discussed below is possible without the work of many others. Even being able to have these ideas is indebited to the work of many existing technologies. We’re using Servo, Rust and Cargo to support durable persistent apps on the client, and as a result benefit from emerging standards such as WebGPU, WebXR, and process and filesystem sandboxing. Our interest here is supporting durable persistent first class apps within the browser; so we are creating a new persistence model for rich apps.

The fact is today that using Web Assembly, WebGPU, Rust and other emerging standards a PWA can reach the same performance as any native computation. It's no longer a case of a web app being slower or jerkier or less pleasant to use. This strengthens the case to actually have persistent web apps at the very least.

What is needed at this point to argue the case isn't performance, but rather sandboxing model of access to local computing resources that insulates applications from each other while allowing access to critical resources such as say bluetooth. Right now native apps (as opposed to web apps) have more powers. Standards bodies work hard to expose new capabilities to the browser. Sometimes the emphasis on privacy and security is so high that capabilities are not fully exposed, and some organizations tightly control their platforms and don't have strong incentives to favor unmanaged app distribution.

## 2. Distributed Computation

But a new possibility takes us in a different direction from merely "local apps". The value is in solving the unsolved. There is a fresh possibility of background agents, and agents run by other people using your computation. Today we all rely on centralized silos to effectively do work for us - to aggregate, organize, search and filter content. If these agents can be distributed over other browser instances - over the web as a whole - then the entire web (including all the browsers browsing it) become a computational fabric that can act on behalf of the user. You can fire off tasks that continue to represent your will, and have them circle back when you are online - or when you re-enter on different physical device.

Although we tend to think of agents as distinct from the data they manage - really these are both similar. Ultimately you have some personal cloud of digital artifacts - some of these may be photographs, some of these may be books that other people have written that you like. You may be running some personal software agents (such as a drawing tool or an aggregator) and you may also be hosting some other peoples data - and distributing some of your data for redundancy as well.

Reconnecting to your data may mean signing into your device, or it may mean using a new device with your private keys and talking to your still active agents.

## 3. Thinking of a browser instance as an app running node

We tend to think of a browser as "an app" - something that renders HTML, with 2D graphics, layout and text, and then a ton of barnacles (3D and so on). HTML is in fact just an "application" of the browser. An entire HTML rendering engine can just be a shared library or resource - effectively just a downloaded package like any other.

The browser in fact is better thought of a node in a computational pool. It runs your work preferentially, but that work can be anything. Local rich apps can deliver high performance granular interactions with your data - and lower performance for other peoples data and computation.

We want to avoid building an operating system, but we also want to avoid the assumption that a browser is just one thing or one app. Instead we want to appreciate it as something in-between; more as a common core for a variety of rendering engines, apps and technologies. We can start to think of these capabilities as "libraries" or tools. To do this well involves ideas around package and dependency management. In Rust we have Crates and Cargo. Many other packages and systems each have their own package and dependency management. These are ideas that we are very used to in general. An app running environment doesn't need to think of any one layout engine as "special" - it is just another thread that is running - based on some library - produced based on the users whim - and using certain resources such as the users interaction and screen.

## 4. Browsers working together

Ultimately we want to create a computational environment where millions of browsers can work together to help users solve their problems. These are services run by the users for the users - as a collective. Browsers can collaborate on developing a shared understanding of a website, pre-scanning it and digesting it and optimizing it for future page loads. Or even allowing social markup of websites - to correct errors in a website itself. There are all kinds of powers that you can have when you start to see the browsers together as a single computational fabric. To do that we need to enable browsers to durably run code received over the web in a safe trustworthy way. But the real power is when we start pointing our web browsers at the real world.

When you look towards the future where the web is part of a heads up display, where your browser is doing semantic partitioning and analysis of the world around you and where millions of other browsers are doing the same thing - then we see a significant inversion from today. It is the clients that are doing the sense making and sharing that knowledge with each other together.

In a persistent agent model the world becomes very different. A browser becomes a lens, like a smart car, that is aggregating, understanding, and acting on behalf of the user intelligently. It's less about bringing up a browser to look up something, and more like the browser is part of the background fabric of your life.

## 5. Resolving competing agent views

Of course the famous dystopian view of the future of the web is one where these agents don't cooperate, or where you don't control them. See [Hyper-Reality](https://www.youtube.com/watch?v=YJg02ivYzSs) by [Keiichi Matsuda](https://km.cx).

We do believe some of this vision is true - that interfaces will start to blend with the real world, that there will be virtual actions or verbs attached to everyday objects, and that the browser as your user-agent will in some ways invert the current display architectures that we are used to.

But this means competition for that one scarce resource - your attention. In a heads up world, with pass through vision rigs, where the browser is "in the world" rather than a distraction "from the world" we will likely see software agents need to work together to define what gets priority. Instead of each app rendering to a separate page your user agent will arbitrate and filter many apps attempting to render to the same view. We believe this will create new challenges for accessibility and for filtering and sense-making and that this needs to be explored.

It's worth noting that most 3d interactive content is in fact described in grammars that are not terribly different from HTML. They are often using some kind of directed acyclic graph - with nodes that describe the rendering behaviors - not unlike like a christmas tree decorated with ornaments. However, nobody has been able to successfully propose a single 3D grammar - the space of 3D is too rich and too full of possibilities for every 3d app to be represented using the same scheme. The grammar for Minecraft is utterly different than the grammar for Breath Of The Wild or say Daz3D. But - if we are going to have some kind of common lingua franca where apps are all contributing to one view of the world - we will need to find some trade language that all apps can agree to - at least when speaking to that shared view.
