# Doctate

A convention for improving citations in [markdown](https://en.wikipedia.org/wiki/Markdown) documents using [CURIE](https://en.wikipedia.org/wiki/CURIE)s.

When referring to a [country][register:country], [local authority][register:local-authority-eng]
or indeed anything recorded in a [GOV.UK register](https://www.gov.uk/government/publications/registers/registers)
use the `<register-name>:<key-value>` as a [link-label](http://spec.commonmark.org/0.27/#link-label):

    [The Czech Republic][country:CZ]
    [Ashlyns School][school-eng:117578]
    [BT Ltd][company:02216369]
    [Cabinet Office][government-organisation:cabinet-office]
    [Minister for the Cabinet Office][government-role:minister-for-the-cabinet-office]
    [Francis Maude][government-person:francis-maude]

The displayed text can be whatever you like, as can be the [shortcut reference](http://spec.commonmark.org/0.27/#shortcut-reference-link), which can be a link to a human-friendly page:

    [country:CZ]: https://www.gov.uk/government/world/czech-republic
    [school-eng:117578]: https://www.compare-school-performance.service.gov.uk/school/117578
    [company:02216369]: https://beta.companieshouse.gov.uk/company/02216369
    [government-organisation:cabinet-office]: https://www.gov.uk/government/organisations/cabinet-office
    [government-person:francis-maude]: https://www.gov.uk/government/people/francis-maude 
    [government-role:minister-for-the-cabinet-office]: https://www.gov.uk/government/ministers/minister-for-the-cabinet-office

The text will be rendered by any markdown processor as follows:

* [The Czech Republic][country:CZ]
* [BT Ltd][company:02216369]
* [Ashlyns School][school-eng:117578]
* [Cabinet Office][government-organisation:cabinet-office]
* [Minister for the Cabinet Office][government-role:minister-for-the-cabinet-office]
* [Francis Maude][government-person:francis-maude]

## Example documents

* [The Statistics and Registration Service Act 2007 (Disclosure of Revenue Information) Regulations 2015][legislation:uksi-2015-1227]

## Why would I do this?

Tools can help editors ensure consistent naming in documents and make global changes, for example, to update the text when an organisation changes its name.

Improving the precision of links helps with search and analysis, especially where the same text can refer to multiple things.

We can write markdown processors which use the CURIEs to produce [microdata](https://en.wikipedia.org/wiki/Microdata_(HTML)), [RDFa](https://en.wikipedia.org/wiki/RDFa), [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD)  and other annotations.

## Background

This simple idea won the ['solved problem' prize](https://twitter.com/psd/status/800394376040116224) 
at the [Accountability Hack 2016](http://accountabilityhack.org/), though much of the day was spent
exploring text mining tools and extending editors,
notably [Dillinger](http://dillinger.io/) as tools to support this way of working — see the [hackday notes](https://hackpad.com/Doctate-eNPz3vV2FrT).

[register:country]: https://country.register.gov.uk
[register:local-authority-eng]: https://local-authority-eng.register.gov.uk

[legislation:uksi-2015-1227]: store/legislation/uksi-2015-1227.md

[country:CZ]: https://www.gov.uk/government/world/czech-republic
[school-eng:117578]: https://www.compare-school-performance.service.gov.uk/school/117578
[company:02216369]: https://beta.companieshouse.gov.uk/company/02216369
[government-organisation:cabinet-office]: https://www.gov.uk/government/organisations/cabinet-office
[government-person:francis-maude]: https://www.gov.uk/government/people/francis-maude 
[government-role:minister-for-the-cabinet-office]: https://www.gov.uk/government/ministers/minister-for-the-cabinet-office
