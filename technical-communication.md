  
# Full-Text Search  
  
In text retrieval, full-text search refers to techniques for searching a single computer-stored document or a collection in a full-text database. Full-text search is distinguished from searches based on metadata or parts of the original texts represented in databases (such as titles, abstracts, selected sections, or bibliographical references). In a full-text search, a search engine examines all of the words in every stored document as it tries to match search criteria (for example, the text specified by a user). Full-text-searching techniques became common in online bibliographic databases in the 1990s. Many websites and application programs (such as word processing software) provide full-text-search capabilities. Some web search engines, such as google.com, employ full-text-search techniques, while others index only a portion of the web pages examined by their indexing systems.  
  
## Indexing  
  
When dealing with a small number of documents, it is possible for the full-text-search engine to directly scan the contents of the documents with each [query]. However, when the number of documents to search is potentially large, or the quantity of search queries to perform is substantial, the problem of full-text search is often divided into two tasks: indexing and searching. The indexing stage will scan the text of all the documents and build a list of search terms (often called an [index], but more correctly named a [concordance]).  
  
## Classification  
  
According to two types of data classification, search is also divided into two types: structured data search and unstructured data search.  
For structured data, we usually can use relational databases (MySQL, Oracle, etc. ) of the table way to store and search can also be indexed.  
There are two main methods for searching unstructured data, that is, full-text data:  
  
## 1. Sequential Scanning  
  
You can also know its approximate search method through the text name, that is, query specific keywords in a sequential scanning manner.  
For example, give you a newspaper and let you find where the text “RNG” appears in the newspaper. You need to scan the newspaper from beginning to end, and then mark the sections where the keyword appeared and where it appeared.  
This method is undoubtedly the most time-consuming and least effective. If the typesetting of the newspaper is small, and there are many sections or even multiple newspapers, it will be almost after you scan your eyes.  
  
## 2. Full-Text Search  
  
Sequential scanning of unstructured data is slow. Can we optimize it? Isn’t it enough to make our unstructured data somehow structured?  
A part of the information in the unstructured data is extracted, reorganized to make it have a certain structure, and then the data with a certain structure is searched to achieve a relatively fast search.  
This approach constitutes the basic idea of ​​full-text retrieval. This part of information extracted from unstructured data and then reorganized is called an index.  
Taking newspaper reading as an example, we want to follow the news of the NBA Finals. If we are all NBA fans, how can we quickly find newspapers and sections of NBA news?  
The full-text search method is to extract keywords from all sections of all newspapers, such as ” Harden ”, ” NBA ”, ” James ”, ” Lake ” and so on.  
Then index these keywords, and by indexing, we can correspond to the newspapers and sections in which the keywords appear. Note the difference between directory search engines.  
  
## Abstract  
  
Today, every kind of text, audio, and visual data, which are thought to be transformed into pieces of information, are stored for long periods for processing. The concept of Bid Data is not only associated with the data stored, but also with the system involving hardware and software that collects, processes, stores, and analyzes the data. As the data grows bigger, their physical storage options must be provided in a distributed architecture. Solr and Elasticsearch are among the most preferred tools which makes this storage process easier.  
As a part of the Apache Lucene project, Solr is a software that was started to be developed in 2004 with the searching features of full text,  
multiple search, dynamic clustering, database-integrated, open source, and elasticity. Similarly, Elasticsearch is a new open-source tool for  
real-time, full-text, and distributed search, which was launched in 2010 using the Lucene library.  
Although Solr and Elasticsearch have similar features, many parameters differentiate one from the other such as intended use, type of use, and query and indexing performances. This study analyzes the differences between Solr and Elasticsearch with regards to their query and indexing speeds, ease and difficulties of use, configuration forms, and architectures in light of the literature, and the results are discussed regarding these tools’ performances.  
  
## Solr  
  
Solr is an open-source enterprise search platform, written in Java,  
from the Apache Lucene project and its major features include full-  
text search hit highlighting, faceted search, real-time indexing, dynamic clustering, database integration, NoSQL features, and rich document (e.g., Word, PDF) handling.  
Apache Solr is an open-source search platform built on a Java library called Lucene. It provides search functionality for Apache Lucene in a user-friendly way. As an industry participant for almost a decade, it is a mature product with a strong and extensive user community.  
If it is properly deployed and well managed, it can become a highly reliable, scalable, and fault-tolerant search engine.  
Many internet giants such as Netflix, eBay, Instagram, and Amazon ( CloudSearch ) use Solr because it can index and search multiple sites.  
  
The main feature list includes:  
- research all  
- protruding  
- Faceted search  
- Real-time indexing  
- Dynamic cluster  
- Database integration  
  
## Elasticsearch  
  
Elasticsearch is also another distributed and open-source analysis  
and search tool which was developed using the Lucene library. It was  
designed for Scalability, security, and easy management. Using its query language that indexes structural and non-structural, and time-based data, provides rapid search and powerful analysis capabilities.  
  
