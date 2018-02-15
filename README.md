# org.expertmedia.membership_periods
CIVICRM Module Extension
## This extension is created as a test for Compucorp application process and is not ready for production deployment

# Membership Periods
This describes how to set up one or more membership types that you can use to manage your organisation's members. It also explains the concept of membership statuses and how your organisation can use them to define a membership life-cycle.

## Installation
We would like to ask you to install a copy of Drupal 7 and CiviCRM:
### Drupal 7
You can use ([Drupal 7 Installation Guide](https://www.drupal.org/docs/7/install))
as a guide to install Drupal 7.
### For CiviCRM
You can use ([CiviCRM Installation Guide](http://wiki.civicrm.org/confluence/display/CRMDOC/Installation+and+Upgrades))
as a guide to install Drupal 7 and CiviCRM.


## The Motivation
Currently, when a membership is renewed in CiviCRM the `end date` field on the membership
itself is extended by the length of the membership as defined in CiviCRM membership type configuration
but no record of the actual length of any one period or term is recorded. As such it is not possible
to see how many “terms” or “periods” of membership a contact may have had. 

This implies that if a membership commenced on `1 Jan 2014` and each term was of `12 months`
 in length, by `1 Jan 2016` the member would be renewing for their 3rd term. The terms would be:

|Term/Period | Start Date| End Date|
|---         | ---       | ---     |
|1 | 1 Jan 2014 | 31 Dec 2015 |
|2 | 1 Jan 2015 | 31 Dec 2016 |
|3 | 1 Jan 2016 | 31 Dec 2017 |

The aim of this extension is to extend the CiviCRM membership component so that when a 
membership is created or renewed a record for the membership `period` is recorded. 

The membership period is also connected to a contribution record if a payment is taken
 for membership or renewal.

## Requirement:

Create a new CiviCRM extension that creates a new entity (inc database schema install) for the membership period. The membership period should have a start date, end date, should be linked to a membership and it should also be possible to display a linked contribution record.

Create an API for this new entity that can be used like a normal CiviCRM API.

Create new functionality that will populate the membership period when a membership record is created or updated. Use an appropriate CiviCRM approach for this (Hint : Check Civicrm Hooks. For more details on using CiviCRM hooks see ([https://wiki.civicrm.org/confluence/display/CRMDOC/Hook+Reference](https://wiki.civicrm.org/confluence/display/CRMDOC/Hook+Reference))
Create a simple but appropriate display somewhere on the contact record to show the membership periods with a link to contribution records if a payment was recorded for the renewal. We would suggest that either some modification of the display of memberships to show within each membership the periods, or failing that, a new contact tab would be acceptable.

### Write appropriate unit tests for your work wherever possible. We would advise using TDD to ensure complete test coverage.

Bonus points will be obtained by:
- Ensuring compatibility with latest CiviCRM v4.7.
- Well organised code with an appropriate structure.
- Writing good and appropriate unit tests with full coverage
- Comprehensively documenting your solution in the read me
### Submission instructions:
Upload the completed project to your Github account, and send us a link to the repository for the extension.
Please also host your completed solution on AWS free tier or similar hosting so we can review it in action as easily as possible. 

If you need more infformation on other options, refer to [the CiviCRM API](https://docs.civicrm.org/dev/en/latest/api/)

## License
Copyright © 2018 [Ekeh Chukwuemeka](https://github.com/ekeh).
Licensed under the [GNU Affero Public License 3.0](https://github.com/Ekeh/org.expertmedia.membershipperiods/blob/master/LICENSE.md/LICENSE.md)
