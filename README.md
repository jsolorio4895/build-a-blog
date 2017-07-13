# build-a-blog
LC101 assignment

This small, flask-based app implements a blog.

## Entity Analysis

* A _blog_ is a series of _entries_
* Each _entry_ includes a _title_ and a _body_

## Requirements

The app must meet several requirements:

* List all previous blog entries in chronological order
* List all previous blog entries in reverse-chronological order
* Allow anybody to create a new blog entry
* Display the individual blog entry after creation
* Include a menu bar with available commands

### Non-requirements

* No authentication or authorization is required
* All access can be anonymous

## User stories

### Story 0
* **As** an anonymous visitor to the site
* **When** I arrive at the site (route "/")
* **Then** I see a list of previous blog entries in oldest-first order

### Story 1
* **As** an anonymous visitor ON the site
* **When** on any page
* **Then** I can see a menu of actions available to me

### Story 2
* **As** an anonymous visitor ON the site
* **When** on any page
* **And** I click on the "List all entries (newest-first)" menu item
* **Then** I see a list of previous blog entries in newest-first order

### Story 3
* **As** an anonymous visitor ON the site
* **When** on any page
* **And** I click on the "List all entries (oldest-first)" menu item
* **Then** I see a list of previous blog entries in oldest-first order

### Story 4
* **As** an anonymous visitor ON the site
* **When** I click on the "Create new entry" menu items
* **Then** I see a form for entering a title and a body

### Story 5
* **As** an anonymous visitor on the "Create new entry" form page
* **When** I supply a _title_
* **And** I supply a _body_
* **And** I click the "Save" button
* **Then** I see my new entry on a page by itself

### Story 6
* **As** an anonymous visitor on the "Create new entry" form page
* **When** I DO NOT supply a title
* **Or** I DO NOT supply a body
* **And** I click the "Save" button
* **Then** I see the same form with my given values (if any) for _title_ and _body_ with an error message


## User accessible command (the menu items):
* List all entries (oldest-first)
* List all entries (newest-first)
* Create new entry

## Routes

* **"/"** - GET: redirect to "/blog"
* **"/blog"** - GET: Display list of all entries with default sort order (oldest-first)
* **"/blog?sort=newest"** - GET: Display list of all entries newest-first
* **"/blog?entry=ID"** GET: Display entry with id=ID
* **"/new_entry"** - GET: Display new entry form; POST: Process new entry



