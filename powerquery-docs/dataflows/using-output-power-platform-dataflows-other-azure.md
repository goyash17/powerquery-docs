---
title: Using the output of Power Platform dataflows from other Azure Data workloads
description: Using the output of Power Platform dataflows from other Azure Data workloads
author: radacad

ms.service: powerquery
ms.reviewer: v-douklo
ms.topic: conceptual
ms.date: 05/25/2020
ms.author: v-douklo
---

# Using the output of Power Platform dataflows from other Azure Data workloads

Depending on the storage for the output of the Power Platform dataflows, you can use that output in other Azure services.

## The benefits of working with the output of Power Platform dataflows

Using Power Platform dataflows, you can reshape data, clean the data, and prepare the data for further analysis and consumption. There are many other Azure data services that work with data as an input and provide actions. 

- Azure Machine Learning can consume the output of dataflows and use it for machine learning scenarios (for example, predictive analysis).
- Azure Data Factory can get the output of dataflows in a much larger scale, combined with the data from big data sources, for advanced data integration solutions.
- Azure Databricks can consume the output of dataflows for applied data science algorithms and further AI with the big data scale in the Apache Spark backend.
- Other Azure data services can use the output of Power Platform dataflows to do further actions on that data.

## Dataflows with external Azure Data Lake Storage Gen2 

If you've connected an external Azure Data Lake Storage Gen2 storage to the Power Platform dataflows, you can connect to it using any Azure services that have Azure Data Lake Storage Gen2 as a source. These services could be Azure Machine Learning, Azure Data Factory, Azure Databricks, Azure Analysis Services, and so on.

In any of these services, use Azure Data Lake Storage Gen2 as the source. You'll be able to enter the details of your storage and connect to the data in it. The data is stored in CSV format, and is readable through any of these tools and services. The following screenshot shows how Azure Data Lake Storage Gen2 is a source option for Azure Data Factory.

![Using the output of Power Platform dataflows in external ADLS gen 2](media/ADFSourcedFromADLSGen2.png)

## Dataflows with Common Data Services

If you're using standard dataflows that store the data in Common Data Services, you can still connect to Common Data Services from many Azure services. The following screenshot shows that in Azure Data Factory the output of a dataflow from Common Data Services can be used as a source.

![Using the output of Power Platform dataflows from Common Data Services](media/ADFSourcedFromCDS.png)

## Dataflows with internal Azure Data Lake Storage Gen2

If you're using the internal Azure Data Lake storage that is provided by Power Platform dataflows, then that storage is exclusively limited to the Power Platform tools, and isn't accessible from other Azure data workloads.



