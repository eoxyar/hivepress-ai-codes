# hivepress-ai-codes
Some ai generated plugins 
HP Conditional Dropdowns
WordPress Plugin for HivePress — User Guide


What is this plugin?
HP Conditional Dropdowns adds linked parent → child dropdown fields to your HivePress-based WordPress site. When a user selects a value in the parent field (e.g. a car brand), the child field (e.g. model) automatically updates to show only the relevant options.
The plugin works across all HivePress forms: Add Listing, Edit Listing, Search, and Filter — with no code required.

Key Features
    • Conditional dropdowns: parent selection filters child options instantly
    • Works in Add Listing, Edit Listing, Search, and Filter forms
    • Category restriction: show field pairs only for specific listing categories
    • CSV import / export for bulk data management
    • Mobile-friendly admin interface
    • Custom icons and display formats for listing attributes
    • Select2 / AJAX compatible

Setup Guide
Step 1 — Create a Field Pair
Go to HivePress → Conditional Dropdowns and click Add New Pair.
Fill in the following fields:
Field	Description
Pair Name	Internal label, e.g. "Brand / Model"
Parent Field Slug	Lowercase, no spaces. e.g. brand — this becomes the meta key
Parent Field Label	Display name users see, e.g. "Brand"
Child Field Slug	e.g. model
Child Field Label	e.g. "Model"
Restrict to Categories	Optional. Leave empty to show on all listing categories

Step 2 — Add Conditional Data
Go to Conditional Data and select your pair. Enter parent → child pairs, one row at a time, or import a CSV file.
CSV format: two columns, no header row. Column 1 = parent value, Column 2 = child value. One pair per line.

Step 3 — Done
The fields appear automatically in all HivePress forms. No shortcodes or template edits needed.

Value Naming Rules
Field values are stored in the database as plain strings. Two conventions apply:
Spaces → Underscores
Values with spaces must use underscores: Alfa_Romeo is automatically displayed as Alfa Romeo everywhere.
Numeric Values → underscore prefix
Values that are only numbers (e.g. 80, 145) must be prefixed with _. Store them as _80, _145 — the prefix is stripped automatically in all dropdowns, so users always see 80, 145.
The underscore prefix also ensures numeric models sort at the top of dropdown lists, before alphabetical entries.

Summary:

What you store in DB =========What users see

Alfa_Romeo======Alfa Romeo

_80 ======	80

_145 ======	145

A3 ======	A3

Grand_Cherokee ======	Grand Cherokee



⚠ Important Warning
If you deactivate or delete the HP Conditional Dropdowns plugin, all conditional field data stored in listings will be lost. Always keep the plugin active as long as listings depend on it.
