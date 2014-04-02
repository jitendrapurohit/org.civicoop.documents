# Document storage in CiviCRM

## Functionality

* Store documents on the contact cart
* A document can be linked to more than one contact
* Version management with a document
* Custom search to find documents

## Technical background

There is an entity **CRM_Documents_Entity_Document** which contains 
all the information for a document. E.g. the linked contact ID's. 
Every document contains one or more **CRM_Documents_Entity_DocumentVersion** 
for a version of the document. A Document version contains a link to the file
which is a **civicrm_entity_file** item.

## Hooks

The following hooks are available in this module

* **hook_documents_get_status($doc, &$status)** this hook is called while checking the status of the document. The returned status is 0 (for doc is not in use) or 1 (document is in use).

## Roadmap

### Beta3

* ~~Link documents to cases~~
* Search document by case type
* ~~Links to contacts doesn't always seem to work well~~
* Store the user context upon search (e.g. for going back on a edit form)
* ~~Store the user context in the case (e.g. for going back after adding/editing a document in the case context) ~~
* ~~Document appears twice in search result when added to more than one contact~~
* ~~Removing contact from document when a contact is removed~~
* Removing document on a merge of duplicate contacts
* Update a document which is linked to a case when the client of the case are changed
* ~~Update a document when a case is removed~~
* ~~Search with a modified date range~~


### Future (dreaming)

* Add file type icons (such as pdf/doc etc...)
* Add tagging to to a document
* Search with tags
* Add hooks for linking documents to custum entities (e.g. campaigns)
* Add a connection with ownCloud for interacting with documents
* Add functionality to work together on a document with the webODF functionality