Technical Specifications of Elasticsearch  
Elasticsearch is a document-based tool. Each entry in Elasticsearch  
is a structured JSON document. In other words, each data sent to  
elasticsearch for indexing is a JSON document. It is necessary to know some basic concepts to understand the structure of Elasticsearch. 
These are as follows:  
  
Index: An index is like a database in a relational database. Each  
The elastic search index is a structured JSON document.  
Type: A type is like a table in a relational database. Elasticsearch  
indexes can include more than one type.  
Mapping: This is managing how the data transferred  
types on indexes should be handled. It is equal to the identification of  
data type (string, integer, double, boolean) before adding the data  
in the traditional databases. Elasticsearch automatically realizes  
mapping based on the data, however, this can also be done  
manually.  
Shard/Sharding: It is the horizontal distribution of data to other  
machines on the network in database technologies. Thanks to  
sharding technology, data can be divided into pieces based on the  
existing physical facilities. Elasticsearch divides indexes into 5  
shards by default to store them. ElasticSearch can be extended with near real-time search. One of its main features is multi-tenancy.  
The main feature list includes:  

- Distributed search  
- Multi-tenant  
- Analysis search  
- Grouping and aggregation  
  
## Elasticsearch or Solr, Which is better?  

1. Installation and configuration  
Compared to Solr, Elasticsearch is easy to install and very lightweight. In addition, you can install and run Elasticsearch in minutes.  
Overall, if your application uses JSON, then Elasticsearch is a better choice.  
Otherwise, use Solr because its schema.xml and solrconfig.xml are well documented.  
2. Maturity  
Elastic search is more stable and is growing rapidly.  
Solr is more mature, and flexible since it still is an open source.  
3. Documents  
Solr scored high here. It is a very well-documented product with clear examples and API use case scenarios.  
Elasticsearch ‘s documentation is well organized, but it lacks good examples and clear configuration instructions.  
4. QPS Test  
Queries per second (QPS) is a common measure of the amount of  
Search traffic is an information retrieval system, such as a search  
engine or a database receives during one second.  
In the QPS test conducted between Elasticsearch and Solr, indexing  
was continued as a continuation of the previous test. QPS figures  
were measured for both tools while the indexing process was active.  
Elasticsearch reached 30 QPS speed, while Solr remained at 15 QPS speed when sending similar search requests.  
In another QPS test conducted with 40 million pieces of data  
(between 200 and 1000 words), it was observed that Solr had better  
performance.  
  
## Conclusions  
Solr and Elasticsearch are two similar search platforms that are  
both Lucene-based, has similar coding languages, intended use and  
styles.  
  
1. They are similar tools in terms of technical features.  
2. Elasticsearch supports more coding languages than Solr.  
3. Solr uses less disk space considering the size of data after  
indexing.  
4. Regarding the indexing duration, Elasticsearch had a better  
performance in short data, while Solr was better in long  
data.  
5. Both tools are rapid search tools.  
6. Because of its ease of use, Elasticsearch is more popular among new developers. However, if you are already used to working with Solr, keep using it, as there are no specific advantages to migrating to Elasticsearch.  
7. If you need it to process analytic queries in addition to search text, Elasticsearch is the better choice.  
8. Both have great operational tools, although Elasticsearch has attracted DevOps crowds more because of its easy-to-use API, so you can create a more vivid tool ecosystem around it.  
9. Solr is still more text-oriented. Elasticsearch, on the other hand, is often used for filtering and grouping, analyzing query workloads, not necessarily text searches. Elasticsearch developers invest a lot of effort at the Lucene and Elasticsearch levels to make such queries more efficient ( reducing memory footprint and CPU usage. Therefore, Elasticsearch is a better choice for applications that require not only text search but also complex search time aggregation.  
10. Cost: Solr and Elasticsearch are both open source, but Elasticsearch offers additional paid features and support. However, Solr's license allows for more flexibility in commercial use.  
11. Performance: Elasticsearch has a reputation for faster performance, especially in terms of search speed and indexing. Solr, on the other hand, is known for its scalability and robustness.  
12. Sharding: Both Solr and Elasticsearch support sharding, but Elasticsearch's implementation is more user-friendly and dynamic.  
13. Monitoring: Both search engines offer monitoring tools, but Elasticsearch has more built-in monitoring features and a more user-friendly dashboard.  
14. Community: Solr and Elasticsearch both have active communities, but Elasticsearch's community is larger and more engaged.  
  
Overall, the choice between Solr and Elasticsearch will depend on your specific use case and priorities. If you value performance and ease of use, Elasticsearch may be the better option, while if you need robustness and flexibility, Solr may be the way to go.  
  
  
## References  
1. https://www.researchgate.net/publication/311916747_An_Analysis_on_the_Comparison_of_the_Performance_and_Configuration_Features_of_Big_Data_Tools_Solr_and_Elasticsearch/link/586d706808ae8fce491b5ca3/download  
2. https://anytxt.net/how-to-choose-a-full-text-search-engine/  
3. https://www.youtube.com/live/upvaxy7zj60?feature=share  
4. https://youtu.be/MMWBdSdbu5k

