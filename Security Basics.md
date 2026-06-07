# Security Basics

# 1.1: What Does "Security" Mean?
Different software has different specific security requirements, but many people divide security requirements into three broad objectives:

- Confidentiality: where users are only allowed to read the information they are authorised to read.
- Integrity: where users are only allowed to modify the information they are authorised to modify. Modifications include additions, changes, and deletions.
- Availability: is where the software continues working even while under attack.

Together, these three objectives form the **CIA Triad**, a foundational model for understanding software security.

In addition to the CIA Triad, many add a fourth security objective: **non-repudiation or accountability.** This ensures that if someone takes certain actions, the system should be able to later prove it, even if the person involved later denies it. Examples include transferring a large sum of money, deleting something important, or sending and receiving important messages. Not every system has these requirements, and even when they do some consider it part of integrity. 

To achieve these objectives, the system need certain supporting mechanisms. Confidentiality and integrity, for example, depend on being able to decide whether an action is authorised (unless all requests are authorised)

## Supporting Mechanisms
1. Identification & Authentication
    - Require users to identify themselves and prove (authenticate) their identity before doing anything that requires authorisation.

2. Authorisation
    - Determine what that user is allowed (authorised) to do before deciding it.
    - You can think of authorisation as a list of what each user is allowed to do. If an attacker can easily add authorisations, then even secure I&A means little. This is critical for implementing confidentiality and/or integrity. 

3. Auditing (Logging)
    - Record important events to help detect and recover from attacks.
    - Typical events include logging in, logging out, and modifying important information.
    - Auditing is often critical for implementing non-repudiation and accountability requirements.

*Note*
   *- What you do specifically depends on the software you're developing. If you're developing a lower-level library, you might not directly implement any of these mechanisms, but you still have to make sure that what you are doing will fit into a larger program.*


# 1.2: Security Requirements
To create software, you need to know what you want it to do. Requirements are simply what a product or service needs to do or be.

**Note that some software must comply with special laws or regulations, especially where vulnerabilities could cause serious harm (medical, financial, military). Selling software across jurisdictions can also trigger additional legal requirements.*

Requirements might not always be in a single formal document. Sometimes new requirements are captured in issue trackers or discussed with users.

Even for smaller projects, where nothing is written down, it's a good idea to record high-level security requirements in one place. That way, anyone modifying or using your software understands its security goals.