---
layout: post
title:  Self Sovereign Identity
category: Philosophy
tags: [ssi]
---

# Why is Self Sovereign Identity useful?

There's a certain optimism when we speculate about the future of the Web. There's been a lot of fresh thinking about how to fix a lot of the kinds of things that feel broken right now.

At the same time the broken things feel large. For example some people are pretty worried about centralization, how large content aggregators become chokepoints for what media many of us are permitted to consume. We worry about making sure that marginalized voices can get online and be heard. We worry about healthy sincere conversations, and some of the tensions around freedom of speech versus bad actors and outright trolling or intent to cause injury. We see media being used to mislead us, with industrial strength fake media production being used to steer the behavior of large groups of people. It can be very hard to distinguish what is real from what is fake.

We're also drowning in advertising - which I would argue is directly related to this (I will explore more further on). For creatives the web can be a very difficult place to be seen or heard - to actually be able to do creative work in a sustainable way. Creatives have to become very creative about making money - even more so than would seem necessary. There does seem to be an uphill battle against larger publishing hubs, and difficulty in building direct sincere relationships with fans. At the same time there are options. Patreons and Kickstarters are a way to build durable support if you are a creative and also as a form of content discovery even for consumers. And we do see some emerging micropayments technology such as Coil.

I'd argue these topics are aspects of a single topic: identity. Obviously the larger scope of these concerns is beyond what can be done here, and there are many different opinions, but I try to sketch out at least some of the basics:

## 1. Identity itself

Identity is a perennial concern of both individuals and the services they are trying to use. A website is effectively an application, or a user agent or user proxy. It gives a user privileges to perform certain actions, to have access to certain data. Your bank does its best to make sure that you are you, and then it lets you move money around.

What we've seen on the web is a consolidation of account management. Now we see Google and other services provide authentication services - where users authenticate against the one service to access many other services. But this creates some risk for the user. They are first of all beholden to that services terms (which may change), and as well the services don't always interoperate with each other. It seems like this is a result of the original framing of the web.  The web arguably
emerged in an academic setting where identity was a more of a given, and where money was less important. Everybody was trusted. There was less emphasis on transactional relationships. A university setting is a utopia in some senses. Once you're in it becomes a space where ostensibly one is supposed to focus on deeper matters rather than simply money itself. There's a trust because there is a gate around the entire system.

But today there's no reason why people cannot self-certify their identity and own their own data. It's equally easy to let users self-sign whatever documents they are publishing to the server. And if users self-sign then they can manufacture whatever persona they wish, on whatever services they wish, and they can do so even if they are offline. The power of public key cryptography is that you are capable of authenticating yourself, or whatever persona you have manufactured. We already see this with public ledger technology such as Metamask. Using Metamask to publish to a public ledger there's no question of a sign in - or an accountability to others. While at the same time if you are worried about losing your private keys you can always use a third party service to manage your mnemonics.

Note in my mind a persona that earns credibility over time is totally separate from "you". We can burn our identity if we behave badly, but there should be an opportunity to try again, to learn. Of course starting over can take years to re-earn trust.

Self Sovereign Identity has to be the foundation of the future of the web. Furthermore it needs to be built into the browser. This feels like a useful starting point for many other future oriented web conversations. Any powers that we have to control, deny, permit a person to have an identity, even say from say a governance perspective, has to take place at a different level than where we are asserting that control today.

## 2. Social Trust Graphs

One of the bigger problems that people all over the web are complaining about today is "fake news". It's a good example of a problem that is easier to solve once you have some form of public key signing.

There is so much news that is either maliciously misframed or outright manufactured that it can overwhelm people who are not used to this. But it isn't hard to build cryptographically secure signing systems that help assert that a post or article or photograph was indeed certified by a specific party. Techniques used by PGP, KeyBase and even DNS or Bitcoin itself can quickly separate fake from real.

We all rely on DNS hundreds of times every day. For example we use DNS to be certain that when we're going to Google that we're actually going to google. It's extremely trustworthy. By a similar measure we should be able to trust that if a person makes a claim or statement that that person and their claim is actually from that party - regardless of what service or website the claim is uttered on. There's really no reason why we should have to trust the service itself in fact if the claim is simply signed by that party and logged as such anywhere on the net, and we are connected to that party by a social network.

Where the value of self sovereign identity emerges is in fact more around social trust. If I know that a person is "real", and you know me, then transitively you can have some second order trust that that third party is real to you as well. We can add up the weight of thousands of second, third, fourth and fifth order connections to create a social trust score. This score is different for every participant. It is different from every perspective. It doesn't assert that a person is "good" or "bad" but simply that they are real. And in fact it doesn't even necessarily assert that they are a person - it simply asserts that a persona that made one utterance earlier is arguably the same persona that is making a current utterance now.

In a world where we have self sovereign identity we can start to build social trust graphs. It becomes more expensive for a cluster of bad actors to talk themselves up in such a world. One can also imagine all kinds of other scoring, and one can imagine how more famous people, or well known organizations, can become hubs in such trust graphs. But fundamentally the starting point is simply letting people self sign their own public persona at will.

