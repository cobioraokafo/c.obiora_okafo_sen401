# 4. Configuration Identification and Version Control

## 4.1 Configuration Identification

Configuration identification is the process of identifying and defining the software components, documents and other project items that must be controlled throughout the development of the Online Examination Management System (OEMS).

It ensures that every important project item can be uniquely identified, tracked and managed throughout the software development lifecycle.

## 4.2 Configuration Items

The following items have been identified as configuration items (CIs) in the OEMS project:

- Software requirements and system specifications.
- System design documents and architecture diagrams.
- Source code files and application modules.
- Database schemas and scripts.
- Test plans, test cases and test reports.
- Configuration files and deployment documentation.
- Software Configuration Management Plan (SCMP).

These items will be placed under configuration control to ensure that changes are properly documented, tracked and approved.

## 4.3 Configuration Item Identification

Each configuration item shall be assigned a unique identifier to make it easy to locate, reference and track throughout the project.

The following naming convention will be used:

- OEMS-REQ-001 – Requirements document.
- OEMS-DES-001 – System design document.
- OEMS-SRC-001 – Source code component.
- OEMS-TST-001 – Testing documentation.
- OEMS-SCMP-001 – Configuration management plan.

Each item shall also have a description, version number and assigned owner where applicable. This will improve traceability and prevent confusion when managing project changes.

For example, when the requirements document is updated, its version number will be increased and the change will be recorded in GitHub with the relevant Jira task reference.

## 4.4 Version Control

Git and GitHub shall be used to manage and track changes to the OEMS project files. Git will maintain the history of changes, while GitHub will provide a shared repository for collaboration and storage of project deliverables.

Team members shall work on their assigned branches instead of making changes directly to the main branch.

Each change shall be committed with a meaningful commit message containing the relevant Jira task key. Changes shall be submitted through Pull Requests and reviewed by at least one other team member before being merged into the main branch.

This process will help prevent unauthorized changes, maintain project history and support collaboration among team members.

## 4.5 Version Numbering

The OEMS project shall use a version numbering system in the format Major.Minor.Patch.

- Major: Indicates significant changes to the system.
- Minor: Indicates the addition of new features or sections.
- Patch: Indicates minor corrections, bug fixes or updates.

For example, version 1.2.0 represents major version 1, minor version 2 and patch version 0.

Version numbers shall be updated when approved changes are made to configuration items.

## 4.6 Configuration Baselines

A configuration baseline is an approved version of a configuration item that serves as a reference point for future development.

The OEMS project shall establish baselines at important milestones, including requirements approval, system design approval, testing completion and final release.

Once a baseline has been approved, any changes to it must be documented, reviewed and approved before implementation.

This ensures that the project maintains consistency and that approved versions can be recovered when necessary.

## 4.7 Configuration Control and Traceability

All changes to identified configuration items shall be tracked through GitHub commits and Pull Requests. Each change shall be linked to its corresponding Jira task where applicable.

The change history shall identify the person responsible, the modification made and the version affected.

This will ensure accountability, improve traceability and make it easier to monitor changes throughout the development of the OEMS.
