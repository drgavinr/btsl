# wiki-dumps

Dumps of the entire [By The Sword Linked](https://www.bytheswordlinked.uk/) wiki.

## Contents

- [Data](#data)
- [Copyright acknowledgements](#copyright-acknowledgements)
- [Mediawiki configuration](#mediawiki-configuration)
    - [Mediawiki extensions](#mediawiki-extensions)
    - [Custom namespaces](#custom-namespaces)
    - [Interwiki links](#interwiki-links)
    - [Other local settings](#other-local-settings)

## Data

Data files available are as follows:

- by-the-sword-linked-RDF-dump.rdf.zip: all semantic properties from individual entities in the wiki exported as OWL DL serialized as RDF/XML. This does not include free text or non-semantic template parameters. Has to be zipped otherwise it's too big to upload to Github.
- by-the-sword-linked-Wikitext-Structure.xml: the wikitext source code of every page in the following namespaces: Mediawiki, Project, Property, Template, Form, Category, Help. This gives the data structures of the wiki without the content. Exported as [wikitext XML](https://www.mediawiki.org/wiki/Help:Export#Export_format).
- by-the-sword-linked-Wikitext-Content.xml.zip: the wikitext source code of every page in the following namespaces: Main, Events, Locations. This gives the content which goes with the data structures above. Exported as [wikitext XML](https://www.mediawiki.org/wiki/Help:Export#Export_format). Has to be zipped otherwise it's too big to upload to Github.
- btsl-logo.svg: the site logo.

For more information about the project and data, see:

- [Introductory blog post](https://bytheswordlinked.hcommons.org/2019/02/26/introduction/) explains the aims and scope of the project.

These wiki pages give further information. They can no longer be viewed on the web, but they are included in the archived content:

- **Help:Create** a page gives an overview of the basic entity types.
- **Help:Data structures** gives more details of the semantic properties and how they are used by each entity type.
- **Help:Dates** explains how the project handles the difference between the Julian and Gregorian calendars.
- **Project:Progress** gives an overview of what is and isn't included in the data.

## Copyright acknowledgements

The data includes data reused from the following sources under the following licences, which legally require attribution:

- [Open Government Licence](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/):
    - [The National Archives of the UK](https://www.nationalarchives.gov.uk/)
    - [National Records of Scotland](https://www.nrscotland.gov.uk/)
    - [Ordnance Survey of Great Britain](https://www.ordnancesurvey.co.uk/business-government/tools-support/open-data-support)
    - [Natural England](https://data.gov.uk/dataset/21104eeb-4a53-4e41-8ada-d2d442e416e0/national-character-areas-england)
    - [Natural Resources Wales](https://data.gov.uk/dataset/10ba5624-bc9c-47ec-9bfa-69a46620b23d/national-landscape-character-areas-nlca)
- [Creative Commons Attribution](https://creativecommons.org/licenses/by/4.0/) licence (CC-BY):
    - [British Library EThOS thesis metadata](https://doi.org/10.23636/ybpt-nh33) (2021 version)
- not formally licensed but effectively same as CC-BY:
    - [Wikishire](http://wikishire.co.uk/lookup/)
    - [Historic County Borders Project](http://www.county-borders.co.uk/)
- [Creative Commons Attribution ShareAlike](https://creativecommons.org/licenses/by-sa/4.0/) licence (CC-BY-SA):
    - [English Wikipedia](https://en.wikipedia.org/wiki/Main_Page)
    - [Linking Experiences of World War One](https://www.collaborativecollections.org/WorldWarOne/Main_Page)

 ## MediaWiki configuration

 These sections contain more detailed information about how to set up MediaWiki to work like By The Sword Linked.

 ### MediaWiki extensions

 These extensions are bundled with MediaWiki and must be enabled:

 - CategoryTree
 - Cite
 - InputBox
 - Interwiki
 - ParserFunctions

 By The Sword Linked also uses these extensions, which are not bundled with MediaWiki:

 - [JulianGregorianDate](https://github.com/drgavinr/julian-gregorian-date)
 - [Semantic MediaWiki](https://www.semantic-mediawiki.org/)
 - [Maps](https://maps.extension.wiki/)
 - [PageForms](https://www.mediawiki.org/wiki/Extension:Page_Forms)
 - [TitleKey](https://www.mediawiki.org/wiki/Extension:TitleKey)

 ### Custom namespaces

 These namespaces need to be added:

 - 3000 Locations
 - 3001 Locations_talk
 - 3002 Events
 - 3003 Events_talk

In addition, the Locations and Events namespaces need to have subpages and semantics enabled, and should be counted as content namespaces.

 ### Interwiki links

Special:Interwiki should have the following added:

Prefix: marinelives

URL: `http://www.marinelives.org/wiki/$1`

 ### Other local settings

For dumps up to and including 13 February 2024, you will need to disable parser strict mode to allow multiple assignments of properties in one semantic tag:

`$smwgParserFeatures = SMW_PARSER_INL_ERROR | SMW_PARSER_HID_CATS;`

Dumps made on or after 17 February 2024 will not need this as they no longer use multiple assignments. Extra properties are assigned using the #set parser function instead.
