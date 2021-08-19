# Allowed Values package

A set of forms and templates intended to be used on Properties pages to ease the
process of defining list of values allows and a couple of other settings for a Property. 

# Pages

* `Property:Allows value` - redefines the built-in SMW Allow value property
* `Template:FormField` - provides a `{{FormField}}` template for PageForms
* `Template:Get default value` - retrieves default value from selected Property
* `Template:Get values` -  retrives list of allowed values for a Property
* `Template:Only existing` - helper template for a `{{field}}`
* `Form:Property` - main form to edit Property pages
* `Template:Property` - template for Property pages
* `Property:Suggests value` -  property for suggestions
* `Property:Value` - base property for `Allows value` and `Suggests value`

# Examples

* `Form:TestPeropertyFormUsage` - example form
* `Property:TestProp1` - example property

# Usage 

* Create new property using `Special:FormEdit/Property`
* Use `FormField` template to link properties to PageForms form like below:

```
{{FormField|FieldName|PropertyName|<nowiki>|input type=tokens</nowiki>}}
```

This will link all the allowed, suggested values automatically, same as the default value
for a property.

# Requirements

* PageExchange
* PageForms
* SemanticMediaWiki

# Setup

* Add the following to the bottom of your LocalSettings.php: 
```php
$wgPageExchangePackageFiles[] = 'https://raw.githubusercontent.com/NationalGalleryOfArt/mediawiki-pages-AllowedValues/main/page-exchange.json';

```
* Navigate to `Special:Packages` and install the package.
* (Optional) Run `php maintenance/runJobs.php`.

