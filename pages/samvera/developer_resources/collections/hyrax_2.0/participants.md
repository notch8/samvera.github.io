---
title: "FAQ - Collection Participants"
keywords: Participants, Collection, FAQ
categories: How to Do All the Things
permalink: collection_extensions_faq_participants.html
folder: samvera/how-to/collection_extensions/hyrax_2.0/faq_participants.md
sidebar: home_sidebar
tags: [development_resources]
a-z: ['FAQ - Collection Participants', 'Collection Extensions - Participants', 'Participants for Collections']
version:
  id: 'hyrax_2.0-master'
---

### What participants can be set for a collection?

#### Manager

Managers of a collection can add to and remove works from the collection, modify collection metadata, and delete the collection.

Impact:

* the manager is given `edit_access` for the collection, which is checked to allow editing of the collection metadata
* the manager is added to the permissions_template_access for the collection as a `manager`, which is checked to allow a user to add works to the collection
* any works created directly in the collection will give the manager 'edit_access' of the work

TODO: Setting edit_access on works could complicate what happens if a manager is removed.

#### Depositor

Depositors of a collection can view the collection and add works to it, even if the visibility permissions of the collection otherwise would not permit them to view it.

Impact:

* the depositor is given `view_access` for the collection, which allows the depositor to see the collection even when it would otherwise be hidden based on visibility settings
* the depositor is added to the permissions_template_access for the collection as a `depositor`, which is checked to allow a user to add works to the collection
* does NOT give the depositor any special access to works in the collection
* depositors have `edit_access` to works they create only

#### Viewer

Viewers of this collection can view it even if the visibility permissions of the collection otherwise would not permit them to view it.

Impact:

* the viewer is given `view_access` for the collection, which allows the depositor to see the collection even when it would otherwise be hidden based on visibility settings


### What participants can be set for a collection type?

#### Collection Type Manager

Managers of a collection type can edit collections other users created, including adding to and removing works from a collection, modifying collection metadata, and deleting collections, only for collections of the type they manage.

Impact:

* the manager is given `edit_access` for all collections created with type being managed, which is checked to allow editing of the collection metadata
* the manager is added to the permissions_template_access as a `manager` for all collections created of this type, which is checked to allow a user to add items to and remove items from a collection

TODO: What else?

#### Collection Creator

Creators of collections of this type can create and manage their own collections.

Impact:

* the creator is given `edit_access` for any collections they create of this type, which is checked to allow editing of the collection metadata
* the creator is added to the permissions_template_access as a `manager` for the collections they create of this type, which is checked to allow a user to add items to and remove items from a collection


#### What happens when I add a participant to a collection type?

#### What happens when I remove a participant from a collection type?

#### What happens when I add a participant to a collection?

TODO: This is a good question.  How does it work for admin_sets?  If a user or group is added, I assume they are added to the permissions_template_access table with manage or deposit permissions as appropriate.  What about all the existing works... is edit_access added?  Do you have to cycle through all works in the admin_set?

#### What happens when I remove a participant from a collection?

TODO: This is a good question.  How does it work for admin_sets?  If a user or group is removed, I assume they are removed from the permissions_template_access table.  What about all the existing works... is edit_access revoked?  How can you tell if the edit_access was granted via admin_set's participants or granted via the work's sharing tab?  Do you have to cycle through all works in the admin_set?

### How do these interact with the participants set in admin sets?

TODO: add in description



