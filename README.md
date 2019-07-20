# CISSP Crib Notes

## Security Architecture
### Bell-LaPadula Model: 
"no read up" policy and "no write down" policy to protect data confidentiality

### Biba Model: 
Basically opposite of Bell-LaPadula. Has "no read down" and "no write up" policy to protect data integrity.

### Lipner Model: 
Combines elements of Bell-LaPadula and Biba. Can use Bell-LaPadula alone to
protect confidentiality, or can be combined with Biba to preserve
confidentiality and integrity.

### Chinese Wall / Brewer Nash Model:
Designed to mitigate conflicts of interest. Uses conflict of interest
categories to mitigate security risks

### Graham Denning Model:
Uses access controll matrix (ACM) to map subjects and objects to a series of
rules:

- Create/delete objects and subjects
- Read, grant, delete and transfer access

### harrison-Ruzzo-Ullman Model:
Extends the Graham Denning Model by including rights integrity.


## Secure Software Development

### Static Testing:
Includes walkthroughs, sanity checks, syntax checks, and logical code reviews.
Static testing is passive, code is not run.

### Dynamic Testing:
Tests the code while it is executing.

### Black Box Testing:
No source code is provided. Expects tester to find a problem the same way a
consumer might.

### White Box Testing
Provides source code, documentation, etc to the tester.


## Misc:
### ISC2 Code of Ethics:
- 1. Protect society, the common good, necessary public trust, and the
     infrastructure.
  - This canon expects you to promote good security practices to the public,
    and improve upon the security infrastructure for the benefit of the public.
- 2. Act honorably, justly, responsibly and legally
- 3. Provide dilligent and competent service to principals.
- 4. Advance and protect the profession.
  - This includes not developing professional relationships with individuals or
    organizations who could hurt the profession.

If you must choose between "acting honorably, justly, responsibly and legally"
and "advancing and protect the profession", choose the former.

### Slack Space on a Disk:
The unused space within a cluster.

### X.400
A set of directory guidelines replaced by SMTP.

### Service Account
Enabled an application to perform system-level actions.

### How to hide a spoofing attack
DoS
