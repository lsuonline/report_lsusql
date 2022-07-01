# LSU Report API (Formerly AD-hoc database queries)

This report plugin allows Administrators to set up arbitrary database queries
to act as LSU API Reports. Reports can be of two types, either run on demand,
or scheduled to run automatically. Reports can be grouped into categories,
which helps when you have a lot of them.

Other users with the right capability can go to Administration -> Reports ->
LSU Report API and see a list of queries to which they have access.
Results can be viewed on-screen, downloaded as CSV, or consumed via webservice
in any supported data format.

Reports can contain administratively configurable placeholders, in which 
case, the user running the report is presented with a form where they can 
enter the values to substitute for the placeholders before running the report.

Scheduled reports can also be set to be send out be email whenever they are
generated.

If a column has a name ending in `date` and contains integer values, then they
will be assumed to be unix timestamps, and formatted as dates. If a query
placeholder has a name ending in `date`, then users will be give a date-time
selector to input the value of that parameter.

Pairs of columns where one is called `name`, and the other called `name_link_url`
will be displayed as a single column containing links with link text from
`name` and the target URL from `name_link_url`.

You can set a limit on the maximum number of rows returned by a query up 
to an administratively configured hard limit.

See http://docs.moodle.org/en/Custom_SQL_queries_report for more information.


## Acknowledgements

This plugin was created by the Open University (http://www.open.ac.uk/), but now
has contributions from many others, as can be seen in the git log. Thanks all.

The forked version was created by Louisiana State University (https://www.lsu.edu/)
and adds the following features.
1. Per report user access
1. Per report settings for unescaped content for consumable use
1. Global settings to add more prohibited word replacements for consumable use

Coupling the new features with API creates a powerful automated integrations tool.


## Installation and set-up

This plugin should be compatible with Moodle 3.9+.

