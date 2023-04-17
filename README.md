# sig-clients

This is the repository for the Clients Special Interest Group (sig-clients) in
the Sigstore project. This group has the following provisional mission until the
next meeting where we'll discuss it:

> Make Sigstore clients across languages/ecosystems easy-to-write, compatible,
> and secure by providing shared designs/documentation, data formats, and test
> suites.

In general, we'll try to avoid telling individual implementations what to do,
though we may have criteria for various official statuses (e.g., what
constitutes a "supported" client).

## Projects

sig-clients doesn't exclusively own most of these, but you may be interested:

- [protobuf-specs](https://github.com/sigstore/protobuf-specs): cross-client data formats, especially for serializing 
- [sigstore-conformance](https://github.com/sigstore/sigstore-conformance): conformance test suites for clients
- [architecture-docs](https://github.com/sigstore/architecture-docs]): specifications
- Sigstore client implementations in various languages:
  - Go: [sigstore-go](https://github.com/sigstore/sigstore-go), [Cosign](https://github.com/sigstore/cosign), [Gitsign](https://github.com/sigstore/gitsign),
  - Java: [sigstore-java](https://github.com/sigstore/sigstore-java)
  - JavaScript: [sigstore-js](https://github.com/sigstore/sigstore-js)
  - Python: [sigstore-python](https://github.com/sigstore/sigstore-python)
  - Ruby: [sigstore-ruby](https://github.com/sigstore/sigstore-ruby)
  - Rust: [sigstore-rs](https://github.com/sigstore/sigstore-rs)
[policy-controller](https://github.com/sigstore/policy-controller)

## Get Involved

(*You'll need to join [sigstore-dev@googlegroups.com](https://groups.google.com/g/sigstore-dev) for access to many of these (to prevent spam).*)

We welcome contributions from all! Great ways to help include:

- Use a Sigstore client and provide feedback (in the form of GitHub issues, chatter on Slack, etc.).
- Contribute to any of the above projects: you can just jump in on GitHub (generally best to file issues, ask whether anybody is working on something, etc. before just firing off a PR; see the `CONTRIBUTORS.md` or `CONTRIBUTING.md` in the respective repository).
- Say hi in Slack!
- Join a meeting (open to all community members; see below).

**Meetings.** Check the [sigstore community calendar](https://calendar.google.com/calendar/u/0?cid=ZnE0a2dvbTJjZTQzaG5jbmJjZmphMmNrMjBAZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ) for meeting invitations/times (see [community](https://github.com/sigstore/community) repository for more). We recognize that various constraints (time zones, connectivity, privacy concerns) mean that meetings aren't a great way for everybody to contribute. We strive to make important decisions asynchronously, via design documents and GitHub issues. At the same time, synchronous meetings can be really useful for hashing out complex issues quickly. We'll record these meetings (links should be in the notes docs).

- sig-clients meeting (monthly; [notes](https://docs.google.com/document/d/1PNbBZSG3QC8hWVYBx6YDppaXwmSLDfx7t66ECaGa8y4/edit#heading=h.hb09y2f8i7to))
- Sigstore Java (weekly; [notes](https://docs.google.com/document/d/1R7mL-IUrc2Z_LuOIvwDWshVuPQS_2VNE_cIQx4Oy5zw/edit))
- Sigstore Golang (biweekly; [notes](https://docs.google.com/document/d/1EcJIhqSS9E86cHAQXaXiu2_r1s0kNbHz4uLLwwGo-vw/edit#heading=h.td0phy2bwk06))

**Slack.** We also communicate on [Slack](https://links.sigstore.dev/slack-invite). Channels that might be of interest include: `#clients`, `#java`, `#ruby-gems`, `#sigstore-rust`, `#sigstore-go`, `#cosign`.

## Governence

We're still sorting this out for SIGs. Come back soon!

## Roadmap

You'll need to join [sigstore-dev@googlegroups.com](https://groups.google.com/g/sigstore-dev) for access to many of these (to prevent spam).

Last updated: 2023-04-17. See also [project-wide roadmap](https://github.com/sigstore/community/blob/main/ROADMAP.md) (possibly out-of-date).

*This currently represents @znewman01's brain dump; at the next client meeting, we'll work through this.*

**Short-term (months).**

Goal: focusing on Cosign in the near-term as the most widely-used client. If
other clients like what we're doing there, they can emulate it. Document
expectations for clients.

- Tech debt: Cosign refactor, port innards to sigstore-go ([cosign#2462](https://github.com/sigstore/cosign/issues/2462), [cosign#844](https://github.com/sigstore/cosign/issues/844))
- Bundles ([cosign#2131](https://github.com/sigstore/cosign/issues/2131))
- Policy enhancements: improve Cosign UX
  - [Sugar for common OIDC providers](https://github.com/sigstore/cosign/issues/2838)
  - [New GitHub claims](https://github.com/sigstore/cosign/issues/2719)
  - [Clearer verification options](https://github.com/sigstore/cosign/issues/2648)
  - [Guidance in identity assertions](https://github.com/sigstore/cosign/issues/2804)
- Complete the [architecture docs draft](https://docs.google.com/document/d/1-OccxmZwkZZItrfOnO3RP8gku6nRbtJpth1mSW3U1Cc/edit) and port it to GitHub.

**Medium-term (quarters).**

Goal: make Cosign more flexible 

- BYO PKI, private deployments
- [cosign#2858](https://github.com/sigstore/cosign/issues/2858), [cosign#2568](https://github.com/sigstore/cosign/issues/2568), [cosign#2632](https://github.com/sigstore/cosign/issues/2632), [cosign#2630](https://github.com/sigstore/cosign/issues/2630), [cosign#2808](https://github.com/sigstore/cosign/issues/2808), [cosign#2255](https://github.com/sigstore/cosign/issues/2255)
- Policy enhancements
  - Declarative verification
    - Along the lines of [Hammurabi](https://hammurabi.jameslarisch.com/) for web PKI, [sigstore-go#35](https://github.com/sigstore/sigstore-go/issues/35), [sigstore-python#299](https://github.com/sigstore/sigstore-python/pull/299).
    - Possibly using Rego/CUE (something datalog-inspired)
  - Fancier policies
    - Unification between Cosign and policy-controller
    - e.g., SBOM https://github.com/sigstore/cosign/issues/1954
- Testing: [conformance test suite](https://github.com/sigstore/sigstore-conformance)
  - "End-to-end" tests: hook up to [clients](https://github.com/sigstore/sigstore-conformance/issues/61)
  - ["Fuzz tests"](https://github.com/sigstore/sigstore-conformance/issues/64)

**Long-term (eventually).**

- [Plumbing and porcelain](https://git-scm.com/book/en/v2/Git-Internals-Plumbing-and-Porcelain) model for Cosign.
- Policy: sophisticated verification policies.
  - Integration with [TUF](https://theupdateframework.com/)/[in-toto](https://in-toto.io/).
- [Can we avoid writing every new Sigstore client from scratch?](https://docs.google.com/document/d/1xrnvZr9o7utL8xtgT-heKVWAk0aOagjg2YB5Onarzxk/edit)
- <Your ideas here!>


## Security

Should you discover any security issues, please refer to Sigstore's [security
process](https://github.com/sigstore/community/blob/main/SECURITY.md)
