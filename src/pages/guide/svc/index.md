---
title: Semantic Version Checker | Commerce Testing
description: Learn how to use the Semantic Version Checker tool to test your Adobe Commerce and Magento Open Source code.
---

# Semantic Version Checker

Executing the Semantic Version Checker is a simple process, but it requires an external tool.

## Run on local changes

To run the Semantic Version Checker on local changes:

1. Clone the `magento-semver` tool to your local machine:

   ```bash
   git clone git@github.com:magento/magento-semver.git
   ```

1. Navigate to the cloned repository and run `composer install` to install the project dependencies:

   ```bash
   cd magento-semver && composer install
   ```

1. To run the Semantic Version Checker, we need one folder with the feature changes and another folder with mainline code (without changes), so you may need to clone the GitHub repository to a separate folder to perform the comparison.

1. Navigate the `magento-semver` folder and run the Semantic Version Checker compare command:

   ```bash
   bin/svc compare ../magento2-mainline ../magento2
   ```

The first parameter is the mainline code without any changes, and the second parameter is the path to the folder with your changes.
The results of the Semantic Version Checker are outputted to the console.
