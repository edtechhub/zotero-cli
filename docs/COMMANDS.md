# Zotero API

Details for 
https://www.zotero.org/support/dev/web_api/v3/basics

`<prefix>` below means `/users/<userID>` or `/groups/<groupID>`.

## Collection

| URI | Description | zotero-cli |  
|---|---|---|
| &lt;prefix>/collections | Collections in the library | collections |
| &lt;prefix>/collections/top | Top-level collections in the library | collections --top |
| &lt;prefix>/collections/&lt;collectionKey> | A specific collection in the library | collections --key ABC |
| &lt;prefix>/collections/&lt;collectionKey>/collections | Subcollections within a specific collection in the library | |

## Items

| URI | Description | zotero-cli |
|---|---|---|
| &lt;prefix>/items | All items in the library, excluding trashed items | items |
| &lt;prefix>/items/top | Top-level items in the library, excluding trashed items | items --top |
| &lt;prefix>/items/trash | Items in the trash | trash |
| &lt;prefix>/items/&lt;itemKey> | A specific item in the library | item --key ABC |
| &lt;prefix>/items/&lt;itemKey>/children | Child items under a specific item | item --key ABC --children |
| &lt;prefix>/publications/items | Items in My Publications | publications |
| &lt;prefix>/collections/&lt;collectionKey>/items | Items within a specific collection in the library | items --collection ABC|
| &lt;prefix>/collections/&lt;collectionKey>/items/top | Top-level items within a specific collection in the library | items  --collection --top |

## Searches
(Note: Only search metadata is currently available, not search results.)

| URI | Description | zotero-cli |
|---|---|---|
|&lt;prefix>/searches	| All saved searches in the library | searches |
|&lt;prefix>/searches/<searchKey>	| A specific saved search in the library | |

## Tags
| URI | Description | zotero-cli |
|---|---|---|
| &lt;prefix>/tags | All tags in the library | tags |
| &lt;prefix>/tags/&lt;url+encoded+tag> | Tags of all types matching a specific name | |
| &lt;prefix>/items/&lt;itemKey>/tags | Tags associated with a specific item | |
| &lt;prefix>/collections/&lt;collectionKey>/tags | Tags within a specific collection in the library | |
| &lt;prefix>/items/tags | All tags in the library, with the ability to filter based on the items | |
| &lt;prefix>/items/top/tags | Tags assigned to top-level items | |
| &lt;prefix>/items/trash/tags | Tags assigned to items in the trash | |
| &lt;prefix>/items/&lt;collectionKey>/items/tags | Tags assigned to items in a given collection | |
| &lt;prefix>/items/&lt;collectionKey>/items/top/tags | Tags assigned to top-level items in a given collection | |
| &lt;prefix>/publications/items/tags | Tags assigned to items in My Publications | |

## Other URLs
| URI | Description | zotero-cli |
|---|---|---|
| /keys/&lt;key> | The user id and privileges of the given API key.Use the DELETE HTTP method to delete the key. This should generally be done only by a client that created the key originally using OAuth. | key |
| /users/&lt;userID>/groups | The set of groups the current API key has access to, including public groups the key owner belongs to even if the key doesn't have explicit permissions for them. | |

