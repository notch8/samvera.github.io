---
title: "FAQ - Collection Nesting"
keywords: Nesting, Collection, FAQ
categories: How to Do All the Things
permalink: collection_extensions_faq_nesting.html
folder: samvera/how-to/collection_extensions/hyrax_2.0/faq_nesting.md
sidebar: home_sidebar
tags: [development_resources]
a-z: ['FAQ - Collection Nesting', 'Collection Extensions - Nesting', 'Nesting of Collections']
version:
  id: 'hyrax_2.0-master'
---

### What is collection nesting?

Collections that have collections as members.

### Can a collection have collections and works as members?

Yes.  A collection can have all sub-collections, all works, or a combination of both.

### Is there a limit to how deep the nesting can go?

The depth of nesting is not limited. There may be performance issues with deep nesting.  The UI may be challenging for deep nesting.

TODO: Do we want to impose a limit?

### Can a collection be its own descendant?

No. An ancestor validation is performed when a collection is added to another collection to prevent circular chains.

### Can collections of different types be nested?

No.  At this time, nesting is limited to collections of the same type.  For example, you can nest a User Collection in a User Collection AND you can nest an Organizational Collection in an Organization Collection, but you can NOT nest a User Collection in an Organizational Collection.

In the future, this could be relaxed to allow a configuration that identifies which collection types can be nested in which, if this is determined to be a priority.
