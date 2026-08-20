# Pull request description (paste this into the PR body)

**Name:** <your full name, as you want it publicly credited>

Renewal Desk — a renewal quote and price-change notice batch built on the
SuperDocs API. For a list of fabricated renewing accounts it produces a renewal
quote and an account-specific price-change notice per account, with a human
approval gate that holds anything above a defined increase before the batch can
be called complete.

Folder: `use-cases/noormdafsar/renewal-desk/`

A live run over 10 accounts spent 13 operations: 3 auto-approved and exported,
4 held for review (3 approved, 1 rejected outright), 3 deliberately skipped with
named reasons. The gate caught a fabricated claim and an internal-flag leak
before either reached a customer — both documented in the project README.
