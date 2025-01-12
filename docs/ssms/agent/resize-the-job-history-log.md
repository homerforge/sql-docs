---
description: "Resize the Job History Log"
title: Resize the Job History Log
ms.prod: sql
ms.prod_service: sql-tools
ms.technology: ssms
ms.topic: conceptual
helpviewer_keywords: 
  - "jobs [SQL Server Agent], history"
  - "resizing job history log"
  - "size [SQL Server], job history log"
  - "logs [SQL Server], jobs"
  - "SQL Server Agent jobs, history"
  - "historical information [SQL Server], jobs"
ms.assetid: ddee1ce8-9d1b-4017-9894-bf7256aed95d
author: markingmyname
ms.author: maghan
ms.reviewer: ""
ms.custom: seo-lt-2019
ms.date: 01/19/2017
monikerRange: "= azuresqldb-mi-current || >= sql-server-2016"
---

# Resize the Job History Log

[!INCLUDE[applies-to-version/_ssnoversion.md](../../includes/applies-to-version/sqlserver.md)]

> [!IMPORTANT]  
> On [Azure SQL Managed Instance](/azure/sql-database/sql-database-managed-instance), most, but not all SQL Server Agent features are currently supported. See [Azure SQL Managed Instance T-SQL differences from SQL Server](/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent) for details.

This topic describes how to set size limits for [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Agent job history logs by using SQL Server Management Studio.

- **Before you begin:**  

    [Security](#Security)  

- **To set size limits for job history logs, using:**  

    [SQL Server Management Studio](#SSMS)

## <a name="BeforeYouBegin"></a>Before You Begin  

### <a name="Security"></a>Security

For detailed information, see [Implement SQL Server Agent Security](../../ssms/agent/implement-sql-server-agent-security.md).  

## <a name="SSMS"></a>Using SQL Server Management Studio

*To resize the job history, log based on raw size*

1. In **Object Explorer,** connect to an instance of the [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion_md.md)], and then expand that instance.

2. Right-click **SQL Server Agent**, and then select **Properties**.

3. Select the **History** page, and then confirm that **Limit size of job history log** is checked.

4. In the **Maximum job history log size** box, enter the maximum number of rows the job history log should allow.

5. In the **Maximum job history rows per job** box, enter the maximum number of job history rows to allow for a job.

**To resize the job history, log based on time:**

1. In **Object Explorer**, connect to an instance of the [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion_md.md)], and then expand that instance.  

2. Right-click **SQL Server Agent**, and then select **Properties**.

3. Select the **History** page, and then select **Remove agent history**.

4. Select the appropriate number of **Days**, **Weeks**, or **Months**.