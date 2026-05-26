# Parameterized Dynamic Multi-File Processing Pipeline - Azure Data Factory

## 🚀 Project Overview
This project showcases a **metadata-driven, dynamic file processing pipeline** in Azure Data Factory. Instead of hardcoding file names, this pipeline utilizes a `Get Metadata` and `ForEach` design pattern to identify and process all files within a source directory automatically. This approach is standard for scalable, automated ETL/ELT workflows.

## 🛠️ Key Technical Features
* **Dynamic File Discovery**: Uses `Get Metadata` to scan containers and identify child items.
* **Iterative Orchestration**: Implements a `ForEach` activity to process multiple files in a single execution.
* **Parameterized Design**: Utilizes parameterized Linked Services and Datasets to ensure reusability across development, test, and production environments.
* **Scalable Architecture**: Template-based design allowing for easy maintenance and expansion.

## 🏗️ Architecture & Flow
1.  **Get Metadata**: Identifies all objects (files) in the source ADLS Gen2 path.
2.  **ForEach**: Iterates through the file list retrieved from the metadata.
3.  **Copy Activity**: Moves data from source to destination, utilizing dynamic expressions for source/sink naming.

## 💻 Technologies Used
* **Azure Data Factory (ADF)**: Orchestration and control flow.
* **Azure Data Lake Storage (ADLS) Gen2**: Primary data storage.
* **Git Integration**: CI/CD workflows using GitHub for version control.
* **Expressions/JSON**: Advanced ADF expression language for dynamic property handling.

## 📸 Pipeline Visuals
*(Note: Upload your screenshots to a `/screenshots` folder in this repo to display them here)*
* **Pipeline Overview**: `<img width="469" height="238" alt="image" src="https://github.com/user-attachments/assets/f2e025d9-0421-4d85-b225-c244db859969" />
`
* **Get Metadata Configuration**: `<img width="491" height="314" alt="image" src="https://github.com/user-attachments/assets/c247ce97-5290-4686-9c83-931470edeaf0" />
`
* **ForEach Iteration**: `<img width="490" height="302" alt="image" src="https://github.com/user-attachments/assets/5dbca2c4-5689-4e7f-ad5c-076c18f6ea30" />
`

## ⚙️ How to Deploy & Run
1.  **Configure Linked Services**: Link your ADLS Gen2 account with your credentials.
2.  **Dataset Setup**: Ensure the dataset path parameter matches your source folder structure.
3.  **Validation**: Run the pipeline in **Debug** mode to verify child-item discovery.
4.  **Publish**: Commit changes to the `main` branch and publish from the collaboration branch.

## 🧠 Key Learnings
* **Dynamic Patterns**: Mastered the `Get Metadata` + `ForEach` design pattern.
* **Data Orchestration**: Learned to pass dynamic items through pipeline parameters and context variables (`@item().name`).
* **Portfolio Building**: Practiced Git-based ADF development, including branching, pull requests, and documentation.

## 🚀 Future Roadmap
* [ ] Implement **Error Handling & Logging** framework.
* [ ] Build a **Medallion Architecture** (Bronze → Silver → Gold) pipeline.
* [ ] Develop **Event-driven triggers** based on Blob creation.
* [ ] Pursue **Microsoft Certified: Azure Data Engineer Associate (DP-203)**.

---
**Made by Rajendra K** *Aspiring Azure Data Engineer | Cloud Computing Enthusiast | Open to Opportunities* [GitHub Profile](https://github.com/Rajendra-DataEngineer) | [(https://www.linkedin.com/in/rajendra-k-08a99840a?utm_source=share_via&utm_content=profile&utm_medium=member_android)]
