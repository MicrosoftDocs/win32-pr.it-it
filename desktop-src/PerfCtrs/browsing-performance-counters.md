---
description: Codice di esempio che illustra come sfogliare i contatori delle prestazioni.
ms.assetid: 44c5cfa8-6449-45d8-ac30-979b99c086de
title: Esplorazione dei contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73ceac3faf0cddc251d7e7ebdbccff5e905519d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312188"
---
# <a name="browsing-performance-counters"></a><span data-ttu-id="34fa4-103">Esplorazione dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="34fa4-103">Browsing Performance Counters</span></span>

<span data-ttu-id="34fa4-104">Nell'esempio seguente viene illustrato come chiamare [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) per visualizzare i contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="34fa4-104">The following example shows how to call [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) to browse performance counters.</span></span> <span data-ttu-id="34fa4-105">Nell'esempio viene inoltre illustrato come raccogliere e formattare i dati dei contatori non elaborati per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="34fa4-105">The example also shows how to collect and format raw counter data for display.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST ULONG SAMPLE_INTERVAL_MS    = 1000;
CONST PWSTR BROWSE_DIALOG_CAPTION = L"Select a counter to monitor.";

void wmain(void)
{
    PDH_STATUS Status;
    HQUERY Query = NULL;
    HCOUNTER Counter;
    PDH_FMT_COUNTERVALUE DisplayValue;
    DWORD CounterType;
    SYSTEMTIME SampleTime;
    PDH_BROWSE_DLG_CONFIG BrowseDlgData;
    WCHAR CounterPathBuffer[PDH_MAX_COUNTER_PATH];

    //
    // Create a query.
    //

    Status = PdhOpenQuery(NULL, NULL, &Query);
    if (Status != ERROR_SUCCESS) 
    {
       wprintf(L"\nPdhOpenQuery failed with status 0x%x.", Status);
       goto Cleanup;
    }

    //
    // Initialize the browser dialog window settings.
    //

    ZeroMemory(&CounterPathBuffer, sizeof(CounterPathBuffer));
    ZeroMemory(&BrowseDlgData, sizeof(PDH_BROWSE_DLG_CONFIG));

    BrowseDlgData.bIncludeInstanceIndex = FALSE;
    BrowseDlgData.bSingleCounterPerAdd = TRUE;
    BrowseDlgData.bSingleCounterPerDialog = TRUE;
    BrowseDlgData.bLocalCountersOnly = FALSE;
    BrowseDlgData.bWildCardInstances = TRUE;
    BrowseDlgData.bHideDetailBox = TRUE;
    BrowseDlgData.bInitializePath = FALSE;
    BrowseDlgData.bDisableMachineSelection = FALSE;
    BrowseDlgData.bIncludeCostlyObjects = FALSE;
    BrowseDlgData.bShowObjectBrowser = FALSE;
    BrowseDlgData.hWndOwner = NULL;
    BrowseDlgData.szReturnPathBuffer = CounterPathBuffer;
    BrowseDlgData.cchReturnPathLength = PDH_MAX_COUNTER_PATH;
    BrowseDlgData.pCallBack = NULL;
    BrowseDlgData.dwCallBackArg = 0;
    BrowseDlgData.CallBackStatus = ERROR_SUCCESS;
    BrowseDlgData.dwDefaultDetailLevel = PERF_DETAIL_WIZARD;
    BrowseDlgData.szDialogBoxCaption = BROWSE_DIALOG_CAPTION;

    //
    // Display the counter browser window. The dialog is configured
    // to return a single selection from the counter list.
    //

    Status = PdhBrowseCounters(&BrowseDlgData);

    if (Status != ERROR_SUCCESS) 
    {
        if (Status == PDH_DIALOG_CANCELLED) 
        {
            wprintf(L"\nDialog canceled by user.");
        }
        else 
        {
            wprintf(L"\nPdhBrowseCounters failed with status 0x%x.", Status);
        }
        goto Cleanup;
    } 
    else if (wcslen(CounterPathBuffer) == 0) 
    {
        wprintf(L"\nUser did not select any counter.");
        goto Cleanup;
    }
    else
    {
        wprintf(L"\nCounter selected: %s\n", CounterPathBuffer);
    }

    //
    // Add the selected counter to the query.
    //

    Status = PdhAddCounter(Query, CounterPathBuffer, 0, &Counter);
    if (Status != ERROR_SUCCESS) 
    {
        wprintf(L"\nPdhAddCounter failed with status 0x%x.", Status);
        goto Cleanup;
    }

    //
    // Most counters require two sample values to display a formatted value.
    // PDH stores the current sample value and the previously collected
    // sample value. This call retrieves the first value that will be used
    // by PdhGetFormattedCounterValue in the first iteration of the loop
    // Note that this value is lost if the counter does not require two
    // values to compute a displayable value.
    //

    Status = PdhCollectQueryData(Query);
    if (Status != ERROR_SUCCESS) 
    {
        wprintf(L"\nPdhCollectQueryData failed with 0x%x.\n", Status);
        goto Cleanup;
    }

    //
    // Print counter values until a key is pressed.
    //

    while (!_kbhit()) 
    {
        Sleep(SAMPLE_INTERVAL_MS);

        GetLocalTime(&SampleTime);

        Status = PdhCollectQueryData(Query);
        if (Status != ERROR_SUCCESS) 
        {
            wprintf(L"\nPdhCollectQueryData failed with status 0x%x.", Status);
        }

        wprintf(L"\n\"%2.2d/%2.2d/%4.4d %2.2d:%2.2d:%2.2d.%3.3d\"",
                SampleTime.wMonth,
                SampleTime.wDay,
                SampleTime.wYear,
                SampleTime.wHour,
                SampleTime.wMinute,
                SampleTime.wSecond,
                SampleTime.wMilliseconds);

        //
        // Compute a displayable value for the counter.
        //

        Status = PdhGetFormattedCounterValue(Counter,
                                             PDH_FMT_DOUBLE,
                                             &CounterType,
                                             &DisplayValue);
        if (Status != ERROR_SUCCESS) 
        {
            wprintf(L"\nPdhGetFormattedCounterValue failed with status 0x%x.", Status);
            goto Cleanup;
        }

        wprintf(L",\"%.20g\"", DisplayValue.doubleValue);
    }

Cleanup:

    //
    // Close the query.
    //

    if (Query) 
    {
       PdhCloseQuery(Query);
    }
}
```



 

 



