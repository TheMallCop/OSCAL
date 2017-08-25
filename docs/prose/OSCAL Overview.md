# OSCAL Overview
This is an overview of the Open Security Controls Assessment Language (OSCAL). It explains why OSCAL is needed, who will benefit from the OSCAL work, what the OSCAL team has been working on, what the major challenges are in the OSCAL work, and what the future plans are for the OSCAL project.

## Terminology

Before discussing OSCAL, it is important to define three key OSCAL terms:
 * *Control*: A safeguard or countermeasure designed to satisfy a set of defined security and/or privacy requirements. While this is based on the NIST Special Publication (SP) 800-53 definition of "control", in the context of OSCAL it refers to a similar kind of requirement from a control catalog. 
 * *Catalog*: A set of security control definitions. Examples include the hundreds of controls in NIST SP 800-53, the 100+ controls in ISO 27002, and the practices in COBIT 5. 
 * *Profile*: A set of security requirements; also called a baseline or overlay. Examples include the control baselines in NIST SP 800-53, the FedRAMP baselines, and the PCI DSS requirements. A profile is basically selecting a set of security requirements from one or more control catalogs.

## Major challenges in security controls assessment

OSCAL is attempting to address a number of challenges around security controls and security controls assessment. The core challenge, and one of the primary reasons for creating OSCAL, is that concepts like security controls and profiles are represented today largely in proprietary ways. In many cases they are written in prose documents that are imprecise, lead to differences in interpretation, and are not machine-readable, meaning that the prose instructions require someone to do data entry into a tool in order for the tool to use the information. 

Organizations are also struggling with information systems that have many different components, and some components require the use of different profiles per component, which is commonly the case with cloud environments. Also, the cloud environments can be multitenant or have mixed ownership of components. We need to be able to assess the security of these systems against a number of requirements, owners, etc.—to do that simultaneously and provide these views to stakeholders. 

On top of that there are situations where a single system needs to support multiple regulatory frameworks. For example, the U.S. Department of Veterans Affairs is a federal agency (Federal Information Security Modernization Act (FISMA) and NIST Cybersecurity Framework requirements) and a healthcare institution (Health Insurance Portability and Accountability Act (HIPAA) requirements) that has credit card transactions (Payment Card Industry Data Security Standard (PCI DSS)). There is no shortage of requirements for some organizations that have multiple regulatory frameworks. 

Assessing all these security controls is extremely complex. Because of that complexity, it’s largely a manual process today. The OSCAL project is trying to change that. 

## The purpose of OSCAL

OSCAL is an attempt to standardize how security controls are represented, how a control implementation for a given system is represented, and how that information is best used and reports generated in a standardized way that can be used by both humans and machines. That means formats are needed that can be generated by machines for communicating with other machines, but can also easily be reformatted so humans can read the information. By standardizing the representation of this information, OSCAL information can be interoperable by having a well-defined specification with information that’s going to be used, imported, and used interoperably for security control assessments. The goal is to keep OSCAL as simple as possible and provide extensive automation for tools to use.