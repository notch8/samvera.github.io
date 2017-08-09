---
title: "FAQ - Collection Discovery"
keywords: Discovery, Collection, FAQ
categories: How to Do All the Things
permalink: collection_extensions_faq_discovery.html
folder: samvera/how-to/collection_extensions/hyrax_2.0/faq_discovery.md
sidebar: home_sidebar
tags: [development_resources]
a-z: ['FAQ - Collection Discovery', 'Collection Extensions - Discovery', 'Discovery of Collections']
version:
  id: 'hyrax_2.0-master'
---

### What does it mean for a collection to be discoverable?

Collections that are discoverable will have the collection itself included in search results, showing the collection title and summary metadata.

### Are items of a discoverable collection discoverable?

Not necessarily. The collection's setting for discovery does NOT effect the discoverability of the items in the collection.  All items in a collection are discoverable based on their own settings.

WHY NOT? The items in a collection can be in other collections which also have discoverability settings.  It would be complicated to sort through all the possible combinations and produce an intuitive, predicatable behavior.

### Do collections have to be public to be discoverable?

Yes, for public users.  For logged in users, collections will show up in search results if they can edit the collection.

### Where do I configure discoverability of a collection?

For an individual collection, you set discoverability on the new/edit form for the collection on the Discovery tab.

### If a collection type is NOT discoverable, can I set the visibility to Public?

No, if the collection type of a collection has discoverable=false, the new/edit form will not show the Discoverability tab.  All collections of this type will have visibility=Private.

### Why can't I set a collection to Public?

Whether a collection can be set to discoverable is determined by the collection type.  The site admin congifures a collection type to have discoverable on/off.

### Where do I configure discoverability of a collection type?

Dashboard -> Settings -> Collection Types -> new/edit a collection type

### Can I change the discoverability setting of the collection type?

Yes and no... This setting is per collection type.  Once a collection of a type is created, the Settings configurations are not modifiable.  This includes includes the Discoverable setting.  Up to that point that you create a collection of that type, you can change the Settings, including Discoverable.
