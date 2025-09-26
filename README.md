# Real-Time Customer Review Analytics Pipeline in Azure

*A professional, end-to-end data engineering project demonstrating the ingestion, real-time processing, and visualization of streaming customer review data using the Microsoft Azure stack.*

---

## 📖 Project Overview
This project showcases a complete, real-time (or near-real-time) data engineering pipeline. The primary goal is to ingest a continuous stream of customer product reviews, process them on the fly, and store them in a data lake for visualization. This demonstrates a practical application of modern, event-driven data architecture and cloud services.

---

## 🏛️ Architecture Diagram
The pipeline follows a modern, event-driven architecture, moving data from a live source to a processing engine and then fanning out to storage and visualization layers.


![Architecture Diagram]([link_to_your_architecture_diagram.png](https://github.com/NaranBhusal/Azure-Real-Time-Analytics-Pipeline/blob/5f566b7fd7c28fca03bbc3a815e47906a52b8914/raw.png))

**The data flows through the following stages:**
1.  **Data Ingestion:** A real-time stream of review data is sent to **Azure Event Hubs**, a high-throughput data ingestion service.
2.  **Stream Processing:** **Azure Stream Analytics** continuously reads from the Event Hub. Its job is to process each review as it arrives and send the results to a long-term storage location.
3.  **Data Storage:** The processed data is stored in **Azure Data Lake Storage (ADLS) Gen2**, organized by date and time for efficient querying.
4.  **Visualization:** **Power BI** connects directly to the Data Lake to create an interactive dashboard that can be refreshed to show the latest review data and insights.

---

## 🛠️ Technologies Used
* **Cloud Provider:** Microsoft Azure
* **Data Ingestion:** Azure Event Hubs
* **Stream Processing:** Azure Stream Analytics
* **Data Storage:** Azure Data Lake Storage (ADLS) Gen2
* **Business Intelligence:** Power BI
* **Data Source Simulation:** Python (Pandas, azure-eventhub)

---

## ✨ Final Dashboard
The final result is an interactive Power BI dashboard that provides key insights into customer feedback, product scores, and common themes in reviews.

*(Upload your dashboard screenshot to your repository and link to it here)*
![Power BI Review Dashboard](link_to_your_dashboard_screenshot.png)

---

## 🚀 Key Learnings & Future Improvements
This project was a deep dive into real-time data processing on the Azure platform. Key skills demonstrated include:
* Setting up and configuring a real-time ingestion endpoint with Event Hubs.
* Building and debugging a stream processing job with Stream Analytics.
* Handling complex authentication and firewall issues between various cloud services.
* Connecting Power BI to a data lake and transforming semi-structured data (JSON).

For a production environment, future improvements could include:
* Re-integrating the **Azure AI Language service** for real-time sentiment analysis (pending subscription availability).
* Securing all credentials and keys using **Azure Key Vault**.
* Deploying all resources using **Infrastructure as Code** (e.g., ARM Templates or Terraform).
