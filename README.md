# Healthcare-Insurance-Company-SD
## Solution:
### Create/Configure Ecosystem
The first thing we should do is to configure an environment. As we are getting the data in various formats and the data are being stored in local databases or files to our AWS storage (s3 bucket), we will first need to configure our AWS ecosystem in such a way that the AWS services can be integrated with the local system so that it can read the data.

#### Data Ingestion
<ul>
  <li>Create a storage in AWS like s3 bucket to store the original data. We can create folder that denotes input and output. Input folders would contain all the incoming data and the output folders would contain all the processed/transformed data. The requirements want us to publish the result data in the AWS Redshift however we can still save the output data after cleaning into s3 and only select the data that we need to be pushed to RedShift.</li>

  <li>Learn the types/format: From the requirements we can see that we have 7 datasets. 6 of them are .csv files and 1 on them is .json file. We have to create a script that reads the data in various files and formats. This script will be written in any IDE that can run Python and Spark. We will be using Python to import the spark and utilize spark to load the data into S3 using various file formats.</li>
  
  <li>We should also make sure on how we want to process the data either batch or streaming or both. This depends on the volume of data we are generating every second/minute/hour.</li>

</ul>

#### Data Processing
<ul>
  <li>After the data is in s3 buckets, we can now create our ETL pipeline. </li>

  <li>The ETL would consist of various data cleaning and transformation techniques. This process would deal with any missing values, any duplicates, necessary columns, etc</li>
</ul>

#### Data Warehousing
<ul> 
  <li>After, we have our processed data. We will create various tables with specific schema in our Redshift. We would probably have at least 7 tables in our redshift, and we will increase and decrease the tables and schema if necessary.</li>

  <li>Now, that we have our cleaned data and the organized location where we can store them, we can finally publish our clean data to the Redshift table. When all the required data are in Redshift, we can begin SQL to query and get answers to our requirements.</li>
 </ul>
  
#### Reporting
<ul>
  <li>Moreover, redshift can also be integrated with various visualization tools for the visual representation of the data and easier understanding of the analysis.</li>
</ul>

### Use Cases
<ul>	
  <li>Migrating Data from one ecosystem to another ecosystem.</li>
  <li>When dealing with different data sources and formats and bring all data into one storage.</li>
  <li>Need to do some analysis on the past/historical data and the data are not organized properly.</li>
</ul>

### Technologies and Platforms to be used in this solution
Technologies and Platforms to be used are as follows:
<ul>
  a.	Amazon Web Services Platform
  <ul>
  <li>AWS S3</li>
  <li>AWS Redshift</li>
    
  </ul>
</ul>
<ul>
  b.	Programming/Scripting Languages
  <ul>
    <li>Python</li>
    <li>PySpark</li>
    <li>SQL</li>
  </ul>
</ul>
<ul>
  c.	Reporting Services
  <ul>
    <li>Databricks</li>
  </ul>
</ul>
<ul>
  d.	Project Management
  <ul>
    <li>JIRA</li>
  </ul>
</ul>
<ul>
  e.	CI/CD
  <ul>
  <li>Jenkins</li>
  <li>GitHub</li>
  </ul>
</ul>







