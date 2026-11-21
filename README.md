# 🎫 IT Service Management with ServiceNow

### Incident Management | Service Catalog | Change Management | Reporting | Problem Management

**Domain:** IT Support / IT Service Management (ITSM)  
**Platform:** ServiceNow Personal Developer Instance (PDI)  
**Framework:** ITIL  
**Environment:** ServiceNow Brazil (or available release)  
**Project Type:** Hands-On IT Support Simulation  

---

## 📌 Project Overview

This project demonstrates the implementation of core IT Service Management (ITSM) workflows using ServiceNow, an enterprise platform used to manage IT incidents, service requests, changes, and operational activities.

The objective was to simulate common responsibilities performed by IT Support Specialists, Service Desk Analysts, and ITSM Administrators within an enterprise environment.

Using a ServiceNow Personal Developer Instance (PDI), the lab covers the complete incident management process, from initial ticket creation and troubleshooting through resolution and closure.

The project also explores service catalog configuration, change request management, operational reporting, and problem management.

These exercises demonstrate how structured ITSM processes improve service delivery, accountability, documentation, and operational visibility.

---

## 🎯 Project Objectives

The primary objectives were to:

1. Configure and access a ServiceNow Personal Developer Instance.
2. Create, categorize, prioritize, and assign incident tickets.
3. Document troubleshooting activities and manage incident states.
4. Resolve incidents with appropriate resolution documentation.
5. Configure a self-service catalog item with custom request variables.
6. Create and manage a change request with documented implementation, testing, and rollback plans.
7. Generate operational reports to analyze incident trends.
8. Create a Problem record to document root cause analysis and preventive actions.
9. Demonstrate familiarity with ITIL-aligned service management processes.

---

## 💼 Business Scenario

### Enterprise IT Service Desk Operations

An organization's IT department receives support requests involving software failures, account access issues, hardware provisioning, and infrastructure maintenance.

Without a centralized ticketing platform, requests can become difficult to track, prioritize, assign, and resolve efficiently.

To improve service delivery, the organization uses ServiceNow to standardize its IT support operations.

As an IT Support Analyst working within a simulated enterprise environment, the responsibilities include:

- Logging and categorizing incidents reported by employees.
- Assigning incidents to the appropriate support teams.
- Documenting troubleshooting procedures and resolutions.
- Processing employee equipment requests through a self-service portal.
- Managing planned infrastructure changes through formal approval workflows.
- Creating operational reports to identify support trends.
- Investigating recurring incidents through Problem Management.

The project simulates these responsibilities within a controlled ServiceNow developer environment.

---

## 🛠️ Technologies & Tools

| Technology / Tool | Purpose |
|-------------------|---------|
| ServiceNow PDI | ITSM simulation environment |
| ServiceNow Incident Management | Incident tracking and resolution |
| ServiceNow Service Catalog | Self-service request management |
| ServiceNow Change Management | Change planning and authorization |
| ServiceNow Reporting | Incident analysis and visualization |
| ServiceNow Problem Management | Root cause documentation |
| ITIL Framework | IT service management practices |
| Web Browser | ServiceNow administration and portal access |

---

## ✨ Key Features

### Incident Management
- Incident creation and categorization
- Impact and urgency assessment
- Automated priority assignment
- Assignment group configuration
- Work note documentation
- Incident resolution and closure
- Activity history and audit tracking

### Service Request Management
- Custom service catalog item creation
- Mandatory and optional intake variables
- Hardware request form configuration
- Self-service portal validation

### Change Management
- Change request documentation
- Risk and impact assessment
- Maintenance window scheduling
- Test and backout planning
- Approval workflow simulation

### Operational Reporting
- Incident volume by priority
- Open incidents by category
- Data filtering and visualization
- Operational trend interpretation

### Problem Management
- Root cause analysis
- Workaround documentation
- Permanent remediation planning
- Incident-to-Problem relationships
- Known Error classification

---

# 🏗️ Lab Environment

## ServiceNow Developer Environment

The project uses a ServiceNow Personal Developer Instance (PDI), providing an isolated environment for practicing enterprise ITSM workflows.

