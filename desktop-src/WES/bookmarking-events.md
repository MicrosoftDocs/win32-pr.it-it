---
title: Eventi di segnalibro
description: Un segnalibro identifica un evento in un canale o un file di log.
ms.assetid: e7eeafc3-deb9-4cdc-9763-f784db7333be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d7fb4aef883a51084420c5a2d78e4f0ff25dac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299941"
---
# <a name="bookmarking-events"></a><span data-ttu-id="31b0b-103">Eventi di segnalibro</span><span class="sxs-lookup"><span data-stu-id="31b0b-103">Bookmarking Events</span></span>

<span data-ttu-id="31b0b-104">Un segnalibro identifica un evento in un canale o un file di log.</span><span class="sxs-lookup"><span data-stu-id="31b0b-104">A bookmark identifies an event in a channel or log file.</span></span> <span data-ttu-id="31b0b-105">È possibile utilizzare un segnalibro quando si esegue una query per o si sottoscrive eventi per iniziare a leggere gli eventi da tale evento con segnalibro.</span><span class="sxs-lookup"><span data-stu-id="31b0b-105">You can use a bookmark when you query for or subscribe to events to begin reading events from that bookmarked event.</span></span> <span data-ttu-id="31b0b-106">In genere si crea un segnalibro dell'ultimo evento nel set di risultati (presupponendo che siano stati enumerati tutti gli eventi nel set di risultati).</span><span class="sxs-lookup"><span data-stu-id="31b0b-106">Typically you create a bookmark of the last event in the result set (assuming that you have enumerated all events in the result set).</span></span>

<span data-ttu-id="31b0b-107">Nella procedura riportata di seguito viene descritto come creare un segnalibro da un evento.</span><span class="sxs-lookup"><span data-stu-id="31b0b-107">The following procedure describes how to create a bookmark from an event.</span></span>

<span data-ttu-id="31b0b-108">**Per creare un segnalibro da un evento**</span><span class="sxs-lookup"><span data-stu-id="31b0b-108">**To create a bookmark from an event**</span></span>

1.  <span data-ttu-id="31b0b-109">Chiamare la funzione [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) per creare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="31b0b-109">Call the [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) function to create a bookmark.</span></span> <span data-ttu-id="31b0b-110">Passare **null** per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="31b0b-110">Pass **NULL** for the argument.</span></span>
2.  <span data-ttu-id="31b0b-111">Chiamare la funzione [**EvtUpdateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtupdatebookmark) per aggiornare il segnalibro con l'evento.</span><span class="sxs-lookup"><span data-stu-id="31b0b-111">Call the [**EvtUpdateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtupdatebookmark) function to update the bookmark with the event.</span></span> <span data-ttu-id="31b0b-112">Passare l'handle all'evento come argomento.</span><span class="sxs-lookup"><span data-stu-id="31b0b-112">Pass the handle to the event as the argument.</span></span>
3.  <span data-ttu-id="31b0b-113">Chiamare la funzione [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) per creare una stringa XML che rappresenta il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="31b0b-113">Call the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to create an XML string that represents the bookmark.</span></span> <span data-ttu-id="31b0b-114">Passare EvtRenderBookmark come flag di rendering.</span><span class="sxs-lookup"><span data-stu-id="31b0b-114">Pass EvtRenderBookmark as the rendering flag.</span></span>
4.  <span data-ttu-id="31b0b-115">Rende permanente la stringa XML da utilizzare in un secondo momento (ad esempio, è possibile salvare in maniera permanente la stringa XML in un file o nel registro di sistema).</span><span class="sxs-lookup"><span data-stu-id="31b0b-115">Persist the XML string for use later (for example, you can persist the XML string in a file or the registry).</span></span>

<span data-ttu-id="31b0b-116">Nella procedura riportata di seguito viene descritto come creare un segnalibro utilizzando una stringa di segnalibro XML che è stata salvata in modo permanente nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="31b0b-116">The following procedure describes how to create a bookmark using an XML bookmark string that was persisted in the previous procedure.</span></span>

