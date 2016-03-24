## Pull-Request Subjects

The following are examples of good subjects:

 * `CRM-12345 - Fix Paypal IPNs when moon is at half-crescent (waxing)`
 * `(WIP) CRM-67890 - Refactor SMS callback endpoint`
 * `(NFC) CRM_Utils_PDF - Improve docblocks`

A few elements to include:

 * **CRM-XXXXX** - JIRA Issues - Every issue filed in [JIRA](http://issues.civicrm.org/)
   has a unique ID. A bot will setup crosslinks between the JIRA issue and PR.
 * **Description* - Provide a brief description of what the pull-request does.
 * **(WIP)** - "Work in Progress" - If you don't feel that the changes are ready
   to be merged, include the `(WIP)` tag. This can be useful if you want to
   discuss the changes with other developers or get automated test results.
 * **(NFC)** - "Non-Functional Change" - Most patches are designed to
   change functionality (e.g. fix an error message or add a new button).
   However, some changes are non-functional -- e.g. they cleanup the
   code-style, improve the comments, or improve the test-suite.

## Review and Release Processes

TODO

## Testing

Pull-requests will be subjected to automated testing. In particular:

 * The pull-request will have a colored dot indicating its status:
   * **Yellow**: The automated tests are running.
   * **Red**: The automated tests have failed.
   * **Green**: The automated tests have passed.
 * Code-style tests are executed first. If the code-style in this patch is inconsistent, the remaining tests will be skipped.
 * The primary tests may take 20-120 min to execute. It includes the following suites: `api_v3_AllTests`, `CRM_Core_AllTests`, `Civi\AllTests`, `civicrm-upgrade-test`, and `karma`.
 * Some tests are always skipped: `CRM_AllTests`, `WebTest_AllTests`
 * If the automated test fails, click on the red dot to investigate details. Check for information in:
   * The initial summary. Ordinarily, this will list test failures and error messages.
   * The console output. If the test-suite encountered a significant error (such as a PHP crash),
     the key details will only appear in the console.
 * There are a handful of unit tests which are time-sensitive and which fail sporadically. See: https://forum.civicrm.org/index.php?topic=36964.0

For detailed discussion about these tests, see http://wiki.civicrm.org/confluence/display/CRMDOC/Testing

## Updating a pull-request

TODO
