---
title: Esecuzione di query per gli eventi
description: È possibile eseguire una query per gli eventi da un canale o da un file di log.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6fa69f9b1308cd7ebbc4e4510692bb25ab031ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300382"
---
# <a name="querying-for-events"></a><span data-ttu-id="3a9b7-103">Esecuzione di query per gli eventi</span><span class="sxs-lookup"><span data-stu-id="3a9b7-103">Querying for Events</span></span>

<span data-ttu-id="3a9b7-104">È possibile eseguire una query per gli eventi da un canale o da un file di log.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-104">You can query for events from a channel or a log file.</span></span> <span data-ttu-id="3a9b7-105">Il canale o il file di log può esistere nel computer locale o in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-105">The channel or log file can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="3a9b7-106">Per specificare gli eventi che si desidera ottenere dal canale o dal file di log, utilizzare una query XPath o una query XML della struttura.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-106">To specify the events that you want to get from the channel or log file, you use an XPath query or a structure XML query.</span></span> <span data-ttu-id="3a9b7-107">Per informazioni dettagliate sulla scrittura della query, vedere [utilizzo degli eventi](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="3a9b7-107">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="3a9b7-108">Per eseguire query sugli eventi, chiamare la funzione [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) .</span><span class="sxs-lookup"><span data-stu-id="3a9b7-108">To query events, call the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) function.</span></span> <span data-ttu-id="3a9b7-109">È possibile specificare l'ordine in cui gli eventi vengono restituiti (dal meno recente al più recente (impostazione predefinita) o più recente al meno recente) e se tollerare espressioni XPath non valide nella query. per informazioni dettagliate su come la funzione ignora le espressioni in formato non valido, vedere il flag [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) .</span><span class="sxs-lookup"><span data-stu-id="3a9b7-109">You can specify the order in which the events are returned (oldest to newest (the default) or newest to oldest) and whether to tolerate malformed XPath expressions in the query (for details on how the function ignores the malformed expressions, see the [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) flag).</span></span>

<span data-ttu-id="3a9b7-110">Nell'esempio seguente viene illustrato come eseguire una query sugli eventi da un canale utilizzando un'espressione XPath.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-110">The following example shows how to query events from a channel using an XPath expression.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent); // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;
    LPWSTR pwsPath = L"<Name of the channel goes here>";
    LPWSTR pwsQuery = L"Event/System[EventID=4]";

    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath | EvtQueryReverseDirection);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"The channel was not found.\n");
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call the EvtGetExtendedStatus function to try to get 
            // additional information as to what is wrong with the query.
            wprintf(L"The query is not valid.\n");
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="3a9b7-111">Nell'esempio seguente viene illustrato come eseguire una query sugli eventi da un canale utilizzando una query XML strutturata.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-111">The following example shows how to query events from a channel using a structured XML query.</span></span> <span data-ttu-id="3a9b7-112">Gli eventi vengono restituiti in ordine dal più recente al meno recente.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-112">The events are returned in order from newest to oldest.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

// The structured XML query.
#define QUERY \
    L"<QueryList>" \
    L"  <Query Path='Name of the channel goes here'>" \
    L"    <Select>Event/System[EventID=4]</Select>" \
    L"  </Query>" \
    L"</QueryList>"

DWORD PrintQueryStatuses(EVT_HANDLE hResults);
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);  // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;

    hResults = EvtQuery(NULL, NULL, QUERY, EvtQueryChannelPath | EvtQueryTolerateQueryErrors);
    if (NULL == hResults)
    {
        // Handle error.
        goto cleanup;
    }

    // Print the status of each query. If all the queries succeeded,
    // print the events in the result set. The status can be
    // ERROR_EVT_CHANNEL_NOT_FOUND or ERROR_EVT_INVALID_QUERY among others.
    if (ERROR_SUCCESS == PrintQueryStatuses(hResults))
        PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="3a9b7-113">Se si usa una query XML strutturata e si passa il flag EvtQueryTolerateQueryErrors a [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), la funzione ha esito positivo anche se è possibile che una o più query della query strutturata siano in realtà non riuscite.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-113">If you are using a structured XML query and pass the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), the function succeeds even though one or more of the queries in the structured query may have actually failed.</span></span> <span data-ttu-id="3a9b7-114">Per determinare quali query della query strutturata hanno avuto esito positivo o negativo, chiamare la funzione [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) .</span><span class="sxs-lookup"><span data-stu-id="3a9b7-114">To determine which queries in the structured query succeeded or failed, call the [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) function.</span></span> <span data-ttu-id="3a9b7-115">Se non si passa il flag EvtQueryTolerateQueryErrors, la funzione **EvtQuery** avrà esito negativo con il primo errore rilevato nella query.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-115">If you do not pass the EvtQueryTolerateQueryErrors flag, the **EvtQuery** function will fail with the first error that it finds in the query.</span></span> <span data-ttu-id="3a9b7-116">Se la query ha esito negativo con errore \_ evt \_ query non valida \_ , chiamare la funzione [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) per ottenere una stringa di messaggio che descrive l'errore XPath.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-116">If the query fails with ERROR\_EVT\_INVALID\_QUERY, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function to get a message string that describes the XPath error.</span></span>

