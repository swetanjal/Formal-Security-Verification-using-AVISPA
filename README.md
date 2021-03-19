# Team 4

- Swetanjal Dutta - 20171077
- Paryul Jain - 20171083
- Eesha Dutta - 20171104
- Meghana Bommadi - 20171165

### Paper Title: 

On the Design of Blockchain-Based Access Control Scheme for Software Defined Networks

### Objective of the protocol being verified:

Establish shared secret key between Controller and Switch.

### Roles:
- Registration Authority
- Controller
- Switch

### Protocol is secure against:

1. Replay Attack:
To protect replay attack, we have utilized
both the random numbers along with current system times-
tamps. Therefore, the old replayed messages can be easily
detected by the respective recipients by checking the times-
tamps attached in the received messages. Thus, the proposed
BACC-SDN is resilient against “replay attack”.

2. Spoofing Attack:
This attack takes place when a malicious switch impersonates a legitimate switch.
Assume adversary A controlling SSW_p first
eavesdrops all the communication messages msg 1 = {Conid, Swiid , Certcon , Acon , Bcon , TS1} and msg 2 = {Conid, Swiid, Certswi, Aswi, SKVSwiCon, TS2}. A may attempt to
construct Aswi and SKVSwiCon from the eavesdrop messages
to impersonate SSW_j in the consecutive sessions. However, to
construct valid Aswi and SKVSwiCon, A requires the knowledge of {fcon-swi (Conid , Swiid ), r1 , r2}.
We know that fcon-swi is a hash function known only to the legitimate controller and switch. r1 and r2 are not sent in the clear rather they are present inside a hash function, making them hard to be guessed. Hence, BACC-
SDN resists spoofing attack.

3. Man in the middle attack:
In this attack, an adversary
A may capture the access control request message msg 1
from public channel, and try to tamper the request message and generate another valid message Msg 1. Without knowing the credentials fcon−swi(Conid, Swiid) and r1, A cannot compute the different values Acon and Bcon. Similarly, for message msg2, without knowledge  of the credentials fcon-swi(Swiid, Conid) and r2, A cannot also compute valid
Aswi and SKVSwiCon. Hence, BACC-SDN is not prone to
man-in-the-middle attack.

