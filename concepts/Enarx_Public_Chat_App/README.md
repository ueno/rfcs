# Title (Ex. 00000: RFC Topic)
- Authors: [your name](you@github-email) -- email is optional
- Status: [PROPOSED](/README.md#proposed)
- Since: 20YY-MM-DD (date you submit your PR)
- Status Note: (explanation of current status)  
- Supersedes: (link to anything this RFC supersedes)
- Start Date: 20YY-MM-DD (date you started working on this idea)
- Tags: feature, protocol

## Summary

We are currently using Gitter for Enarx's public chat. We are beginning to notice its shortcomings, and believe it will not meet our needs as we scale. This RFC proposes that we switch our public chat app to Zulip, a more feature-rich and better-organized alternative.

## Motivation

We have noticed some intermittent reliability issues with Gitter recently. Combined with a number of other feature shortcomings, we're growing a little frustrated with it, and we're exploring alternatives. Zulip seems to be the best.

## Tutorial

_As if Zulip is set up as our default chat app:_

Enarx's public chat lives on Zulip. If you'd like to get involved in the conversation, you can join us at `<public-chat-link>`. You'll need to create an account -- you have options for Github and Google login, or you can use email. 

Once you've created an account, come on in and have a look around!

Zulip organizes categories of messages into [**streams**](https://zulipchat.com/help/about-streams-and-topics). This is roughly analogous to "channels" or "rooms" in other chat apps. By default, you're subscribed to the `#general` stream, which contains general project discussion.

We've split different areas of discussion into other streams, which you are free to [join](https://zulipchat.com/help/browse-and-subscribe-to-streams). For example, if you have a question or point of discussion related to Enarx development, you can move to the `#dev` stream. Once there, you'll see messages organized into [**topics**](https://zulipchat.com/help/about-streams-and-topics). You can browse previously-discussed topics and reply to them by clicking on a message in that topic. Alternatively, you can [start a new one](https://zulipchat.com/help/start-a-new-topic) if you haven't seen your topic discussed yet. You can name it whatever you like (just be sure it's descriptive).

If you're talking about code, feel free to use Markdown to format your code as part of your messages! Zulip's Markdown also supports syntax highlighting for specific languages.

If you need to show us an image, you can upload one as part of your message. There's a handy button next to the compose box.

Finally, if you just absolutely _need_ more Enarx discussion in your life, you can use the Zulip mobile apps for iOS and Android to chat on the go.

## Reference

Here is a handy chart with direct feature comparisons to our current solution, Gitter.

| **Comparison**                              | **Gitter**                                                                                                                                                    | **Zulip**                                                                                                                                                                             |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fundamentals**                            |                                                                                                                                                               |                                                                                                                                                                                       |
| FOSS                                        | Yes (MIT)                                                                                                                                                     | Yes (Apache 2.0)                                                                                                                                                                      |
| Reliability                                 | We've encountered some issues                                                                                                                                 | TBD                                                                                                                                                                                   |
| E2E Encryption                              | No                                                                                                                                                            | No                                                                                                                                                                                    |
| Publicly-visible chat                       | Yes                                                                                                                                                           | Not by default; `zulip-archive` is a workaround (see below for details)                                                                                                               |
| Maintained?                                 | Yes, though they admit they don't have enough resources to develop key features (ex. mobile app)                                                              | Yes                                                                                                                                                                                   |
| **App support**                             |                                                                                                                                                               |                                                                                                                                                                                       |
| Web app                                     | Yes                                                                                                                                                           | Yes                                                                                                                                                                                   |
| Mobile apps                                 | Yes (iOS and Android), though they are not maintained, tend to break, and may be officially deprecated in the future. Android does not support notifications. | Yes (iOS and Android)                                                                                                                                                                 |
| Native Linux                                | Yes                                                                                                                                                           | Yes                                                                                                                                                                                   |
| Native Mac                                  | Yes                                                                                                                                                           | Yes                                                                                                                                                                                   |
| Native Windows                              | Yes                                                                                                                                                           | Yes                                                                                                                                                                                   |
| **Organization**                            |                                                                                                                                                               |                                                                                                                                                                                       |
| Multiple rooms                              | Yes                                                                                                                                                           | [Yes](https://zulipchat.com/help/about-streams-and-topics) (they're called "streams")                                                                                                 |
| Custom topics                               | No (chat is just a chronological stream of consciousness)                                                                                                     | [Yes](https://zulipchat.com/help/about-streams-and-topics) (and they support custom names)                                                                                            |
| Threading                                   | Technically yes, but it's poorly implemented/missing features and we do not use it                                                                            | Yes, with custom topics                                                                                                                                                               |
| Global chat search                          | No                                                                                                                                                            | [Yes](https://zulipchat.com/help/search-for-messages)                                                                                                                                 |
| Message pinning                             | No                                                                                                                                                            | Locally, but not globally                                                                                                                                                             |
| **Features**                                |                                                                                                                                                               |                                                                                                                                                                                       |
| Github integration                          | No (there is an option for it, but it uses the deprecated Github Services and does not work)                                                                  | Yes                                                                                                                                                                                   |
| Sign-up ease                                | Easy (Github login)                                                                                                                                           | Easy (Github, Google, email login) -- worth noting email confirmations usually take a long time to arrive                                                                             |
| Direct linking to specific messages in chat | No                                                                                                                                                            | Yes                                                                                                                                                                                   |
| File uploads/image sharing                  | No                                                                                                                                                            | Yes                                                                                                                                                                                   |
| Bridging to other networks                  | Barebones                                                                                                                                                     | Officially for [Matrix](https://zulip.com/integrations/doc/matrix) and [IRC](https://zulip.com/integrations/doc/irc), but functionally broken (only syncs a stream and not a channel) |
| Markdown support                            | Yes                                                                                                                                                           | Yes                                                                                                                                                                                   |
| Syntax highlighting                         | Yes                                                                                                                                                           | Yes                                                                                                                                                                                   |
| **UX/UI/Other considerations**              |                                                                                                                                                               |                                                                                                                                                                                       |
| UI complexity                               | Fairly straightforward                                                                                                                                        | Slightly higher learning curve                                                                                                                                                        |
| Dark mode                                   | Yes                                                                                                                                                           | Yes                                                                                                                                                                                   |
| Emoji reactions to messages                 | No                                                                                                                                                            | Yes                                                                                                                                                                                   |
| Custom emoji                                | No                                                                                                                                                            | Yes                                                                                                                                                                                   |

## Drawbacks

There are two major drawbacks to Zulip we should strongly consider before a move.

**Community**

The community we’ve begun building up on Gitter is easily the biggest reason we have to stay. If we move chat clients, we’d be asking them to juggle around yet another chat app, and their existing lines of communication would end up unsupported by us. This is not ideal, and a big con to moving.

The counter-argument to this is that if a change is going to happen, it’s better that it happens sooner rather than later. If we truly feel that Gitter won’t meet our needs (especially as we scale), a change now will be far less painful than when we’re a lot larger.

**Public chat visibility**

The biggest thing Gitter does significantly _better_ than Zulip is the ability to read messages when logged out. If someone new to the project is idly curious what's going on in chat, they can just look at our chat log in Gitter -- no login required.

Zulip, on the other hand, requires a login, which presents a barrier to people being able to see the discussions going on about Enarx. An idle observer would need to create an account, which they might not want to do.

There is a potential workaround present, however, with [`zulip-archive`](https://github.com/zulip/zulip-archive). This is a tool, runnable as a Github Action, that archives our chat logs and publishes them on a publicly-accessible Github Pages site. For Enarx, this may manifest itself as a sub-link of `enarx.github.io` -- for example, we may be able to point people to `enarx.github.io/zulip-archive` for a publicly-accessible chat record.

In terms of implementation, it seems fairly straightforward, and there are examples of this being done on an organizational level (see [here](https://leanprover-community.github.io/archive/)). An Enarx deployment of this tool would look fairly similar. We would need to create a new repository within the Enarx organization to hold the chat record, though it shouldn't need to be maintained after `zulip-archive` is set up.

## Rationale and alternatives

We think Zulip is the superior choice due to a number of feature advantages it has over Gitter and other solutions.
- Organization
    - Zulip has topic-based organization, allowing better separation of thoughts and tasks than Gitter, which only allows for a chronological feed.
    - Like Gitter, it supports multiple rooms (known as “streams”). It also promotes stream discoverability better than Gitter.
    - Zulip supports chat search, where Gitter offers nothing of the sort.
- App support (especially mobile)
    - Gitter’s mobile app is, to put it kindly, not very good. It doesn’t support notifications at all, it is slow, and it doesn’t register read messages well. Additionally, Gitter themselves do not officially recommend their own apps, and [say](https://gitter.im/apps) they may be deprecated in the future. Zulip’s mobile apps work well, do support notifications, and generally support a larger subset of features.
    - Both have desktop Linux apps available, though both are also available in browser.
    - Both have Windows and Mac desktop clients.
- Nice-to-have features
    - Zulip supports file uploads, where Gitter does not. This can be helpful if we need to share a screenshot, for example.
    - Zulip allows users to link to a unique message in the chat.
    - Zulip appears to have much more robust integration support, including Github integration. Gitter’s Github integration is out of date and does not work.

In terms of alternatives: Following Enarx's design principles of open development, we strongly value FOSS solutions, of which there are, unfortunately, few. Beyond Zulip, there's:

- Gitter, which we've already discussed
- Matrix, which has some nice security/privacy features, but otherwise looks high-maintenance and not necessarily as feature-complete as Zulip.
- IRC, which is a non-starter.

## Prior art

We have used Gitter for a while, and have had annoyances with it for a while, as previously discussed. Beyond that, Enarx has not used any other public chat apps.

## Unresolved questions

We still have no reference point for how reliable Zulip is. This, unfortunately, is something we can only learn with experience.

## Future Possibilities

One particularly exciting possibility is Zulip's robust integration potential. Zulip has a powerful [bot](https://zulipchat.com/api/running-bots) framework, which ould potentially open up interesting automation opportunities with Github and elsewhere.
