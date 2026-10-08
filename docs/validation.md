# Validation and next evidence

[Case study](../README.md) · [Decisions and iteration](decisions-and-development.md) · [Screenshots](media.md)

**Audit date: 7 October 2026.** These are retained results from that checkpoint, not new checks run when this showcase was published. The runs were assistant-executed under Isaac's instructions. This repository summarises them without publishing application code, raw logs or private records.

The inspected application version was `0.1.10-beta-research`, with model `0.1.6-pilot`, evidence `0.1.6` and report schema `1.1`. These versions describe different parts of the same checkpoint.

## Recorded results

| Check | Result on 7 October | What it establishes |
|---|---|---|
| Node application suite | **72 passed; 0 failed; 0 skipped** | Specified behaviours passed the retained automated tests |
| TypeScript check | **Passed** | The inspected source passed static type checking |
| Evidence validation | **Passed** | Retained evidence links, season rules and audit hashes passed the validator |
| Register and release integrity | **Passed** | Retained exports and hashes matched the expected artifacts |
| Production build | **Completed** | The audited checkout produced its build artifacts |
| Built artifact exposure check | **Passed** | The scoped check did not find the checked raw research material in public output |
| Historical zero-score reproduction | **Earlier source failed as expected; correction and baseline passed** | The controlled fixture detects the historical defect and confirms the specified correction |
| Development Python suite | **Blocked** | Required testing dependencies were unavailable; no fresh passing result is claimed |
| Signed-out live browser check | **Homepage, privacy, terms and account gate observed** | Public surfaces and the ordinary access gate were presented |

Earlier targeted Node runs are subsets of the 72-test suite and are not added again. Historical release-note claims are not substituted for fresh results. Build completion is not a latency benchmark; the build reported large-client-chunk warnings.

## What the automated tests cover

- Membership and owner controls, revoked/expired access, cache isolation and request boundaries.
- Separate newsletter consent and account lifecycle behaviour.
- Bounded research responses, report minimisation and exclusion of raw research from public output.
- Postcode input and lookup failure states.
- Journey release gates, validation, limits and null-duration handling.
- Stale inputs, unsupported pathways, equivalent comparison denominators and assessment state rendering.

These use controlled application adapters and fixtures, including simulated identity and provider responses. They do not establish a fresh live-provider call, the hosting ingress identity guarantee or a complete production security review.

## What remains unverified

| Remaining work | Why it matters |
|---|---|
| Approved non-owner research and export walkthrough | Confirms the complete normal-user path beyond the signed-out gate and controlled tests |
| Fresh map, evidence and comparison captures | Documents the current deployed UI rather than historical saved images |
| Development Python suite with dependencies installed | Establishes the state of the separate development backend tests |
| Provider evaluation and real journey validation | Supports a later decision on enabling tester journeys |
| Mobile and assistive-technology assessment | Tests usability beyond source-level fallback behaviour |
| Consented adult pilot | Measures whether users can complete tasks and interpret uncertainty correctly |

Production database records and applied migration state were not queried for the audit. No production data was mutated by these checks. No adoption, retention, customer conversion, recruitment benefit, routing-accuracy percentage or production-scale performance result is claimed.

## A useful next pilot

Ask adult testers to find an academy record, locate the evidence behind one field, distinguish category confidence from entrance confidence, and explain why an unavailable assessment is not a zero-opportunity result. Record task completion, interpretation errors and timings with sample size and test conditions.

Those measurements would evaluate the product's usefulness and clarity. They would remain separate from claims about a child's football success.
