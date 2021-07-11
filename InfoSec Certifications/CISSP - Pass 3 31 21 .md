# CISSP - Pass 3/31/21

**Ivan CISSP Active Recall Notes | Q1 2021**

*Total Questions: 243*

- **Domain 1: Security and Risk Management |** 31: 1, 2, 3

    *CORE:*

    - What is security and risk management?

        CIA, Security Governance & Risk mgmt issues, legal, regulatory, and compliance environment impacting security professionals, security policies and education framework

    - What are the goals of InfoSec?
        - CIA Triad
            - Protect info and systems from unauthorized access
                - Compromised by disclosure attacks
            - Protect info and systems from unauthorized modifications
                - Compromised by alteration attacks
            - Ensure that info and systems are available for authorized users when needed
                - Compromised by denial attacks
    - What are examples of confidentiality controls?
        - Access controls restrict users from accessing sensitive information without permission
        - Encryption protects information at rest or in transit
        - Steganography hides info within images or other files
    - What are examples of integrity controls?
        - Sources of integrity failures: intentional alteration, user error, software or hardware error, acts of nature
        - Hashing: hash functions create message digests for large files
            - Changes in hash values indicate changes in the underlying file
            - Foundation for Digital Signatures - which help with non-repudiation
                - Creating and verifying a digital signature: compute the hash value of a message > encrypt the hash with the sender’s private key > decrypt the signature with the sender’s public key > compute the hash value of the message > compare the values from steps 1 & 2
                - Digital signatures can also be used to create digital certificates > used to transmit public keys securely
    - What are examples of availability controls
        - Failure causes: malicious attackers, component failures, application failures, utility failures
        - Redundant components: protect a system against failure of a single part
        - High availability (HA): protect services against the failure of a single server
        - Fault tolerance: protect services against disruption from a small failure
        - OS and app patching also enhance availability

    *Security Governance:*

    - What is aligning security with the business?
        - Security leader: serves as SME on issues of CIA
        - Business leader: understand the mission, goals, and objectives of the broader organization
        - Security pros must balance security with business needs
        - **!! watch out for questions that try to trick you into making unbalanced decisions/only wearing the security hat**
        - Administrative tasks are important contributions to the business
    - What are organizational processes?
        - Security governance
            1. Info governance committee
            2. Risk mgmt committee
            3. Board of directors
        - Ensure governing bodies understand risk and controls > find a security governance model that fits your org
        - Corporate acquisitions require integration of controls > eliminate redundancies and ensure compatibility
        - Corporate divestitures require separation of controls
    - What are control frameworks?
        - Help to guide security program design
        - Control objectives for IT (COBIT): business control framework
        - ISO 27001: part of a series of business standards
        - NIST 800-53: mandatory for federal agencies

    *Compliance & Ethics:*

    - What is legislative & regulatory compliance?
        - Compliance obligations:
            1. Criminal law - deter and punish acts detrimental to society
            2. Civil law - resolve disputes
            3. Administrative law - facilitate effective government
            4. Private regulations - flow from contractual relationships
    - What is privacy compliance & regulations?
        - HIPAA - Health Insurance Portability & Accountability Act
            1. Covers providers, insurers, and information clearinghouses
        - FERPA - Family Educational Rights & Privacy Act
            1. Regulates handling of student educational records
        - GLBA - Gramm Leach Bliley Act
            1. Regulates financial institutions
        - COPPA - Childrens Online Privacy Protection Act
            1. Protects privacy of children under 13
        - Privacy act of 1974
            1. Applies to federal government agencies
        - GDPR - General Data Protection Regulation
            1. European privacy law > processing must be lawful transparent and fair
            2. Data must be collected for specific, legitimate purposes
            3. Collect the minimum amount of data to fulfill business purpose
            4. Ensure the accuracy of info
            5. Delete info when no longer needed
            6. Protect security of personal info
    - What are computer crimes & regulations?
        - CFAA - computer fraud and abuse act
            1. Prohibits unauthorized access to computer systems
            2. Prohibits the creation of malicious code
        - ECPA - electronic communications privacy act
            1. Restrict government interception of communication
        - ITADA - Identity theft and assumption deterrence act
            1. Makes identity theft a federal crime
    - What are software licensing agreements?
        - Agreement types:
            1. Negotiated contracts
            2. Click-through agreements
            3. Shrink-wrap agreements
    - What is intellectual property?
        - Copyrights - protect creative works
            1. Granted to the creator automatically
            2. Provided for 70yrs beyond creators death
        - Trademarks - protect words and symbols
            1. Granted upon registration
            2. Provided for renewable 10-yr periods
            3. Granted contingent upon active use in commerce
        - Patents - protect inventions
            1. Requirements: novelty, usefulness, nonobviousness
            2. Generally last for 20 years
            3. Patents require public disclosure of the invention
            4. Trade secrets offer an alternative to patent protection
        - Trade secrets
    - What are import & export controls?
        - Export controls - restrict flow of goods and data
            1. ITAR (international traffic in arms regulations) - cover “defense articles”
            2. EAR - export administration regulations - cover “dual use” technologies
            3. OFAC - office of foreign asset control - cover sanctioned countries
    - What are data breaches?
        - Common PII elements: SSNs, drivers license numbers, bank account numbers
        - Organizations must generally notify victims and government officials of a breach
        - **!! many data breach notification laws include exemptions for encrypted information**
    - What are ethics, per ISC2?
        - Protect society, the common good, necessary public trust and confidence, and the infrastructure
        - Act honorably, honestly, justly, responsibly and legally
        - Provide diligent and competent service to principles
        - Advance and protect the profession
        - **!! ISC2 members are required to report breaches of the Code of Ethics to ISC2 for investigation**

    *Security Policy:*

    - What is a security policy framework?
        - Policies > standards > guidelines > procedures
        - Policies provide the foundation for a security program, are written carefully over a long period of time, require compliance from all employees, are approved at the highest levels of the org
        - Standards provide specific details of security controls, derive their authority from policies, follow a less rigorous approval process, compliance required from employees
        - Guidelines provide security advice to the org, follow best practices for industry, suggest optional practice (not mandatory)
        - Procedures outline step-by-step process for an activity, may require compliance, depending on the circumstances
        - **!! policies and standards are mandatory, guidelines are optional, procedures can be either.**
    - What examples of security policies?
        - Factors affecting security policy:
            1. Culture of the org, industry, regulatory environment
        - Common policies:
            1. Infosec policy
                - Designation of individual responsible for security
                - description of security roles and responsibilities
                - Authority for creation of security standards
                - Authority for incident response
                - Process for policy exceptions and violations
            2. Privacy policy
            3. Acceptable use policy
                - Aka responsible use policy
                - Describe how individuals may use information systems
                - Prohibits illegal activity
                - Describes what personal use is permitted
                - Least privilege - assign users only the minimum set of permissions necessary for their jobs
                - Separation of duties - prevents users from simultaneously holding two conflicting permissions
                - Mandatory vacation - force privileged users to take one or two weeks of consecutive vacation annually
                - Job rotation - rotate users in and out of positions with sensitive responsibilities

    *Business Continuity:*

    - What is BCP?
        - A set of controls designed to keep a business running in the face of adversity, whether natural or man-made
        - Defining BCP scope: business activities, systems, controls
        - Business impact assessment (BIA) - risk assessment that identifies and prioritizes risk
    - What are BCP controls?
        - Redundancy protects against the failure of a single component
        - Single point of failure analysis - identifies and removes (SPOFs), SPOF analysis continues until the cost of addressing risks outweighs the benefit
        - IT contingency scenario examples:
            1. Sudden bankruptcy of key vendor
            2. Insufficient storage or compute capacity
            3. Failure of utility service

            Remember to perform succession planning for as well!

    - What is HA and FT?
        - HA - uses multiple systems to protect against service failure
        - FT - makes a single system resilient against technical failures
        - Load Balancing - spreads demand across systems
        - Common points of failure:
            1. Power supply, storage media
        - Redundant Array of inexpensive disks (RAID)
            1. RAID 1 - disk mirroring: stores the same data on two different disks
            2. RAID 5 - disk striping with parity: uses 3 or more disks to store data and parity information
            3. **!! know that disk mirroring requires two disks while disk striping with parity requires three**
            4. **!! RAID is a fault tolerance technique, NOT a backup strategy**
        - Network quality of service (QoS) - provides critical services with protected network capacity

    *Personnel Security:*

    - What are ways to improve personnel security and why is it important?
        - **Improving personnel security**
            - Your security program should be built upon a solid policy foundation
            - Handle policy violations carefully!
            - What use of personal resources is acceptable on corporate networks and with corporate data?
            - Education is the best defense against social engineering attacks
            - The insider threat is significant - 25%
                1. Insider threat defense: background investigation, monitoring, manager training, data loss prevention (DLP)
        - **Security in the hiring process**
            - Pre Employment screening checks the background of potential employees
                1. Criminal records checks, sex offender registry, reference checks, education and employment verification, credit checks
            - Employment agreements: NDAs, asset return agreements
        - **Employee termination process**
            - Every employee eventually leaves the organization
            - Revoke access promptly but not prematurely
            - Retrieve organization property
        - **Employee privacy**
            - Minimization - collect minimal info and store it only as long as needed
            - Limited access - as few employees as possible should have access
            - Use encryption (cryptography to render info unreadable without the necessary decryption key) and data masking (removes portions of sensitive info to reduce its sensitivity
        - **Social networking**
            - Use multifactor authentication

    *Risk Management:*

    - What is a risk assessment?
        - Identifies and prioritizes risks
        - Key terms:
            1. Threat: external force jeopardizing security
                - **!! threat vectors are the specific methods that threats use to exploit a vulnerability**
            2. Vulnerability: weaknesses in security controls
            3. Risks: the combination of a vulnerability and a corresponding threat
        - Prioritize risks by likelihood and impact
            1. Likelihood: probability that a risk will occur
            2. Impact: amount of expected damage
        - Qualitative risk assessment: uses subjective ratings to evaluate risk likelihood and impact (low, medium, high)
        - Quantitative risk assessment: use objective numeric ratings to evaluate risk likelihood and impact
    - What is a quantitative risk assessment & what are the key formulas and metrics to consider?
        - Perform quant risk assessment for a single risk and asset pair
        - Asset value (AV) - estimate value of the asset in dollars
        - Exposure factor (EF) - expected % of damage to an asset
        - Single-loss expectancy - cost of damage if it happens once: AV * EF = SLE
        - Annualized rate of occurrence (ARO) - number of times a risk is expected to occur each year
        - Annualized loss expectancy (ALE) - expected dollar loss from a risk in any given year, SLE * ARO = ALE
        - **!! be prepared to work through a quantitative risk assessment calculation on the exam**
        - MTTF (mean time to failure) - mean time to failure: average time a nonrepairable component will last
        - MTBF (mean time between failures) - average time gap between failures of a repairable component
        - MTTR (mean time to repair) - average time required to return a repairable component to service
    - What are the 5 risk management actions?
        - Risk avoidance - changes the organizations business practices
        - Risk transference - shifts the impact of a risk to another organization
        - Risk mitigation - reduces the likelihood or impact of the risk
        - Risk acceptance - accepts the risk without taking further action
        - Risk deterrence - take actions that dissuade a threat from exploiting a vulnerability
    - How would you describe security control selection and implementation?
        - Security controls are the procedures and mechanisms that an organization puts in place to manage security risks
        - Defense in depth - multiples controls for one objective
        - We categorize controls by their purpose or mechanism of action
        - Purpose:
            1. Preventive - stop security issue from occuring in the first place
            2. Detective - identify that a potential security issue has taken place
            3. Corrective - remediate security issues that have already occurred
        - Action:
            1. Technical - use technology to achieve security control objectives
            2. Operational - use human-driven processes to manage technology in a secure manner
                - **!! technical controls are implemented by technology; operational controls are implemented by people**
            3. Management / administrative - improve the security of the risk mgmt process itself
        - False positive errors - occur when a control inadvertently triggers when it should not
        - False negative errors - occur when a control fails to trigger in a situation where it should

    *Threat Modeling:*

    - How are threats identified and how does TM help?
        - **Identifying threats**: Use a structured approach to threat mgmt
            - 1. Asset focus - use the asset inventory as the basis for the analysis
            - 2. Threat focus - identify how specific threats may affect each info system
            - 3. Service focus - identify the impact of various threats on a specific service
        - **Understanding attacks**
            - STRIDE model categorizes attacks
                1. S - spoofing
                2. T - tampering
                3. R - repudiation
                4. I - information disclosure
                5. D - denial of service (DOS)
                6. E - elevation of privilege / privilege escalation
            - Diagramming attacks > reduction analysis: breaks down a system down into smaller components, helps simplify complex systems for security reviews
        - **Technology and process remediation**
            - Threat modeling should prompt periodic reviews of the security infrastructure
            - Threat modeling should inform the rest of the security program

    *Vendor Management:*

    - How should you manage vendor relationships?
        - **Managing vendor relationships**
            - Ensure that vendor security policies are at least as stringent as your own
            - Steps: vendor selection > onboarding > monitoring > offboarding
    - What are vendor agreements?
        - Service-level requirement (SLR) - document specific requirements that a customer has about any aspect of a vendors service performance
            1. Examples: system response time, service availability, data preservation, etc
            2. Document SLRs in a service-level agreement (SLA)
        - Memorandum of understanding (MOU)
        - Business partnership agreement (BPA)
        - Interconnection security agreement (ISA)
        - Include security requirements in SLRs, SLAs, and other agreements
        - Security and compliance terms:
            1. Document security and compliance requirement facilitate customer monitoring of compliance, ensure the right of audit and assessment
        - **Vendor information mgmt**
            - Agreements should contain cleat data ownership language
            - Agreements should limit data sharing with third parties
            - Agreements should include data protection provisions
    - What are third-party security services?
        - **Third-party security services**
            - Managed security service providers (MSSPs): provide security services for other orgs as a managed service > must be carefully monitored
                1. Can manage an entire security infrastructure, monitor system logs, manage firewalls and networks, IAM
                2. MSSP relationships should be carefully documented

    *Awareness & Training:*

    - What is Security policy training and procedures?
        - Security training: provides users with the knowledge they need to protect the orgs security
        - Security awareness: keeps the lessons learned during security training
        - Training Methods:
            1. Classes, integration with orientations, online providers, vendor-provided classroom training
        - Customize training based upon user roles
        - Review training materials regularly to ensure relevance
    - What is Compliance training?
        - Ensure that an orgs infosec controls are consistent with the laws, regs, and standards that govern the orgs activities
        - Include compliance obligations in security training
        - Begin compliance efforts with a gap analysis
        - **User habits**
            - Passwords, clean desk policy, physical security (tailgating), BYOD policies, social media and peer-to-peer networks
        - **Awareness program reviews**
            - 1. training
            - 2. education
            - 3. Awareness
            - Verity that the amount of training, education, and awareness is appropriate for each employee
- **Domain 2: Asset Security |** 10: 1,1

    *Data Security:*

    - What is data security?
        - **Understanding data security**
            - Data at rest: data stored for later use
            - Data in motion: data being sent over a network between two systems
            - Data Security Controls:
                1. Clear policies and procedures covering data use and security
                2. Encryption to protect sensitive info
                3. Access controls on stored data
            - Big Data: the use of datasets much larger than those that may be handled by conventional data processing and analytic techniques (instead of typical relational DBs, will utilize new tech lik nosql)
                1. Requires special security consideration
    - What are data security policies?
        - Policy criteria
            1. Foundational authority for data security efforts
            2. Clear expectations for data security responsibilities
            3. Guidance for requesting access to information
            4. Process for granting policy exceptions
        - Data classification policies: describe security levels
            1. Military: top secret > secret > confidential > unclassified
            2. Business: highly sensitive > sensitive > internal > public
        - Data storage policies (protects data at rest): describe appropriate storage locals, access control requirements, encryption requirements
        - Data transmission policies (protects data in motion): describes appropriate data transmissions, encryption requirements, acceptable transmission mechanisms
        - Data lifecycle policies: describe end-of-life for data
            1. Data retention policies: specify the minimum and/or max periods that an org will retain different data elements
            2. Data disposal policies: describe proper techniques for destroying data that is no longer needed by the org
    - What are data security roles?
        - Data owner: business leaders with overall responsibility for the data, set policies and guidelines for their data sets
        - Data steward: handle the day-to-day data governance activities, they are delegated responsibility by data owners
        - Data custodian/processor: store and process information, and are often IT staff members
        - Data owners and processors bear responsibility for data privacy
        - **!! system ownership and data ownership are two different concepts**
    - What is data privacy?
        - The 10 Generally Accepted Privacy Principles (GAPP)
            1. 1. Management - orgs handling private info should have policies, procedures, and governance structures in place to protect privacy
            2. 2. Notice - data subjects should receive notice that their info is being collected and used, as well as access to the privacy policies and procedures followed by the org
            3. 3. Choice and consent - the org should inform data subjects of their options regarding the data they own and get consent from those individuals for the collection, storage, use, and sharing of that info
            4. 4. Collection - the org should only collect personal info for purposes disclosed in their privacy notices
            5. 5. Use, retention, and disposal - orgs should only collect and use personal info for disclosed purposes and they should dispose of the data securely as spoon as it is no longer needed for the disclosed purpose
            6. 6. Access - orgs should provide data subjects with the ability to review and update their personal info
            7. 7. Disclosure to 3rd parties - orgs should only share info with 3rd parties if that sharing is consistent with the purposes disclosed in privacy notices and they have the consent of the individual to share that info
            8. 8. Security - the org must secure private info against unauthorized access, either physically or logically
            9. 9. Quality - the org should take reasonable steps to ensure that the private info they maintain is accurate, compete, and relevant
            10. 10. Monitoring and enforcement - the org should have a program in place to monitor compliance with its privacy policies and provide a dispute resolution mechanism
    - How do you limit data collection?
        - Notice and consent is just the first level of restriction on data collection
        - Never collect undisclosed info, even if it seems “incidental”
        - Minimize information collected - delete unneeded information quickly
        - Ensure that your data collection practice are fair and lawful
        - Monitor third parties - verify their privacy practices

    *Data Security Controls:*

    - What are security baselines?
        - **Developing security baselines**
            - Baseline security standards describe minimum requirements
            - Elements:
                1. Administered by a named individual
                2. Protected against unauthorized access
                3. Does not jeopardize other systems or data
                4. Remains under positive control
                5. Complies with data security requirements
            - Baselines are generic - they cover an uncertain future
            - Baselines may include specific requirements for handling different categories of information
            - Specific security standards for:
                1. Operating systems
                2. Mobile devices
                3. Network infrastructure components
                4. Appliances
            - System configuration managers automate policy deployment
            - Monitoring is critical - watch for baseline deviations
    - How can you leverage industry standards and customize security standards?
        - **Leveraging industry standards**
            - Sources of security standards: vendors, government agencies (NIST), independent organizations (CIS - center for internet security)
            - Industry standards provide an excellent starting point
        - **Customizing security standards**
            - Scope and tailor standard to meet the orgs needs
                1. Change requirements and specify in documentation; document the reason for any deviations
            - More stringent settings may be required based upon data sensitivity or system criticality
    - What are file permissions?
        - ACLs restrict access to files and folders
        - NTFS permissions
            1. Full control - grants complete authority over a resource
            2. Read - allows the user to read the file
            3. Read & execute - read and execute an application
            4. Write - allows user to create files and modify their contents
            5. Modify - read, write, and adds delete
        - Linux file system access commands
            1. Chown - changes file or directory user owner
            2. Chgrp - changes a file or directory group owner
            3. Chmod - changes the permissions on a file or directory
            4. Linux file permissions: read - r, write - w, execute - x
            5. Linux file ownerships: user owner - u, group owner - g, other - o
            6. **!! remember that the “o” means “others”, not “owner”, when working with Linux permissions**
    - What is data encryption?
        - Encryption protects data - using algorithms and secret keys
        - Most encryption uses software
        - Full disk encryption protects an entire hard drive
        - Database encryption protects the contents of databases from attack
        - Hardware encryption is more efficient than software encryption
            1. Hardware security modules (HSMs) use dedicated hardware for encryption, decryption, and key mgmt
            2. Trusted platform module (TPMs) bring hardware encryption to typical computers
            3. Some hard drives and USB devices have built-in encryption technology
    - What is information classification?
        - Data classification policies - assign info into categories, known as classifications
        - Assigned based upon: sensitivity
        - Classification guides other security decisions like asset classification
        - Assume that info on a system is classified at the highest level authorized for use on that system
        - Labeling requirements - identify sensitive info
        - Securely dispose of info when no longer needed
- **Domain 3: Security Architecture and Engineering |** 53: 2, 1, 12

    *Security Engineering:*

    - What are secure design principles?
        - Security is a design element. “Bolt-on” security rarely works.
        - subject/object model:
            1. Subject: requesting access
            2. Object: object being accessed
            3. Clearly designating subjects and objects improves design quality
        - Failure modes
            1. Fail open - failed security controls are bypassed
            2. Fail secure - failed security controls block access
        - Isolation & segmentation
            1. Network segmentation
            2. Process isolation
            3. Memory segmentation
            4. Virtual machine isolation
    - What are security models?
        - Multilevel security - systems designed to operate at different security levels simultaneously, whale enforcing confidentiality and integrity constraints that restrict access between security levels
        - Bell-lapadula - enforces confidentiality
            1. Simple security rule - no “read up”
            2. Property - no “write down”
            3. **!! the bell-lapadula model is rarely implemented outside of military applications**
        - Biba Model - enforces integrity
            1. Simple integrity property - no “read down”
            2. Integrity property - no “write up”
            3. **!! the bell-lapadula and biba models are important for the exam but rarely used in the real world**
    - What are security requirements?
        - Trusted computer system evaluation criteria (TCSEC)
            1. Became known as the orange book
            2. Content DoD computer security requirements
            3. Replaced by Common Criteria (unified evaluation process)
        - Certification and accreditation
            1. Certification - determines that a system meets security criteria
            2. Accreditation - approves use of a system in a specific environment
                - Accreditation decisions:
                - Authorization to operate (ATO)
                - Interim authorization to operate (IATO)
                - Interim authorization to test (IATT)
                - Denial of authorization to operate (DATO)
            3. **!! certification & accreditation are different; accreditation and authorization are the same**

    *Cloud Computing & Virtualization:*

    - What is virtualization?
        - Host machines run on physical hardware
        - Host machines provide services to several virtualized guest machines
        - The hypervisor tricks each guest into thinking it is running on dedicated hardware
        - Type 1 hypervisor: bare metal hypervisor - hypervisor runs on top of the hardware
        - Type 2 hypervisor: physical machine runs its own OS, then hypervisor runs as a program (common for personal computer use)
        - Designed to enforce isolation and prevent VM escape
    - What are cloud computing models?
        - Cloud computing is the next logical advance in enterprise IT
        - Cloud computing - the delivery of computing resources as a service over a network
        - Benefits: flexibility, scalability, agility, cost effectiveness
        - Models:
            1. Private cloud - organization uses a dedicated cloud infrastructure
            2. Public cloud - organization uses a shared tenancy infrastructure
            3. Hybrid cloud - org uses both private and cloud computing
        - Public cloud computing uses a shared responsibility model
        - **!! no cloud model is inherently superior to the other approaches, it all depends upon the context**
    - What are public cloud tiers?
        - Software as a service (SaaS) - [Box, DropBox, Outlook, etc]
            1. Customer purchases basic computing resources
        - Infrastructure as a service (IaaS) - [AWS, Azure, Google Cloud]
            1. Customer purchases basic infrastructure components
        - Platform as a service (PaaS) - [AWS Lambda]
            1. Customer purchases an entire app
        - Security responsibilities - determine and understand customer vs vendor responsibilities

    *Hardware Security:*

    - What is memory protection?
        - Memory types:
            1. Read-only memory (ROM): contents may not be changed by applications or the operating system [CPU chip]
            2. Random access memory (RAM): contents may be changed by applications and the operating system
        - Memory management
            1. OS tracks what applications are using each segment of memory
            2. OS grants request for additional memory
            3. OS frees up memory when no longer needed
        - OS restricts access to memory segments
        - Segmentation fault: error that occurs when an app requests unauthorized access to a memory segment
        - Memory leak: apps accumulate memory over time and fail to release it when its no longer needed
    - What is interface protection?
        - Application programming interface (API) - allow direct interaction with applications
        - Interface types: physical interfaces, virtual interfaces
        - Covert channels: allow backdoor communication
            1. 1 - covert storage channels: ICMP echo request,
            2. 2 - covert timing channels: port knocking
    - What are HA & FT, in detail?
        - HA - uses multiple systems to protect against service failure
        - FT - makes a single system resilient against technical failures
        - Load Balancing - spreads demand across systems
        - RAID - redundant array of inexpensive disks
            1. RAID 1 - disk mirroring: stores the same data on two different disks
            2. RAID 5 - disk striping with parity: uses 3 or more disks to store data and parity information
        - QoS for network load

    *Client & server vulnerabilities:*

    - What are Client and server vulnerabilities?
        - **Client and server vulnerabilities**
            - The burden of creatwing most web content rests with the server
            - Applets shift the burden - code executed on the client
            - Executing code locally presents a security risk
            - Local caches - caches store frequently used records to save clients the time of performing repeated lookups and reduce the burden on servers
                1. Cache poisoning - insert false records in local caches
                2. Local caches also exist for ARP and files retrieved from internet
    - What are Server security issues?
        - Data flow control
            1. 1 - controlling bandwidth consumption: use network devices and server operating systems
            2. 2 - understanding sensitive data flows: use data-flow maps to apply controls appropriately
        - Database servers store massive amounts of sensitive info
        - DB focused attacks:
            1. Aggregation - individuals with a low-level security clearance may be able to piece together sensitive info by combining the facts available to them
            2. Inference - individuals can figure out sensitive info from the facts available to them
    - What are NoSQL databases?
        - Use key-value stores
        - 1. Key - unique value used to identify and locate info stores in the table
        - 2. Value - data associated with a key that is stored for later retrieval by the app
        - Each key may have a different structure of value
    - What are Large-scale parallel and distributed systems?
        - client/server computing
        - Large-scale parallel data: example = SETI - search for extraterrestrial intelligence
        - Grid computing - assembled te unused processing capability of many computer at different locations to form a virtual supercomputer with a centralized computer
        - Peer to peer (P2P) - p2p nodes all have equal importance on the network: bitTorrent, bitcoin, TOR ; has security concerns

    *Web Security:*

    - What is OWASP top ten?
        - Injection flaws - insert unwanted transaction code
        - Broken authentication - exploits session mgmt
        - Sensitive data exposure - discloses confidential info
        - XML external entities - allow remote code execution
        - Broken access control - allows unauthorized access
        - Security misconfigurations - occur in many possible locations
        - Cross-site scripting (XSS) - inserts malicious scripts on websites
        - Insecure deserialization - allows api exploitation
        - Using vulnerable components - jeopardizes application security
        - Insufficient logging - frustrates security analysis
    - What is SQL injection prevention?
        - Apps request data from DB using the structured query language (SQL)
        - **!! you wont need to write SQL on the exam, but you should know how SQL injection works**
        - Example:

        SELECT username, password

        FROM user_accounts

        WHERE username = <username>;

        - Semicolons separate SQL statements
        - Two dashes indicate comments
        - Single quotes are critical to SQL injection
        - Two defenses:
            1. Input validation - protects against unsafe user input by checking it on the server before executing commands
            2. Parameterized SQL - precompiles SQL code on the db server to prevent user input from altering query structure
    - What is Cross-site scripting prevention?
        - XSS - occurs when attacker embeds malicious scripts in a 3rd party website that are later run by innocent visitors to that site
        - HTML enhances websites with formatting and images, uses Tags < … >
            1. The <script> tag allows devs to embed code in a page
        - XSS attackers embed scripts in sites without permission
        - Use input validation! Dont allow <script> tags in user-supplied input
    - What is Cross-site request forgery prevention?
        - **!! cross-site request forgery, CSRF, XSRF, and “sea surf” all refer to the same attack**
        - CSRF/XSRF attacks leverage the fact that users are often logged in to multiple sites at the same time and use one site to trick the browser into sending malicious requests to another site without the user’s knowledge
        - Secretly sends requests often using image tags
        - Defense:
            1. Prevent the use of HTTP GET requests
            2. Auto-log users out after a short idle period
    - What is Fuzz testing & session hijacking?
        - Software testing technique that feeds software many different input values in an attempt to cause an unpredictable state or unauthorized access; ex: ZAP - zed attack proxy
        - Only fuzz test with permission
        - **Session hijacking**
            - Cookie values - weak if guessable

    *Mobile Security:*

    - What is Mobile device security?
        - Full device encryption
        - Complex password and biometric authentication
        - Remote wiping technology removes data from lost or stolen devices, only works if connected to network
        - Lock mobile devices automatically after entering password too many times
    - What is Mobile device mgmt (MDM)?
        - MDM features
            1. Device config mgmt
            2. Prevent users from modifying security settings
            3. Control data stored on devices
            4. Manage apps installed on devices
                - 1. Application blacklisting - prohibit the installation of specified apps on mobile devices
                - 2. Application whitelisting - only allow the installation of approved apps on mobile devices
            5. Storage segmentation
    - What is Mobile device tracking & mobile app security?
        - Over 3.1mil mobile devices are stolen annually
        - Asset tracking software - manages device inventories; tracks entire lifecycle of device
        - Authentication - use strong credential mgmt, rely upon central authentication
        - Encrypt all sensitive info in transit and at rest, practice strong key mgmt
        - Geotagging may disclose sensitive locations
    - What is Bring your own device (BYOD)?
        - Core issues around BYOD are about ownership
        - BYOD onboarding: ensure the device meets security requirements and is safely configured
        - BYOD offboarding: remove all corporate info from the personally owned device

    *Smart device security:*

    - What are Industrial control systems (ICS)?
        - **Industrial control systems (ICS)**
            - ICS monitor and control industrial processes [electrical, gas, water, etc]
            - Types:
                1. Supervisory control and data acquisition (SCADA)
                    - Remote monitoring (water, gas pipelines)
                    - Remote telemetry, report back to control system
                    - Have multiple points of attack
                2. Distributed control systems (DCS)
                    - Focus on controlling processes
                    - Use sensors and feedback systems
                    - Have multiple points of attack
                3. Programmable logic controllers (PLC)
                    - Handle specialized input and output
                    - Ensure uninterrupted processing
    - What is smart home tech, and how do you secure IoT?
        - **Smart home technology**
            - Computer controlled and network connected devices
            - **!! the CISSP exam uses the term embedded systems to refer to smart devices**
        - **Securing the internet of things**
            - 1. Auto updates - install without users intervention when available
            - 2. Manual updates - requires user check for updates
            - Firmware version control - updates applied in orderly fashion
            - Security wrappers - vets request for embedded systems (mini-firewall for the embedded device)
            - Use diverse and redundant security controls to protect embedded devices
        - **Secure networking for the internet of things**
            - Network segmentation: separates untrusted devices
            - **!! network segmentation is the most important control for embedded devices**
            - **!! embedded device security controls are effective for mainframes as well**

    *Encryption:*

    - What is encryption?
        - Cryptography is the use of mathematical algorithms to transform info into an encrypted form that is not readable by unauthorized individuals
        - Cryptography does provide authorized indians with the ability to transform it back into readable form through decryption
        - Algorithms - serve as mathematical recipes
        - Encrypt and Decrypt are the two main processes
    - What is Symmetric and asymmetric cryptography?
        - Symmetric algorithms (shared secret): encryption and decryption operations use the SAME key
            1. n(n-1)/2
        - Asymmetric algorithms (public key): encryption and decryption operations use DIFFERENT keys / kay pair
            1. Public key - freely distributed to everyone with whom the user would like to communicate
            2. Private key - held in secret by the user and not disclosed to anyone else
            3. Anything encrypted with one key from a pair can be decrypted with the other key from that same pair
        - **!! keys used to encrypt and decrypt using asymmetric cryptography must be from the same pair**
        - Asymmetric is slower but scales much better for larger orgs
    - What are the goals of cryptography?
        - 1 - confidentiality: authorized access only
        - 2 - integrity: no unauthorized changes
        - 3 - authentication: proof of identity claims
        - 4 - nonrepudiation: verifiable origin of a message - through digital signatures, only possible with asymmetric cryptography
    - What are Codes and ciphers?
        - **!! codes and ciphers are two different things**
        - Code - system that substitutes one word or phrase for another. Codes are intended to provide secret and/or efficiency.
            1. I.e. efficiency in the ten code system used by police (10-4 , etc)
            2. Seemingly meaningless phrases may convey messages
        - Ciphers - system that uses mathematical algorithms to encrypt and decrypt messages
            1. 1 - stream ciphers: operate on one character, or bit, of a message at a time
            2. 2 - block ciphers: operate on large segments of the message at the same time
            3. Substitution ciphers: change the characters in a message
            4. Transposition ciphers: rearrange the characters in a message
            5. Substitution and transposition are the building blocks of modern cryptography
    - How do you choose encryption algorithms?
        - **!! don't try to build your own encryption algorithm unless you really know what you’re doing**
        - Use algorithms proven to be secure
    - What is the perfect encryption algorithm?
        - One-time pad: it is an unbreakable encryption algorithm
        - Sender and receive have identical pads, key is at least as long as the message
        - One-time pads are unbreakable because they are totally random, using one-time pads is very difficult
    - What is The cryptographic lifecycle?

        By NIST: Initiation > development and acquisition > implementation and assessment > operations and maintenance > sunset

    - What is Digital right management (DRM)?

        Provides the owners of IP with the technical means to prevent the unauthorized use of their content through the use of encryption technology

    *Symmetric Cryptography:*

    - What is DES?
        - Designed by IBM in the 1970s, intended to serve as federal encryption standard
        - DES uses an encryption operation called the feistel function for 16 rounds of encryption; each F-box performs a combo of substitution and transposition operations
        - No longer considered secure
        - KEY FACTS: symmetric algorithm, block cipher operating on 64-bit blocks, key length of 56 bits, now considered insecure
    - What is 3DES?
        - Applies DES to plaintext three times with three keys: K1, K2, K3
        - **!! double DES is no more secure than standard DES, due to the meet-in-the-middle attack**
        - Triple DES is considered secure through 2030 (keying mode 1)
        - KEY FACTS: symmetric algorithm, block cipher operating on 64-bit blocks, effective key length of 112 bits (when using key mode 1, 3 different keys), key mode 1 is considered secure
    - What are AES, Blowfish, and Twofish?
        - AES KEY FACTS: symmetric algorithm, block cipher operating on 128-bit blocks, key length of 128, 192, or 256 bits, considered secure
        - Blowfish KEY FACTS: symmetric encryption algorithm, block cipher operating on 64-bit blocks, key length anywhere between 32 and 448 bits, not considered secure
        - Twofish KEY FACTS: symmetrics encryption algorithm, block cipher operating on 128-bit blocks, key length of 128, 192, or 256 bits, considered secure
    - What is RC4?

        KEY FACTS: symmetric, stream cipher, variable length key between 40 bits and 2048 bits, not secure

    - What is steganography?
        - Hides data in large files
        - Often uses innocent-looking high-resolution images, slight modifications to image pixels may hide information

    *Asymmetric cryptography:*

    - What is Rivest-shamir-adleman (RSA)?
        - **!! users create RSA key pairs using two large prime numbers**
        - Slow, usually used to Transfers symmetric keys
        - Patent is now expired
        - KEY FACTS: asymmetric algorithm, variable length key between 1024 and 5096 bits, considered secure
    - What is PGP and GnuPG?

        Pgp relies upon other encryption algorithms, it's a framework

    - What is Elliptic-curve and Quantum cryptography?
        - Elliptic-curve cryptography (ECC) does not depend on prime factorization, uses the EC discrete log problem
        - **!! you wont need to know the details of ECC, remember that it doesn't use prime factorization**
        - Quantum computing - uses quantum mechanics principles
            1. May be stronger than nay modern approach - needs to develop

    *Key Management:*

    - What is Key exchange?

        Symmetric cryptography requires exchanging a shared secret key in advanced

    - What is Diffie-hellman?
        - p and g must be large values to achieve strong security
        - ECDH - uses the EC discrete log problem
    - What is Key escrow?
        - Encryption key escrow - allows government access to keys
        - Recovery agents - allow internal access to lost keys
    - What is Key stretching?
        - Algorithm takes a relatively insecure value, such as a password, and uses mathematical techniques to strengthen it, making it harder to crack
        - 1 - Salting: adds a value to the encryption key to make it more complex
        - 2 - Hashing: adds time to the verification process by requiring more math
        - PBKDF2 - password based key derivation function v2
            1. Uses salting and hashing to stretch a key
            2. Should be used at least 4000 times
        - Bcrypt - key stretching with blowfish

    *PKI*:

    - What are Trust models?
        - Personal knowledge, Web of trust (WOT), Public key infrastructure (PKI)
        - WOT - relies on indirect relationships; participants digitally sign the public keys of people they know personally
            1. Decentralized approach, high barrier to entry, requires technical knowledge
        - PKI builds upon the web of trust
    - What is PKI and digital certificates?
        - Relies upon trusted certificate authorities (CAs)
            1. CAs are trusted 3rd party orgs who verify the identity of individuals or orgs and then issue digital certs containing both identity info and a copy of the subjects public key
            2. Digital certs are the identity cards of the digital world
            3. After authenticating identity, the CS provides a digital cert contrianing the public key
    - What are Hash functions?
        - One-way functions that transform a variable length input into a unique, fixed-length output > cannot be reversed
        - Hash functions may fail if they are reversible, are not collision resistant
        - **!! know which hash functions are considered insecure and which remain score today**
        - MD5 (message digest 5), hash is also called message digest
            1. Created by Ron Rivest, also created RSA encryption
            2. Produces 128-bit hashes, no longer secure
        - SHA (secure hash algorithm)
            1. Created by NIST as a government standard
            2. SHA-1
                - Produces 160-bit hash value, not secure
            3. SHA-2
                - Consists of a family of six hash functions
                - Produces output of 224, 256, 384, and 512 bits
                - Still secure
            4. SHA-3
                - Designed as an eventual replacement for SHA-2
                - Produces hashed of user-selected fixed length
        - RIPEMD
            1. Created as an alternative to government-sponsored hash functions
            2. Produces 128, 160, 256, and 320-bit hashes
            3. 128-bit not secure
        - HMAC - hash based message authentication code
            1. Combines symmetric cryptography and hashing
            2. Provides authentication and integrity
            3. Create an veriy message authentication code by using a secret key in conjunction with a hash function
        - Hash functions are used with asymmetric cryptography for digital signatures and digital certificates
    - What are Digital Signatures?
        - Use asymmetric cryptography to achieve integrity, authentication, and non-repudiation
        - Use private keys to create digital signatures
        - Digitally signing messages does not provide confidentiality
        - **Create a digital certificate**
            - Uses the X.509 standard
        - **Revoke a digital certificate**
            - 1. CRL - certificate revocation list: CAs provide a list of the serial numbers of revoked certificates
            - 2. OCSP - online certificate status protocol: CAs provide a realt-ime service that allows users to verify that a certificate is not revoked
            - Most modern browsers implement OCSP

    *Cryptanalytic Attacks:*

    - What are Brute-force attacks?
        - Repeatedly guess keys, also called known ciphertext attacks
        - Flawed algorithms may be susceptible to brute force attacks
    - What are Knowledge-based attacks?
        - Frequency analysis - detects patterns in ciphertext
        - **!! you wont need to perform cryptanalysis on the CISSP exam. You just need to know the different techniques**
        - Known plaintext attack: attacker has access to an unencrypted message
        - Chosen plaintext attack: attacker can create an encrypted message of his or her choice

    *Physical security:*

    - What are Data center environmental controls?
        - Air temperatures
            1. Expanded envelope - between 64.4 - 80.6 ‘oF
        - Humidity:
            1. High humidity: leads to condensation that may damage electronic equipment
            2. Low humidity: leads to static electricity that may damage electronic equipment
            3. Dew Point Range - between 41.9 and 50.0 ‘oF
        - HVAC systems keep temp and humidity under control
        - Servers draw cool air in the front and expel hot air out the back
            1. Utilize the hot aisle/cold aisle approach - makes cooling data centers more efficient
            2. **!! watch for exam questions that are indirectly covering the hot aisle/cold aisle strategy**
    - What is Data center environmental protection?
        - Fires require three sustaining elements: heat, fuel, oxygen
        - Water is dangerous in a data center environment
        - Fire extinguishers:
            1. Class A - common combustibles (wood, cloth & trash)
            2. Class B - flammable liquids (gas & oil)
            3. Class C - electrical fires (data centers)
            4. Class D - heavy metal fires (industrial applications)
            5. Class K - kitchen fires (fats & oils)
        - **!! be able to identify the classes of fire extinguishers on the exam , when in doubt check the labels**
        - Water:
            1. 1. Wet pipe systems: contain water in the pipes ready to deploy when a fire strikes
            2. 2. Dry pipe systems: do not contain water until a valve opens during a fire alarm
        - Chemical systems deprive fires of oxygen
        - EMI - electromagnetic interference: monitor for all EMI issues
    - What are Physical security control types?
        - Intended effect categories
            1. Deterrent controls - intended to prevent an intruder from trying to access a secure area
            2. Preventative - intended to block an intruder from accessing a secure area
            3. Detective controls - intended to alert security personnel to a potential or actual security violation
        - Mechanism of action categories
            1. Technical controls: use technology to deter, prevent, or detect security violations
            2. Administrative controls rely upon business processes to enhance physical security
        - Compensating controls - fill known gaps in security
        - **!! physical security controls are a common problem area for candidates taking the exam**
        - **Physical security control types, Visitor management**
- **Domain 4: Communications and Network Security |** 53: 1, 2, 5

    *TCP/IP Networking:*

    - What is TCP/IP?
        - Transmission control protocol
            1. 1. TCP - connection oriented protocol, reliable - guarantees delivery through acknowledgement, is widely used for critical apps
                - TCP Flags (3 way handshake)
                    - SYN: opens a connection
                    - FIN: closes a connection
                    - ACK: acknowledges a SYN or FIN
            2. 2. UDP - lightweight, connectionless protocol, does not send acknowledge or guarantee delivery, used for voice and video apps
        - Internet protocol - routes info across networks, provides an addressing scheme (IP addresses), delivers packets from source to destination, servers as a network layer protocol
        - OSI model (P, D, N, T, S, P, A):
            1. 

                [https://lh5.googleusercontent.com/NCUKl4-hdAaBctKMCiueYqKEGoQEROYc6278hlhFSXbhME9t1yRQgMTdXvB-7fzkgOIH8BoUD0vUvmhmeS5eVgHSWx0g5kk6UeiLGQUhWREetO8shLc8ucfcbW8cCHwyveF8rkjR](https://lh5.googleusercontent.com/NCUKl4-hdAaBctKMCiueYqKEGoQEROYc6278hlhFSXbhME9t1yRQgMTdXvB-7fzkgOIH8BoUD0vUvmhmeS5eVgHSWx0g5kk6UeiLGQUhWREetO8shLc8ucfcbW8cCHwyveF8rkjR)

        - TCP/IP Model - comparison:
            1. 

                [https://lh3.googleusercontent.com/nGuxiQxfr3RjbyyLuDyqnVZF77-l2fQ7Wf8GI2IK6mooyO30Zsf9wP1C5EcbRNw6Nr1McEyMlovE7u909K1zY8ug2Hx5eupYc_-8iVGQX6FS-6didbS1yDhueJe3OAkZLxB2iFrd](https://lh3.googleusercontent.com/nGuxiQxfr3RjbyyLuDyqnVZF77-l2fQ7Wf8GI2IK6mooyO30Zsf9wP1C5EcbRNw6Nr1McEyMlovE7u909K1zY8ug2Hx5eupYc_-8iVGQX6FS-6didbS1yDhueJe3OAkZLxB2iFrd)

        - **!! know the seven layers of the OSI model and the four layer of the TCP/IP model**
    - What is IP Addressing?
        - Written in dotted quad notation - 4 number separated by 0’s
        - Why the range 255?
            1. 8-bit binary numbers
            2. 2 to the 8th = 256 possible values
            3. Start counting at 0
            4. Range: 0-255 (256 values)
        - Uniquely identify systems on the network
        - Must not be rescued on internet-connected systems
        - May be reused if on private networks (NAT)
        - Divided into two part - network portion, host portion
        - Two addresses involved in every communication: source & destination
        - IPv6 replaces IPv4 due to address exhaustion
            1. Uses 128 bits (compared to 32 for IPv4)
            2. Consists of eight groups of four hexadecimal numbers
    - What is DNS?
        - translate domain names into IP addresses
        - DNS functions over UDP port 53
        - DNS functioning
            1. 1. User types domain name into browser
            2. 2. Computer sens a DNS query to the local DNS server
            3. 3. DNS server responds with an IP address
            4. 4. Computer contacts the server at that IP address
        - A hierarchical system: orgs designate server that are authoritative for their domains
        - Windows: can use nslookup (built-in to OS), Linux: can use dig
        - Some content filters alter DNS query results
    - What are network ports?
        - Network ports, like apartment numbers, guide traffic to the correct final destination
        - 16-bit binary numbers
        - Port ranges:
            1. 0-1023: well-known ports
            2. 1024-49,151: registered ports
            3. 49,152-65,525: dynamic ports
            4. **!! memorize the list of common ports before taking the exam**
        - 

            [https://lh6.googleusercontent.com/fD7Y8tGyf5Uk_ZgnfQ08CuAXo0KqxGLWm911DpJbpU8iYsWknkjm8AicHbS58Gz7g4ltmk1BX7V_iPw81pFvkqbpw-5ZsyWsgQbuL15cHyhcBj1TV_8lekf1RduaAOSCq6MSrS0b](https://lh6.googleusercontent.com/fD7Y8tGyf5Uk_ZgnfQ08CuAXo0KqxGLWm911DpJbpU8iYsWknkjm8AicHbS58Gz7g4ltmk1BX7V_iPw81pFvkqbpw-5ZsyWsgQbuL15cHyhcBj1TV_8lekf1RduaAOSCq6MSrS0b)

    - What is ICMP?
        - Housekeeping protocol of the internet - ping command
        - Sends ICMP echo requests , if ICMP echo reply is received then system is online
        - Traceroute command - identifies network paths
    - What are Multilayer protocols?
        - TCP/IP is the most common multilayer protocol set
        - Distributed network protocol (DNP3) - provides network connectivity for SCADA systems
            1. DNP3 at work

        [https://lh5.googleusercontent.com/4eGaXw5PP1O_Bnsv5k4mPLJLRlI5YHFDUkZUMGDWM9ISzhb7CULE-Vbmb4bK01BHdIUQwoBTawBvXGRlOpR_xtNKRf7O9a6biRKoCaTs6U-vOQ6CtPZsXOFJ8bVPQlCwxwGXy7bl](https://lh5.googleusercontent.com/4eGaXw5PP1O_Bnsv5k4mPLJLRlI5YHFDUkZUMGDWM9ISzhb7CULE-Vbmb4bK01BHdIUQwoBTawBvXGRlOpR_xtNKRf7O9a6biRKoCaTs6U-vOQ6CtPZsXOFJ8bVPQlCwxwGXy7bl)

        1. DNP3 OSI model:

        [https://lh3.googleusercontent.com/wgm7jb8Pp_iYyikosH-WkxJnMRI_zCSU7A1zsYzBAktbeSwOB9kS3nS7QzKL2m8hANUAqlLgls1qh5nKmA3JwBkPSDhxC_6FyimuBiB2dIOOCBxt33xDrXpbSB2BkIPPlzM-FDiF](https://lh3.googleusercontent.com/wgm7jb8Pp_iYyikosH-WkxJnMRI_zCSU7A1zsYzBAktbeSwOB9kS3nS7QzKL2m8hANUAqlLgls1qh5nKmA3JwBkPSDhxC_6FyimuBiB2dIOOCBxt33xDrXpbSB2BkIPPlzM-FDiF)

    *Network security devices:*

    - What are Switches and routers?
        - The connectivity building blocks of a network
        - Switches create networks
        - Reside in wiring closets and connect the computers in a building together
            1. Ethernet jacks are at the other end of network cables connected to switches
            2. WPAs connect to switches and create Wi-Fi networks
        - Routers connect networks together
    - What are Firewalls?
        - Act as network security guards, blocking unwanted traffic
        - Usually sit between routers and the internet
        - Usually connect three networks together: internal, internet, and DMZ
        - DMZ:
            1. Contains system that must accept direct external connections
            2. Isolates those systems due to risk of compromise
            3. Protects internal network from compromised DMZ systems
        - Stateful inspection - tracks open connection
        - Firewall rule contents:
            1. Source system address
            2. Destination system address
            3. Destination port and protocol
            4. Action (allow or deny)
        - Implicit deny principle: if the firewall receives traffic that is not explicitly allowed by a firewall rule, that traffic must be blocked
        - **!! understand the implicit deny principle of firewall**
        - Web App firewalls: specifically protect web apps by using app awareness to peer deep into the app layer and block web attacks
    - What are Load balancers, proxies, and web security gateways?
        - Load balancing = several servers share the load
            1. Security functions: SSL certificate mgmt, URL filtering, other web app tasks
        - Proxies = browse websites on behalf of end users, sits in the middle of the connection
            1. Provides anonymization, only see proxy’s IP
            2. Performance boosting by caching frequent pages
            3. Content filtering
        - Web security gateways
            1. Set between web users and internet
            2. Scan requests coming from users
            3. Scan responses coming from the internet
            4. Filter out potential malicious attacks
    - What are VPNs and VPN concentrators?
        - 1. Site-to-site VPNs: connect remote offices to each other and headquarters
        - 2. Remote Access VPNs: provide remote access to corporate networks for mobile users
        - VPN endpoints
            1. Firewalls, routers, server, dedicated VPN concentrators
        - 1. IPsec: network layer VPN protocol commonly used for site-to-site VPNs but difficult to configure
        - 2. SSL/TLS: application layer VPN protocol commonly used for remote access VPNs and easier to configure
    - What is Network intrusion detection and prevention?
        - IDS - monitor network traffic
            1. Alert admins to suspicious activity
            2. Require someone to monitor and take appropriate action
        - IPS - block suspicious activity automatically
            1. 1. False positive error: IDS/IPS triggers an alert when an attack did not actually take place
            2. 2. False negative error: IDS/IPS fails to trigger an alert when an actual attack occurs
        - IDS/IPS use:
            1. Signature detection systems
                - Contain db’s with rules describing malicious activity
                - Alert admins to traffic matching signatures
                - Fail to detect brand new attacks
                - Reduce false positives
            2. Anomaly detection systems
                - Build models of “normal” activity
                - Alert admins to activity not matching the normal model
                - Detect previously known attacks
                - Increased false positive rates
                - **!! anomaly detection, behavior-based detection, and heuristic detection are the same thing**
            3. IPD development modes
                - 1. In-band (inline) deployments: device sits in the path of network communications, device can block suspicious traffic from entering the network
                - 2. Out-of-band (passive) deployment: device connects to a SPAN port on a switch, device can react after suspicious traffic enters the network
    - What are protocol analyzers?
        - Allow deep inspection of traffic
        - Troubleshoot network issues
        - Investigate security incidents
        - Eavesdrop on confidential communications
    - What is Unified threat management?
        - Combine multiple security functions in a single appliance
        - Basic functions:
            1. Protecting network against attacks
            2. Blocking unsolicited traffic
            3. Routing traffic to and from the internet
    - What are Content distribution networks (CDNs)?
        - **!! content delivery networks and content distribution networks are the same thing**
        - CDNs provide a shared web infrastructure , benefits:
        - Provide on-demand scaling
        - Cost efficient
        - Locality of content
        - Security enhancements (DDoS protection & web app firewall functionality)
    - What are Modems?
        - Modulator and demodulator = MO DEM
        - Security considerations: block inbound requests, find alternative technologies, leverage strong authentication

    *Designing secure networks:*

    - What is Public and private addressing?
        - 1. Public IP Addresses: assigned by a central authority and are routable over the internet
            1. Centrally managed by ICANN - distributes large blocks of addresses to regional authorities for distribution
            2. IPv4 are scarce, no large blocks available
        - 2. Private IP Addresses: available for anyone’s use but not routable over the internet
            1. Are reserved for use on private networks, not internet routable
            2. Ranges:
                - Class A: 10.0.0.1 - 10.255.255.255
                - Class B: 172.16.0.1 - 172.31.255.255
                - Class C: 192.168.0.1 - 192.168.255.255
        - Orgs mix public and private addresses
        - NAT (network address translation) - translates private IP addresses
        - PAT (port address translation) - allows multiple systems to share the same public address, assigns unique ports to each communication
    - What is Subnetting?
        - Subdivides large networks

        - Subnet masks identify the dividing line between network and host addresses
        - 

            [https://lh3.googleusercontent.com/oC9xs332-bAx3pVcflFwJIMgsYSAADd3Qnxoe-Up3Be8o8F0WSYVW4gJgKdaoM25a6JsqeqYDo666r5LkzpwKPYcVSigJQlvAzHouXcPGtvWb4nVP7ndYgYu7RkQ1ZIk8rysUx3i](https://lh3.googleusercontent.com/oC9xs332-bAx3pVcflFwJIMgsYSAADd3Qnxoe-Up3Be8o8F0WSYVW4gJgKdaoM25a6JsqeqYDo666r5LkzpwKPYcVSigJQlvAzHouXcPGtvWb4nVP7ndYgYu7RkQ1ZIk8rysUx3i)

    - What is VLANs and network segmentation?
        - Virtual LANs: separate systems on a network into logical groups based upon function, regardless of physical location
        - VLANs extend the broadcast domain (at layer 2)
        - Configure VLANs:
            1. Enable VLAN trunking
            2. Assign switchports to VLANs
    - What is Network access control?
        - ntercepts network traffic coming from unknown devices and verifies that the system and user are authorized before allowing further communication
        - Uses 802.1x authentication
        - NAC roles: user & device authentication, role-based access, posture checking
        - NAC performs posture checking, device that fail go into a quarantine VLAN
    - What is remote network access?
        - 1. Remote shell - provides command-line access to a remote system
        - 2. Remote desktop - provides graphical access to the desktop of the remote system
        - Older Linux systems used telnet for remote access, telnet is extremely insecure because it does not provide any encryption
            1. Alternative is SSH since it uses encryption
    - What is Desktop and application virtualization?
        - VDI - provides network-based access to a desktop computing environment
        - Application virtualization allows users to “steam” apps to their desktops
        - Screen scraping provides access to mainframes
        - **!! screen scraping is rarely used, but it is covered on the CISSP exam**
    - What is Defense in depth?
        - Orgs should use multiple, overlapping security controls to achieve each of their security objectives
        - Defense in depth example - Eavesdropping:
            1. Encryption through VPN
            2. Encryption at the app layer (HTTPS)
            3. Segmentation with VLANs
        - Defense in depth - access control:
            1. Network access control
            2. Role-appropriate VLANs
            3. MAC filtering
            4. Port security
        - Defense in depth - perimeter:

        [https://lh5.googleusercontent.com/pvB9BwNDZUu1obM5GkTD5PSRA5LB-rGMCIuOO2daTyRCQnomVwj01_XVEIHRjTWKeQkJXqJLK9M3C-gHHz5FUjz9z7nZ1ambGvSxGUT5RtUnAKColW6QbdO8p5e6qBTiHZQoJKkp](https://lh5.googleusercontent.com/pvB9BwNDZUu1obM5GkTD5PSRA5LB-rGMCIuOO2daTyRCQnomVwj01_XVEIHRjTWKeQkJXqJLK9M3C-gHHz5FUjz9z7nZ1ambGvSxGUT5RtUnAKColW6QbdO8p5e6qBTiHZQoJKkp)

        - **!! keep the defense in depth principle front of mind during the CISSP exam**

    *Specialized networking:*

    - What is Telephony?
        - VoIP
            1. Carries voice comms over data networks
            2. Converts voice from analog to digital form
            3. Transmits using the internet protocol
        - Encryption protects VoIP traffic, but affects voice quality, can also use segmentation when encryption is not viable
    - What is Multimedia collaboration?
        - Extensible messaging and presence protocol (XMPP): provides an open-source, standards-based alternative to proprietary messaging protocols. It was originally known as Jabber
        - SMS (short message service) - provides convenient, popular means to use the cellular network for text, picture, and video messaging
            1. No encryption of content
            2. No strong authentication
            3. Easy to spoof identity
        - 3rd party apps provide strong security for messaging
    - What are Storage networks?
        - Storage networks demand large quantities of dedicated bandwidth
        - 1. Network attached storage (NAS): simple, self-contained storage devices that commonly use CIFS and NFS
        - 2. Storage area networks (SAN): complex, massive storage systems that require dedicated networks
    - What is MPLS?
        - Most networks use IP-based routing
        - Multi protocol packet layer switching (MPLS) - uses fixed paths determined by the first router in the path
        - Considered a layer 2.5 protocol, MPLS networks are like a tunnel through the network
        - MPLS routing protocols:
            1. LDP - label distribution protocol
            2. RSVP - TE (reservation resource protocol - traffic engineering)

    *Secure network management:*

    - What is Firewall rule management?
        - Firewalls protect network, they control access at network borders
        - Firewall rules define how the firewall should act when it sees a new connection request
        - Firewall admins must watch for rule configuration errors
            1. Shadowed rules - rules that won't be executed because of its position in the rule base ; firewalls read TOP - DOWN
            2. Promiscuous rules - allow more access than necessary
            3. Orphaned rules - allow access to decommissioned systems and services
    - What is Router configuration security?
        - Rouerts perform basic filtering, they can reduce the load on firewalls
        - **!! you wont need to know the syntax of router access control list commands**
        - Router access control lists restrict network traffic, similar to firewall rules
    - What is Switch configuration security?
        - Maintain physical switch security
        - VLAN security
            1. VLAN pruning - limit the unnecessary exposure of VLANs by limiting the number of switches where they are trunked, especially for sensitive VLANs
            2. VLAN trunk negotiation - disable auto trunk negotiation to prevent VLAN hopping attacks
            3. Port security - limit the devices that may connect to a network switch port by MAC address
                - 1. Static port security
                - Dynamic “sticky” port security
    - What is Maintaining network availability?
        - Flooding attacks - overwhelm network devices:
            1. 1. SYN floods - fill connection state tables on firewalls with half-open connection entries
            2. 2. MAC floods - fill switch’s MAC address table with many entries, causing it to flood traffic on all ports
            3. Flood guard technology: protects network devices against these attacks
            4. Port security is also effective against MAC flooding
        - Routing loops - allow broadcast storms
            1. Spanning Tree Protocol (STP) - prevents broadcast storms by implementing loop prevention
    - What is Networking monitoring?
        - Firewall log details:
            1. Details about attempted connections
            2. Timestamps
            3. Relevant firewall rule
        - Firewall log uses:
            1. Security incident investigation
            2. Network issue troubleshooting
            3. Anomalous activity detection
        - Network flow data (netflow)
            1. Source and destination systems
            2. Source and destination ports
            3. Timestamps
            4. Amount of data transferred
            5. Netflow is quite useful, it doesn't capture what was communicated but does identify who, when, and how much
        - SIEM - security information and event mgmt: network security systems that automate the collection and analysis of logs from many different systems for security purposes, SIEMs facilitate rapid analysis
    - What is SNMP?
        - Provides admins with a means to centrally configure and monitor network devices, SNMP automates these tasks
        - SNMP components:
            1. 

                [https://lh4.googleusercontent.com/TwctkkcI9CS7g6yS8YGHY8KN5yzMxeDPl-uMG15xuwc5adktpgN7cNpLQxRfzZT1lXdYssoSfsMUoBnXz2s8WgFi2FfAOx6U17NtcoPS-Bu4ThPBRkiK0YvSNvHuYeCyu6Elnb7i](https://lh4.googleusercontent.com/TwctkkcI9CS7g6yS8YGHY8KN5yzMxeDPl-uMG15xuwc5adktpgN7cNpLQxRfzZT1lXdYssoSfsMUoBnXz2s8WgFi2FfAOx6U17NtcoPS-Bu4ThPBRkiK0YvSNvHuYeCyu6Elnb7i)

        - **!! sue SNMPv3, earlier versions have critical security flaws**

    *Virtualized networks:*

    - What is Software defined networking (SDN)?
        - Network functions:
            1. Control plane - responsible for making routing and switching decisions
            2. Data plane - responsible for carrying out the instructions of the control plane
        - SDN separates the control plane from the data plane
        - SDN makes the network programmable, through SDN controller
        - Security benefits: allows granular network config, facilitates faster response to security incidents
        - SDN does increase network complexity, requires use of strong access controls
    - What is Port isolation?
        - **! port isolation and private VLANs are the same thing**
        - Port isolation restrict traffic from a source port to a single destination port
        - Why use it:
            1. Prevents devices on the same switch from communicating with each other
            2. Blocks data-link-layer attacks, such as ARP spoofing
        - Port isolation works very well when provided public access, i.e. hotel wifi

    *Network attacks:*

    - What are Denial-of-service attacks?
        - Makes a resource unavailable for legitimate users
        - Sends a huger number of requests to a server
        - If difficult to distinguish between legitimate user
        - DDoS - a DoS attack that utilizes a botnet
        - Amplified DDoS attack: amp factor = degree to which the attack increases in size, like a smurf attack
    - What are Eavesdropping attacks?
        - Rely on a compromised communications path; network device tapping, DNS or ARP poisoning
        - MiTM attack
        - Replay attack
    - What are Other network attacks?
        - Packets - basic unit of network communications
            1. Contain a data payload to be sent
            2. Christmas tree attack - uses packet flags to exploit a system
            3. Christmas tree packet - all flags set to one, some systems cant handle all flags being set - this is a DoS attack
        - DNS - translates common domain names into IP addresses for the purpose of networking
            1. DNS poisoning - redirects or intercepts traffic
        - ARP - translates logical IP addresses into the hardware (MAC) addresses on the LAN
            1. ARP poisoning (only works on local network)
        - Typosquatting (URL hijacking): an attack that consists of registering domain names similar to official sites, hoping that users will make a typo and visit their site

    *Transport encryption:*

    - What is TLS and SSL?
        - These are transport encryption technologies that allow for the secure exchange of public encryption keys over otherwise untrusted networks, use certificates to facilitate secure comms
        - TLS - encrypts network communications
        - **!! TLS depends upon pairings of encryption and hash functions known as cipher suites**
        - **!! session keys are also known as ephemeral keys**
        - SSL - insecure predecessor to TLS, has been deprecated
    - What is IPsec?
        - Framework, set of protocols that adds security to TCP/IP
        - IPsec secures the entire payload
        - 1. Encapsulating security payload (ESP) - provides confidentiality and integrity protection for packet payloads
        - Authentication headers (AH) - provides integrity protection for packet headers and payloads
        - You can combine ESP + AH
        - Security associations (SAs) - identify cryptographic algorithms
        - 1. Site-to-site VPNs: encrypted tunnels connecting two networks together in a manner that is transparent to users
        - 2. End-user VPNs - provide encrypted remote network access for individual systems
    - What is Tor and perfect forward secrecy?

        Tor - The Onion Router (Tor) - is a software package that uses encryption and relay nodes to facilitate anonymous internet access

    *Wireless networking:*

    - What is wireless networking?
        - Wi-fi standard governs comms on many wireless networks
        - Wifi devices replace network cables with radio transmitters and receivers
        - WAPs connect wireless networks to wire networks and the internet
        - **!! wifi signals travel over open airwaves and are subject to undetectable interception**
    - What is WEP, WPA, and WPA2?
        - Encryption hides the contents of network comms from eavesdroppers
        - WEP (wired equivalent privacy) - weak, not secure
        - WPA (wifi protected access) - uses TKIP (temporal key integrity protocol) to implement strong encryption
        - WPA2 - uses CCMP to apply the advanced encryption standard (AES) to wireless networks
    - What is Wireless authentication?
        - Preshared keys (PSKs) - require entry of a password
            1. Limitations - changing network encryption key is a big burden, not scalable; identifying users and revoking individual user access is impossible
        - Enterprise authentication - uses username and password
            1. Lightweight EAP (LEAP) - insecure
            2. EAP (extensible authentication protocol) - broad framework with many variants, some secure, some not
            3. Protected EAP (PEAP) - tunnels EAP inside encrypted TLS session
            4. **!! make sure you understand the security status of the specific EAP variants in use on your network**
        - Captive portals - redirect to an authorization page
    - What is Wireless signal propagation?
        - Site survey - determines optimal AP placement
        - Manipulating power level modifies wireless signal range
    - What are Propagation attacks?
        - Jamming and interference
        - War driving - attackers will cruise neighborhoods and commercial areas, using tools that capture info about wifi networks
            1. Can map as well - i.e wigle.net
    - How do you prevent rogues and evil twins?
        - Attackers can utilize the Karma toolkit
        - Rogue AP detection: enterprise-grade wireless has built-in intrusion detection capabilities; unknown radios on the network can be identified; handheld tools can also help pinpoint them
    - What are Bluetooth and NFC attacks?
        - NFC = near field communication attacks, used in Bluetooth
        - Bluejacking, blue snarfing
        - NFC security: turn off discoverable mode when not in use; apply firmware updates; watch for suspicious activity

    *Host security:*

    - What is Operating system security?
        - Issues: security settings, patch mgmt, trusted OS’s
        - Trusted operating systems - have undergone formal evaluation, known as the common criteria
        - **!! be familiar with the definition of trusted operating systems**
    - What is Malware prevention?
        - Malware = malicious software
        - Viruses - spread by human action
        - Worms - spread by themselves
        - Trojan horses - disguise themselves
        - Spyware - gathers information
        - Antimalware
            1. Signature detection - watches for known patterns of virus activity
            2. Behavior detection - watches for deviations from normal patterns of activity
            3. **!! the same software packages perform antimalware and antispyware functions**
            4. Spam filtering - removes unwanted email
    - What is Application management?
        - Application control - restricts software that may run
            1. Whitelisting - admins create a list of all the apps that may run on a system
            2. Blacklisting - admins create a list of the apps that are prohibited on a system
            3. Send apps control logs to your SIEM or log repo for analysis
        - Host software baselining - identifies expected system software
    - What is Host-based network security controls?
        - Default deny principle - block anything not explicitly allowed
        - Network firewalls - hardware devices that regulate connections between two networks
        - Host firewalls - software components of an operating system that limit connections to a server
        - **!! granting network access requires configuring both network and host firewalls**
        - IDS & IPS systems also come in both network or host based
    - What is Hardware security?
        - Cable locks
        - **!! remember to secure the other end of the locking cable**
        - Security tags
    - What is Virtualization security?
        - Modern datacenter leverage virtualization technology
        - Virtual machines are nothing more than files
        - As a security tool:
            1. Sandboxing untrusted software
            2. Testing security controls
        - Elasticity - expanding and contracting virtualized resources to meet changing usage demands on either a server or service basis
        - **!! virtualization platforms must be patched, just like operating systems and applications**
- **Domain 5: Identity and Access Management |** 30: 1, 5

    *IAM:*

    - What is IAM?
        - The set of controls and processes that ensure computer systems have consistent method to identify the entities authorized to access systems and resources, nd ensure that only authorized access occurs
        - IAM programs control physical and logical access to info, systems, devices, and facilities
    - What is IAA?
        - 1. Identification - claim identify; i.e. username
        - 2. Authentication - proves identity; i.e. password
        - 3. Authorization - user is allowed to access; i.e. ACLs
        - **!! remember that identification and authentication are separate and distinct steps**

    *Identification*:

    - How would you describe usernames, access cards, biometrics, registration & identity proofing?
        - **Usernames and access cards**
            - Usernames usually easily identify the individual, used for identification
            - Access cards often serve as proof of employment, may perform both identification and authentication
        - **Biometrics**
            - Something you are; used for both identification and authentication
            - 
        - **Registration and identity proofing**
            - Registration process: request > approval > identity proofing > issuance
                1. Separation of duties is critical in the registration process
            - Identity proofing: photo identification, fingerprinting, background checks

    *Authentication:*

    - What are Authentication factors?
        - Something you know: normally a password
        - Something you are: biometrics
        - Something you have: requires physical possession of a device
        - 1. False acceptance error: system misidentifies an individual as an authorized user, measures by the false acceptance rate (FAR)
        - 2. False rejection: system fails to recognize an authorized user, measured by false rejection rate (FRR)
    - What is Multi-factor authentication?
        - Combines authentication techniques from two or more of the authentication categories: something you know, something you have, something you are, somewhere you are, and something you do
        - I.e. password + smartcard / OTC, OTP to phone, fingerprint + PIN
        - Techniques must be different to be multifactor
        - **!! make sure examples of authentication techniques are really different factors**
    - What is Password authentication protocols (PAP)?
        - Does not use encryption, vulnerable to eavesdropping
        - CHAP is the secure alternative
    - What is SSO and federation?
        - Federated identity mgmt - individuals may have accounts across multiple systems, federated identity mgmt share identify info, this reduces the number of individual identities a user must have
            1. I.e. Google sign in, facebook sign in, etc.
        - Single-sign-on - authentication systems that shares a single authentication session across multiple systems, avoiding asking users to log in multiple times
    - What is RADIUS and TACACS?

        [https://lh6.googleusercontent.com/Ou2_ETwhQJYshdxW1bh-TR142UU2aDVIEPpZE0c48rh9Rhu-dTITP2ZzsNmPWK_bP4G0Vwt2xxTWSngy3hNtNCSepwna3fNvWPm32bD3aBfAbphnaATfRJfqOjsNXUVCxb7aymjF](https://lh6.googleusercontent.com/Ou2_ETwhQJYshdxW1bh-TR142UU2aDVIEPpZE0c48rh9Rhu-dTITP2ZzsNmPWK_bP4G0Vwt2xxTWSngy3hNtNCSepwna3fNvWPm32bD3aBfAbphnaATfRJfqOjsNXUVCxb7aymjF)

        - **!! remember that a RADIUS client is usually an application server**
        - TACACS is an alternative for RADIUS, current standard is TACACS+
            1. Improves by using TCP instead of UDP, fully encrypted authentication session, RADIUS does not
    - What is Kerberos and LDAP?
        - Ticket-based authentication system that allows users to authenticate to a centralized service and then use tickets to gain access to distributed services

        [https://lh6.googleusercontent.com/rUyHQ4x30TmYEOd5AVn9Rbs00E0_5HCJaIdAuJZZf3jbzzjuo-l-JbKnm8s9L4_cGBj2HRciEeZ-esmHDGLwvEFavaYbjwjpiN8uqIgaM48tHq883KxaMefM-W1-OOPpdYLJo1Dh](https://lh6.googleusercontent.com/rUyHQ4x30TmYEOd5AVn9Rbs00E0_5HCJaIdAuJZZf3jbzzjuo-l-JbKnm8s9L4_cGBj2HRciEeZ-esmHDGLwvEFavaYbjwjpiN8uqIgaM48tHq883KxaMefM-W1-OOPpdYLJo1Dh)

        - LDAP - provides the means to query a centralized directory service, such as Microsoft Active Directory
        - Kerberos handles authentication, LDAP provides means to query info stored in the directory service
        - PORTS
            1. Kerberos uses port 88
            2. LDAP uses port 389
            3. Secure LDAP uses port 636
        - NTLM was the windows standard before Kerberos, should not used anymore; weak encryption and vulnerable to pass the hash attack
    - What is SAML?
        - Security assertion markup language - allows SSO within a web browser across a variety of systems
        - Benefits: true SSO experience for end users, no credential access for service providers
    - What is Identity as a service (IDaaS)?
        - Allows orgs to move IAM to the cloud
        - 1. Directory integration - synchronize with an orgs existing on-prem or cloud based directory to brain user info
        - 2. Application integration - replace the authentication services for many SaaS products, simplifying the user and admin experience
        - IDaaS allows the user of multi factor authentication
    - What is OAuth and OpenID Connect?
        - OAuth - authorization protocol designed to work across a variety of web services
        - OpenID Connect - identification and authentication protocol designed to work with OAuth
    - What is Certificate-based authentication?
        - Digital certs contain a signed copy of a user’s public key
        - 

            [https://lh6.googleusercontent.com/cqvxfdrrdt39lmLVcNyS5Nvz5ze85rRb7dmo2_d4bQHopmVkIMEm97Mnf7amo8iGoe_ISao3og-KyRRgDSE0AYjXPinSaSviUDKr5UkI7kaVXARmqYLMCPbdTMp2F9Ya64SzF_ZA](https://lh6.googleusercontent.com/cqvxfdrrdt39lmLVcNyS5Nvz5ze85rRb7dmo2_d4bQHopmVkIMEm97Mnf7amo8iGoe_ISao3og-KyRRgDSE0AYjXPinSaSviUDKr5UkI7kaVXARmqYLMCPbdTMp2F9Ya64SzF_ZA)

        - Certificate authorities create digital certs for public keys used in authentication
            1. Used in SSH connection, smart cards (PIV/CAC), network access (802.1x)

    *Accountability*:

    - What is accountability?
        - The ability to race every action taken on a system back to an individual user without any ambiguity, and without allowing the user to deny responsibility for that action
        - 1. Identification - each user must have a UNIQUE identifier, such as a username. There may be no use of shared or generic accounts.
        - 2. Authentication - strong authentication prevents unauthorized users from gaining access. IT also prevents users from denying their activity
        - Logs must be secure - key point in Domain 7
    - What is Session management?
        - Uses timeouts and screensavers to disconnect user sessions that have going idle .this prevents an unauthorized individual from taking control of an abandoned user session
        - Timeouts:
            1. Disconnect user sessions after a predetermined time
            2. Disconnect user sessions after a period of inactivity
            3. Require re-authentication for sensitive activities
        - Screensavers are a common timeout mechanism

    *Credential Management:*

    - What is account and privilege management?
        - Least privilege - users should have only the minimum set of permissions necessary for their job function
        - Separation of duties - sensitive functions should require action by two separate users
        - Job rotation - regularly move people between jobs to prevent fraud
        - Mandatory vacation - enforce periods of time when employees have no access to systems
        - Account mgmt lifecycle:
        - 

            [https://lh3.googleusercontent.com/Cmw9oF8pYEQJfTuP69OH6NLt3P0hVKHhfC7o-s4jXj8Nov9lYQl8nFpYwe8Qt22nlhxLT05J0lfBmLpXgOFfn1VdZZV6VzHfdQs-MgDKGH5hIAk4seapSI6I8hFo28ewU3TL5wRs](https://lh3.googleusercontent.com/Cmw9oF8pYEQJfTuP69OH6NLt3P0hVKHhfC7o-s4jXj8Nov9lYQl8nFpYwe8Qt22nlhxLT05J0lfBmLpXgOFfn1VdZZV6VzHfdQs-MgDKGH5hIAk4seapSI6I8hFo28ewU3TL5wRs)

    - What is GPO?

        Group policy objects (GPO) - apply config settings to users and computers

    - What are Password policies?
        - Password length: at least 8 characters
        - Password complexity: alphanumeric mixed
        - Password expirations: forces users to change passwords periodically
        - Password history and reuse
        - Account lockout: after several unsuccessful attempts
        - Disable unused account
    - How do you manage roles?
        - Roles group permissions - allowing shared security settings
        - Windows security groups - implement role-based security
            1. Simplify account mgmt
            2. Admins may assign permissions to new user by adding a role to that user
        - Roles eliminate dangers - shared and generic accounts
    - What is account monitoring?
        - Account security issues:
            1. Inaccurate permissions - prevent legitimate work, grant extra access (privilege creep)
            2. Illegitimate account use - unauthorized use of permitted access
        - User access review should be performed
            1. Perform listing of user permissions, review permissions with mgrs, make any necessary changes, focus on users who recently changed roles
        - Continuous account monitoring
            1. Alert admins to strange activity
            2. Flag unusual activity such as: unusual login locations, strange login times, deviations from normal behavior, bulk downloading of sensitive info
    - What is Provisioning and deprovisioning?
        - Provisioning - after onboarding, admins create authentication credentials an grant appropriate authorization
        - Deprovisioning - during offboarding process, admins disable accounts and revoke authorizations at the appropriate time
        - 1. Normal workflow - disables accounts on a scheduled basis for planned departures
        - 2. Emergency workflow - immediately suspends access when user is unexpectedly terminated

    *Authorization*:

    - What is Authorization?
        - Least privilege
            1. Limits potential damage from an insider attacks
            2. Restricts the ability of an external attacker to leverage a compromised account
        - Separation of duties
        - Privilege creep - situation that occurs when a user accumulates excess permissions after shifting job responsibilities one or more times
            1. Account reviews limit privilege creep
        - **!! be able to identify least privilege and separation of duties**
    - What is MAC?
        - Access control system where the OS enforces security policies that users may not modify, usually implemented as a rule-based OS
        - Security-enhanced Linux (SELinux) uses mandatory access controls
    - What is DAC?
        - Access control system where permissions may be set by the owners of files, computers, and other resources - most common type.
        - Windows NTFS permissions are an example
    - What are ACLs?
        - Resource owners set DAC permissions through the use of access control lists
        - NTFS permissions:
            1. Full control
            2. Read
            3. Read & execute
            4. Write
            5. Modify
    - What is Database access control?
        - Microsoft SQL server authentication types:
        - 

            [https://lh6.googleusercontent.com/rwjsWPh7wBPawg7KHAab8RmfXCpYiZg9bQfZJo_2TFuzvOTNSkSKnF4N4haNQMpFY6IIAO2MIwTxNytgEa5Rzi5vngbA1PGNLj7y8aTc6hteIWcZ-41WdW6ASt79sUui_Nq7IzfV](https://lh6.googleusercontent.com/rwjsWPh7wBPawg7KHAab8RmfXCpYiZg9bQfZJo_2TFuzvOTNSkSKnF4N4haNQMpFY6IIAO2MIwTxNytgEa5Rzi5vngbA1PGNLj7y8aTc6hteIWcZ-41WdW6ASt79sUui_Nq7IzfV)

        - Microsoft SQL server authorization types:
            1. Role-based authorization - manages permissions through roles that are assigned to users by admins
            2. Account-based authorization - manages permissions by making explicit permission grants to each account
    - What are Advanced authorization concepts?
        - Implicit deny principle - any action that is not explicitly allowed must be denied
        - **!! the implicit deny rule is a critical concept on the exam**
        - Role-based access control - permissions are grouped together into functional roles and users are assigned to those roles
        - Time of day restrictions limit the use of resources during certain hours

    *Access Control Attacks:*

    - What are Watering hole attacks?
        - Websites spread malware effectively
            1. Users trust the websites they visit, to some extent
            2. Browsers and add-ons often have vulnerabilities
            3. Users are conditioned to click OK on security warnings
        - 

            [https://lh6.googleusercontent.com/H83Vzlqj8_4fARQRlG63IASOxFEJkRBNBH4FIf9kyCZVVSFTxWKjASL2tFJecHQcuZ1DAanrxICKFwL3i6iDP3dhsyLbwmYZ5EUmOioP2Z_W00oyOvwHC_H-9TzAbrv4dmWDDF5E](https://lh6.googleusercontent.com/H83Vzlqj8_4fARQRlG63IASOxFEJkRBNBH4FIf9kyCZVVSFTxWKjASL2tFJecHQcuZ1DAanrxICKFwL3i6iDP3dhsyLbwmYZ5EUmOioP2Z_W00oyOvwHC_H-9TzAbrv4dmWDDF5E)

    - What are Social engineering attacks?
        - Manipulating people into divulging info or performing an action that undermines security
        - There are six main reasons that social engineering attacks are successful. These include authority and trust, intimidation, consensus and social proof, scarcity, urgency, and familiarity in liking.
        - Education is the solution.
    - What are Impersonation attacks?
        - SPAM - unsolicited email
        - Phishing - stealing credentials
        - Spear phishing - targeted attack
        - Whaling - targeted attacks on executives
        - Vishing - voice phishing
        - SPIM - instant messaging spam
        - Spoofing - faking an identity
- **Domain 6: Security Assessment and Testing |** 22: 2

    *Threat assessment:*

    - What are Security assessment tools?
        - Vulnerability assessment tools:
            1. Passive - observe activity
            2. Active - interact with machines, can disrupt
        - Honeypots - attractive decoy machines
        - Honeynets - decoy networks
        - Protocol analyzers - peek into network traffic
    - How do you Scan for threats and vulnerabilities?
        - 1. Port scanners
            1. Scan ports , probe system for open network ports
        - 2. Vulnerability scanners
        - 3. Application scanners
        - I.e. NMAP
    - What are Threat assessment techniques?
        - Baseline reporting
            1. Provides initial review of a system’s security status
            2. Compares the current config to the expected baseline config
            3. It can be automated with tools, i.e. MBSA (microsoft baseline security analyzer)
        - Attack surface reviews
            1. Enumerates the “attack surface”, all possible paths of attacks
            2. Makes heavy use of port, vulnerability, and application scanners
            3. Adopts the mindset of an attacker
        - Code review
            1. Performs assessments of software security
            2. Includes peer code review for an extra set of eyes to detect security issues
            3. Should be a mandatory part of promotion and release process for new code
        - Architecture review
            1. Dissects how everything fits together
            2. Analyzes the interaction of various systems
    - What is Penetration testing?
        - Testers actually attack systems and networks
        - They verity that threats exist and exploit known vulnerabilities
        - They also test security controls by attempting to bypass/defeat them
        - 

            [https://lh6.googleusercontent.com/K3hTZcwtgaCkyTDX9FcksLwz7BsO2cncLDYcFLwDLx6h_2eGYofXI_dN5RGbuL3u-SlzZ6k998E3Mzg8KJzWsxbnoP70dYzaN7wW3VZAeIGL4DzanciFTFuHPU0uPfTYF1qrQD-p](https://lh6.googleusercontent.com/K3hTZcwtgaCkyTDX9FcksLwz7BsO2cncLDYcFLwDLx6h_2eGYofXI_dN5RGbuL3u-SlzZ6k998E3Mzg8KJzWsxbnoP70dYzaN7wW3VZAeIGL4DzanciFTFuHPU0uPfTYF1qrQD-p)

        - Types:
            1. White box - attackers have full knowledge of the network environment
            2. Black box - attackers have no knowledge of the network environment
            3. Gray box - attackers have some knowledge of the network environment
    - What is non-intrusive and intrusive scanning?
        - Non-intrusive scanning - a safe mode that won't disrupt system operation
        - Intrusive scanning - a dangerous mode that might disrupt system operation

    *Log monitoring:*

    - What is monitoring log files?
        - Requires regular review
        - Reporting automation
            1. Alarms and alerts - proactively notify you of suspicious activity
        - Trend analysis
            1. Points out activity that deviates from past patterns
        - **!! practice interpreting log files before taking the CISSP exam**
    - What is Security information and event management (SIEM)?
        - Systems generate far too many log records for manual analysis
        - AI can help solve security data overload
        - 1. Central, secure collection point for logs
        - 2. Source of AI
        - SIEM has access to log entries from across the org

    *Software testing:*

    - What is code review?
        - Use peer analysis to assess code
        - Fagan inspections follow a formalized, six-step code review process:
            1. Planning - prep materials, identifying participants, schedule review
            2. Overview - assign roles to participants
            3. Preparation - participants review code
            4. Meeting - reviewers discuss and formally identify any code defects
            5. Rework - developers correct code defects
            6. Follow-up - leader verifies that defects were corrected
        - Most orgs use a less formal review process, usually modified Fagan inspections
    - What are code tests?
        - Code tests - use technology to inspect software
            1. Static - use automated techniques to analyze code for errors and security flaws without actually executing it
            2. Dynamic - execute code to verify that it is functioning correctly and does not have security flaws
        - Synthetic transactions supply inputs to code with known, expected outputs - important for dynamic testing
        - **!! code review, static testing, and dynamic testing are complementary, rather than competitors**
    - What is fuzz testing?
        - Software testing technique that feeds software many different input values in an attempt to cause an unpredictable state or unauthorized access
        - Only fuzz test with permission!
    - What is Interface testing?
        - APIs - define interactions between systems, must be tested carefully
        - UIs and physical interfaces should be tested
    - What is Misuse case testing?
        - Evaluates software from the attacker’s perspective, related to pentesting
        - Brainstorming sessions are an effective way to develop misuse cases
        - Should use developers who worked on the project as well as “fresh eyes”
        - Examples:
            1. Unexpected input (in size or input)
            2. Missing input
            3. Injection attacks
            4. Unavailable funds
    - What is Test coverage analysis?
        - Test coverage - percent of software tested
        - Computing test coverage: test coverage = case tested/total cases
        - Variables - use cases, functions, lines of code, conditional branching

    *Disaster recovery:*

    - What is DR?
        - Disaster recovery capabilities are designed to restore a business to normal operations asap. Disaster recovery is a subset of business continuity
        - RTO - recovery time objective: max amount of time that it should take to recover a service after a disaster
        - RPO - recovery point objective: max time period from which data may be lost in the wake of a disaster
        - **!! disaster recovery efforts end only when the business is operating normally in its primary facility**
    - What are Backups?
        - Provide a data “safety net”
        - Backup media:
            1. Tape backups
            2. Disk-to-disk backups
            3. Cloud backups
        - Back up types:
        - 

            [https://lh5.googleusercontent.com/_gIzv6fKKFxhDqjzB0gJ5mbWy-4iTjtQ-AEWPAGCtcBXeOWwk9lLrvWoD8TtJFHayslDDivxUDbu0FTsIu9vGdaucw_f-nKAtiCsIDlOjN9P4BGCnrx0GDNW98awrottZ3vHvplu](https://lh5.googleusercontent.com/_gIzv6fKKFxhDqjzB0gJ5mbWy-4iTjtQ-AEWPAGCtcBXeOWwk9lLrvWoD8TtJFHayslDDivxUDbu0FTsIu9vGdaucw_f-nKAtiCsIDlOjN9P4BGCnrx0GDNW98awrottZ3vHvplu)

        - **!! understand what backups need to be restored in the event of a disaster**
        - Incremental use less space but take more time
        - Media rotation strategies - allows restore of backup media
            1. GFS (grandfather-father-son)
    - What is Validating backups?
        - Verifying backups is a critical availability control
        - Built-in backup verification - validates backup completion
        - Backup logs are only useful if someone actually reviews them
        - Regularly test backups
            1. Request a single file restoration from a specific point in time
            2. Request the restoration of a server or an entire service
    - What are Disaster recovery sites?
        - Provide alternate data processing
        - Hot - full operational DCs, very expensive
        - Cold - empty DCs, stocked with core equipment, network, and environmental controls, inexpensive but takes much longer to activate
        - Warm - stocked with all necessary equipment and data, data not maintained in parallel fashion
    - What is Testing BC/DR plans?
        - Goals:
            1. Validate the plan functions correctly
            2. Identify necessary plan updates
        - DR test types
            1. Read-through: aka checklist reviews, ask each team member to review their role in the DR process and provide feedback
            2. Walk-through: gather team together for a formal review of the DR plan, aka Tabletop exercise
            3. Simulation test: use a practice scenario to test the DR plan
            4. Parallel test: activate the DR facility, but do not switch operations there
            5. Full-interruption test: switch primary ops to the alternative facility, and can be very disruptive to business - rare
        - DR testing strategies often combine multiple types of tests, prepare written report at the conclusion of each test

    *Assessing security processes:*

    - What is Management review and approval?
        - Verify accuracy and completeness
        - Create a culture of oversight
        - Privileged user action reviews
            1. Override normal security controls
            2. Need careful management oversight
            3. Require vetting and authorization
        - Account management reviews
            1. Every active user is associated with a current employee
            2. Permissions are appropriate
            3. Changes were approved and documented
    - What are Security metrics?
        - Security metrics should be defined in advance
        - Metric types:
            1. KPI - demonstrate the success of the security program present backward-looking perspective on security
            2. KRI - predict the likelihood of future risks materializing
            3. Present forward-looking perspective on security
        - ITIL security KPIs
            1. Decrease in breaches
            2. Decrease in breach impact
            3. Increase in strong SLAs
            4. Number of new controls
            5. Time to implement controls
            6. Number of major incidents
            7. Number of incident-related outages
            8. Number of training events
        - KRI criteria
            1. Business impact
            2. Effort to implement, measure , and support
            3. Reliability
            4. sensitivity
    - What are Audits and assessments?
        - Evaluate security controls, report on their effectiveness, recommend improvements
        - Assessments are usually requested internally, while audits are often imposed by external requirements
        - Audits follow a formal standard and used planned tests, should have clearly defined scopes
        - User access reviews - validate rights and permissions
        - **!!user access reviews are a common source of questions on the exam**
    - What is control management?
        - Orgs should test controls regularly
        - Every rule as an exception
            1. Exceptions must be carefully managed
        - Compensating controls mitigate the risk of exceptions
- **Domain 7: Security Operations |** 27: 1

    *Investigations & forensics:*

    - Describe Conducting investigations in detail.
        - Administrative investigations - investigate internal issues
            1. Seek to resolve technology issues
            2. Restore normal operations as quickly as possible
            3. Involve root cause analysis
            4. May also look into HR
            5. Have low standards of evidence
        - Criminal investigations - carried out by government and law agencies
            1. Involve the possibility of fines and jail time
            2. Use the **beyond a reasonable doubt** standard of evidence
        - Civil investigations - non criminal offenses involving dispute between two parties
            1. Do not involve the possibility of fines and jail time
            2. Use the **preponderance of the evidence** standard
        - Regulatory investigations - conducted by government
            1. May be civil or criminal in nature
            2. Regulatory investigations may involve compliance with industry standards - these are always civil cases
            3. Interviews are a valuable tool available to investigators
        - **!! cybersecurity investigators should leave interrogations to law enforcement**
    - What are evidence types?
        - Real evidence - consists of tangible objects
        - Documentary evidence - consists of written info
            1. **Authentication rule: Documents must be authenticated by testimony**
            2. **Best evidence rule: original documents are superior to copies**
            3. **Parol evidence rule: written contracts are assumed to be the entire agreement**
        - Testimonial evidence - consists of witness statements
            1. Direct evidence - witness provides evidence based upon his or her own observations
            2. Expert opinion - expert witness draws conclusions based upon other evidence
            3. Testimonial evidence may not consist of hearsay
    - What is forensics?
        - Investigative techniques that collect, preserve, analyze, and interpret digital evidence
        - Investigations must never alter evidence
        - Volatility - relative permanence of a piece of evidence; evidence that may not last long is more volatile than more permanent sources of evidence
            1. More volatile evidence should be gathered first
                - Network traffic
                - Memory contents
                - System and process data files
                - Logs
                - Archive records
    - What is System and file forensics?
        - Write blockers, aka forensic disk controllers, prevent accidental modification of disks during imaging
        - Hashes protect evidence - they provide a unique file signature
            1. Use to demonstrate that a file has not been altered
        - **!! never try to perform forensic yourself unless you’ve received appropriate training**
    - What is Network forensics?
        - Wireshark monitors networks, capturing full packet data
        - Full packet capture requires lots of storage
        - Netflow summarizes traffic - providing high-level info
            1. IP addresses and ports
            2. Timestamp
            3. Amount of data transferred
            4. Routers and firewalls capture netflow data
    - What is Software forensics?
        - Intellectual property - software forensics may be used to resolve IP disputes between two parties
        - Malware origins - software forensics may be used to identify the author of malicious software found on a system
    - What is Embedded device forensics?

        special=purpose computers located inside smart devices found in homes, businesses, and industrial settings - i.e. cars

    - What is Chain of custody?
        - Provides paper trail for evidence
        - Evidence logs must be available to present in court
    - What is E-discovery?
        - 3 major steps - preservation > collection > production
        - Litigation holds require the preservation of relevant electronic and paper records

    *Logging & monitoring:*

    - What Correlates security event information?
        - SIEM
            1. Central, secure collection point for logs
                - All systems send log entries directly to the SIEM
            2. Source of AI
                - SIEMS detect patterns that other systems might miss
    - What is Continuous security monitoring?
        - Maintaining ongoing awareness of information security, vulnerabilities, and threats to support org risk mgmt decisions
        - NIST SP 800-137

        [https://lh5.googleusercontent.com/eFvMGWH2hGL-lwTgWE3pq7L418aiu4RDSMI77A4ceSyA-Ky0YTMQYeGypReASM2lYEgz62KsPEPjOJxZVQRnMi3kOgqhYGQeHQapO5P55CkXd8xThan2C6uzZrsTVyTCRYIDgpqh](https://lh5.googleusercontent.com/eFvMGWH2hGL-lwTgWE3pq7L418aiu4RDSMI77A4ceSyA-Ky0YTMQYeGypReASM2lYEgz62KsPEPjOJxZVQRnMi3kOgqhYGQeHQapO5P55CkXd8xThan2C6uzZrsTVyTCRYIDgpqh)

    - What is Data loss prevention (DLP)?
        - Tech solutions that search systems and monitor networks for sensitive info that is unsecured and provide the ability to remove the information, block the transmissions, or encrypt the stored data
        - Host based DLP - uses software agents installed on a single system
        - Network-based DLP - scans network transmissions for sensitive info
        - Pattern matching - recognizes known patterns of sensitive info such as SSNs
        - Watermarking - identifies sensitive info using electronic tags

    *Resource security:*

    - What is Physical asset management?
        - Build an asset inventory - integrate it with other processes
        - Media mgmt - tracks highly sensitive data
    - What is Change and configuration management?
        - Ensure that an org follows a standard process for requesting, reviewing, approving, and implementing changes to info systems
        - Request for change (RFC)
            1. Description of change
            2. Expected impact
            3. Risk assessment
            4. Rollback plan
            5. Identify of those involved
            6. Proposed schedule
            7. Affected configuration items
        - Changes must be approved by relevant authorities
        - Config mgmt - tracks specific device settings
        - Baselines - provide a config snapshot
        - Versioning - assigns numbers to each version
    - What is Virtualization?
        - Host machines run on physical hardware
        - Host machines provide services to several virtualized guest machines
        - The hypervisor tricks each guest into thinking it is running on dedicated hardware
        - Type 1 hypervisor (common in enterprise):
            1. 

                [https://lh4.googleusercontent.com/Fpc4jxZOozietuOwh6zkStrIDINpQ9ML32YWxy9fpeOaReRjIMg1g3R-IUirqYNyDIlvl462_0jskAb4V1ccdFwYWvvUDTa-SeBBnsFeB-jGGiHLfgwyRknTnE6YoHbidi3Fk4AD](https://lh4.googleusercontent.com/Fpc4jxZOozietuOwh6zkStrIDINpQ9ML32YWxy9fpeOaReRjIMg1g3R-IUirqYNyDIlvl462_0jskAb4V1ccdFwYWvvUDTa-SeBBnsFeB-jGGiHLfgwyRknTnE6YoHbidi3Fk4AD)

        - Type 2 Hypervisor (common in personal):
            1. 
            2. **Virtualization security**

                [https://lh4.googleusercontent.com/MYUYxsqR2cYqE4NyMJBnYu7IgwdZLbGCbcPNnv-WS6N6jcLdfgRXF0K20Wk6jQHMFXosqdTzSM_7fjU1TFwQ_89zipZTMFjdc9CiqT0m5MbIUro-Elf2_x25KMwWdB9qTv5gNcQc](https://lh4.googleusercontent.com/MYUYxsqR2cYqE4NyMJBnYu7IgwdZLbGCbcPNnv-WS6N6jcLdfgRXF0K20Wk6jQHMFXosqdTzSM_7fjU1TFwQ_89zipZTMFjdc9CiqT0m5MbIUro-Elf2_x25KMwWdB9qTv5gNcQc)

        - Virtual machines are nothing more than files
        - Elasticity - expanding and contracting virtualized resources to meet changing usage demands on either a server or service basis
        - Virtual SANs - pool storage resources across VMs
        - **!! virtualization platforms must be patched, just like OSs and Apps**
    - What are Cloud computing models?
        - Cloud computing is the next logical advance in enterprise IT
        - Cloud computing 0 the delivery of computing services over a network
        - Private cloud - org uses a dedicated cloud infrastructure
        - Public cloud - org uses a shared tenancy infrastructure
        - Hybrid cloud - org uses both private and public cloud
        - **!! no cloud model is inherently superior to the other approaches, it all depends upon the context**
    - What are public cloud tiers?
        - Software as a service - SaaS - customer purchases an entire app
        - Infrastructure as a service - IaaS - customer purchases servers/storage
        - Platform as a services - PaaS - customer purchases app a platform

    *Security principles:*

    - What is Need to know and least privilege?
        - Limits information access
        - Least privilege - limits system permissions
        - Privilege aggregation jeopardizes least privilege
    - What is Separation of duties and responsibilities?
        - No individual should possess two permissions, that in combination, allow them to perform a highly sensitive action
        - Two-person control - requires the authorization of two separate individuals to carry out a sensitive action; aka dual control
    - What is Privileged account management?
        - Password vaulting - store admin passwords
        - Command proxying - eliminate the need for direct server access
        - Monitoring - log administrative user activity
        - Credential management - rotate passwords and access keys

    *Incident management:*

    - What is an IR program?
        - **Build an incident response program**
            - IR program components:
                1. Policy and plan documentation
                    - Policy provides foundational authority for the program
                    - Defines incidents that fall under the policy
                    - Includes incident prioritization scheme
                2. Procedures for incident handling
                    - Contain the details of your plan
                3. Guidelines for communicating externally
                4. Structure and staffing model for the team
                5. Description of relationships with other groups
    - What is Incident identification?
        - First responders must act fast - isolate affected systems
        - **!! the highest priority of a first responder must be containing damage through isolation**
    - What is mitigation?
        - Control damage and loss to the org through containment
        - Containment strategy evaluation
            1. Damage potential
            2. Evidence preservation
            3. Service availability
            4. Resource requirements
            5. Expected effectiveness
            6. Solution timeframe
            7. mitigation ends with stability - business functioning without danger
    - What is Recovery and reconstitution?
        - Remove effects of the incident and return to normal operations
        - Reconstitution corrects vulnerabilities
        - Use a phased approach to recovery and reconstitution
    - What is Lessons learned and reporting?
        - Provides incident responders with an opportunity to reflect on the incident response efforts and offer feedback that will improve the orgs response to future incidents
        - Use a trained facilitator
        - Create a report that includes lessons learned and recommendations

    *Personnel safety:*

    - What is Employee safety?
        - **!! watch for tricky questions that ask your to prioritize other actions over personal safety**
        - Human life is FIRST PRIORITY
    - What is Emergency management?
        - Emergency mgmt plans should be based upon a risk assessment
        - Every organization must develop its own, unique, emergency management plan that reacts to the geographic, structural, and operating characteristics of their business environment.
- **Domain 8: Software Development Security |** 17: 1, 2

          *SDLC:*

    - What are Development methodologies?
        - Begin with business requirements and translate them into a design
        - Waterfall model
        - Spiral model
        - Agile approach
    - What are Maturity models?
        - Maturity Models provide a way for organizations to evaluate themselves against a standard benchmark and identify the next steps in evolving their software development practices.
        - SW CMM - software capability maturity model - assesses an orgs software development practices:
            1. 

                [https://lh4.googleusercontent.com/C0aW263cj41nz-l9FJ6C0GayM8dO-w7hYF7dDteRod2kNrSMkktehi8I9ezY0C-pBO1KVLLJ8XWbCr7RAQKtd9zUdCMndnW_gErJ_vWEOMK7gWR0Q5cn8fjibWmBD-4rnb_GTZTu](https://lh4.googleusercontent.com/C0aW263cj41nz-l9FJ6C0GayM8dO-w7hYF7dDteRod2kNrSMkktehi8I9ezY0C-pBO1KVLLJ8XWbCr7RAQKtd9zUdCMndnW_gErJ_vWEOMK7gWR0Q5cn8fjibWmBD-4rnb_GTZTu)

        - IDEAL model:
            1. Initiating, Diagnosing, Establishing, Action, Learning
    - What is Operation, maintenance, and change management?
        - Software development is never finished, until decommissioned
        - Change management
            1. Request control - request control manages, evaluates, and prioritizes inbound requests from customers
            2. Change control - grants permission for devs to make changes to app code
            3. Release control - moves the code from the dev environment into production
    - What is DevOps?
        - Merging two words - development and operations
        - Goals:
            1. Build collaborative relationships
            2. Embrace automation
            3. Facilitate rapid release of code
            4. Provide a stable operating environment
        - Devops and agile are deeply related - both seek continuous integration
        - Infrastructure as Code - scripts the creation of resources; advantages:
            1. Increases scalability of environments
            2. Reduces user error
            3. Facilitates testing of new code

    *Software security issues:*

    - What is cross-site scripting (XSS)?
        - An attacks tricks user’s browser into downloading a script from one site and executing it on another site
        - If the user is logged into the second site, the command may succeed
        - Requirements:
            1. Reflected input - input provided by the user is later displayed to other users
            2. Unvalidated input - input not scrubbed for security issues
        - Protect by Validating all user input, input validation
    - How do you Prevent SQL injection?
        - Applications request data from DB using SQL
        - **!! know how SQL injection attacks work**
        - Semicolons separate SQL statements
        - Two dashes indicate comments
        - Single quotes are critical to SQL injection
        - Defend using input validation and parameterized queries
    - What is Privilege escalation?
        - Gains admin access
        - Attacks often exploit buffer overflow vulnerabilities
        - Perform input validation, patch, enforce least privilege principle, use DEP and ASLR
    - What is Directory traversal?
        - This attack allows an attacker to manipulate the file system structure on a web server
        - Use input validation and set strict file system access controls
    - What are Overflow attacks?
        - Excess input - making app function not as expected
        - Protect with input validation
    - What are Cookies?
        - Data stored by websites in the browsers of users, particularly useful to recognize users, used to remember information
        - Can be used across sites
    - What are Code execution attacks?
        - Occurs when an attacker exploits a vulnerability in a system that allows the attacker to run commands on that system
        - Arbitrary code execution - attacker runs commands of their choice
        - Remote code execution - take place over a network connection
        - Protect by limiting admin access, patch,

    *Secure coding practices:*

    - What are Code repositories?
        - Store softwares source code, perform version control, coordinate changes among multiple devs
        - Promote code reuse
    - What is Third-party code?
        - Library - contains shared software code
        - Software development kit (SDK) - provides programming resources
        - Application programming interface - provides programming resources
    - What is Code signing?
        - Digital signatures provide nonrepudiation
        - Code signing applies digital sigs to software

    *Software security assessment:*

    - What is Software Risk analysis and mitigation?
        - Risk analysis identifies issues, mitigation reduces their likelihood and impact
        - Integrate security with the SDLC - avoid bolt-on security
        - Mitigate software risks:
            1. Input validation
            2. Encrypt sensitive data
            3. Enforce least privilege principle
            4. Test all code prior to development
    - What is Software testing?
    - What is Acquired software?