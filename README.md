
# End-to-End ETL Pipeline for Data Processing and Visualization

This repository contains an **End-to-End ETL Pipeline** project that automates data extraction, transformation, and visualization, leveraging tools like Apache Airflow, AWS S3, Snowflake, and Tableau.

![ETL Pipeline Diagram](https://github.com/sovit-nayak/redfin-pipeline/blob/main/Redfin/img/Pipeline.png)


## **Project Overview**
This project demonstrates how to design and implement a fully automated ETL pipeline to process real estate data from Redfin, ensuring efficient and scalable insights for stakeholders.

## **Workflow Overview**
1. **Data Extraction:**
   - Real estate data is extracted from **Redfin** using Python scripts for initial processing.

2. **Automation with Airflow:**
   - **Apache Airflow** is deployed on an **EC2 instance** to schedule, orchestrate, and monitor all tasks in the ETL pipeline.
   - Airflow ensures that each stage runs reliably and is updated weekly.

3. **Data Storage in AWS S3:**
   - Raw data is stored in an **S3 bucket** for archival and backup.
   - Transformed data is stored in a separate S3 bucket to prepare it for downstream processing.

4. **Integration with Snowflake:**
   - An **S3 trigger** activates **Snowpipe**, which loads the transformed data into Snowflake.
   - A **database schema** and tables are created in Snowflake to organize and structure the data for analytics.

5. **Visualization in Tableau:**
   - Snowflake is connected to Tableau to design interactive and dynamic dashboards.
   - The dashboards provide actionable insights into real estate trends for stakeholders.

## **Key Features**
- Fully automated ETL pipeline with **weekly updates**.
- Scalable and reliable data storage using AWS S3.
- Clean and well-defined data schema in Snowflake for efficient querying.
- Insightful, interactive dashboards built in Tableau.

## **Technologies Used**
- **Python**: Data extraction and preprocessing.
- **Apache Airflow**: Task orchestration and automation.
- **AWS S3**: Data storage for raw and transformed datasets.
- **Snowflake**: Data warehousing and schema management.
- **Tableau**: Data visualization and reporting.

## **Challenges and Learnings**
- Seamlessly integrating multiple tools and ensuring data flow consistency.
- Optimizing task dependencies in Airflow for better performance.
- Designing a robust data schema to support real-time analytics and visualization.

## **How to Run the Project**
1. Clone this repository:  
   ```bash
   git clone <repository-url>
   ```
2. Set up an EC2 instance and deploy Apache Airflow for orchestration.
3. Configure AWS S3 buckets for raw and transformed data storage.
4. Set up Snowflake with the required schema and Snowpipe for data loading.
5. Connect Snowflake to Tableau for visualization.

## **Future Improvements**
- Incorporate **predictive analytics** using machine learning models.
- Add real-time streaming capabilities for continuous updates.
- Expand the dashboard to include more advanced KPIs and insights.

## **Contact**
Feel free to reach out if you have any questions or suggestions about the project!

---

### **License**
This project is licensed under the MIT License - see the LICENSE file for details.
