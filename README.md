# anyone.live

The World Wide Web's chat

## The Concept

anyone.live aims to be a platform that hosts conversations relating to web addresses.

Chat rooms are identified by domain names.

No website gets scraped. No brand gets partnered. There's only a simple check to make sure the address provided is a real place.

Users can freely converse about anything they like. The web address they have provided is simply the "reference of the conversation".

## Usage

```
anyonelive [ADDRESS] [OPTIONS]

OPTIONS

Just a rant, why am I the only one that bothers organizing options alphabetically ?

-h --host          Specify the host server. Defaults to https://anyone.live
-l --lurk-mode     Read-only mode. Account login skipped. Users logged in can see lurkers and get notified when they are connected.
-s --server-mode   Start as a dedicated server. There is no hybrid server / client mode. Open a second instance for chat.
-t --tribe-size    Specify how many users should ideally be in one room (the tribe count). The system will give warnings and display chat differently based on that number.
```

## Experience

This is work in progress, so I'm writing down what I hope the UX would be like, and obviously I'm going to be busy working my way towards that.

- Download the app, run it. It's probably a simple console app at first, it may have a GUI eventually.
- Sign in with an OAuth account. The main reason for this is to limit the propensity for impersonation and name switching.
- Point to an address on the web. It can be simply a domain or a specific page.
- The app will auto-manage if there are TOO MANY or NOT ENOUGH* people at the given address
- The chat starts streaming
- The app will display of the chat tree with parent and children addresses, with their current user counts.

*TOO MANY or NOT ENOUGH, means that each address is going to keep track of the activity in their parent addresses, such as domain.com/somecategory/something will show you the chat for that specific page, but will let the chat from domain.com and domain.com/somecategory filter through in some capacity
