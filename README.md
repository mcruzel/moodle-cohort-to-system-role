# moodle-cohort-to-system-role
Assign cohort members to a moodle role. Particulary useful for system-wide roles which can't be assigned by bulk users upload.

# Cohorts in bulk users upload

[Bulk users upload on Moodle](https://docs.moodle.org/400/en/Upload_users) allow you to assign cohort to members by csv. For this, use *cohort1*, *cohort2*... columns on your csv.

You don't need to use this script for assigning roles in courses ; you can use others methods like bulk upload enrolments. There is useful plugins for that (tool_uploadenrolmentmethods, local_mass_enroll, local_bulkenrol etc.). However, you can't use this methods for system-wide roles. This is the aim of this script.

# Moodle webservices used

This script use the following Moodle's webservices :
- core_cohort_get_cohort_members
- core_role_assign_roles

You need to create an [account] (user + password)(https://docs.moodle.org/400/en/Using_web_services) for the webservices.

# Libraries used

This script use the folliwing libraries :
- json
- requests

# Variables

You need to modify the following variables on the script (depends to your context)
- *moodle url*
- *cohortid* : the cohort (id) whose members will be added to the system role. Check the url of the cohort from the cohorts dashboard for retrieving the cohortid.
- *roleid* : the id of the role which you want to add members from the aimed cohort. Check the url of the role from the system-wide roles dashboard for retrieving the roleid.
