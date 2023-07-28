# wiki-dumps
This folder provides dumps of the entire [By The Sword Linked](https://www.bytheswordlinked.uk/) wiki.

Data files available are as follows:

- by-the-sword-linked-RDF-dump.rdf.zip: all semantic properties from the wiki exported as OWL DL serialized as RDF/XML. This does not include free text or non-semantic template parameters. Has to be zipped otherwise it's too big to upload to Github.
- by-the-sword-linked-Wikitext-dump.xml.zip: the wikitext source code of every page in the wiki exported as [wikitext XML](https://www.mediawiki.org/wiki/Help:Export#Export_format). Has to be zipped otherwise it's too big to upload to Github.
- by-the-sword-linked-Wikitext-Structure.xml: the wikitext source code of every page in the following namespaces: Property, Template, Form, Category, Help. This gives the data structures of the wiki without the content.

Some of the wiki templates rely on tag extensions that have not yet been released to the public.

For more information about the project and data, see:

- [Introductory blog post](https://bytheswordlinked.hcommons.org/2019/02/26/introduction/) explains the aims and scope of the project.
- [Help:Create a page](https://www.bytheswordlinked.uk/wiki/Help:Create_a_page) gives an overview of the basic entity types.
- [Help:Data structures](https://www.bytheswordlinked.uk/wiki/Help:Data_structures) gives more details of the semantic properties and how they are used by each entity type.
- [Help:Dates](https://www.bytheswordlinked.uk/wiki/Help:Dates) explains how the project handles the difference between the Julian and Gregorian calendars.
- [Project:Progress](https://www.bytheswordlinked.uk/wiki/Project:Progress) gives an overview of what is and isn't included in the data.

The data includes data reused from the following sources under the following licences, which legally require attribution:

- [Open Government Licence](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/):
    - [The National Archives of the UK](https://www.nationalarchives.gov.uk/)
    - [National Records of Scotland](https://www.nrscotland.gov.uk/)
    - [Ordnance Survey of Great Britain](https://www.ordnancesurvey.co.uk/business-government/tools-support/open-data-support)
    - [Natural England](https://data.gov.uk/dataset/21104eeb-4a53-4e41-8ada-d2d442e416e0/national-character-areas-england)
    - [Natural Resources Wales](https://data.gov.uk/dataset/10ba5624-bc9c-47ec-9bfa-69a46620b23d/national-landscape-character-areas-nlca)
- Creative Commons Attribution licence:
    - [British Library EThOS thesis metadata](https://doi.org/10.23636/ybpt-nh33)
- not formally licensed but effectively same as CC-BY:
    - [Wikishire](http://wikishire.co.uk/lookup/)
    - [Historic County Borders Project](http://www.county-borders.co.uk/)
