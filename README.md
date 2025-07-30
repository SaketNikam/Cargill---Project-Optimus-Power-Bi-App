# Cargill---Project-Optimus-Power-Bi-App
This is an overview for the Project Optimus I delivered during my tenure at Cargill.


Project Optimus was a business-driven analytics solution designed to monitor and improve mandatory procedure compliance during operator shift work at Cargill manufacturing plants. The solution addressed near real-time visibility and compliance issues by integrating Cargill’s internal application Accelerator with Azure-based data infrastructure and Power BI reporting tools.  

Architecture Overview  
Front-End Interface – Accelerator   
(Operators used Accelerator, Cargill's internal portal, to input procedure checklists, updates, and shift-related entries.)  

Data Lake Storage – Azure Data Lake Gen2   
Raw data from Accelerator was stored securely in Azure Data Lake Gen2 for further processing and analysis.  

Data Transformation Layers  
Azure Databricks handled large-scale batch transformations and cleaning of operator logs.  
Power BI Dataflows standardized business logic across different plants and unified shift data.  
Power Query was used within reports to apply additional filtering and calculated columns.  

Analytical Layer – Power BI Reports & Semantic Models  
Plant-specific Power BI reports showed procedure completion rates, shift logs, and safety metrics.  
Semantic Models provided a reusable, governed data model layer for self-service BI.  
Combined Dataflows aggregated shift data across plants while handling plant-specific logic.  

Distribution Layer – Power BI App  
A centralized Power BI App was built for consolidated distribution to plant managers and supervisors.  
Users could view performance trends across shifts, track procedure compliance, and monitor safety incidents.  

Challenges Faced  
Shift Schedule Variability:  
Each plant had different shift timings and rules, making it difficult to unify and report shift data uniformly across plants.  
Refresh Latency & Timeliness Issues:  
High latency (1–2 hours) in backend Power BI dataflows caused delays in report updates. Operators often completed their shifts before data was refreshed, limiting real-time monitoring by team leads.  
Data Governance & Validation:  
With multiple plants feeding data into the system, ensuring clean, validated, and consistent procedure tracking data was a significant challenge.  

Business Impact  
Provided plant supervisors and safety managers with real-time dashboards to track compliance.  
Enabled cross-shift reporting, improved data transparency, and reduced manual follow-ups.  
Built a scalable analytics foundation for future operational analytics use cases in manufacturing.  

