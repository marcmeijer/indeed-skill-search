# indeed-skill-search
variations of skill search notebooks

![Datbos logo](logo.png)
  

## Contents

1. [Background](#Background)
1. [Setup](#Setup)
1. [Data](#Datas)
1. [Metrics](#Metrics)
1. [Run Parameters](#Run)
1. [Output](#Output)
1. [Modifications](#Modification/Improvements)


### Background
This algorithm assembles job postings of a specified job title "data+scientist" and scans the content for specific key job skill terms associated with job title to determine the frequency of term usage and associated "importance" of the skill in the field. 

### Setup
A run environment is created with 
- python   2.7
- lxml     4.3.3
- nltk     3.4.1
- bs4      0.0.1

### Data
All data is mined from the indeed website and uses the Indeed search term analytics for improved search location and post discovery. Country search is hard coaded. There are algorithm notebooks for Germany (_de) and The Netherlands (_nl)

### Metrics
The individual skill terms are accumlated as per total number of job postings rather than total number of occurances to account for the multiple occurances in the same postings though still reflecting the added "importance" of repeated mention.

### Run parameters
- Job search title can be changed in the Job URL List code block
- Job search city and state can be changed in the Execution code block
- Job search terms can be added or changed in the Key Search Term code block
  * prog_lang_dict
    * R, Python, Java, C++, Ruby, Perl, Matlab, JavaScript, Scala
  * analysis_tool_dict    
    * Excel, Tableau, D3.js, SAS, SPSS, D3, Tensorflow
  * hadoop_dict,
    * Hadoop, MapReduce, Spark, Pig, Hive, Shark, Oozie, ZooKeeper, Flume, Mahout
  * database_dict ,
    * SQL, NoSQL, HBase, Cassandra, MongoDB, AWS

### Output 
- Number of job postings found and the corresponding number of pages
- Page count as job pages are processed
- Total rume time posted
- Plot of each search term in order of "importance"

### Modification/Improvements
- improve runtime by changing NLP from NLTK to SpaCy algorithms
- Adjust for international searches
- integrate into Docker and flask for integrated independent execution
