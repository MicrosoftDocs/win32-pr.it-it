---
description: Nell'esempio seguente vengono scritti i dati sulle prestazioni in tempo reale in un file di log.
ms.assetid: a1bc40ea-d928-495a-abc0-daf097202a12
title: Scrittura dei dati sulle prestazioni in un file di log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afce3c85b36d66f1b621e4c4f174bff327e6084a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312072"
---
# <a name="writing-performance-data-to-a-log-file"></a>Scrittura dei dati sulle prestazioni in un file di log

Nell'esempio seguente vengono scritti i dati sulle prestazioni in tempo reale in un file di log. Nell'esempio vengono chiamate le funzioni [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) e [**chiamata PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) per creare una query per raccogliere i dati del contatore del tempo del processore. Nell'esempio viene quindi chiamata la funzione [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) per creare il file di log in cui scrivere i dati. Nell'esempio viene chiamata la funzione [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) per raccogliere un campione e aggiornare il file di log una volta al secondo per 20 secondi.

Per un esempio in cui viene letto il file di log generato, vedere [lettura dei dati sulle prestazioni da un file di log](reading-performance-data-from-a-log-file.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_PATH    = L"\\Processor(0)\\% Processor Time";
CONST ULONG SAMPLE_INTERVAL_MS = 1000;

void DisplayCommandLineHelp(void)
{
    wprintf(L"The command line must include a valid log file name.\n"); 
}

void wmain(int argc, WCHAR **argv)
{
    HQUERY hQuery = NULL;
    HLOG hLog = NULL;
    PDH_STATUS pdhStatus;
    DWORD dwLogType = PDH_LOG_TYPE_CSV;
    HCOUNTER hCounter;
    DWORD dwCount;

    if (argc != 2) 
    {
        DisplayCommandLineHelp();
        goto cleanup;
    }

    // Open a query object.
    pdhStatus = PdhOpenQuery(NULL, 0, &hQuery);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhOpenQuery failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Add one counter that will provide the data.
    pdhStatus = PdhAddCounter(hQuery,
        COUNTER_PATH,
        0,
        &hCounter);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhAddCounter failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Open the log file for write access.
    pdhStatus = PdhOpenLog(argv[1], 
        PDH_LOG_WRITE_ACCESS | PDH_LOG_CREATE_ALWAYS,
        &dwLogType,
        hQuery,
        0, 
        NULL,
        &hLog);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhOpenLog failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }
 
    // Write 10 records to the log file.
    for (dwCount = 0; dwCount < 10; dwCount++) 
    {
        wprintf(L"Writing record %d\n", dwCount);

        pdhStatus = PdhUpdateLog (hLog, NULL);
        if (ERROR_SUCCESS != pdhStatus)
        {
            wprintf(L"PdhUpdateLog failed with 0x%x\n", pdhStatus);
            goto cleanup;
        }

        // Wait one second between samples for a counter update.
        Sleep(SAMPLE_INTERVAL_MS); 
    }

cleanup:

    // Close the log file.
    if (hLog)
        PdhCloseLog (hLog, 0);

    // Close the query object.
    if (hQuery)
        PdhCloseQuery (hQuery);
}
```



 

 



