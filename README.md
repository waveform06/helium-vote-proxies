# What is a Voting Proxy?

A voting proxy is a wallet that can vote on behalf of other wallets. A voting wallet can choose to assign their votes to a given proxy.

An example of this would be assigning your voting power to your friend who knows more about Helium. 

## What is Recursive Assignment?

A proxy voter can assign all of their votes to another proxy. So, for example, you could assign your votes to a friend who assigns those votes to a neighbor. Vote assignments form a chain of trust, and in the ideal case concentrate voting power around knowledgeable and trusted individuals.

## Can I override Proxy Votes?

Yes! If you do not like the vote your proxy makes, you can always override it. You can also revoke the assignment at any time!

## Seasons

Proxy voting is split up in yearly seasons, similar to government election cycles. All proxies are reset on August 1st. This ensures that proxies must work to keep their voting power, and voters must reevaluate their assignments yearly.

# Adding a Proxy

To add a proxy, fork this repository and make a pull request containing the following:

- An entry in [proxies.json](/proxies.json)
- Any necessary files and assets in a folder under the [proxies](/proxies) folder

First, add the proxy to the [proxies.json](/proxies.json) file. Each proxy should have the following properties:

| Property    | Description                                                                                                                                                                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name        | The name of the proxy. This could be the name of a person, or a voting entity.                                                                                                                                                                |
| image       | A profile picture for the proxy. This will be displayed in the proxy discovery UI and in search. This should be a file path to the jpeg or png.                                                                                               |
| description | A short description of the proxy. This will be displayed in the proxy discovery UI                                                                                                                                                            |
| detail      | A filepath to a markdown file containing a more detailed biography of the proxy. This should describe voting philosophies, and any other relevant information to those choosing to delegate. This will be displayed in the proxy discovery UI |
| networks    | An array of networks you participate in votes for                                                                                                                                                                                             |

## Example

You can see examples of other proxies listed in [proxies.json](/proxies.json). The format is as follows:

```
{
  "wallet": "ex1iPHN3wCAUSwPrNENvxMW1w6ggZRQwYUmQwmAn646",
  "name": "Example Proxy",
  "image": "./proxies/example/image.png",
  "description": "Example proxy voter",
  "detail": "./proxies/example/detail.md"
}
```

You can further check the [example](./proxies/example) subdirectory to see examples of the image and detail.
