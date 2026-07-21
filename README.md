# Vanpool Participant & Financial Management System (VP-FMS)

## Badges
![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Code Style](https://img.shields.io/badge/code%20style-VBA%20OOP-blue)
![Platform](https://img.shields.io/badge/platform-MS%20Access%20%2F%20VBA-red)
![Shell](https://img.shields.io/badge/shell-Windows%20PowerShell-1081C2)
![Compliance](https://img.shields.io/badge/compliance-MIL--STD--498-green)
![License](https://img.shields.io/badge/license-MIT-blue)

## Project Description
The **Vanpool Participant & Financial Management System (VP-FMS)** is a specialized relational database application engineered on Microsoft Access and Visual Basic for Applications (VBA). It provides structured participant tracking, roster management, automated monthly expense-splitting algorithms, and complete financial audit logging for vanpool operations.

Built using a hybrid RAD/Modular architecture, the application pairs bound Access forms for fast UI interaction with isolated VBA Class Modules and Standard Modules to handle business rules, data validation, and financial calculations.

> [!IMPORTANT]
> **Mandatory Configuration Control: Dual-Tracking Strategy**
> To support line-by-line GitHub diff analysis and pull request code reviews within an MS Access environment, this repository enforces a strict dual-tracking architecture:
> 1. The master binary database file resides inside the `/database/` directory.
> 2. **ALL** underlying VBA source components MUST be explicitly exported as flat text files into designated source directories prior to staging any Git commit:
>    - Class Modules (`.cls`) -> `/src/classes/`
>    - Standard Modules (`.bas`) -> `/src/modules/`
>    - Form & Report Code (`.cls`) -> `/src/forms/`
> 3. Commits containing binary updates without matching `/src/` text exports will fail architectural review.

## Workspace Governance & Documentation
All architectural specifications, system designs, and lifecycle documentation follow **MIL-STD-498** software documentation standards. See `docs/00_README.md` for the complete documentation index.

## Repository Directory Structure
```text
Vanpool Participant & Financial Management System/
├── database/
│   └── VP-FMS_Dev.accdb
├── docs/
│   ├── 00_README.md
│   └── 01_OperationalConceptDocument.md
├── src/
│   ├── classes/
│   ├── forms/
│   └── modules/
├── CONTRIBUTING.md
├── LICENSE.md
└── README.md
```

## Installation & Prerequisites

### System & Tooling Prerequisites
- Operating System: Windows 10 / 11
- Database Engine: Microsoft Access 2016 or newer (.accdb format support)
- Shell Environment: Windows PowerShell 5.1+ or PowerShell 7+
- Version Control: Git

### Cloning the Repository
```bash
git clone [https://github.com/your-org/Vanpool-Participant-Financial-Management-System.git](https://github.com/your-org/Vanpool-Participant-Financial-Management-System.git)
cd Vanpool-Participant-Financial-Management-System
```

## Usage
1. **Development Engine:** Open /database/VP-FMS_Dev.accdb within Microsoft Access to access forms and VBE.
2. **Editing Source Code:** Modify VBA source code using the Visual Basic Editor (VBE) inside Access.
3. **Exporting Components:** Prior to committing changes, run the internal Access export utilities to dump all updated modules into their designated `/src/` subdirectories (`/src/modules/`, `/src/classes/`, `/src/forms/`).
4. **Committing Changes:** Execute all Git staging and multi-line commits through PowerShell using the project's standard commit syntax.

## Contributing
Contributions are governed by our internal software engineering baselines. Review CONTRIBUTING.md for branching models, naming conventions, coding style guidelines, and issue tracking workflows.

## Credits
- **Application Architect & Senior Database Architect:** Joint Engineering Team
- **Documentation Standards:** Aligned with MIL-STD-498 engineering specifications

## License

Distributed under the MIT License. See `LICENSE.md` for full licensing details.