# Doctate

A convention for improving citations in markdown documents using [CURIE](https://en.wikipedia.org/wiki/CURIE)s.

## Why?

Tools can help editors ensure consistent naming in documents and make global changes, eg. when an organisation changes its name.

Improving the precision of links helps with search and analysis, especially where the same text can refer to multiple things.

## Markdown

When referring to a [country][register:country], [local authority][register:local-authority-eng],
or indeed anything recorded in a [GOV.UK register](https://www.gov.uk/government/publications/registers/registers),
use the `<register-name>:<key-value>` as a [link-label](http://spec.commonmark.org/0.27/#link-label) as follows:

    [The Czech Republic][country:CZ]
    [BT Ltd][company:02216369]
    [Cabinet Office][government-organisation:cabinet-office]
    [Minister for the Cabinet Office][government-role:minister-for-the-cabinet-office]
    [Francis Maude][government-person:francis-maude]

The [shortcut reference](http://spec.commonmark.org/0.27/#shortcut-reference-link) can be a link to a human-friendly page:

    [country:CZ]: https://www.gov.uk/government/world/czech-republic
    [company:02216369]: https://beta.companieshouse.gov.uk/company/02216369
    [government-organisation:cabinet-office]: https://www.gov.uk/government/organisations/cabinet-office
    [government-person:francis-maude]: https://www.gov.uk/government/people/francis-maude 
    [government-role:minister-for-the-cabinet-office]: https://www.gov.uk/government/ministers/minister-for-the-cabinet-office

which is rendered by any markdown process as follows:

* [The Czech Republic][country:CZ]
* [BT Ltd][company:02216369]
* [Cabinet Office][government-organisation:cabinet-office]
* [Minister for the Cabinet Office][government-role:minister-for-the-cabinet-office]
* [Francis Maude][government-person:francis-maude]

The CURIEs can be used to produce [microdata](https://en.wikipedia.org/wiki/Microdata_(HTML)), [RDFa](https://en.wikipedia.org/wiki/RDFa), [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD)  and other annotations.

## Example documents

* [The Statistics and Registration Service Act 2007 (Disclosure of Revenue Information) Regulations 2015][legislation:uksi-2015-1227]

# Background

This simple idea won the ['solved problem' prize](https://twitter.com/psd/status/800394376040116224) 
at the [Accountability Hack 2016](http://accountabilityhack.org/), though much of the day was spent
exploring text mining tools and extending editors,
notably [Dillinger](http://dillinger.io/) as tools to support this way of working — see the [hackday notes](https://hackpad.com/Doctate-eNPz3vV2FrT).

[register:country]: https://country.register.gov.uk
[register:local-authority-eng]: https://local-authority-eng.register.gov.uk

[legislation:uksi-2015-1227]: store/legislation/uksi-2015-1227.md

[country:CZ]: https://www.gov.uk/government/world/czech-republic
[company:02216369]: https://beta.companieshouse.gov.uk/company/02216369
[government-organisation:cabinet-office]: https://www.gov.uk/government/organisations/cabinet-office
[government-person:francis-maude]: https://www.gov.uk/government/people/francis-maude 
[government-role:minister-for-the-cabinet-office]: https://www.gov.uk/government/ministers/minister-for-the-cabinet-office
