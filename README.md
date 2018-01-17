# ACF Heading Field Type

A WordPress plugin which extends ACF and adds the "Heading" basic field type.

The heading basic field type has two properties:

  - **Label:** The actual text contents to be rendered into the heading
  - **Level:** The level of the heading, which is a number 1 - 6 corresponding to the desired heading level (h1, h2, h3, ...)

The purpose of which is to allow users to control the heading level of a given
module or component of your ACF fields. This is primarily for SEO and
accessibility optimization for a given site, but can be used for other purposes.

## Installation

You can install this plugin in two ways; either by downloading the project and
installing manually, or grabbing the latest version of the plugin from the
GitHub releases tab. See below for more information.

### Manual Installation

To manually install this plugin, do the following:

  1. Download/clone this repository somewhere on your local machine
  2. Zip up the `acf-heading/` directory in the repository
  3. Navigate to your WordPress install's `wp-admin/` page
  4. Go to the Plugins section
  5. Click "Add New"
  6. Click "Upload Plugin" at the top
  7. Choose the zip file you just created
  8. Install and activate the plugin
  9. You're ready to use the heading field!

### Release Installation

If you don't want to zip the plugin up yourself, a zip is provided in the
Releases tab of this repository. Download that, then refer to steps 3 - 9 of
the [Manual Installation](#manual-installation) section.

## Usage

### When Creating Fields

Assuming you installed the plugin correctly, you should see a new option in the
Type dropdown when adding a field in ACF, called "Heading" under the "Basic"
section.

Selecting that will allow you to use this field.

### When Retrieving Data Through Code

When you retrieve a field's data that is of type heading, the data will be an
associative array which has two keys: `"label"` and `"level"`.

`"label"` will be a string that is what the user specified they want the
contents of the heading to be.

`"level"` will be a number, 1 through 6, of what level the user has specified
that they want the heading to be.

So, an example heading field's data would look like:

```
[
    "label" => "This is my heading!",
    "level" => "3"
]
```

## Legal

The terms "ACF" and "Advanced Custom Fields" are copyright Advanced Custom
Fields and Elliot Condon Web Development.