<span data-ttu-id="3a9b7-117">Nell'esempio seguente viene illustrato come determinare l'esito positivo o negativo di ogni query in una query strutturata quando si passa il flag EvtQueryTolerateQueryErrors a [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span><span class="sxs-lookup"><span data-stu-id="3a9b7-117">The following example shows how to determine the success or failure of each query in a structured query when passing the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span></span>


```C++
// Get the list of paths in the query and the status for each path. Return
// the sum of the statuses, so the caller can decide whether to enumerate 
// the results.
DWORD PrintQueryStatuses(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    PEVT_VARIANT pPaths = NULL;
    PEVT_VARIANT pStatuses = NULL;

    wprintf(L"List of channels/logs that were queried and their status\n\n");

    if (status = GetQueryStatusProperty(EvtQueryNames, hResults, pPaths))
        goto cleanup;

    if (status = GetQueryStatusProperty(EvtQueryStatuses, hResults, pStatuses))
        goto cleanup;

    for (DWORD i = 0; i < pPaths->Count; i++)
    {
        wprintf(L"%s (%lu)\n", pPaths->StringArr[i], pStatuses->UInt32Arr[i]);
        status += pStatuses->UInt32Arr[i];
    }

cleanup:

    if (pPaths)
        free(pPaths);

    if (pStatuses)
        free(pStatuses);

    return status;
}


// Get the list of paths specified in the query or the list of status values 
// for each path.
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;

    if  (!EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            dwBufferSize = dwBufferUsed;
            pProperty = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pProperty)
            {
                EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed);
            }
            else
            {
                wprintf(L"realloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtGetQueryInfo failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

cleanup:

    return status;
}
```



## <a name="reading-events-from-the-result-set"></a><span data-ttu-id="3a9b7-118">Lettura di eventi dal set di risultati</span><span class="sxs-lookup"><span data-stu-id="3a9b7-118">Reading events from the result set</span></span>

<span data-ttu-id="3a9b7-119">Per enumerare gli eventi nel set di risultati, chiamare la funzione [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) in un ciclo fino a quando la funzione non restituisce **false** e la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ \_ altri \_ elementi.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-119">To enumerate the events in the result set, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop until the function returns **FALSE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="3a9b7-120">Gli eventi nel set di risultati non sono statici. i nuovi eventi scritti nel canale verranno inclusi nel set di risultati fino a quando \_ non \_ viene impostato alcun numero di \_ elementi.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-120">The events in the result set are not static; new events that are written to the channel will be included in the result set until ERROR\_NO\_MORE\_ITEMS is set.</span></span> <span data-ttu-id="3a9b7-121">Per migliorare le prestazioni, recuperare gli eventi dal set di risultati in batch (tenendo conto delle dimensioni di ogni evento durante la determinazione del numero di eventi da recuperare).</span><span class="sxs-lookup"><span data-stu-id="3a9b7-121">To improve performance, fetch events from the result set in batches (taking into account the size of each event when determining the number of events to fetch).</span></span>

<span data-ttu-id="3a9b7-122">Nell'esempio seguente viene illustrato come enumerare gli eventi in un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-122">The following example shows how to enumerate the events in a result set.</span></span>


```C++
// Enumerate all the events in the result set. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;

    while (true)
    {
        // Get a block of events from the result set.
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        // For each event, call the PrintEvent function which renders the
        // event for display. PrintEvent is shown in RenderingEvents.
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (ERROR_SUCCESS == (status = PrintEvent(hEvents[i])))
            {
                EvtClose(hEvents[i]);
                hEvents[i] = NULL;
            }
            else
            {
                goto cleanup;
            }
        }
    }

cleanup:

    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}
```



<span data-ttu-id="3a9b7-123">Per informazioni dettagliate sul rendering degli eventi che si ottengono dal set di risultati, vedere [rendering degli](rendering-events.md)eventi.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-123">For details on rendering the events that you get from the result set, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="3a9b7-124">Se si desidera eseguire una query per gli eventi dal punto in cui si è interrotto, creare un segnalibro dell'ultimo evento letto e utilizzarlo alla successiva esecuzione della query.</span><span class="sxs-lookup"><span data-stu-id="3a9b7-124">If you want to query for events from where you left off, create a bookmark of the last event that you read and use it the next time you run your query.</span></span> <span data-ttu-id="3a9b7-125">Per informazioni dettagliate, vedere [segnalibro Events](bookmarking-events.md).</span><span class="sxs-lookup"><span data-stu-id="3a9b7-125">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

 

 