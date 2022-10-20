---
title: Overview
---

## What is SQuiL?

In the absence of a custom user interface, browsing and searching a given database is
hard and usually requires writing custom SQL even in very simple cases.

SQuiL aims to fill that niche between a custom user interface and generic but SQL-centric
database tools.

It derives a rough UI from any database schema as long as foreign keys are present
to allow SQuiL to infer table relationships.

## How can I use SQuiL?

SQuiL aims to be better than other generic tools for

- quickly searching for a specific data row, and
- easily walking through the data along table relations. 

SQuiL comes in two versions:

- SQuiL Web, a docker image that allows you to provide web access to your database and
- SQuiL Desktop, a Windows desktop app that is easier to install for a quick try.

Providing web access to databases is most useful in company internal scenarios: For
example, you may have a web application with a public web interface for your customers,
but you want something quick-and-dirty for internal administration without having
to code another application.

Currently, SQuiL is read-only, but editing features are in the works!

## What is SQuiL not?

SQuiL is not a database administrative tool, although DBAs may find it a useful
addition to their toolbox.

SQuiL does not allow you to make arbitrary SQL queries, and for good reason:

Even over the most restricted connection a sufficiently bad query can make a database server
work virtually forever and consume resources. SQuiL will not execute
such queries against your database and in fact even make sure that all queries against
larger tables have to be along existing indexes: The way to make SQuiL display a
search field for a specific column isn't to reconfigure SQuiL but to add the appropriate
index to your database.

SQuiL wants to provide *safe* access.
