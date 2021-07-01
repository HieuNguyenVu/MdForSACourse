
# DATA STORAGE

## Preview

Author said about core concept that require significant experience and knowledge if plan on taking the Azure Solution Expert exam. They are:

1. Security
2. Networking
3. Compute

Without compute, there is no place to run your application.
Without networking, there is no means to get access to the compute running the application.  
Without security, both your network and comoute are vulnerable to bad actors who may implements some kind of malicious act on you, your customer, or your employees.
***
The author choose to discussing about data before the application because **data has more weight** on the AZ Solution Architect Expert Exam than coding or designing an application does.
Even so, both these aspect (data and application) are fundamental and highly dependent on each other and you cannot have one without the other.

    "It is a captial mistake to theorize before one has data.
    Insensibly one begins to twist facts to suit theories, instead of theories to suit fact."

In this chapter you will :

- learn about AZ Data stores (Databases), other AZ Storage capabilities
- How to protect your data from loss
- How to keep it form being improperly accessed

With all of those options, again you are confronted with some decisions. Do you need AZ SQL, AZ Cosmo DB, Table Storage, AZ Files, Queue Storage.

What kind of redundancies do you need: LRS,ZRS, GRS? What kind migration options are avaiable?
What kind of Azure exist in the context of data
After reading this chapter, those and many additional question will be answered.

Let's first begin a summary of two basic data architectures that the AZ platform is structured for: traditional RDBMS and Big Data

## RDBMS, OLTP, OLAP, and ETL

The first database I ever used was written by yours truly.

Not same with what we call "Database" nowaday. What the author did is instantiate a **group of strings** with **hard-coded** set of data.
Author suppose in sense that would be like and in memory data structure that my code later analyzed and manipulated. That is pretty cool when you think about it 40 years ago.

**1. Flat files**: Exist in the early ages of data manipulation, like text files.
Problem start happening as it became hard to know how the content data was organized or categorized, and whether were any _**logical links**_ between data in a flat file.

That led the industy toward the creation of the _relational database management system (RDBMS)_ concept.

![FIGURE 5.1 A traditional RDBMS scenario](./img/image.png)
FIGURE 5.1 A traditional RDBMS scenario

**2. OLTP**:
Starting with _online transaction processing (OLTP)_ you see the place where the data is stored most commonly from an interaction with some kind of external system. For example, placing an online order or withdrawing cash from an ATM **would both reuslt** in insertion, retrieval, and/or update occurring on a transactional relation database.

**3. OLAP**:
_Online analytical processing_ components that are focused on storing a rather large amount of data from multiple sources into a single location, such as a data warehouse.
    The data warehouse is accessed and processed using, for example, AZ
Analysis Service that creates data models that are useful for rendering human-readable reports using, For example, Power BI.
Finally, the process by which the data flows between OLTP and OLAP is referred to as **4. extract, transform, load, (ETL)** which can be implemented in azure by using an Azure Data Factory ADF.

"FIGURE 5.1 " describe a rather complex RDBMS data architecture solution. This is will be your focus if your target is Azure and your workload requires this solution type.
For principle, those are components, and they can be designed and deployed following numerous other patterns.

***
    Comment of reader: 
***

***

aspect: [N] view point or edge side
full-blown: solve all problem.
high majority of case: =  In a most of case
further: more and more.
properly: [ADV] Correct way.
improperly: not correct way.
traditional: long time ago, "Tet holiday is traditional event."
These day : nowaday

In contrast: nguoc lai,

manipulated: do action
 intended: focus on, purpose on
***
