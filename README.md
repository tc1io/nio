# Nio - A Generic ABAC System

The goal of Nio is to add fine grained authorization capabilities to
systems that use OAuth2 and OpenID Connect for authentication.

Nio implements the concept of [ABAC](https://en.wikipedia.org/wiki/Attribute-based_access_control)

Nio is not a Identity Provider and not an Authorization server but instead aims to complement
use of such systems (including Multi-IdP scenarios) with a general authorization approach.

The name _Nio_ is inspired by the [two wrathful and muscular guardians of the Buddha](https://en.wikipedia.org/wiki/Nio).

# Identity and group management

- Replication of identities and groups from one or more Identity providers using, for example,
  [SCIM](https://datatracker.ietf.org/doc/html/rfc7643).
- Support to combine corresponding identities from different IdP intop one identity in Nio.
- To clarify: Alignment of groups, too - or would that not make sense?

# Realms

Support the creation and management of realms as containers for defined attributes and policies.

# Identity attribute management

A given real defines a set of identity attributes. Nio supports assigning attribute/value pairs to
identities for the context of a given realm. Identities can have attribites assigned in different
realms; there is no relationship between realms and attribute assignments.

Support adding 

Create/update realm
Define/manage usbject attributes per realm
Groups?

# API


GET /policies/{realm}
-> List of policies


GET /subject/{identity}/attributes



# Usage in Resource Server


Realm: hardcoded/known

Extract principal from request
Get attributes of principle
Get policies for realm
Derive resource attributes from request (possible attributes are related/scoped by realm?)
Derive context attributes from request/environment (these are general, realm/impl independent)

permissions = apply policies to subject atts, resource atts, context atts

check if permission exists for the action

Create response
when adding a UI controil, verify permission to activate it exists
when displaying lists, use <?? information> to determine list to display (eg all projects)


# Notes

IAM system manages users and hierarchical groups.

Groups is an attribute
Groups in attributes are flattened (path through tree is collected)
users inherit group atributes
possible attributes are per-realm







