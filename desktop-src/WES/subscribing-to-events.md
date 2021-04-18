---
title: Sottoscrizione di eventi
description: Per sottoscrivere gli eventi, chiamare la funzione EvtSubscribe.
ms.assetid: 1e86deeb-fc59-4658-9353-e4ced7ace89a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889c4ff440a17696fe6d908ff98d632ff7058ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299940"
---
# <a name="subscribing-to-events"></a><span data-ttu-id="e78f0-103">Sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="e78f0-103">Subscribing to Events</span></span>

<span data-ttu-id="e78f0-104">Per sottoscrivere gli eventi, chiamare la funzione [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .</span><span class="sxs-lookup"><span data-stu-id="e78f0-104">To subscribe to events, call the [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span> <span data-ttu-id="e78f0-105">È possibile sottoscrivere gli eventi da uno o più canali amministrativi o operativi.</span><span class="sxs-lookup"><span data-stu-id="e78f0-105">You can subscribe to events from one or more Admin or Operational channels.</span></span> <span data-ttu-id="e78f0-106">Il canale può esistere nel computer locale o in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="e78f0-106">The channel can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="e78f0-107">Per specificare gli eventi che si desidera sottoscrivere, è possibile utilizzare una query XPath o una query XML della struttura.</span><span class="sxs-lookup"><span data-stu-id="e78f0-107">To specify the events that you want to subscribe to, you can use an XPath query or a structure XML query.</span></span> <span data-ttu-id="e78f0-108">Per informazioni dettagliate sulla scrittura della query, vedere [utilizzo degli eventi](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="e78f0-108">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="e78f0-109">Nel registro eventi di Windows sono disponibili due modelli per la sottoscrizione di eventi:</span><span class="sxs-lookup"><span data-stu-id="e78f0-109">Windows Event Log provides two models for event subscription:</span></span>

-   <span data-ttu-id="e78f0-110">Il modello push effettua il push degli eventi in modo asincrono a un callback implementato.</span><span class="sxs-lookup"><span data-stu-id="e78f0-110">The push model pushes events asynchronously to a callback that you implement.</span></span>
-   <span data-ttu-id="e78f0-111">Il modello pull utilizza un handle di evento creato per segnalare quando sono disponibili eventi corrispondenti ai criteri di query.</span><span class="sxs-lookup"><span data-stu-id="e78f0-111">The pull model uses an event handle that you create to signal you when there are events available that match your query criteria.</span></span> <span data-ttu-id="e78f0-112">È quindi possibile enumerare gli eventi nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="e78f0-112">You then enumerate the events in the result set.</span></span>

<span data-ttu-id="e78f0-113">È possibile sottoscrivere eventi passati e futuri, solo eventi futuri o eventi passati e futuri che iniziano dopo l'evento con segnalibro.</span><span class="sxs-lookup"><span data-stu-id="e78f0-113">You can subscribe to past and future events, future events only, or past and future events beginning after the bookmarked event.</span></span>

<span data-ttu-id="e78f0-114">Per informazioni dettagliate sulla sottoscrizione degli eventi, vedere sottoscrizioni [push](#push-subscriptions) o [sottoscrizioni pull](#pull-subscriptions).</span><span class="sxs-lookup"><span data-stu-id="e78f0-114">For details on subscribing to events, see [Push Subscriptions](#push-subscriptions) or [Pull Subscriptions](#pull-subscriptions).</span></span>

<span data-ttu-id="e78f0-115">Per informazioni dettagliate sul rendering degli eventi, vedere [eventi di rendering](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="e78f0-115">For details on rendering the events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="e78f0-116">Per sottoscrivere gli eventi dal punto in cui è stato interrotto, creare un segnalibro prima di terminare la sottoscrizione e usarlo alla successiva sottoscrizione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="e78f0-116">If you want to subscribe to events from where you left off, create a bookmark before ending your subscription and use it the next time you subscribe to events.</span></span> <span data-ttu-id="e78f0-117">Per informazioni dettagliate, vedere [segnalibro Events](bookmarking-events.md).</span><span class="sxs-lookup"><span data-stu-id="e78f0-117">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

## <a name="push-subscriptions"></a><span data-ttu-id="e78f0-118">Sottoscrizioni push</span><span class="sxs-lookup"><span data-stu-id="e78f0-118">Push Subscriptions</span></span>

<span data-ttu-id="e78f0-119">Nell'esempio seguente viene illustrato come sottoscrivere gli eventi, implementare il callback della sottoscrizione ed eseguire il rendering degli eventi.</span><span class="sxs-lookup"><span data-stu-id="e78f0-119">The following example shows how to subscribe to events, implement the subscription callback, and render the events.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent);
DWORD PrintEvent(EVT_HANDLE hEvent);


void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";

    // Subscribe to events beginning with the oldest event in the channel. The subscription
    // will return all current events in the channel and any future events that are raised
    // while the application is active.
    hSubscription = EvtSubscribe(NULL, NULL, pwsPath, pwsQuery, NULL, NULL, 
                                 (EVT_SUBSCRIBE_CALLBACK)SubscriptionCallback, EvtSubscribeStartAtOldestRecord);
    if (NULL == hSubscription)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call EvtGetExtendedStatus to get information as to why the query is not valid.
            wprintf(L"The query \"%s\" is not valid.\n", pwsQuery);
        else
            wprintf(L"EvtSubscribe failed with %lu.\n", status);

        goto cleanup;
    }

    wprintf(L"Hit any key to quit\n\n");
    while (!_kbhit())
        Sleep(10);

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);
}

// The callback that receives the events that match the query criteria. 
DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent)
{
    UNREFERENCED_PARAMETER(pContext);
    
    DWORD status = ERROR_SUCCESS;

    switch(action)
    {
        // You should only get the EvtSubscribeActionError action if your subscription flags 
        // includes EvtSubscribeStrict and the channel contains missing event records.
        case EvtSubscribeActionError:
            if (ERROR_EVT_QUERY_RESULT_STALE == (DWORD)hEvent)
            {
                wprintf(L"The subscription callback was notified that event records are missing.\n");
                // Handle if this is an issue for your application.
            }
            else
            {
                wprintf(L"The subscription callback received the following Win32 error: %lu\n", (DWORD)hEvent);
            }
            break;

        case EvtSubscribeActionDeliver:
            if (ERROR_SUCCESS != (status = PrintEvent(hEvent)))
            {
                goto cleanup;
            }
            break;

        default:
            wprintf(L"SubscriptionCallback: Unknown action.\n");
    }

cleanup:

    if (ERROR_SUCCESS != status)
    {
        // End subscription - Use some kind of IPC mechanism to signal
        // your application to close the subscription handle.
    }

    return status; // The service ignores the returned status.
}

// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", status);
            goto cleanup;
        }
    }

    wprintf(L"%s\n\n", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}
