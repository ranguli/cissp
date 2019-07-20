# CISSP Crib Notes
These are _very_ concise notes with sometimes only a single sentence attributed to a concept designed to jog my memory. If you stumble across this looking for study resources, use something _much_ more comprehensive!

## Computer Hardware / Architecture

### SRAM vs DRAM
- SRAM uses flip-flips or transistors to store information. It does not require constant refreshing. Faster because it doesn't have to refresh, and more expensive because it has more hardware components.
- DRAM use capacitors to store information, which leak charge. Thus they
  require refreshing.

## Networking Security

### Generic Routing Encapsulation (GRE)
- Source IP is not contained in a standard GRE. 
- GRE is a tunneling protocol that can be used to encapsulate protocols in
  packets that will be delivered by a different protocol.   
 

### Modulation Types and 802.11
- 802.11a/n/g all use Orthogonal Frequency Division Multiplexing (OFDM) which
divides a channel into multiple subcarriers, sending the wireless signal by
using multiple parallel datastreams. 
- 802.11b uses Direct Sequence Spread Spectrum (DSSS) that uses chipping codes
  to spread data across an entire frequency spectrum.

### WEP
- The main reason WEP is considered insecure is that it uses a weak 24-bit
Initialization Vecotr (IV). 
- It is sent as clear text. 
- WEP can provide 64-bit or 128-bit encryption, but it is not why it is insecure. The IV makes up most of the WEP key to provide the full 64 or 128 bits.
- WEP supports only static, preshared keys, but it is not the _main_ reason it is insecure.
### Teardrop Attack
An attacker sends several large overlapping IP fragments, which can cause the victim system to crash when it tries to reassemble them. It is considered a DoS attack.

Mnemonic: Overlapping IP fragments make computers shed a _teardrop_. 


### Smurf Attack
An attacker pings a broadcast address by sending ICMP echo request pakcets with
a forged source address. Every device that receives the ICMP ping will reply to
the forged source IP address, potentially overwhelming the source address.

### Fraggle Attack
Smurf attack but uses UDP and chargen packets instead of ICMP echo requests.

### Local Area Denial (LAND) Attack:
An attacker sens an IP packet with the same source and destinaion address and
port. When the victim with that destination address receives the packet, it can
become confused and crash.

## Security Architecture
### Bell-LaPadula Model: 
"No read up" policy and "no write down" policy to protect data confidentiality

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

### Harrison-Ruzzo-Ullman Model:
Extends the Graham Denning Model by including rights integrity.

### Lattice-based Model
Hierarchical model that defines layers of privilege.


## Secure Software Development

## Live Workloads
Simulate how the application behaves when accessed by a large number of users, providing the most accurate stress testing. It should be preferred when testing a software application.

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

### Software Engineering Institute's Capability Maturity Model (CMM):
Consists of various stages of maturity used to describe software. 
1. Initial: Security issues often addressed in a **reactive** way 
2. Repeatable: Security procedures for specific tasks have been developed but
   no organizational standard exists. Still reactive, high potential for error.
3. Defined: Unsophisticated organizational standards have been
   created/documented and implemented.
4. Managed: Formal, **proactive** process for security controls are
   implemented.
5. Optimizing: Security processes have become sophisticated. Orgainzation is
   able to adapt to changing security threats.

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

### Slack Space:
The unused space within a cluster.

### X.400
A set of directory guidelines replaced by SMTP.

### Service Account
Enabled an application to perform system-level actions.

### How to hide a spoofing attack
Use DoS

### Due Diligence
Legal liability concept that requires an organization to continually review its
practices to ensure protection requirements are met. 

### Sherwood Applied Business Security Architecture (SABSA)
Framework that creates a chain of traceability through **six** different
perspectives. Similar to the Zachmann Framework, which is an ACM based
framework.

1. Contextual
2. Conceptual
3. Logical
4. Physical
5. Component
6. Operational

SABSA works by deriving its ACM from the analysis of business security
requirements. 

Mnemonic: SABSA uses _chains_

### Zachman Framework
- **Similar to SABSA however it doesn't provide a chain of traceability**
- Six different perspectives of security design
- Zachman ACM consists of 6 columns containing **Why, How, What, Who Where and
  When.**
- 

### Phases of Incident Response:
1. **Detection** involving discovery of security incident 
2. **Response** is the process of activating the IR team
3. **Mitigation** is the process of containing the incident and preventing
   further damage.
4. **Reporting** is the process of documenting the incident to inform LEO and
   management.
5. **Recovery** is the process of returning the system to production.
6. **Remediation** involves understanding the cause and preventing it.
7. **Lessons Learned** consists of reviewing the incident to determine whether any improvements in response can be made.

D.R.M, R(P/C/M), L.L

**D**etection **R**esponse **M**itigation Re**p**orting Re**c**overy
Re**m**ediation **L**essons **L**earned.


### California Senate Bill 1386
AMong the first privacy beach notification laws in the United States.

### RADIUS Protocol:
- Remote Authentication Dial-In User Service. Combines authentication and authoriziation into a singe functional. Provides a centralized Authentication, Authorization and Accounting (AAA) services for a network.
- Less secure TACACS+.
- RADIUS uses UDP, TACACS+ uses TCP.
- RADIUS encrypts only the password.

### U.S DoD Password Requirements
- Changed every 90 days
- Must be 2 days old before being changed
- Cannot be reused until it has been changed 24 times
- At least **eight** characters long 
- Certain amount of complexity including numbers, letters and symbols.

Mnemonic: 902248

### Senior Management
- Responsible for ensuring all a company's assets (phyiscal and logical) are
  protected. 
- Whereas a Data Owner is Only responsible for ensuring a _particular information asset_ is protected.
- Whereas a Data Custodian is reponsible the _hands-on protection_ of an asset.

### Purpose of OCTAVE, PUSH, and NIST SP 800-30
Used to assess risk.

- OCTAVE establishes a four-phase framework for evaluating risk
- PUSH mathematically associates the impact of a risk event with the likelihood
  that the risk event will occur.
- NIST SP 800-30 establishes a nine step method for assessing risk.

### TACACS+
- Cisco-proprietary AAA protocol, each A is a separate function unlike RADIUS.
- More granular and flexible control than RADIUS.
- Encrypts username and passwords and the entire content of a packet.

Mnemonic: TACACS+ ACK ACKS that we should encrypt things 

### Archive Bit
- Enables backup programs to determine which files need to be backed up. When a file is created or modified, the archive bit is set so that it is included in the next backup operation. The archive bit is cleared everytime a backup is performed.


