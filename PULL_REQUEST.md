# Pull request description (paste this into the PR body)

**Name:** Nooruddin Md Afsar

Renewal Desk — a renewal quote and price-change notice batch built on the
SuperDocs API. For a list of fabricated renewing accounts it produces a renewal
quote and an account-specific price-change notice per account, with a human
approval gate that holds anything above a defined increase before the batch can
be called complete.

Folder: `use-cases/noormdafsar/renewal-desk/`

A live run over 10 accounts spent 14 operations: 3 auto-approved and exported,
4 held for review (3 approved, 1 rejected outright), 3 deliberately skipped with
named reasons. The gate caught a fabricated claim and an internal-flag leak
before either reached a customer — both documented in the project README.

---

**Plumbline** — an extension, built unprompted alongside the above. It reads a
codebase with Python's `ast` module, asks SuperDocs to extract the factual claims
a document makes about that code, and reports where the document has drifted from
what the code actually does. It ships as an MCP server so a coding agent can ask
"which docs did my change just make false?" without leaving the editor.

Folder: `extensions/noormdafsar/plumbline/`

Both projects share one decision: deterministic code computes every number and
every fact, and the model only writes prose. Tests for both run with no API key
and no network.