| Component | Configuration |
|-----------|---------------|
| Platform | ServiceNow |
| Instance Type | Personal Developer Instance |
| Release | Brazil / Available Release |
| User Role | Administrator |
| Environment | Cloud-hosted developer sandbox |
| Data | ServiceNow demonstration records |
| Access | Web browser |

**Instance URL Format:**

```text
https://devXXXXX.service-now.com
```

> **Security Note:** Instance passwords, session tokens, API keys, and other authentication credentials should never be included in a public GitHub repository.

---

# ⚙️ Implementation & Methodology

## 01 — Provisioning the ServiceNow Developer Instance

### Objective

Establish an isolated ServiceNow environment with administrative access to the ITSM modules required for the project.

### 1.1 Create a Developer Account

1. Navigate to [ServiceNow Developer](https://developer.servicenow.com).
2. Select **Sign In**.
3. Choose the option to create a ServiceNow account.
4. Complete the registration process.
5. Verify the registered email address.
6. Sign in to the Developer Portal.
7. Complete the initial developer profile configuration.
8. Accept the Developer Program terms.

### 1.2 Provision a Personal Developer Instance

1. Select **Request Instance** from the Developer Portal.
2. Choose the Brazil release or an available supported release.
3. Submit the instance request.
4. Wait for provisioning to complete.
5. Record the instance URL and administrator username.
6. Store the administrator password securely.

The PDI provides a sandbox for testing ServiceNow configurations without affecting a production environment.

### 1.3 Verify Platform Access

1. Open the provisioned ServiceNow instance.
2. Authenticate using the administrator account.
3. Locate the **All** application navigator.
4. Search for the **Incident** module.
5. Confirm that the incident list and creation options are accessible.

**Verification Criteria:**

- Successful administrator authentication.
- ServiceNow interface loads correctly.
- Incident Management module is accessible.
- Required ITSM applications are available.

**📸 Screenshot Evidence**

<img width="1919" height="864" alt="image" src="https://github.com/user-attachments/assets/d9c90e42-515b-4481-afbc-fb93186f8471" />

---

## 02 — Incident Creation, Troubleshooting, and Resolution

### Objective

Simulate an employee support request and manage the incident through the ITIL-aligned incident lifecycle.

### Business Scenario

**Incident: Microsoft Outlook Connectivity Failure**

An employee contacts the IT Service Desk because Microsoft Outlook cannot connect to the organization's email server.

The employee requires assistance restoring email functionality.

The incident must be documented, prioritized, assigned, investigated, and resolved.

### 2.1 Create an Incident Record

Navigate to:

**All → Incident → Create New**

Configure the incident using the following information:

| Field | Value |
|-------|-------|
| Caller | Allie Pumphrey (demo user) |
| Category | Software |
| Channel | Email |
| Short Description | User cannot access Outlook - Cannot connect to server |
| Impact | 3 - Low |
| Urgency | 3 - Low |
| Assignment Group | Service Desk |
| State | New |

Select **Submit** to create the incident.

Record the generated incident number.

**Example:**

```text
INC0010007
```

The actual incident number depends on the instance.

### Understanding Incident Priority

ServiceNow commonly uses an Impact/Urgency priority matrix to determine incident priority.

For this scenario:

```text
Impact: 2 - Medium
Urgency: 3 - Low

Calculated Priority: 4 - Low
```

The resulting priority depends on the instance's configured priority lookup rules.

This process promotes consistent incident prioritization rather than relying solely on individual analyst judgment.

**📸 Screenshot Evidence**

<img width="1919" height="539" alt="image" src="https://github.com/user-attachments/assets/b68dbfc4-3934-45d1-875f-aaba6991ef2f" />


### 2.2 Assign and Begin Working the Incident

1. Navigate to **Incident → All**.
2. Locate the newly created incident.
3. Click on the incident number.
4. Change the State from **New** to **In Progress**.
5. Assign the incident to the administrator account acting as the support analyst.
6. Select **Update**.

The state transition indicates that the incident has been accepted for investigation.

### 2.3 Document Troubleshooting Activities

The Comments field provides an internal record of troubleshooting actions performed by IT personnel.

For the simulated Outlook connectivity incident, the diagnostic workflow can be documented.

These notes represent a sample troubleshooting scenario and should be adjusted to reflect the actions actually performed or simulated in the lab.

After entering the notes, select **Update** to save the record.

**📸 Screenshot Evidence**

<img width="1842" height="464" alt="image" src="https://github.com/user-attachments/assets/916adcfb-ebec-4f58-9e59-c92ccbf4cdd2" />

<img width="757" height="280" alt="image" src="https://github.com/user-attachments/assets/d7bcef4d-e4d1-44b0-8483-d86f98d68a97" />


### 2.4 Resolve the Incident

After documenting the simulated resolution:

1. Reopen the incident.
2. Change the State to **Resolved**.
3. Select an appropriate Resolution Code.
4. Enter the resolution notes.
5. Save the record.

Use the closest applicable resolution code available in the instance.

<img width="1840" height="542" alt="image" src="https://github.com/user-attachments/assets/89310ae8-3213-40a7-839e-e291fae1b68c" />

### 2.5 Close the Incident

1. Reopen the resolved incident.
2. Review the resolution documentation.
3. Simulate end-user confirmation that the service is restored.
4. Change the State to **Closed**, if permitted by the configured workflow.
5. Select **Update**.

In production environments, resolved incidents may remain in a resolved state until user confirmation or an automated closure policy is satisfied.

### 2.6 Verify the Incident Audit Trail

Review the incident's Activity section.

Confirm that the record contains:

- Initial incident creation.
- Assignment information.
- State changes.
- Troubleshooting work notes.
- Resolution details.
- Closure Informaation

<img width="1390" height="563" alt="image" src="https://github.com/user-attachments/assets/5005c82f-1f37-49e0-a95a-92d91c7ffdfa" />


### Outcome

This exercise demonstrates incident documentation, prioritization, assignment, troubleshooting, resolution, and closure within ServiceNow.

---

## 03 — Service Catalog Configuration

### Objective

Configure a self-service catalog item that allows employees to submit structured hardware requests.

### Business Scenario

**Service Request: New Employee Laptop**

The IT department frequently receives requests for new and replacement laptops.

Requests submitted through email often lack important details, including business justification, required delivery date, and preferred hardware configuration.

To standardize the intake process, a self-service catalog item will be created.

### 3.1 Create the Catalog Item

Navigate to:

**All → Service Catalog → Maintain Items**

1. Select **New**.
2. Create a catalog item using the following configuration.

| Field | Configuration |
|-------|---------------|
| Name | New Laptop Request |
| Catalogs | Service Catalog |
| Category | Laptops |
| Short Description | Request a new or replacement laptop |
| Description | Submit a request for a new or replacement laptop. Requests are reviewed within two business days, with an estimated delivery timeframe of five to seven business days. |

The review and delivery timeframes are illustrative service expectations for this lab, not verified service-level agreements.

3. Save the catalog item.

<img width="1919" height="631" alt="image" src="https://github.com/user-attachments/assets/f3d6951f-190b-44c6-8004-be4821087cfd" />


### 3.2 Configure Request Variables

Catalog variables collect information required to process requests.

Open the newly created catalog item and locate the **Variables** related list.

Create the following variables:

| Question | Type | Mandatory |
|----------|------|-----------|
| Requester Name | Single Line Text | Yes |
| Business Justification | Multi Line Text | Yes |
| Required By Date | Date | Yes |
| Laptop Model Preference | Select Box | No |

For the Laptop Model Preference variable, configure the following choices:

```text
Standard
Developer
Executive
```

Each variable should have a clear question label and appropriate configuration.

**Why Mandatory Fields Matter**

Mandatory fields reduce incomplete requests and help IT teams gather the information necessary for approvals and fulfillment.

Optional fields allow flexibility without creating unnecessary barriers for users.


<img width="1886" height="619" alt="image" src="https://github.com/user-attachments/assets/aad5b4fc-b57e-429d-b530-91929d220b91" />


<img width="934" height="182" alt="image" src="https://github.com/user-attachments/assets/7f256a5c-28e2-4fcd-8916-4a7631f92307" />


### 3.3 Validate the Self-Service Portal

Access the ServiceNow Service Portal:

```text
https://devXXXXX.service-now.com/sp
```

1. Search for **New Laptop Request**.
2. Open the catalog item.
3. Confirm that all four variables appear.
4. Enter sample request information.
5. Submit the request.
6. Verify that a request record is created.

**Expected Request Number Format:**

```text
REQXXXXXXX
```

Depending on the catalog workflow, the request may also generate a Requested Item (RITM) and fulfillment tasks.

### Verification Criteria

- Catalog item is visible to the intended test user.
- Required fields enforce data entry.
- Laptop model choices display correctly.
- The request can be submitted.
- A request record is generated.

<img width="992" height="664" alt="image" src="https://github.com/user-attachments/assets/98cbca4e-45d9-4174-8497-594cf605fbc4" />

<img width="1687" height="158" alt="image" src="https://github.com/user-attachments/assets/c06a74ab-4486-45b0-bc86-4ac0334989fe" />


### Outcome

This exercise demonstrates service catalog administration, structured request intake, and self-service workflow validation.

---

## 04 — Change Request Management

### Objective

Document and simulate the approval process for a planned Windows security patch deployment.

### Business Scenario

**Change Request: Windows Security Patch Deployment**

The IT department must deploy security updates across corporate Windows workstations.

Because the deployment may require workstation restarts and could affect business applications, the change must be planned, documented, and approved.

### 4.1 Create a Change Request

Navigate to:

**All → Change → Create New**

Select the appropriate change type for the instance.

For this lab, a Normal Change is appropriate when demonstrating risk assessment and an approval workflow.

A Standard Change generally represents a pre-authorized, low-risk, repeatable change and may follow a different approval process.

Configure the request:

| Field | Value |
|-------|-------|
| Short Description | Deploy security patch to all Windows workstations |
| Category | Software |
| Risk | Low |
| Impact | 2 - Medium |
| Planned Start | Next available Saturday, 2:00 AM |
| Planned End | Next available Saturday, 6:00 AM |
| Change Type | Normal |

**Change Description:**

```text
Deploy monthly Windows security updates to corporate
workstations.

The deployment will be performed during an approved
maintenance window to minimize operational disruption.

Affected systems may require a restart to complete
the installation.

Pilot testing will be completed before broad deployment.
```

Save the change request.

<img width="1919" height="782" alt="image" src="https://github.com/user-attachments/assets/7581d0e3-ea28-48f4-b9bf-97653044baca" />


### 4.2 Document Implementation Planning

Open the change request and navigate to the **Planning** section.

**Implementation Plan:**

```text
1. Confirm the approved patch list.
2. Verify the target workstation inventory.
3. Deploy updates to five pilot workstations.
4. Monitor pilot systems for installation failures.
5. Validate business-critical applications.
6. Deploy updates to the remaining workstations.
7. Confirm patch installation status.
8. Document deployment results.
```

**Test Plan:**

```text
Deploy updates to five pilot workstations.

Verify:
- Successful patch installation.
- Successful workstation restart.
- Network connectivity.
- User authentication.
- Microsoft 365 application functionality.
- No critical application compatibility issues.

Proceed with deployment only after pilot validation.
```

**Backout Plan:**

```text
If critical issues occur:

1. Stop the remaining deployment.
2. Identify affected systems.
3. Review available patch removal or recovery options.
4. Uninstall the affected update where supported.
5. Restore systems using approved recovery procedures
   if necessary.
6. Validate workstation functionality.
7. Notify affected users and document the outcome.

Estimated rollback window: 2 hours, subject to
the scope and severity of the issue.
```

Save the planning information.

<img width="1918" height="810" alt="image" src="https://github.com/user-attachments/assets/e942e98d-c8ec-42a8-b085-aa3611bb55a1" />


### 4.3 Request Change Approval

1. Open the change request.
2. Complete any mandatory assessment fields.
3. Move the request through the configured assessment workflow.
4. Submit the change for approval.
5. Review the generated approval records.

The exact states and actions depend on the ServiceNow release and change workflow configuration.

### 4.4 Simulate Change Authorization

Within the isolated developer environment, use an authorized test approver to simulate approval.

1. Locate the approval record.
2. Review the change details.
3. Approve the request.
4. Return to the change record.
5. Verify that the approval is recorded.
6. Confirm that the change advances to its next configured state.

<img width="959" height="408" alt="image" src="https://github.com/user-attachments/assets/0e0ae1d2-a18c-4be8-b5a1-5944604d9b92" />


### Outcome

This exercise demonstrates change documentation, risk assessment, maintenance planning, approval tracking, and rollback preparation.

The lab simulates change authorization; it does not deploy patches to production systems.

---

## 05 — Operational Reporting and Incident Analysis

### Objective

Create ServiceNow reports that provide visibility into incident volume, priority distribution, and support demand.

### Business Scenario

IT management requires operational reports to understand:

- How many incidents are being reported?
- Which priority levels account for the most tickets?
- Which service categories generate the greatest support demand?
- Where might additional resources or process improvements be needed?

Two reports will be created to support these questions.

### 5.1 Create an Incident Volume by Priority Report

Navigate to:

**All → Reports → Create New**

Configure the report:

| Setting | Value |
|---------|-------|
| Report Name | Incident Volume by Priority |
| Table | Incident [incident] |
| Visualization | Bar Chart |
| Group By | Priority |
| Filter | Created within the last 90 days |

Save and run the report.

The resulting visualization groups incident records by their assigned priority.

**Analysis Considerations:**

- Identify the most common priority level.
- Review the volume of high-priority incidents.
- Investigate unusual concentrations of critical incidents.
- Compare priority distribution across reporting periods.

A large number of low-priority incidents does not automatically indicate healthy operations; incident volume must be interpreted alongside service impact, resolution performance, and organizational context.

<img width="1441" height="614" alt="image" src="https://github.com/user-attachments/assets/3e4f8548-f086-485f-b3a8-79a3096ec19e" />


### 5.2 Create an Open Incidents by Category Report

Create a second report using the following configuration:

| Setting | Value |
|---------|-------|
| Report Name | Open Incidents by Category |
| Table / Data Source | Incident [incident] |
| Visualization | Pie Chart |
| Group By | Category |
| Filter 1 | State is not Resolved |
| Filter 2 | State is not Closed |

Save and run the report.

These conditions provide a simplified view of unresolved incidents. Depending on the configured incident states, a more precise active-incident filter may be appropriate.

**Analysis Considerations:**

- Identify the category with the highest number of open incidents.
- Determine whether certain services generate recurring support demand.
- Consider whether ticket distribution indicates training or staffing needs.
- Investigate categories with unusually high unresolved volumes.

<img width="1160" height="630" alt="image" src="https://github.com/user-attachments/assets/e8bd0b3e-07cb-4c10-b878-7aba67d0ca3a" />


### 5.3 Interpret Operational Results

Record observations from both reports.

| Metric | Observation |
|--------|-------------|
| Most Common Priority | Critical |
| Highest-Volume Open Category | Inquiry |
| High-Priority Incident Count | 1 |
| Total Open Incidents | 69 |


### Outcome

This exercise demonstrates the ability to transform ITSM records into operational reports and use incident data to support service management decisions.

---

## 06 — Problem Management and Root Cause Analysis

### Objective

Create a Problem record associated with the Outlook incident to document a suspected underlying cause, available workarounds, and proposed permanent corrective actions.

### Business Scenario

**Problem: Recurring Outlook Connectivity Failures**

Following the resolution of an Outlook connectivity incident, the IT department identifies a potential recurring issue affecting laptop users.

The support team suspects that unstable network connectivity may contribute to Outlook synchronization problems.

A Problem record will be created to document the investigation and support future incident handling.

### 6.1 Create a Problem Record

Navigate to:

**All → Problem → Create New**

Configure the record:

| Field | Value |
|-------|-------|
| Category | Software |
| Problem Statement | Recurring Outlook OST corruption on Wi-Fi connected laptops |
| State | New |
| Service | Email / Microsoft Outlook, if available |

Save the record.

<img width="959" height="318" alt="image" src="https://github.com/user-attachments/assets/5c5bf93a-a7a8-41f0-9322-40238307b7d7" />

### 6.2 Document Root Cause Analysis

The scenario uses the hypothesis that interruptions during Outlook synchronization may be associated with cached mailbox issues.

**Example Root Cause Analysis:**

```text
Reported Issue:
Recurring Outlook connectivity and synchronization
failures on laptops connected through unstable Wi-Fi.

Suspected Cause:
Network instability may interrupt synchronization
and contribute to local Outlook cache or profile
issues.

Investigation Required:
1. Review Outlook error logs.
2. Examine network connectivity events.
3. Check Exchange or Microsoft 365 service health.
4. Review affected Outlook profiles.
5. Compare incidents across affected devices.
6. Determine whether OST corruption is reproducible.

Root Cause Status:
Unconfirmed - further technical validation required.
```

A network disconnection alone does not establish OST corruption as the root cause. Additional evidence is required before confirming this diagnosis.

<img width="820" height="334" alt="image" src="https://github.com/user-attachments/assets/0f826d36-a210-4cf1-a9d2-ed50a0d426dd" />


### 6.3 Document a Workaround

**Example Workaround:**

```text
1. Verify network connectivity.
2. Check Microsoft 365 or Exchange service status.
3. Restart Outlook and retest connectivity.
4. Review Outlook profile health.
5. Recreate the Outlook profile or rebuild the
   local cache if troubleshooting supports it.
6. Confirm mailbox synchronization is restored.
```

Rebuilding an Outlook cache should follow appropriate data protection and support procedures.

<img width="821" height="325" alt="image" src="https://github.com/user-attachments/assets/ce361e9b-5741-4fce-88d0-4e05c31778d1" />


### 6.4 Propose Permanent Corrective Actions

**Proposed Fix:**

```text
1. Identify affected devices and network locations.
2. Investigate wireless connectivity stability.
3. Review Outlook client configurations.
4. Validate Microsoft-recommended synchronization
   and cached-mode settings.
5. Apply approved configuration changes where needed.
6. Monitor for repeat incidents.
7. Confirm the underlying cause has been eliminated.
```

Potential corrective actions must be tested before organization-wide deployment.


### 6.5 Link the Problem to the Incident

1. Open the Problem record.
2. Locate the Related Incidents section, if available.
3. Add the previously created Outlook incident.
4. Alternatively, open the incident and populate its Problem reference field.
5. Save the relationship.

**Example Relationship:**

```text
Problem: PRBXXXXXXX
         |
         |
         +---- Incident: INC0010001
               |
               +---- Outlook Connectivity Failure
```

### 6.6 Review Known Error Classification

A Known Error represents a problem for which the underlying cause and relevant handling information have been documented according to the organization's process.

Because the simulated root cause is initially unconfirmed, the Problem should remain under investigation until sufficient evidence supports the diagnosis.

Once the root cause has been validated:

1. Update the root cause documentation.
2. Confirm the available workaround.
3. Transition the Problem to the appropriate Known Error state or classification, if supported by the configured workflow.
4. Save the record.
5. Verify that the related incident remains linked.

### Outcome

This exercise demonstrates the relationship between Incident Management and Problem Management.

Incident Management focuses on restoring service, while Problem Management investigates underlying causes and seeks to reduce future incidents.

---

# 🧪 Testing & Verification

The following checklist summarizes the validation activities for the project.

Mark each item complete only after confirming the result in the ServiceNow instance.

| Test | Expected Result | Status |
|------|-----------------|--------|
| Developer Instance Access | Administrator can access the platform | [Pass] |
| Incident Creation | Incident number generated | [Pass] |
| Priority Calculation | Priority assigned according to configured matrix | [Pass] |
| Incident Assignment | Assigned analyst and group saved | [Pass] |
| Work Note Documentation | Notes visible in activity history | [Pass] |
| Incident Resolution | Resolution details saved | [Pass] |
| Incident Closure | State updated to Closed | [Pass] |
| Catalog Item Publication | Item visible in self-service portal | [Pass] |
| Catalog Request Submission | Request record generated | [Pass] |
| Change Approval | Approval recorded successfully | [Pass] |
| Priority Report | Bar chart generated | [Pass] |
| Category Report | Pie chart generated | [Pass] |
| Problem Creation | Problem record generated | [Pass] |
| Incident-Problem Link | Relationship visible in both records | [Pass] |

---

# 📊 Project Deliverables

The project is designed to produce the following artifacts:

| Deliverable | Description |
|-------------|-------------|
| Incident Record | Documented Outlook support incident |
| Incident Activity History | State changes, work notes, and resolution |
| Service Catalog Item | New Laptop Request form |
| Service Request Record | Submitted catalog request |
| Change Request | Planned Windows patch deployment |
| Change Approval Record | Documented authorization |
| Priority Report | Incident distribution by priority |
| Category Report | Open incidents grouped by category |
| Problem Record | Root cause investigation and remediation plan |
| Screenshot Evidence | Visual documentation of the configured workflows |

---

# 🧠 Skills Demonstrated

### IT Support & Service Desk Operations

- Incident logging and categorization
- Ticket prioritization and assignment
- Troubleshooting documentation
- Resolution and closure procedures
- Support activity tracking

### IT Service Management

- ITIL-aligned Incident Management
- Service Request Management
- Change Enablement
- Problem Management
- Workflow documentation

### ServiceNow Administration

- Navigation of ITSM applications
- Incident record configuration
- Service catalog item creation
- Catalog variable configuration
- Approval record management
- Operational report creation

### Analytical & Documentation Skills

- Incident trend analysis
- Root cause investigation
- Workaround and remediation documentation
- Technical recordkeeping
- Operational reporting

---

# 📚 Key Takeaways

## 1. Accurate Documentation Supports Incident Resolution

Detailed work notes and resolution records allow other analysts to understand the troubleshooting process and reduce duplicated effort.

## 2. Incident Prioritization Supports Effective Resource Allocation

Impact and urgency assessments help service desks prioritize incidents according to business impact and operational needs.

## 3. Self-Service Catalogs Standardize Request Intake

Structured catalog forms reduce incomplete requests and help service teams collect consistent information.

## 4. Change Management Reduces Operational Risk

Documented implementation, testing, approval, and backout procedures help organizations manage planned system modifications.

## 5. Operational Reporting Supports Continuous Improvement

Incident reports provide insight into ticket distribution and potential areas for service improvement.

## 6. Problem Management Addresses Recurring Issues

Incident resolution restores service, while Problem Management investigates underlying causes and supports long-term prevention.

---

# 🚀 Future Improvements

Potential extensions to this project include:

- Configure incident Service Level Agreements (SLAs).
- Create automated incident assignment rules.
- Build a ServiceNow Knowledge Base article for recurring Outlook issues.
- Configure incident escalation notifications.
- Create an ITSM performance dashboard.
- Implement catalog request approval workflows.
- Explore Configuration Management Database (CMDB) relationships.
- Develop incident response and service desk runbooks.

---

# ✅ Conclusion

This project provides practical exposure to enterprise IT Service Management workflows using ServiceNow.

Through simulated incident handling, service catalog configuration, change approval, operational reporting, and problem management, the lab demonstrates foundational skills used in IT Support, Help Desk, and ITSM Administration roles.

The project emphasizes structured troubleshooting, accurate documentation, service request standardization, operational accountability, and continuous service improvement.

These capabilities are directly applicable to organizations that rely on centralized ITSM platforms to manage employee support and maintain reliable IT services.

---

## 📁 Repository Structure

```text
servicenow-itsm-lab/
|
├── README.md
|
├── screenshots/
| ├── incident-management/
| ├── service-catalog/
| ├── change-management/
| ├── reporting/
| └── problem-management/
|
└── docs/
    ├── incident-case-study.md
    ├── change-management-plan.md
    ├── problem-root-cause-analysis.md
    └── testing-results.md
```

---

**Disclaimer:** This project is conducted within a ServiceNow Personal Developer Instance for educational and portfolio purposes. All incidents, requests, changes, and problem investigations are simulated. No production systems or real employee records are affected.
