# Guest-Access-Review-Clean-up

Prerequisites
Microsoft Entra tenant with Azure AD Premium P2 (Identity Governance features).

Global Admin, Identity Governance Admin, or Group Owner rights for the group you’ll review.

At least one guest user handy to test with (invite one if you haven’t already).


Step-by-Step
Jump into Identity Governance

Sign in at https://entra.microsoft.com.

Left-nav ➜ Identity Governance ➜ Access reviews.

Spin up a new review

Click + New access review.

Start with ➜ Teams + Groups 

![image](https://github.com/user-attachments/assets/ad8663fd-cecb-4345-95a4-befb16f45448)

Pick what to review

Scope → Choose Select teams + groups and pick the group you want to police or select All Microsoft 365 groups with guest users for a blanket sweep.

Review scope → Guest users only.

![image](https://github.com/user-attachments/assets/6a970a59-ca68-4108-a3bc-f8ac37060dcb)


Choose reviewers

Reviewers → Group owners (self-service) or nominate a specific person (e.g., yourself).

Automate the outcome

Auto apply results to resource → Enable.

Leave If reviewers don’t respond set to Remove (default) so silent guests get punted.

Frequency – pick Monthly (or Weekly and one time if you want it sooner).

Under End, switch from Never ➜ Occurrences.

Set Number of times = 1.
That tells Entra to open one instance and then stop the series.

Make sure Start date is today (UTC) and Duration is however many days you want to keep the task open (e.g., 1 or 3).

![image](https://github.com/user-attachments/assets/e58b8773-2c38-4c19-9ac5-b38b8647f565)

Result: a single review instance will spin up within ~15 minutes of 00:00 UTC on the start date, you’ll get the Approve/Deny task, and after it closes the series ends automatically (no further monthly runs).

![2025-04-24 19_20_11-My Access and 25 more pages - Personal - Microsoft​ Edge](https://github.com/user-attachments/assets/ac7ded86-e5f0-40cb-a561-fdfeff1fd297)

I manually Denied the unattended guest in my access review.

I navigated back to Entra to view access review detail results to view the denied user.

![image](https://github.com/user-attachments/assets/9b2b629e-9869-4a3c-9faf-54173f144376)