Note however this does necessarily mean that we will no longer be able to completely "silence" or "deplatform" bad actors. Some who are more libertarian may argue this is a good thing - I do not agree - but I accept that one consequence of creating a fabric fundamentally based on SSI is that people cannot be silenced. And there are other mechanisms to downscore or attentuate people who are acting out of malice and who are not engaged in sincere conservations. We can start to look for how often bad actors make utterances that are untrue for example - or score how often they attempt to divide, injure or hurt people around them.

## 3. Public Ledgers

Once you have posts or subjects or utterances that only you can manufacture then a whole realm of other capabilities become possible. Of course we've seen cryptocurrencies take off, and we've also seen NFT take off. But I want to dwell more on some of the fundamentals here a bit.

Public ledgers are important because they create a public space of assertions in a way that has previously required a central authority. The risk of central authorities is that they can fall over, become corrupted, or attract predators themselves. Any system for managing limited edition digital artifacts relies on some kind of authority that can prevent duplication.

In these early days we tend to be thinking that "all transactions should be on the blockchain". But long term it's too expensive, and too environmentally damaging to do that. Even though all ledger systems have costs, publicv ledgers are currently extraordinarily expensive in terms of co2 creation. What communities will want is to do most transactions as lightly as possible, using a "good enough" private ledger. And only move to a public record when it is really critical or really important. Most of our human affairs can be managed privately. The fact is that even the "threat" of being able to write facts to a public ledger by itself makes private ledgers more trustworthy. Everybody knows that if a private ledger starts to fail to honor transactions that it can be replaced with something more robust. We start to see a private ledger as a convenience for speed, rather than the only solution, and it keeps all parties from exploiting control over ledger itself as a lever.

Once participants can begin to make public durable utterances, stemming from their own public/private key - we start to enter a universe where the costs traditionally associated with any kind of creativity become lower. A person can issue tokens in exchange for their labor, a community can track exchanges of labor between peers. Real assets and artifacts can be mirrored digitally, and brokerages and auctions can be formed. Standardization of the ways that these assets are expressed makes it easier for third party services to list those assets - in a sense creating a kind of fungibility (even if the assets themselves are unique).

## 4. Transactions

Right now the concept of a digital artifact - such as video game, an e-book, or a ticket for a concert, or an hour of a persons time - is managed in a series of separate silos. And the silos themselves become chokepoints. There is power in aggregating data, becoming a broker for services. That power can be magnified unduly when the data itself cannot leave because it loses its meaning once removed.

We've tried to have it both ways. To mark digital artifacts as valuable, requiring money, but also ephemeral, as sold only once. Consumers tend to be seen as consumers, rather than as co-creators in a value chain, where they themselves can derive value by helping promote work. Content creators are seen as "the goose that laid the golden egg" - they are harvested for their art, the art separate from them and sold, while they get a small residual. It isn't that centralization is bad, but that there are such high costs with directly forming transactional relationships with potential customers that it has not historically been done. Even services like Patreon can be thought of as aggregation hubs, driving some revenue towards themselves, and often requiring effectively a subscription model.

What's really missing from the fabric of the net here is simple direct low overhead transactional relationships. Exactly like you might have in the real world. In the real world you can go to the corner store, buy an apple and leave. There is no subscription. On the web today this is called micropayments and it largely has not worked out for a variety of reasons. I argue it is still worth trying again and that direct payments should be part of the fabric and part of the possibilities that a creator considers.

If creators and consumers can form direct relationships with each other then this can shift other behaviors on the web. Today advertising dominates because it is a stable easy way to monetize attention. Advertising has some unpleasant or undesirable side effects however. There is an arms race between advertisers and browser creators - one that is unwinnable by either party - but one that has made the experience of browsing the web poor for ordinary users. If creators and consumers can foster direct relationships (by any mechanism) then the incentives behind advertising may be diminished.

## 5. Decentralized Web

Of course people are not necessarily going to be hosting their own data on their own devices. There are still good arguments for cloud hosting. With private keys however users can store remote while still retaining control, and can choose to expose portions of their data to others if they wish. Millions of browsers working together can become a capability for the people as a whole to have a shared storage capability that is entirely decentralized and redundant. People who need high performance data access can use centralized services as well. We've seen these conversations emerging in projects such as https://solidproject.org/about and they have been top of mind at many organizations https://hacks.mozilla.org/2018/07/introducing-the-d-web/ . It isn't that this is new, but rather that without a solid foundation of identity it becomes unduly hard.

## 6. Ecosystem Perspective

In essence the web isn't just consumers who use thin clients to go visit service providers who run walled gardens that host data and code. Instead the web can be a sea of user agents, a sea of data, and a sea of other parties - all co-existing.

The web is best thought of as a complex ecosystem with many participants at all scales. We will always see internet influencers, taste makers, advertisers, large publishers, subscription services, silo account services, walled gardens. But in a healthy ecosystem these are just part of a world where users themselves are first class entities; able to approach service providers with direct transactions, able to withdraw their support, and take their data with them if they wish. In such an ecosystem we diminish some of the pathological behaviors and some of the perverse incentives.
