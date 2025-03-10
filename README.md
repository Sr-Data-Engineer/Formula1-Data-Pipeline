Formula 1 Data Pipeline 🚀

Azure Databricks | Medallion Architecture | Delta Lake

📌 Overview
This project builds a Formula 1 Data Pipeline in Azure Databricks, using Delta Lake and the Medallion Architecture (Bronze, Silver, Gold). The pipeline processes, 
transforms, and analyzes Formula 1 racing data.

📂 Project Structure
Formula1-Data-Pipeline/
│── notebooks/                  # Jupyter Notebooks for each pipeline stage
│── data/                        # Raw datasets (JSON, CSV, Parquet)
│── configs/                     # Configuration files (parameters, secrets)
│── sql_queries/                 # SQL scripts for transformations
│── scripts/                     # Python/PySpark scripts
│── docs/                        # Documentation & PPT
│   ├── project_requirements.pptx  # Requirements document
│── .gitignore                    # Ignore unnecessary files
│── requirements.txt              # Python dependencies
│── LICENSE                       # Project license
│── README.md                     # Documentation (You're here!)


🛠 ️ Tech Stack
Cloud: Microsoft Azure
Compute: Databricks
Storage: Azure Data Lake Storage (ADLS)
Processing: PySpark, Delta Lake
Database: Databricks SQL
Orchestration: Databricks Jobs

🏗 ️ Data Pipeline Architecture
This project follows the Medallion Architecture to structure data efficiently.

1️⃣  Bronze Layer (Raw Data)
Stores raw JSON/CSV data in ADLS.
No transformations, only ingestion.
Data is partitioned by date.

2️⃣  Silver Layer (Processed Data)
Cleans and transforms raw data.
Standardizes column names and removes duplicates.
Joins multiple sources to create meaningful datasets.

3️⃣  Gold Layer (Aggregated Data)
Prepares final tables for reporting.
Includes aggregations like driver standings & constructor standings.
Optimized for analytics (stored in Delta format).

📊 Data Sources
Formula 1 Standings Data
Race Results & Constructors Data

⚙️ Setup & Installation

1️⃣  Clone  the Repository
git clone https://github.com/your-username/Formula1-Data-Pipeline.git
cd Formula1-Data-Pipeline

2️⃣  Create  a Virtual Environment
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

3️⃣  Upload  Notebooks to Databricks

1. Open Azure Databricks.
2. Navigate to Workspace → Create Folder → Formula1-Data-Pipeline.
3. Upload notebooks/ inside the folder.
4. Attach to a Databricks cluster and run.


🚀 Running the Pipeline
1. Bronze Layer:
	Run the notebook to ingest raw data into ADLS (Azure Data Lake Storage).

2. Silver Layer:
	Clean, standardize & join tables.

3. Gold Layer:
	Perform aggregations (standings, race results).
	Run SQL Queries for insights.


📌 Best Practices
Use Delta Lake for ACID transactions.
Optimize with ZORDER & OPTIMIZE commands.
Implement Data Quality Checks in Silver Layer.
Automate Orchestration using Databricks Jobs


📜 License
This project is open-source under the MIT License.


💡 Contributing
Want to improve this pipeline? Follow these steps:

Fork the repo.
Create a new branch (feature-new).
Commit your changes.
Submit a PR.


⭐ If you found this useful, give it a star on GitHub! ⭐