```



## <a name="pull-subscriptions"></a><span data-ttu-id="e78f0-120">Sottoscrizioni pull</span><span class="sxs-lookup"><span data-stu-id="e78f0-120">Pull Subscriptions</span></span>

<span data-ttu-id="e78f0-121">Il modello di sottoscrizione pull utilizza un oggetto evento (vedere la funzione [**CreateEventEx**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) ) per segnalare all'applicazione che nel set di risultati sono presenti eventi che corrispondono ai criteri di query.</span><span class="sxs-lookup"><span data-stu-id="e78f0-121">The pull subscription model uses an event object (see the [**CreateEventEx**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) function) to signal the application that there are events in the result set that match the query criteria.</span></span> <span data-ttu-id="e78f0-122">Creare un costrutto di ciclo che attenda l'oggetto evento fino a quando non viene segnalato l'evento.</span><span class="sxs-lookup"><span data-stu-id="e78f0-122">Create a loop construct that waits on the event object until the event is signaled.</span></span> <span data-ttu-id="e78f0-123">Chiamare quindi la funzione [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) in un ciclo per enumerare gli eventi nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="e78f0-123">Then, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop to enumerate the events in the result set.</span></span> <span data-ttu-id="e78f0-124">Quando la funzione **EvtNext** ha esito negativo e imposta l'ultimo errore in modo che non si verifichino \_ \_ altri \_ elementi, reimpostare l'oggetto evento e attendere che il servizio segnali nuovamente l'oggetto quando sono presenti eventi nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="e78f0-124">When the **EvtNext** function fails and sets the last error to ERROR\_NO\_MORE\_ITEMS, reset the event object and wait for the service to signal the object again when there are events in the result set.</span></span>

<span data-ttu-id="e78f0-125">Nell'esempio seguente viene illustrato come utilizzare il modello di sottoscrizione pull.</span><span class="sxs-lookup"><span data-stu-id="e78f0-125">The following example shows how to use the pull subscription model.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10

DWORD EnumerateResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);
BOOL IsKeyEvent(HANDLE hStdIn);

void __cdecl wmain()
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"*";
    HANDLE aWaitHandles[2];
    DWORD dwWait = 0;

    // Get a handle for console input, so you can break out of the loop.
    aWaitHandles[0] = GetStdHandle(STD_INPUT_HANDLE);
    if (INVALID_HANDLE_VALUE == aWaitHandles[0])
    {
        wprintf(L"GetStdHandle failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Get a handle to a manual reset event object that the subscription will signal
    // when events become available that match your query criteria.
    aWaitHandles[1] = CreateEvent(NULL, TRUE, TRUE, NULL);
    if (NULL == aWaitHandles[1])
    {
        wprintf(L"CreateEvent failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Subscribe to events.
    hSubscription = EvtSubscribe(NULL, aWaitHandles[1], pwsPath, pwsQuery, NULL, NULL, NULL, EvtSubscribeStartAtOldestRecord);
    if (NULL == hSubscription)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else if (ERROR_EVT_INVALID_QUERY == status)
            wprintf(L"The query %s was not found.\n", pwsQuery);
        else
            wprintf(L"EvtSubscribe failed with %lu.\n", status);

        goto cleanup;
    }

    wprintf(L"Press any key to quit.\n");

    // Loop until the user presses a key or there is an error.
    while (true)
    {
        dwWait = WaitForMultipleObjects(sizeof(aWaitHandles)/sizeof(HANDLE), aWaitHandles, FALSE, INFINITE);

        if (0 == dwWait - WAIT_OBJECT_0)  // Console input
        {
            if (IsKeyEvent(aWaitHandles[0]))
                break;
        }
        else if (1 == dwWait - WAIT_OBJECT_0) // Query results
        {
            if (ERROR_NO_MORE_ITEMS != (status = EnumerateResults(hSubscription)))
            {
                break;
            }

            ResetEvent(aWaitHandles[1]);
        }
        else
        {
            if (WAIT_FAILED == dwWait)
            {
                wprintf(L"WaitForSingleObject failed with %lu\n", GetLastError());
            }
            break;
        }
    }

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);

    if (aWaitHandles[0])
        CloseHandle(aWaitHandles[0]);

    if (aWaitHandles[1])
        CloseHandle(aWaitHandles[1]);
}

// Enumerate the events in the result set.
DWORD EnumerateResults(EVT_HANDLE hResults)
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
        // event for display.
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

    // Closes any events in case an error occurred above.
    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}

// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    // The EvtRenderEventXml flag tells EvtRender to render the event as an XML string.
    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    wprintf(L"\n\n%s", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}

// Determines whether the console input was a key event.
BOOL IsKeyEvent(HANDLE hStdIn)
{
    INPUT_RECORD Record[128];
    DWORD dwRecordsRead = 0;
    BOOL fKeyPress = FALSE;

    if (ReadConsoleInput(hStdIn, Record, 128, &dwRecordsRead))
    {
        for (DWORD i = 0; i < dwRecordsRead; i++)
        {
            if (KEY_EVENT == Record[i].EventType)
            {
                fKeyPress = TRUE;
                break;
            }
        }
    }

    return fKeyPress;
}
```



 

 