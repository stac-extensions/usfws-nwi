# USFWS NWI Extension Specification

- **Title:** U.S. Fish & Wildlife Service (FWS) National Wetlands Inventory (NWI)
- **Identifier:** <https://stac-extensions.github.io/usfws-nwi/v1.0.0/schema.json>
- **Field Name Prefix:** fws_nwi
- **Scope:** Item, Collection
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/extensions/README.md#extension-maturity):** Proposal
- **Owner**: @m-mohr

This document explains the U.S. Fish & Wildlife Service (FWS) National Wetlands Inventory (NWI) Extension to the
[SpatioTemporal Asset Catalog](https://github.com/radiantearth/stac-spec) (STAC) specification.
See <https://www.fws.gov/program/national-wetlands-inventory> for details.

- Examples:
  - [Item example](examples/item.json): Shows the basic usage of the extension in a STAC Item
  - [Collection example](examples/collection.json): Shows the basic usage of the extension in a STAC Collection
- [JSON Schema](json-schema/schema.json)
- [Changelog](./CHANGELOG.md)

## Fields

The fields in the table below can be used in these parts of STAC documents:
- [ ] Catalogs
- [x] Collections
- [x] Item Properties (incl. Summaries in Collections)
- [x] Assets (for both Collections and Items, incl. Item Asset Definitions in Collections)
- [ ] Links

| Field Name         | Type      | Description                                                  |
| ------------------ | --------- | ------------------------------------------------------------ |
| fws_nwi:state      | string    | **REQUIRED**. The applicable US state (long name). One of the [allowed values](#allowed-values) below. |
| fws_nwi:state_code | string    | **REQUIRED**. The applicable US state (short code). One of the [allowed values](#allowed-values) below. |
| fws_nwi:content    | \[string] | **REQUIRED**. The content published in this Item. A set of the following allowed values: `historic_wetlands`, `riparian`, `wetlands` |

### Allowed Values

| `fws_nwi:state_code` | `fws_nwi:state`                |
| -------------------- | ------------------------------ |
| AL                   | Alabama                        |
| AK                   | Alaska                         |
| AZ                   | Arizona                        |
| AR                   | Arkansas                       |
| CA                   | California                     |
| CO                   | Colorado                       |
| CT                   | Connecticut                    |
| DE                   | Delaware                       |
| DC                   | District of Columbia           |
| FL                   | Florida                        |
| GA                   | Georgia                        |
| HI                   | Hawaii                         |
| ID                   | Idaho                          |
| IL                   | Illinois                       |
| IN                   | Indiana                        |
| IA                   | Iowa                           |
| KS                   | Kansas                         |
| KY                   | Kentucky                       |
| LA                   | Louisiana                      |
| ME                   | Maine                          |
| MD                   | Maryland                       |
| MA                   | Massachusetts                  |
| MI                   | Michigan                       |
| MN                   | Minnesota                      |
| MS                   | Mississippi                    |
| MO                   | Missouri                       |
| MT                   | Montana                        |
| NE                   | Nebraska                       |
| NV                   | Nevada                         |
| NH                   | New Hampshire                  |
| NJ                   | New Jersey                     |
| NM                   | New Mexico                     |
| NY                   | New York                       |
| NC                   | North Carolina                 |
| ND                   | North Dakota                   |
| OH                   | Ohio                           |
| OK                   | Oklahoma                       |
| OR                   | Oregon                         |
| PacTrust             | Pacific Trust Islands          |
| PA                   | Pennsylvania                   |
| PRVI                 | Puerto Rico and Virgin Islands |
| RI                   | Rhode Island                   |
| SC                   | South Carolina                 |
| SD                   | South Dakota                   |
| TN                   | Tennessee                      |
| TX                   | Texas                          |
| UT                   | Utah                           |
| VT                   | Vermont                        |
| VA                   | Virginia                       |
| WA                   | Washington                     |
| WV                   | West Virginia                  |
| WI                   | Wisconsin                      |
| WY                   | Wyoming                        |

## Contributing

All contributions are subject to the
[STAC Specification Code of Conduct](https://github.com/radiantearth/stac-spec/blob/master/CODE_OF_CONDUCT.md).
For contributions, please follow the
[STAC specification contributing guide](https://github.com/radiantearth/stac-spec/blob/master/CONTRIBUTING.md) Instructions
for running tests are copied here for convenience.

### Running tests

The same checks that run as checks on PR's are part of the repository and can be run locally to verify that changes are valid. 
To run tests locally, you'll need `npm`, which is a standard part of any [node.js installation](https://nodejs.org/en/download/).

First you'll need to install everything with npm once. Just navigate to the root of this repository and on 
your command line run:
```bash
npm install
```

Then to check markdown formatting and test the examples against the JSON schema, you can run:
```bash
npm test
```

This will spit out the same texts that you see online, and you can then go and fix your markdown or examples.

If the tests reveal formatting problems with the examples, you can fix them with:
```bash
npm run format-examples
```
