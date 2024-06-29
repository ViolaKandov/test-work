To determine if the change on March 15, 2259, reduced the time it takes for an ally to submit the test results form after an applicant completes the underwriting tests I followed those steps

1. I had to understand the cvs (Excel files) Applicants Table: Contains personal details of the applicants
Sessions Table: Contains administrative details about the sessions and their statuses.
Events Table: Contains events related to the underwriting session, including timestamps.

2. I used python to Load the data from the provided CSV files.
then I had to tell python refer to the data dictionary to understand the fields and their meanings.
and then I convert relevant date columns to datetime objects, ensuring proper handling of time zones and handle any missing or inconsistent data.

3. Now I Identify the events that mark the completion of underwriting tests (end_of_underwriting) and the submission of test results (Ally submitted test results).
then I Merge the completion and submission events based on the session_id to align the completion and submission times for each session.
Then I had to Compute the time difference (in minutes) between the completion of the underwriting tests and the submission of the test results.
And then I Defined the change date (March 15, 2259) and Split the data into two groups: sessions completed before the change and sessions completed after the change.

4. I calculated the average time to submit the form for both periods (before and after the change).
I also Perform a t-test to statistically compare the two groups and determine if the difference is significant.

5. So based on all the tests results (p-value), conclude whether the change has significantly reduced the time to submit the test results form.
I used the following steps and found out the the changes has significantly reduced the time to submit the test results form.

1. I loaded cvs files to python using pandas
2. I defined change date
3. I filter relevant events
4. I filters relevant events
5. I merge and calculate time differences
6. I separated the data
7. I did statistical analysis to calculate the average time to submit before and after the change
