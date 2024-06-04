# Consent Mode for Google Tags

## Table of Contents
- [Introduction](#introduction)
- [How Consent Mode Works](#how-consent-mode-works)
  - [The gtag() Call](#the-gtag-call)
  - [Restricting Advertising Storage](#restricting-advertising-storage)
  - [Redacting Advertising Data](#redacting-advertising-data)
  - [Restricting Analytics Storage](#restricting-analytics-storage)
- [Handling Consent Updates](#handling-consent-updates)
- [URL Passthrough](#url-passthrough)
- [Support in Google Tag Manager](#support-in-google-tag-manager)
- [Summary](#summary)

## Introduction
Consent Mode enables websites to manage how Google tags utilize cookies and process ad identifiers based on user consent. This functionality is crucial for compliance with privacy regulations.

## How Consent Mode Works
Consent Mode relies on an existing consent management system to determine user consent status. It uses the `gtag()` API to adjust tag behavior accordingly.

### The gtag() Call
The `gtag()` API is integral to Consent Mode, allowing Google tags to automatically detect and adhere to consent settings.

### Restricting Advertising Storage
By setting `ad_storage` to `'denied'`, you can prevent the creation and reading of new advertising cookies, enhancing privacy control.

### Redacting Advertising Data
Activate ads data redaction with `gtag('set', 'ads_data_redaction', true)` for additional restrictions on advertising data storage.

### Restricting Analytics Storage
Set `analytics_storage` to `'denied'` to stop Google Analytics from interacting with first-party cookies.

### Handling Consent Updates
The `update` command allows dynamic modification of consent settings, applicable across various regions.

### URL Passthrough
Enable URL passthrough with `gtag('set', 'url_passthrough', true)` to append advertising parameters to all internal links.

### Support in Google Tag Manager
Google Tag Manager partially supports Consent Mode through the `gtag()` API, but its functionality is currently limited.

### Summary
Consent Mode helps websites manage storage access for advertising and analytics tags, ensuring compliance with privacy regulations such as GDPR. It focuses on restricting storage rather than blocking requests outright.

### Resources
- [Vendor documentation](https://developers.google.com/gtagjs/devguide/consent)
- [Documentation](https://github.com/mtechraw/consent-mode-gtm/blob/main/README.md)
- [GitHub repo](https://github.com/mtechraw/consent-mode-gtm)
