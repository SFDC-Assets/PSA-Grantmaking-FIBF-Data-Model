![Public Sector Accelerators logo](/docs/Logo_GPSAccelerators_v01.png)

# Grantmaking FIBF Data Model

**Ready-made grants data model that aligns with the Federal Integrated Business Framework's (FIBF).**

Accelerator Listing: [Grantmaking FIBF Data Model](https://pubsec-accelerators.my.site.com/accelerators/accelerator/a0wDo0000022Ha1IAE/grantmaking-fibf-data-model)


## Description

The Grantmaking FIBF Data Model is specifically designed to streamline the integration of federal data standards into the Salesforce environment, focusing on grants management. It serves as a comprehensive Accelerator for partners to align with essential Federal requirements, enhancing the efficiency and compliance of their grants management processes.

Key features of the Accelerator include:

**Customized Data Model**
- The package features a robust data model, inclusive of custom Salesforce fields and objects. These elements are meticulously crafted or mapped to key federal forms and frameworks, ensuring seamless alignment with federal standards.
- Integrated Forms:
  - **Application for Federal Assistance (SF-424):** A mandatory form for all grant applications, capturing crucial details like submission type, applicant information, and project timelines.
  - **Budget Information for Non-Construction Programs (SF-424A):** A detailed budget information form tailored for non-construction program applications.
  - **Budget Information for Construction Programs (SF-424C):** Specifically designed for construction-related grant applications, addressing budget details for construction, repair, renovation, and modernization projects.

**Alignment with Federal Integrated Business Framework (FIBF)**
- The package includes fields and mappings that resonate with the FIBF Data Elements, as outlined on [FIBF Grants Management](https://ussm.gsa.gov/fibf-gm/). This integration provides a foundational baseline to develop and uphold data standards within the grants community, encompassing both Federal and industry partners.
- The FIBF Data Elements are structured to offer clear names, definitions, and logical data groupings. These elements are crucial for capturing essential attributes for the inputs and outputs associated with various Business Capabilities in grants management.

**Benefits**
- **Enhanced Compliance:** Ensures adherence to government-wide standard data sets and forms, facilitating compliance with federal mandates.
- **Streamlined Processes:** Simplifies the integration of complex federal forms and data standards into Salesforce, enhancing operational efficiency.
- **Versatility:** Suitable for a wide range of grant applications, including both construction and non-construction programs.


## Included Assets

This Accelerator includes the following assets:
<ol>
  <li>An <strong>unmanaged package</strong> (link below; metadata is also found in the /force-app/main/default/ folder) that includes:
    <ul>
      <li>Custom objects (x10)</li>
      <li>Custom fields (x400)</li>
      <li>Permission set (x1)</li>
      <li>Page layouts (x18)</li>
    </ul>
  </li>
  <li><strong>Documentation</strong>, including:
    <ul>
      <li>This readme file</li>
      <li>PSA Grantmaking Data Model Schema.png (located in the /docs/ folder)</li>
      <li>PSA Grantmaking DataModel-Object Fields Definition.xlsx (located in the /docs/ folder)</li>
    </ul>
  </li>
</ol>


## Before You Install

**License Requirements**

Internal User
<ul>
<li>Public Sector Foundation - Advanced</li>
<li>User License - Standard</li>
<li>Permission Set Licenses</li>
<ul>
  <li>Grantmaking User</li>
<li>Public Sector Access</li>
</ul>
</ul>

External User
<ul>
<li>Customer Community (Plus) for Public Sector</li>
<li>User License - Customer Community Plus or Customer Community Plus Login</li>
<li>Permission Set Licenses</li>
<ul>
  <li>Experience Cloud for Grantmaking</li>
  <li>Public Sector Community</li>
</ul>
</ul>

**General Assumptions**
* You are using this Accelerator in a sandbox or test environment. It is recommended that you not install any Accelerator directly into production environments.
* If you do not have a Salesforce org licensed to you, you may try Public Sector Solutions for free with one of our [trial environments](https://developer.salesforce.com/free-trials/comparison/public-sector).
* You are using this Accelerator in conjunction with the Salesforce Lightning Experience (LEX) - not the Classic UI.


## Installation

Unmanaged package installation link: https://test.salesforce.com/packaging/installPackage.apexp?p0=04t8A000000NAyn

1. **Log in to Your Salesforce Environment:**
   - Use the installation link provided above to log in to your Salesforce sandbox environment.
   - **Note:** If installing in a production org, replace `test.salesforce.com` with `login.salesforce.com` in the installation URL.
  
     <img src="docs/FIBF Package Login.png" width="750" alt="My Image">

2. **Install the Package:**
   - On the installation page, select "Install for All Users".
   - Under the section "What if existing component names conflict with ones in this package?", choose an option that aligns with your implementation requirements. This will determine how the package handles naming conflicts with existing components.
  
     <img src="docs/FIBF Package Install Page.png" width="750" alt="My Image">

## Post-Install Setup & Configuration

1. **Locate the Permission Set:**
   - After successful installation, navigate to the 'Permission Sets' in your Salesforce setup and find the permission set named "Grants FIBF Field Access".
  
     <img src="docs/FIBF Package Permission Set.png" width="750" alt="My Image">

2. **Assign Permission Sets to Users:**
   - Assign this permission set to users who will be working with grants. This action grants them the necessary access to the package components.
   - **Important:** Ensure you review the license requirements stated above to confirm user eligibility for the permission set.

      <img src="docs/FIBF Package Permission Set Assignment.png" width="750" alt="My Image">

**Data Sharing and Roles Setup** [Optional]
1. Compliant Data Sharing

The Compliant Data Sharing feature provides a sophisticated approach to manage and monitor data sharing in compliance with regulations and organizational policies. This   option is ideal for ensuring that Field 1 (GRM Legal Entity Role Type Code) and Field 2 (Agency Person Type Code) are shared and managed in a controlled environment.

Key Components:

* Standard Objects:
    * Funding Award Participant: Manages relationships between users or groups, participant roles, and Funding Award records.
    * Individual Application Participant: Manages relationships between users or groups, participant roles, and Individual Application records.
* Custom Objects:
    * Participant: Represents details of a participant in the context of a custom object record.
    * Participant Role: Defines roles and associated data access levels.
 
[Configure Compliant Data Sharing for Grantmaking](https://help.salesforce.com/s/articleView?id=sf.grmk_configure_compliant_data_sharing.htm&type=5)

2. Set Up Contacts to Multiple Accounts

This approach enables tracking of relationships between contacts and multiple accounts, ideal for managing complex interactions involving Field 1 and Field 2.

Implementation Steps:

1. Review Existing Solutions: Compare existing Account Contact Roles or custom solutions with Contacts to Multiple Accounts.
2. Enable Feature: Go to Account Settings and enable the option to relate a contact to multiple accounts.
3. Customize Fields: Add custom fields to capture unique relationship details. Manage fields in Lightning Experience or Salesforce Classic.
4. Update Page Layouts: Include essential fields in the Account Contact Relationship page layout and add the Related Contacts and Related Accounts related lists to appropriate page layouts.

[Set Up Contacts to Multiple Accounts](https://help.salesforce.com/s/articleView?id=sf.shared_contacts_set_up.htm&type=5)

These options provide flexibility in configuring the package to meet various data sharing and relationship tracking requirements. The choice between Compliant Data Sharing and Setting Up Contacts to Multiple Accounts should be based on the specific data sharing needs and operational dynamics of your Salesforce environment.


## FAQs

**_Q: Are all the FIBF Data Elements included in this Accelerator?_**

A: The initial release of the accelerator includes approximately 20% of the Federal Integrated Business Framework (FIBF) Standard Data Elements. Future releases will incorporate more elements. Additionally, some data elements will need customization for each specific implementation, as they are tailored to the unique procedures of each agency's grants program.

**_Q: Can data elements be mapped to different objects to meet specific customer requirements?_**

A: As an unmanaged package, it offers the flexibility to create, edit, or delete metadata as needed. Consider this package a foundational starting point for your federal grants implementation. It can be adapted to suit specific requirements or even serve as inspiration for further customization. 


## Additional Resources

- [Grantmaking Product Documentation](https://help.salesforce.com/s/articleView?id=sf.grmk_grantmaking.htm&type=5)
- [Grantmaking Data Model](https://architect.salesforce.com/diagrams/template-gallery/public-sector-solutions-grantmaking-data-model)
- [Public Sector Solutions Data Model Developer Reference](https://developer.salesforce.com/docs/atlas.en-us.242.0.psc_api.meta/psc_api/api_psc_overview.htm)


## Revision History

**1.1 Initial Release (31 Dec 2023)** - This initial version includes a mapping of approximately 20% of the Federal Grants Management Standard Data Elements. It comprehensively covers the fields for the SF-424, SF-424A, and SF-424C forms, with each field either newly created or mapped to existing elements. For detailed information on field and object mappings, please see the [PSA Grantmaking DataModel-Object Fields Definition](docs/PSA%20Grantmaking%20DataModel-Object%20Fields%20Definition.xlsx).

## Acknowledgements

- Laura Bell
- Keegan Virtue
- Christine Talbot
- Nicole Peters
- Jen McClure


## Terms of Use

Thank you for using Global Public Sector (GPS) Accelerators.  Accelerators are provided by Salesforce.com, Inc., located at 1 Market Street, San Francisco, CA 94105, United States.

By using this site and these accelerators, you are agreeing to these terms. Please read them carefully.

Accelerators are not supported by Salesforce, they are supplied as-is, and are meant to be a starting point for your organization. Salesforce is not liable for the use of accelerators.

For more about the Accelerator program, visit: [https://pubsec-accelerators.my.site.com/accelerators/](https://pubsec-accelerators.my.site.com/accelerators/)
