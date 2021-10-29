# OpenBank

OpenBank is a bank statement description aggregation service and API

## Why?

"Bank statements are notoriously difficult to read." - Anon

Banks used to have mainframes. So now the whole financial industry is trapped in short and non-sensical descriptions when it comes to the description bank statements.

OpenBank strives to provide a central source using an open platform where anybody can submit descriptions about their bank statements which can in turn help other people to quickly and easily decypher their data.

## Schema description

The schema consists of `Patterns`, `Tags`, and `Entities`.

- `Patterns` are the actual descriptions on your bank statement.
- `Tags` is a way of grouping related transactions. It's similar to categories but more powerful because it's a many to many relationship instead a one to many relationship
- `Entities` are both people who you pay, and people who pay you. It's a broad term for the beneficiery in the case of you having paid someone, but could also be a party that gave you money. `Entities` can be businesses, people, your creditors, and your customers.

### Example

This example strive to explain the terms:

On your statement you see this:

```
25 Oct WINCH MOTORS 5123*6543 21 OCT - 83.40
Cheque card purchase
```

The `Pattern` that is matched in this case is `WINCH MOTORS`
The `Entity`, also known as friendly name, is `My Local Garage`

Since we can both put petrol in at our local garage and buy sweets attaching an tag is complicated. The goal of OpenBank is to attach `Tags` only when the option is clear.

Other notes about this transaction:

- ` 5123*6543` information is disregarded as it's private.
- The date of the transaction is 25 Oct but the actual purchase took place on the 21st of October. The reason for the discrepency is because card transactions take a number of days to clear.
- The amount was `- 83.30`

## Roadmap

- Remove vanilla biolerplate on Welcome and Jetstream boiler on Dashboard
- Get brand logo in Jetstream
- When you're logged into the application, /contact /about etc must change to Logout
- Display Social Login type on profile
- Fix Nova permissions so that it's visible for everyone
- Implement policies so that nobody can delete user
- Change Nova URL from /nova to /admin
- Add contact to dashboard and unify design
- Flesh out more of the About page to describe the basic API
- Make mailto and telto links on about
- Random encrypt password for Socialite
- Link openbank-api.com to site and remove fintech references
- When you submit a contact form, the green is the wrong colour

## Milestones

- First iteration of the alpha website

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Everyone is welcome. Just register for a free account and start contributing.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.