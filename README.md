# Inconsistent Class Purging in Tailwind CSS

This repository demonstrates an uncommon bug in Tailwind CSS where class purging behaves inconsistently, leading to unexpected styling issues.

## Bug Description

The issue involves the purging of unused CSS classes during the build process.  Sometimes, classes that should be removed remain, causing unexpected styling or bloat. Conversely, sometimes necessary classes are removed, leading to missing styles. This inconsistency is observed across various builds, making debugging challenging.

## Reproduction

1. Clone this repository.
2. Run the build process (instructions may vary depending on your project setup).
3. Observe the inconsistencies in the generated CSS file, comparing it with the expected output based on the JavaScript code's use of Tailwind classes.

## Solution

The proposed solution addresses the class purging issue by using a more deterministic approach. This includes precisely defining purge options in your Tailwind configuration and double-checking the included and excluded paths.