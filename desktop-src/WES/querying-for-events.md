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
# <a name="querying-for-events"></a>Esecuzione di query per gli eventi

È possibile eseguire una query per gli eventi da un canale o da un file di log. Il canale o il file di log può esistere nel computer locale o in un computer remoto. Per specificare gli eventi che si desidera ottenere dal canale o dal file di log, utilizzare una query XPath o una query XML della struttura. Per informazioni dettagliate sulla scrittura della query, vedere [utilizzo degli eventi](consuming-events.md).

Per eseguire query sugli eventi, chiamare la funzione [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) . È possibile specificare l'ordine in cui gli eventi vengono restituiti (dal meno recente al più recente (impostazione predefinita) o più recente al meno recente) e se tollerare espressioni XPath non valide nella query. per informazioni dettagliate su come la funzione ignora le espressioni in formato non valido, vedere il flag [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) .

Nell'esempio seguente viene illustrato come eseguire una query sugli eventi da un canale utilizzando un'espressione XPath.


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



Nell'esempio seguente viene illustrato come eseguire una query sugli eventi da un canale utilizzando una query XML strutturata. Gli eventi vengono restituiti in ordine dal più recente al meno recente.


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



Se si usa una query XML strutturata e si passa il flag EvtQueryTolerateQueryErrors a [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), la funzione ha esito positivo anche se è possibile che una o più query della query strutturata siano in realtà non riuscite. Per determinare quali query della query strutturata hanno avuto esito positivo o negativo, chiamare la funzione [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) . Se non si passa il flag EvtQueryTolerateQueryErrors, la funzione **EvtQuery** avrà esito negativo con il primo errore rilevato nella query. Se la query ha esito negativo con errore \_ evt \_ query non valida \_ , chiamare la funzione [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) per ottenere una stringa di messaggio che descrive l'errore XPath.

Nell'esempio seguente viene illustrato come determinare l'esito positivo o negativo di ogni query in una query strutturata quando si passa il flag EvtQueryTolerateQueryErrors a [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).


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



## <a name="reading-events-from-the-result-set"></a>Lettura di eventi dal set di risultati

Per enumerare gli eventi nel set di risultati, chiamare la funzione [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) in un ciclo fino a quando la funzione non restituisce **false** e la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ \_ altri \_ elementi. Gli eventi nel set di risultati non sono statici. i nuovi eventi scritti nel canale verranno inclusi nel set di risultati fino a quando \_ non \_ viene impostato alcun numero di \_ elementi. Per migliorare le prestazioni, recuperare gli eventi dal set di risultati in batch (tenendo conto delle dimensioni di ogni evento durante la determinazione del numero di eventi da recuperare).

Nell'esempio seguente viene illustrato come enumerare gli eventi in un set di risultati.


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



Per informazioni dettagliate sul rendering degli eventi che si ottengono dal set di risultati, vedere [rendering degli](rendering-events.md)eventi.

Se si desidera eseguire una query per gli eventi dal punto in cui si è interrotto, creare un segnalibro dell'ultimo evento letto e utilizzarlo alla successiva esecuzione della query. Per informazioni dettagliate, vedere [segnalibro Events](bookmarking-events.md).

 

 