---
title: Eliminazione di una sottoscrizione di raccolta eventi
description: È possibile eliminare una sottoscrizione di raccolta eventi da un computer locale.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cec036625bbb94e33e71af0f1d9808ad9252a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710132"
---
# <a name="deleting-an-event-collector-subscription"></a><span data-ttu-id="11dea-103">Eliminazione di una sottoscrizione di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="11dea-103">Deleting an Event Collector Subscription</span></span>

<span data-ttu-id="11dea-104">È possibile eliminare una sottoscrizione di raccolta eventi da un computer locale.</span><span class="sxs-lookup"><span data-stu-id="11dea-104">You can delete an Event Collector subscription from a local computer.</span></span> <span data-ttu-id="11dea-105">Prima di poter eliminare il nome della sottoscrizione, è necessario conoscerne il nome.</span><span class="sxs-lookup"><span data-stu-id="11dea-105">You must know the name of the subscription before you can delete it.</span></span> <span data-ttu-id="11dea-106">Per ulteriori informazioni su come elencare le sottoscrizioni correnti in un computer locale, vedere elenco delle sottoscrizioni degli agenti di [raccolta eventi](listing-event-collector-subscriptions.md)oppure digitare il comando seguente al prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="11dea-106">For more information about how to list the current subscriptions on a local computer, see [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or type the following command at the command prompt:</span></span>

<span data-ttu-id="11dea-107">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="11dea-107">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="11dea-108">È possibile usare questo esempio per eliminare una sottoscrizione di raccolta eventi oppure è possibile digitare il comando seguente al prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="11dea-108">You can use this example to delete an Event Collector subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="11dea-109">sottoscrizioni **DS wecutil** </span><span class="sxs-lookup"><span data-stu-id="11dea-109">**wecutil ds** *SubscriptionName*</span></span>

 

<span data-ttu-id="11dea-110">Dopo aver recuperato il nome della sottoscrizione dell'agente di raccolta eventi da eliminare, è possibile specificare il nome della sottoscrizione come parametro per [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span><span class="sxs-lookup"><span data-stu-id="11dea-110">After you retrieve the name of the Event Collector subscription to delete, you can provide the name of the subscription as a parameter to [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span></span>

<span data-ttu-id="11dea-111">Nell'esempio di codice C++ riportato di seguito viene illustrato come eliminare una sottoscrizione di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="11dea-111">The following C++ code example shows how to delete an Event Collector subscription.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    DWORD dwRetVal;
    LPWSTR lpSubname = L"MyTestSubscription";

    // Delete the specified Event Collector subscription.
    if (!EcDeleteSubscription(lpSubname, 0))
    {
        dwRetVal = GetLastError();
        LPVOID lpwszBuffer;

        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);

        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." 
                L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n"
            L"Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="11dea-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11dea-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11dea-113">Elenco delle sottoscrizioni degli agenti di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="11dea-113">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="11dea-114">Informazioni di riferimento sull'agente di raccolta eventi Windows</span><span class="sxs-lookup"><span data-stu-id="11dea-114">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