<span data-ttu-id="31b0b-117">**Per creare un segnalibro usando una stringa di segnalibro XML**</span><span class="sxs-lookup"><span data-stu-id="31b0b-117">**To create a bookmark using an XML bookmark string**</span></span>

1.  <span data-ttu-id="31b0b-118">Ottenere la stringa XML che rappresenta il segnalibro salvato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="31b0b-118">Get the XML string that represents the bookmark that you previously persisted.</span></span>
2.  <span data-ttu-id="31b0b-119">Chiamare la funzione [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) per creare un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="31b0b-119">Call the [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) function to create a bookmark.</span></span> <span data-ttu-id="31b0b-120">Passare la stringa XML per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="31b0b-120">Pass the XML string for the argument.</span></span>

<span data-ttu-id="31b0b-121">Nella procedura riportata di seguito viene descritto come utilizzare un segnalibro in una query.</span><span class="sxs-lookup"><span data-stu-id="31b0b-121">The following procedure describes how to use a bookmark in a query.</span></span>

<span data-ttu-id="31b0b-122">**Per utilizzare un segnalibro in una query**</span><span class="sxs-lookup"><span data-stu-id="31b0b-122">**To use a bookmark in a query**</span></span>

1.  <span data-ttu-id="31b0b-123">Chiamare la funzione [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) per ottenere gli eventi che corrispondono alla query.</span><span class="sxs-lookup"><span data-stu-id="31b0b-123">Call the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) function to get events that match your query.</span></span>
2.  <span data-ttu-id="31b0b-124">Chiamare la funzione [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek) per cercare l'evento con segnalibro.</span><span class="sxs-lookup"><span data-stu-id="31b0b-124">Call the [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek) function to seek to the bookmarked event.</span></span> <span data-ttu-id="31b0b-125">Passare l'handle al segnalibro e al flag EvtSeekRelativeToBookmark.</span><span class="sxs-lookup"><span data-stu-id="31b0b-125">Pass the handle to the bookmark and the EvtSeekRelativeToBookmark flag.</span></span>
3.  <span data-ttu-id="31b0b-126">Chiamare la funzione [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) in un ciclo per enumerare gli eventi che iniziano dopo l'evento con segnalibro, a seconda dell'offset specificato in [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek).</span><span class="sxs-lookup"><span data-stu-id="31b0b-126">Call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop to enumerate the events that begin after the bookmarked event (depending on the offset you specified in [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek)).</span></span>

