# Objectives
To use Microsoft Sentinel for threat management and investigation, covering features like the Mitre Att&ck framework for detecting threats, hunting queries for finding specific data, and custom KQL queries for analysis. We also look at using bookmarks to tag important findings, real-time monitoring through the livestream feature, and restoring archived data for further querying. Additionally, we highlight the use of workbooks for visualizing and customizing data to enhance security monitoring and reporting. Overall, we aim to help users effectively detect, investigate, and visualize security threats within Sentinel.

## Lessons Learned
- Understanding the sequence of events that leads to successful attacks is crucial, and Microsoft Sentinel integrates with the Mitre Att&ck framework to highlight relevant threats within your environment.

- Using hunting queries in Sentinel to enable us find specific data by leveraging built-in queries or creating custom ones, and adjusting time ranges for more accurate results.

- Using bookmarks for tagging important data during investigations, allowing for easy reference, further analysis, and sharing with peers.

- Real-time Monitoring with Livestream: The livestream feature in Sentinel helps monitor query results in real-time, which is valuable for tracking ongoing incidents or analyzing immediate data.

- The ability to restore archived log data for querying is essential for revisiting and analyzing past events or missing information.

- Data Visualization: Workbooks in Sentinel provide customizable visualizations of ingested data, making it easier to analyze and interpret security information.

## Tools Used
<div>
<img src="https://img.shields.io/badge/-Microsoft%20Sentinel-0078d4?style=for-the-badge&logo=microsoft&logoColor=white" alt="Microsoft Sentinel">
<img src="https://img.shields.io/badge/-MITRE%20ATT%26CK%20Framework-f2f2f2?style=for-the-badge&logo=mitre&logoColor=white" alt="MITRE ATT&CK Framework">
<img src="https://img.shields.io/badge/-Hunting%20Queries-a3c2c2?style=for-the-badge&logo=search&logoColor=white" alt="Hunting Queries">
<img src="https://img.shields.io/badge/-Kusto%20Query%20Language%20(KQL)-660066?style=for-the-badge&logo=microsoft&logoColor=white" alt="Kusto Query Language (KQL)">
<img src="https://img.shields.io/badge/-Bookmarks-ffcc00?style=for-the-badge&logo=book&logoColor=white" alt="Bookmarks">
<img src="https://img.shields.io/badge/-Livestream-e63946?style=for-the-badge&logo=twitch&logoColor=white" alt="Livestream">
<img src="https://img.shields.io/badge/-Workbooks-000000?style=for-the-badge&logo=microsoft&logoColor=white" alt="Workbooks">
</div>

## Steps
- We first access Microsoft Sentinel by logging in to Azure portal, in the search bar type Microsoft Sentinel and click on it. Select the Workspace you want to monitor, on the left side panel and click on Threat management, under the Threat management section, find and click on MITRE ATT&CK - this will open up a view showing all the detected threats that are mapped to the MITRE ATT&CK framework techniques. You can filter by techniques, tactics, or severity to focus on the threats that matter the most to your environment.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/4204fdf519e325d52579dabe71a4e3e1a6479d11/Images/Mitre%20in%20sentinel.PNG" width="700" />
</p>

- To work with Hunting Queries in Microsoft Sentinel, after choosing the Sentinel workspace you want to monitor, under Threat Management, we will find and click on Hunting to open and see a list of built-in queries provided by Microsoft, these queries are pre-configured to detect specific threats and suspicious activities. To run a query, click on the desired query from the list and run it by clicking Run query. For specific items (e.g., open ports), if the query returns results, you can click on the results to investigate further. If no results are found, you may need to adjust the settings or time range for the query.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/206b4568d4e114ebb17b18897953b1c991b27b11/Images/Hunting%20queries%20in%20sentinel.PNG" width="700" />
</p>

- To create a custom query, click on New query, you will be directed to the Kusto Query Language (KQL) editor where you can write your own query to look for specific threats, anomalies, or patterns. Adjust the time range for the query by selecting the time picker on the top, after writing the query, click Run to execute it. If necessary, adjust the settings of the query, such as the time range, filters, or other parameters to fine-tune your search results. You can save custom queries for future use, or schedule them to run at regular intervals to monitor for specific threats over time.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/ca959e41728bb2d0e876ff74dff36fe279229875/Images/Creating%20your%20new%20query%20KQL.PNG" width="700" />
</p>

