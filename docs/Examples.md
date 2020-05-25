# Worked examples

## Getting started 
Firstly, you need to have your login details ready. Otherwise you need to supply this with each call:

```
  --api-key API_KEY
  --config CONFIG
  --user-id USER_ID *or* --group-id GROUP_ID
  --indent INDENT
```

Remember that you can store this in `zotero-cli.toml` too.

## What groups do I have access to?

If you want to access a group collection but don't know the GROUP_ID, find it like this:

```
zotero-cli groups
```

# Collections
## Display collections

Once the login details are set up, and you have the GROUP_ID, e.g. show your collections

```
zotero-cli collections --help
zotero-cli collections
```

Note down a key (K35DEJSM). Show sub-collections of that collection

```
zotero-cli collections --key K35DEJSM
```

## Adding and removing items to/from a collection

TODO

# Items
## Getting item information

Use the same key (K35DEJSM). Show some items

```
zotero-cli items --help
zotero-cli items --top
zotero-cli items --collection K35DEJSM
```

## Item types and item fields (with localised names) 

```
zotero-cli types
zotero-cli fields --type=book
```

## Updating the collections for an item

TODO


## Update an existing item:

Properties not included in the uploaded JSON are left untouched on the server.

```
zotero-cli update-item --key ITEM_KEY UPDATE.json
```

Add or remove item from several collections

```
zotero-cli item --key ABC --addtocollection=DEF --removefromcollection=GHI,JKL
```

With --replace, you submit the item's complete editable JSON to the server, typically by modifying the downloaded editable JSON — that is, the contents of the data property — directly and resubmitting it.

```
zotero-cli update-item --key ITEM_KEY NEW.json
```


## Item creation

Here is how you use create-item:

```
zotero-cli create-item --template book > book.json
gedit book.json
zotero-cli create-item book.json
```
For further options, see `zotero-cli create-item --h`.



# Attachments

# Getting attachments
```
zotero-cli.ts attachment [-h] --key KEY --save SAVE
```



# Generic get request
```
zotero-cli get /apipath
```