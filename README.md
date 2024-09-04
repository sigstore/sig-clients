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

sig-clients doesn't own these, but these are relevant projects:

- [protobuf-specs](https://github.com/sigstore/protobuf-specs): cross-client data formats, especially for serializing 
- [sigstore-conformance](https://github.com/sigstore/sigstore-conformance): conformance test suites for clients
- [architecture-docs](https://github.com/sigstore/architecture-docs): specifications
- Sigstore client implementations in various languages:
  - Go: [sigstore-go](https://github.com/sigstore/sigstore-go), [Cosign](https://github.com/sigstore/cosign), [Gitsign](https://github.com/sigstore/gitsign),
  - Java: [sigstore-java](https://github.com/sigstore/sigstore-java)
  - JavaScript: [sigstore-js](https://github.com/sigstore/sigstore-js)
  - Python: [sigstore-python](https://github.com/sigstore/sigstore-python)
  - Ruby: [sigstore-ruby](https://github.com/sigstore/sigstore-ruby)
  - Rust: [sigstore-rs](https://github.com/sigstore/sigstore-rs)
- [policy-controller](https://github.com/sigstore/policy-controller)
- [Enterprise Contract](https://github.com/enterprise-contract)

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

**Slack.** We also communicate on [Slack](https://links.sigstore.dev/slack-invite). Channels that might be of interest include: `#clients`, `#java`, `#ruby-gems`, `#sigstore-rust`, `#sigstore-go`, `#cosign`, `#gitsign`.

## Governence

This Sig is co-chaired by [Fredrik Skogman]([url](https://github.com/kommendorkapten)) and [Appu Goundan]([url](https://github.com/loosebazooka))

## Roadmap

This has moved to the [client section of the community roadmap](https://github.com/sigstore/community/blob/main/ROADMAP.md#client-sdks).

## Security

Should you discover any security issues, please refer to Sigstore's [security
process](https://github.com/sigstore/sig-clients/security/policy).
