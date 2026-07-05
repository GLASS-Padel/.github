# Governance

This document describes how the GLASS Padel organisation is run: who holds
which responsibilities, how access is granted, and how decisions are made. It
reflects the current, deliberately simple structure and will be revised as the
team grows.

## Roles

The engineering team is organised by function rather than seniority. Every
engineer is trusted equally with the day-to-day work of the repositories they
own; the distinctions below describe responsibility, not rank.

| Function            | Owner                    |
| ------------------- | ------------------------ |
| Engineering lead    | Baki                     |
| Backend             | Alperen, Emir            |
| Mobile              | Emir, Eren               |
| DevOps and infra    | Umut                     |

## Teams

Access is administered through GitHub teams, so that a person's permissions
follow their function and are changed in one place.

| Team      | Purpose                                         | Members             |
| --------- | ----------------------------------------------- | ------------------- |
| `leads`   | Architecture, direction, cross-repo oversight   | Baki, Umut          |
| `backend` | Backend and API engineering                     | Alperen, Emir, Umut |
| `mobile`  | Mobile application engineering                  | Emir, Eren          |
| `devops`  | Infrastructure, deployment and operations       | Umut                |

## Access model

The organisation follows least privilege. Engineers hold the **Maintain** role
on the repositories they work on, which covers everything required to build,
review and merge: pushing branches, managing issues and pull requests, and
editing repository content. It deliberately excludes the three irreversible
administrative actions, which are reserved for the organisation owner:

- deleting a repository,
- changing a repository's visibility (private to public),
- managing who has access to a repository.

This keeps day-to-day work unobstructed while ensuring no single mistake can
expose or destroy the organisation's code.

Repository access by function:

| Repository       | leads    | backend  | mobile   |
| ---------------- | -------- | -------- | -------- |
| `glass-web-app`  | Maintain | Maintain |          |
| `glass-mobile`   | Maintain |          | Maintain |

`glass-backend` access is administered separately and is not modified through
this document.

## Ownership

The organisation has a single owner, Umut, who holds administrative control over
settings, membership and billing. Owner-level responsibilities are documented
here so they are transparent to the whole team rather than concentrated silently.

## Decision-making

Technical decisions are made by the engineers responsible for the affected area,
in consultation with the lead where a change is cross-cutting or architectural.
Changes to this governance model, to team structure, or to organisation-wide
policy are made by the owner in consultation with the lead.

## Security

- Two-factor authentication is required of every member.
- Secrets are never committed to any repository.
- Vulnerabilities are reported privately, as described in `SECURITY.md`.

## Amending this document

Propose changes by opening a pull request against this file. Amendments take
effect once approved by the owner.
