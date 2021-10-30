# OpenBank

OpenBank is a bank statement description aggregation service and API

## Why?

_"Bank statements are notoriously difficult to read."_ - Anon

Banks used to have mainframes. So now the whole financial industry is trapped in short and non-sensical descriptions when it comes to line item descriptions on bank statements.

The banking system tries to alleviate this problem by providing categories for transactions - however - these categories aren't very accurate at all because there are too many permutations and different ways of spending your money and what exactly is possible.

The OpenBank API strives to provide a central source using an open platform where anybody can submit descriptions about their bank statements which can in turn help other people to quickly and easily decypher their data.

## Solution

The API schema consists of `Patterns`, `Tags`, and `Entities`.

- `Patterns` are the actual descriptions on your bank statement.
- `Tags` is a way of grouping related transactions. It's similar to categories but more powerful because it's a many to many relationship instead a one to many relationship
- `Entities` are both people who you pay, and people who pay you. It's a broad term for the beneficiery in the case of you having paid someone, but could also be a party that gave you money. `Entities` can be persons, businesses, your creditors, customers, etc.

### Example

This example strives to explain the terms:

On a bank account statement you might see this:

```
25 Oct WINCH MOTORS 5123*6543 21 OCT - 83.40
Cheque card purchase
```

The `Pattern` that is matched in this case is `WINCH MOTORS`

The `Entity`, written in a more friendly name, is `My Local Fuel Station`

Since we can both re-fuel at our local fuel station and buy sweets at their shop, attaching an tag is complicated. The goal of OpenBank is to automatically assign a`Tags` only when the option is clear but still allow the end-user to tag the transaction with another category.

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

Based on https://keepachangelog.com/en/1.0.0/

## Contributing

Everyone is welcome. Just register for a free account and start contributing.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.