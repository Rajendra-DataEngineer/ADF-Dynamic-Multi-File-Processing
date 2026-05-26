# 3. Parameterized Multi-File Processing Pipeline

## Project Overview
This project demonstrates a **dynamic and reusable file processing pipeline** in Azure Data Factory. It automatically discovers and processes multiple files from a source folder using `Get Metadata` + `ForEach` pattern with full parameterization.

## Key Features
- Dynamic file discovery using Get Metadata Activity
- Parameterized Dataset for reusability
- ForEach Activity for iterative processing
- Dynamic Copy Activity using expressions (`@item().name`)
- Scalable and production-ready design

## Architecture
1. **Get Metadata** → Scans source folder and returns list of files
2. **ForEach** → Iterates through each file
3. **Copy Activity** → Processes each file dynamically
- **Source**: Azure Data Lake Storage Gen2 (Parameterized)
- **Sink**: Azure SQL Database

## Technologies Used
- Azure Data Factory (V2)
- Azure Data Lake Storage Gen2
- Parameterized Datasets & Pipelines
- Expressions & Dynamic Content

## Screenshots

![Get Metadata Activity]<img width="491" height="314" alt="image" src="https://github.com/user-attachments/assets/c247ce97-5290-4686-9c83-931470edeaf0" />
*Get Metadata configuration to fetch file list*

![ForEach Activity]<img width="490" height="302" alt="image" src="https://github.com/user-attachments/assets/5dbca2c4-5689-4e7f-ad5c-076c18f6ea30" />
*ForEach loop processing multiple files*

![Pipeline Overview]<img width="469" height="238" alt="image" src="https://github.com/user-attachments/assets/f2e025d9-0421-4d85-b225-c244db859969" />
*Complete Parameterized Multi-File Pipeline*


* ## How to Run
1. Update Linked Services
2. Configure Dataset parameters (`FolderName`, `FileName`)
3. Run pipeline in Debug mode
4. Pass values to pipeline parameters

## Learnings
- Implementing dynamic file processing patterns
- Working with Get Metadata + ForEach combination
- Creating reusable parameterized pipelines
- Using expressions like `@item().name` and `@dataset().parameter`

---
**Made by Rajendra K**  
Aspiring Azure Data Engineer | Open to UK Relocation
`

