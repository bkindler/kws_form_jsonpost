
bkindler Form JSON POST Finisher
==========
#### Custom form finisher "HTTP POST Content-Type: application/json"

This TYPO3 extension adds a custom form finisher "HTTP POST Content-Type: application/json" to the TYPO3 form framework which call plain HTTP Request (POST Content-Type: application/json) to transfer data via cURL.
The transmitted Data will be generated as array from the Form Fields.

#### This version supports TYPO3
![CUSTOMER](https://img.shields.io/badge/11_LTS-%23A6C694.svg?style=flat-square)
![CUSTOMER](https://img.shields.io/badge/12_LTS-%23A6C694.svg?style=flat-square)

#### Composer support
`composer req bkindler/kws-form-jsonpost`

***

## Install
Copy the extension folder to `\typo3conf\ext\ `, upload it via extension
manager or add it to your composer.json.

***

## Usage
1. Add Finisher "HTTP POST/GET" to your form
2. Set target URL in the finisher
3. Optional: Set username/password in the finisher if authentication is required
4. Optional: Set additional variables that are needed (e.g: optinSetupId for MailingWork)
5. Optional: Activate "Convert field key to integer" if target needs keys to be integer
   * id must be included in identifier
   * (hidden) honeypot key could not be converted -> may need to be disabled in the form.yaml
6. The transmitted Form Data will be generated automatically as array from the Fields identifier as key and value as value
- for Testing https://webhook.site could be used

***

## Update & Migration from hive_facts
1. notice finisher settings from HTTP POST Finisher (hive_form_post)
2. remove HTTP POST Finisher (hive_form_post)
3. in composer.json replace `beewilly/hive_form_post` with `"teufels/tt3-form-post":"^1.0"`
4. Composer update
5. add HTTP POST Finisher (tt3-form-post) using noted settings

***

## Update & Migration from [ ṯeufels ] Form POST Finisher
1. add HTTP JSON POST Finisher (kws-form-jsonpost) using noted settings

***


## Customization
- tbd.

***

## Documentation
- tbd.

***

## Changelog
### [1.0.1] - 2024-10-09
- - intial from [tt3-form-post](https://bitbucket.org/teufels/tt3-form-post/src/) `release/v12`

