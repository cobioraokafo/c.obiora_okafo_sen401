# Change Management, Testing and Release

This section explains how changes to the Online Examination Management System (OEMS) are requested, reviewed, approved, tested and released. The aim is that every change is traceable, reviewed by another person, and verified before it reaches the main branch.

## 1. Change Requests

Any team member can request a change, for example a bug fix, a new feature or a documentation update. Every request is recorded as a **Jira ticket** (e.g. ETD-12) containing:

- A short title and description of the change and why it is needed
- The affected part of OEMS (e.g. exam creation, exam taking, grading, user accounts)
- A priority (Low, Medium or High)
- An assignee

Example: "ETD-12: Allow lecturers to extend the time limit of an ongoing exam."

## 2. Change Review

1. The assignee creates a Git branch named after the Jira ticket (e.g. `ETD-12`). Work is never done directly on `main`.
2. Changes are committed to that branch. Every commit message begins with the Jira key, e.g. `ETD-12 Add exam time extension option`.
3. When the work is ready, the assignee opens a **GitHub Pull Request** from the branch into `main`. The PR title includes the Jira key and the description explains what was changed.
4. The assignee requests a review from another group member, who checks the changes for correctness, consistency with other sections or modules, and clarity.

## 3. Change Approval

The `main` branch is protected. A change cannot be merged unless:

- At least **one other team member** has reviewed and approved the Pull Request
- Any review comments have been addressed

Nobody may push directly to `main` or approve and merge their own work. The group leader oversees approvals to keep contributions consistent.

## 4. Testing

Before a change is merged, it is tested on its own branch so that faults do not reach `main`. Testing for OEMS covers:

- **Functional testing:** the changed feature works as described in the Jira ticket (e.g. a lecturer can extend an exam's time and students see the new time).
- **Regression testing:** related OEMS features still work, such as logging in, starting an exam, submitting answers and viewing results.
- **Data checks:** exam submissions and grades are saved correctly and not lost or duplicated.
- **Documentation checks:** for documentation changes, the content is accurate and consistent with the rest of the SCMP.

If a test fails, the ticket stays In Progress. The fix is committed to the same branch and the Pull Request updates automatically for re-review.

## 5. Release

A change is released once it is approved and tested:

1. The Pull Request is merged into `main`.
2. The merge is recorded in GitHub history, which links the Jira key, commit, review and approver.
3. Releases of OEMS are given a version number (e.g. `v1.1.0`) as a Git tag, and the change is noted in the release notes or changelog.
4. The Jira ticket is moved to **Done** only after the Pull Request has been merged.

## 6. Ticket Status Summary

| Jira Status | Meaning |
|---|---|
| To Do | Work has not started |
| In Progress | Work has started and the working branch exists |
| Done | Work has been reviewed and the Pull Request merged into `main` |

## 7. Traceability

Each change can be traced from Jira ticket, to branch, to commits, to Pull Request, to merge into `main`. This lets the team see who made a change, why, who approved it, and when, and makes it possible to roll back a change if it causes a problem.