<span data-ttu-id="31b0b-127">Per un esempio, vedere [uso di un segnalibro in una query](#using-a-bookmark-in-a-query).</span><span class="sxs-lookup"><span data-stu-id="31b0b-127">For an example, see [Using a bookmark in a query](#using-a-bookmark-in-a-query).</span></span>

<span data-ttu-id="31b0b-128">Nella procedura riportata di seguito viene descritto come utilizzare un segnalibro in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="31b0b-128">The following procedure describes how to use a bookmark in a subscription.</span></span>

<span data-ttu-id="31b0b-129">**Per usare un segnalibro in una sottoscrizione**</span><span class="sxs-lookup"><span data-stu-id="31b0b-129">**To use a bookmark in a subscription**</span></span>

1.  <span data-ttu-id="31b0b-130">Chiamare la funzione [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) per sottoscrivere gli eventi che corrispondono alla query.</span><span class="sxs-lookup"><span data-stu-id="31b0b-130">Call the [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function to subscribe to events that match your query.</span></span> <span data-ttu-id="31b0b-131">Passare l'handle al segnalibro e al flag EvtSubscribeStartAfterBookmark.</span><span class="sxs-lookup"><span data-stu-id="31b0b-131">Pass the handle to the bookmark and the EvtSubscribeStartAfterBookmark flag.</span></span>
2.  <span data-ttu-id="31b0b-132">Se è stata implementata la funzione di [**\_ \_ callback sottoscrizioni evt**](/windows/win32/api/winevt/nc-winevt-evt_subscribe_callback) , il callback riceverà gli eventi che iniziano dopo l'evento con segnalibro.</span><span class="sxs-lookup"><span data-stu-id="31b0b-132">If you implemented the [**EVT\_SUBSCRIBE\_CALLBACK**](/windows/win32/api/winevt/nc-winevt-evt_subscribe_callback) function, your callback will receive events that begin after the bookmarked event.</span></span>
3.  <span data-ttu-id="31b0b-133">Se non è stato implementato il callback, chiamare la funzione [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) in un ciclo per enumerare gli eventi che iniziano dopo l'evento con segnalibro.</span><span class="sxs-lookup"><span data-stu-id="31b0b-133">If you did not implement the callback, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop to enumerate the events that begin after the bookmarked event.</span></span>

<span data-ttu-id="31b0b-134">Per un esempio, vedere [uso di un segnalibro in una sottoscrizione](#using-a-bookmark-in-a-subscription).</span><span class="sxs-lookup"><span data-stu-id="31b0b-134">For an example, see [Using a bookmark in a subscription](#using-a-bookmark-in-a-subscription).</span></span>

## <a name="using-a-bookmark-in-a-query"></a><span data-ttu-id="31b0b-135">Uso di un segnalibro in una query</span><span class="sxs-lookup"><span data-stu-id="31b0b-135">Using a bookmark in a query</span></span>

<span data-ttu-id="31b0b-136">Nell'esempio seguente viene illustrato come utilizzare un segnalibro in una query.</span><span class="sxs-lookup"><span data-stu-id="31b0b-136">The following example shows how to use a bookmark in a query.</span></span> <span data-ttu-id="31b0b-137">Nell'esempio viene espansa l'esempio nell' [esecuzione di query per gli eventi](querying-for-events.md).</span><span class="sxs-lookup"><span data-stu-id="31b0b-137">The example expands on the example in [Querying for Events](querying-for-events.md).</span></span>


```C++
// Enumerate all the events in the result set beginning with the bookmarked event. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;
    LPWSTR pwsBookmarkXml = NULL;
    EVT_HANDLE hBookmark = NULL;

    // Get the persisted bookmark XML string.
    pwsBookmarkXml = GetBookmarkedString();

    // If the bookmark string was persisted, create a bookmark and
    // seek to the bookmarked event in the result set.
    if (pwsBookmarkXml)
    {
        hBookmark = EvtCreateBookmark(pwsBookmarkXml);
        if (NULL == hBookmark)
        {
            wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
            goto cleanup;
        }

        if (!EvtSeek(hResults, 1, hBookmark, 0, EvtSeekRelativeToBookmark))
        {
            wprintf(L"EvtSeek failed with %lu\n", GetLastError());
            goto cleanup;
        }
    }

    // Enumerate the events in the result set after the bookmarked event.
    while (true)
    {
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (status = PrintEvent(hEvents[i]))
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

    if (ERROR_NO_MORE_ITEMS == status)
    {
        // Get the last event in the result set, use it to create a
        // bookmark, render the bookmark as an XML string, and persist the string.
        if (ERROR_SUCCESS != (status = SaveBookmark(hResults)))
            wprintf(L"\nFailed to save bookmark\n");
    }
    else
    {
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (NULL != hEvents[i])
                EvtClose(hEvents[i]);
        }
    }

    if (pwsBookmarkXml)
        free(pwsBookmarkXml);

    return status;
}

// Get the bookmark XML string from wherever you persisted it.
LPWSTR GetBookmarkedString(void)
{
    LPWSTR pwsBookmarkXML = NULL;

    // TODO: Add the code to get the bookmark XML string from storage.

    return pwsBookmarkXML;
}


// Persist the bookmark XML string. This example assumes that we've read through
// the result set and are persisting the last event as the bookmark.
DWORD SaveBookmark(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    DWORD dwReturned = 0;
    LPWSTR pBookmarkXml = NULL;
    EVT_HANDLE hBookmark = NULL;
    EVT_HANDLE hEvent = NULL;

    // Seek to the last event in the result set and get the event.
    if (!EvtSeek(hResults, 0, NULL, 0, EvtSeekRelativeToLast))
    {
        wprintf(L"EvtSeek failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    if (!EvtNext(hResults, 1, &hEvent, INFINITE, 0, &dwReturned))
    {
        wprintf(L"EvtNext failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    // Create a bookmark and update it with the last event in the result set.
    hBookmark = EvtCreateBookmark(NULL);
    if (NULL == hBookmark)
    {
        wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

    if (!EvtUpdateBookmark(hBookmark, hEvent))
    {
        wprintf(L"EvtUpdateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

    // Render the bookmark as an XML string that you can then persist.
    if (!EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pBookmarkXml = (LPWSTR)malloc(dwBufferSize);
            if (pBookmarkXml)
            {
                EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount);
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

    // TODO: Add code to persist bookmark XML string.

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    if (hBookmark)
        EvtClose(hBookmark);

    if (hEvent)
        EvtClose(hEvent);

    return status;
}
```



## <a name="using-a-bookmark-in-a-subscription"></a><span data-ttu-id="31b0b-138">Uso di un segnalibro in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="31b0b-138">Using a bookmark in a subscription</span></span>

<span data-ttu-id="31b0b-139">Nell'esempio seguente viene illustrato come utilizzare un segnalibro in una sottoscrizione push.</span><span class="sxs-lookup"><span data-stu-id="31b0b-139">The following example shows how to use a bookmark in a push subscription.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent);
DWORD PrintEvent(EVT_HANDLE hEvent);
EVT_HANDLE GetBookmark();
DWORD SaveBookmark(EVT_HANDLE hBookmark);


void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    EVT_HANDLE hBookmark = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";

    // Get the saved bookmark.
    hBookmark = GetBookmark();

    // Subscribe to existing and furture events beginning with the bookmarked event.
    // If the bookmark has not been persisted, pass an empty bookmark and the subscription
    // will begin with the second event that matches the query criteria.
    hSubscription = EvtSubscribe(NULL, NULL, pwsPath, pwsQuery, hBookmark, (PVOID)hBookmark, 
                                 (EVT_SUBSCRIBE_CALLBACK)SubscriptionCallback, EvtSubscribeStartAfterBookmark);
    if (NULL == hSubscription)
    {
        wprintf(L"EvtSubscribe failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Hit any key to quit\n\n");
    while (!_kbhit())
        Sleep(10);

    status = SaveBookmark(hBookmark);

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);

    if (hBookmark)
        EvtClose(hBookmark);
 }


// The callback that receives the events that match the query criteria. Use the 
// context parameter to pass the handle to the bookmark, so you can update the bookmark
// with each event that you receive.
DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hBookmark = (EVT_HANDLE)pContext;

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

            if (!EvtUpdateBookmark(hBookmark, hEvent))
            {
                wprintf(L"EvtUpdateBookmark failed with %lu\n", status = GetLastError());
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


EVT_HANDLE GetBookmark(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hBookmark = NULL;
    LPWSTR pBookmarkXml = NULL;

    // Set pBookmarkXml to the XML string that you persisted in SaveBookmark.

    hBookmark = EvtCreateBookmark(pBookmarkXml);
    if (NULL == hBookmark)
    {
        wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    return hBookmark;
}


DWORD SaveBookmark(EVT_HANDLE hBookmark)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pBookmarkXml = NULL;

    if (!EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pBookmarkXml = (LPWSTR)malloc(dwBufferSize);
            if (pBookmarkXml)
            {
                EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount);
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

    // Persist bookmark to a file or the registry.

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

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



 

 