# NIO - A Generic ABAC System


# API


GET /policies/{realm}
-> List of policies


GET /subject/{identity}/attributes

# Usae for management

Create/update realm
Define/manage usbject attributes per realm
Groups?


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







