---
description: Nell'esempio seguente vengono letti i dati scritti in un file di log nell'esempio relativo alla scrittura dei dati sulle prestazioni in un file di log.
ms.assetid: acec1506-473a-43c9-9b57-ad8c00e8f250
title: Lettura dei dati sulle prestazioni da un file di log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43932dae6f4f3d486ad22df14954991594bd48b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312091"
---
# <a name="reading-performance-data-from-a-log-file"></a>Lettura dei dati sulle prestazioni da un file di log

Nell'esempio seguente vengono letti i dati scritti in un file di log nell'esempio relativo alla [scrittura dei dati sulle prestazioni in un file di log](writing-performance-data-to-a-log-file.md) . Usa la funzione [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per recuperare i dati dal file di log e la funzione [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) per formattare i dati per la visualizzazione.


```C++
#include <windows.h>
#include <stdio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_PATH    = L"\\Processor(0)\\% Processor Time";

void DisplayCommandLineHelp(void)
{
    wprintf(L"The command line must contain a valid log file name.\n");
}

void wmain(int argc, WCHAR **argv)
{
    HQUERY hQuery = NULL;
    HCOUNTER hCounter = NULL;
    PDH_STATUS status = ERROR_SUCCESS;
    DWORD dwFormat = PDH_FMT_DOUBLE; 
    PDH_FMT_COUNTERVALUE ItemBuffer;

    if (argc != 2) 
    {
        DisplayCommandLineHelp();
        goto cleanup;
    }

    // Opens the log file to write performance data
    status = PdhOpenQuery(argv[1], 0, &hQuery);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"PdhOpenQuery failed with 0x%x\n", status);
        goto cleanup;
    }
   
    // Add the same counter used when writing the log file.
    status = PdhAddCounter(hQuery, COUNTER_PATH, 0, &hCounter);
   
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"PdhAddCounter failed with 0x%x\n", status);
        goto cleanup;
    }

    // Read a performance data record.
    status = PdhCollectQueryData(hQuery);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"PdhCollectQueryData failed with 0x%x\n", status);
        goto cleanup;
    }

    while (ERROR_SUCCESS == status) 
    { 
        // Read the next record
        status = PdhCollectQueryData(hQuery);

        if (ERROR_SUCCESS == status)
        {
            // Format the performance data record.
            status = PdhGetFormattedCounterValue(hCounter,
                dwFormat,
                (LPDWORD)NULL,
                &ItemBuffer);

            if (ERROR_SUCCESS != status)
            {
                wprintf(L"PdhGetFormattedCounterValue failed with 0x%x.\n", status);
                goto cleanup;
            }

            wprintf(L"Formatted counter value = %.20g\n", ItemBuffer.doubleValue);
        }
        else
        {
            if (PDH_NO_MORE_DATA != status)
            {
                wprintf(L"PdhCollectQueryData failed with 0x%x\n", status);
            }
        }
    }

cleanup:

    // Close the query.
    if (hQuery)
        PdhCloseQuery(hQuery);
}
```



 

 