- We now look at bookmarking results for investigation in Microsoft Sentinel, from the previous queries that we run either built-in or a custom query, review the results displayed in the table or list. For our case, we are looking for suspicious words in an email, you might select entries with high-risk alerts or unusual patterns.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/46c600fe6b1fec54a1b1ead0767353e45015ff33/Images/Running%20the%20selected%20query.png" width="700" />
</p>

- Identify and select the results that are most relevant to your investigation, click on the checkboxes next to the results or events you want to bookmark, look for the Bookmark option often located at the top of the results page, click on Add to Bookmarks and provide some details, such as bookmark title and description. View your saved bookmarks, go to the Bookmarks section under Hunting. After saving bookmarks, you can always return to them to continue your investigation, e.g. opening a case, alerting other team members, or escalating the issue.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/d36760423ba5be831b12512cfcf2338e2744d75a/Images/Adding%20bookmark%20from%20query%20results.PNG" width="300" />
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/d36760423ba5be831b12512cfcf2338e2744d75a/Images/Bookmarks%20displayed%20in%20the%20bookmark%20tab.PNG" width="300" />
</p>

- To use Livestream for Real-Time Data Monitoring in Microsoft Sentinel, go to the Hunting section to use pre-built queries or custom queries for monitoring, simply select an appropriate query for live monitoring. Look for the Livestream option by clicking on ellipsis and select Add to livestream, this will stream data as it comes in based on the query you’ve selected - it allows you to view live events, alerts, or trends as they occur in near real-time, to keep the data flowing, stay on the Livestream page. You can stop the Livestream or pause the query at any time to review or take further action.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/5ed1ac56274d0b8225c90ad1b35f1117a0b6f0c4/Images/Livestream%20a%20query.PNG" width="300" />
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/5ed1ac56274d0b8225c90ad1b35f1117a0b6f0c4/Images/Livestream%20a%20query%202.PNG" width="300" />
</p>

- To retrieve archived log data in Microsoft Sentinel and perform KQL queries on it, we first log into the Azure portal, search for Microsoft Sentinel and select your Sentinel workspace. Under the General tab in the left-hand menu, find and click on Search blade which is where you can search for archived log data or logs that have been ingested over time. To restore or retrieve archived logs, you first need to select the correct table where the logs were previously stored, examples of this tables are SecurityEvent, AzureDiagnostics, CommonSecurityLog etc. 
- Once you know which table you want to query, ensure that you select it in the search interface. If you want to restore data from specific periods, make sure to adjust the time range accordingly in the time filter at the top of the page

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/fed59337c80184fb2dea535a1391c8611b159ce9/Images/Retrieving%20archived%20log%20data.PNG" width="700" />
</p>

- If the data was archived or purged, you may need to reingest it for querying. This can be done if the data is still available in the Azure Monitor Logs or another storage account linked with your Sentinel workspace. If the data was archived in another storage account, you may need to move or restore it back into your Sentinel workspace.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/66c4909b81d7eb69f0110132b1c5f0c47a0f7e57/Images/Restored%20signin%20logs.PNG" width="700" />
</p>

- After selecting the appropriate table and ensuring the logs are available for reingestion, you can perform KQL queries to analyze the data. Under the General tab in the left-hand menu, go to the Logs section, and use Kusto Query Language (KQL) to write queries and analyze the restored logs as shown in the image below. Once your query runs, review the results for patterns or anomalies. You can export the results to save the data for further analysis or reporting.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/70b2133b0c9eda30c8486270f641afa1585788ea/Images/Restored%20signin%20logs%20in%20KQL.PNG" width="700" />
</p>

- To perform quick searches in Microsoft Sentinel without using the Hunting feature. In your Sentinel workspace, under the General section in the left-hand menu, click on Search, Search blade allows you to quickly search from the search bar at the top for specific keywords, logs, or data across the various tables in your Sentinel workspace. Press Enter to perform the search, the results will appear below the search bar showing you the data entries that match your search criteria. You can export the search results in CSV format for further analysis or reporting.

<p align="center">
  <img src="https://github.com/NgethaWachira/Investigating-Threats-Using-Sentinel-Queries/blob/e1ccf39f591386cad36d7efeb7f91be0734dc439/Images/Managing%20searches%20with%20keywords.PNG" width="700" />
</p>













