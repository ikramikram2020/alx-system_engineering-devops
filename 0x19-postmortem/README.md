### Postmortem :

#### Issue Summary

- **Duration**:
  - **Start**: August 13, 2024, 10:00 AM (UTC)
  - **End**: August 13, 2024, 12:00 PM (UTC)
- **Impact**:
  - The website was completely down for 2 hours.
  - Users saw a 404 error page and couldn’t access the site.
  - Around 70% of users were affected by this downtime.
- **Root Cause**:
  - The issue was caused by incorrect DNS records. The DNS records were outdated due to a recent server change, making the website unreachable.

#### Timeline

- **10:00 AM (UTC)**: The issue was first detected by a monitoring alert that indicated the website was down.
- **10:05 AM (UTC)**: An engineer on call saw the alert and confirmed that the website was not accessible.
- **10:10 AM (UTC)**: The team started investigating and found that the DNS records might be the problem.
- **10:30 AM (UTC)**: The initial assumption was that the issue was related to server configuration, but this was not correct.
- **10:45 AM (UTC)**: Further investigation showed that the DNS records were pointing to an old IP address.
- **11:00 AM (UTC)**: The team updated the DNS records with the correct IP address.
- **11:15 AM (UTC)**: The website started working again for users once the DNS changes took effect.
- **12:00 PM (UTC)**: The incident was fully resolved, and normal service was restored.

#### Root Cause and Resolution

- **Root Cause**:
  - The website's DNS records were outdated because they had not been updated after a recent server migration. This misconfiguration caused the website to be unreachable to users.
- **Resolution**:
  - The DNS records were corrected to point to the new server's IP address. Once the changes were made and propagated, users were able to access the website again.

#### Corrective and Preventative Measures

- **Improvements**:
  - Implement automated checks to verify DNS configurations are updated correctly after any server changes.
  - Set up enhanced monitoring to detect DNS-related issues earlier.
- **Tasks**:
  - Create and implement automated DNS configuration checks.
  - Develop a checklist for updating DNS records during server migrations.
  - Add alerts for potential DNS configuration problems.
  - Regularly review and test the DNS configuration process to ensure accuracy.

