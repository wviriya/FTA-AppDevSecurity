# Secure Software Development Lifecycle
Security should be built into an application to make it more resilient against attacks. Any control or solution that you apply after the software is shipped can only do so much to reduce the likelihood of exploitation if the code is filled up with vulnerabilities. In this session, we would talk about the strategies that you can deploy and the frameworks that you can adopt to make security a part of your design.

## The frameworks
There are many secure software development frameworks being used out in the world but two of them are very popular:
1.	Microsoft Secure Development Lifecycle.
2.	SafeCode fundamental practices for Secure Software Development.

## Basic Components of Secure Software Development


### Design

#### 1. Secure Design Principles

- **Economy of mechanism:** keep the design of the system as simple and small as possible.
- **Fail-safe defaults:** base access decisions on permission (a user is explicitly allowed access to a resource) rather than exclusion (a user is explicitly denied access to a resource).
- **Complete mediation:** every access to every object must be checked for authorization.
- **Least privilege:** every program and every user of the system should operate using the least set of privileges necessary to complete the job.
- **Least common mechanism:** minimize the amount of mechanism common to more than one
user and depended on by all users.
- **Psychological acceptability:** it is essential that the human interface be designed for ease of use, so that users routinely and automatically apply the protection mechanisms correctly.
- **Compromise recording:** it is sometimes suggested that mechanisms that reliably record that a compromise of information has occurred can be used in place of more elaborate mechanisms that completely prevent loss.
- **Defense in depth:** design the system so that it can resist attack even if a single security vulnerability is discovered or a single security feature is bypassed. Defense in depth may involve including multiple levels of security mechanisms or designing a system so that it crashes rather than allowing an attacker to gain complete control.
- **Fail securely:** a counterpoint to defense in depth is that a system should be designed to remain secure even if it encounters an error or crashes.
- **Design for updating:** no system is likely to remain free from security vulnerabilities forever, so developers should plan for the safe and reliable installation of security updates.


#### 2. Threat Modelling
**How does threat modelling differ in the cloud?**
The purpose of cloud threat modeling (threat modeling of cloud systems and services) is like that of non-cloud threat modeling. In both cases prioritized mitigations are derived, an assessment of security considerations is made, and threats are identified.
If you make use of PaaS or SaaS services in your organization, you might have to focus on the capabilities of the service whike keeping in mind the shared responsibilities model.

Purpose of threat modelling
- Identifying, analyzing, and rating security threats
- Producing prioritized mitigations
- Assisting and informing attack surface analysis and risk reduction

Polular threat modelling methodologies
- STRIDE (Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, Elevation of privilege)
- MITRE ATT&CK
- OWASP Threat Modelling
- PASTA(Process for Attack Simulation and Threat Analysis)

Core Threat modelling activities in the cloud:
1. **Identify threat modeling security objectives**: Identify security objectives and requirements.  What are the organization’s policies and business needs? Also identify the target system’s architecture, including its components, roles, services, and dependencies. As a complement to standard goals setting for a threat modeling exercise (identifying most impactful controls or most pressing threats, protecting confidentiality, etc.), it is important to set cloud threat modeling security objectives, such as identifying the most risk-averse cloud service and 
deployment models (IaaS, PaaS, SaaS) to determine whether “cloud” or cloud architecture (such as PaaS and multi-tenancy) are permissible.
2. **Set the scope of the assessment**: Provide an overview of the systems or applications under review (data, applications, systems, users, controls, etc.) by identifying and scoring assets. 
    - Is the PaaS control plane in scope?
    - Is the cloud account in scope?
    - Is it advisable to make an inclusive scoping?
3. **System and application decomposition**: This typically covers breaking down the system into subsystems and examines the interaction among the various smaller components. Decompose the system further to identify how it functions and how those functions can be vulnerable. For example, how does the application ensure the confidentiality of data in transmission? 
    - Understand trust boundaries (external facing, internal facing, privileged, 
unauthenticated, etc.). Understand cloud trust boundaries like trust in and segregation controls against the CSP#, cross service and account trust, and multi-tenancy segregation controls.
    - Identify entry and exit points to the system (input and output) and format. Consider cloud unique entry points such as cloud management API, managed API gateways, inbound and outbound connectivity, and integrations. Furthermore, map crosscloudcross cloud services relationships.
    - Map the data flows in the system. Consider cloud unique data flows and stores such as cloud EMR# and ETL services, blob storage, and account log trails.
4. **Identify and rate the threats**: Identify the threats, type of attacks, and the various ways a given system, or its functionalities can be misused by an external attacker or malicious user. Identify cloud unique threats using industry resources such as the CSA Top Threats. Do not neglect to assess threats to “Availability” even though many controls to that end would be baked in the CSA platform and infrastructure. Give special consideration to human errors, 
insider threats, misconfigurations, and poor design.
5. **Identify weaknesses and gaps in the system design and components** to aid the security decisions and define the scope and nature of security testing. Consider common and impactful cloud design, implementation weaknesses, and account for defense-in-depth design/controls: 
    - Egregious Eleven #2 - Misconfiguration and Inadequate Change Control
    - EE #3 - Lack of Cloud Security Architecture and Strategy
    - EE #4 - Insufficient Identity, Credential, Access, and Key Management
    - EE #7 - Insecure Interfaces and APIs
5. **Design and prioritize mitigations and controls** applicable to the predetermined threats and reflect how those controls would reduce the threat or risk level. Leverage cloud security controls (matrix) and focus on controls that disrupt cloud threats, including “attack kill chains,” even when some cloud and application misconfigurations and weaknesses are in place.
6. **Communicate and call to action**: Communicate the identified threats, their potential impact and severity as well as the applicable and proposed controls. Make the modeling data and insights available. Communicate cloud design decisions and core enabling cloud controls.
7. **Periodic reevaluation**: Cloud platforms are rapidly evolving and never static; hence, the threat model needs to be, too. Periodic review and update of the threat model will ensure that the threat model remains relevant and highly useful to the team. This is especially true if there are material changes to the overall architecture (for example, components/services added or removed, etc.). An outdated threat model may lull the team into a false sense of security where new threat vectors are not considered and thus not evaluated. 

#### 4. Develop an Encryption Strategy



### Secure Coding Practices

### Manage inherent risk posed by third party software

### Perform Static Analysis, Dynamic Analysis and Penetration testing

### Manage Security Findings

### Manage Response and Disclosure 




 