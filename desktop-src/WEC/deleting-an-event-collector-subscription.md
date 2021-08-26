---
title: Eliminazione di una sottoscrizione dell'agente di raccolta eventi
description: È possibile eliminare una sottoscrizione di Agente di raccolta eventi da un computer locale.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9edf2f9dda2b6393ab147d5f58ff8f889952eaeb7f31f82080558697f117f3c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006091"
---
# <a name="deleting-an-event-collector-subscription"></a>Eliminazione di una sottoscrizione dell'agente di raccolta eventi

È possibile eliminare una sottoscrizione di Agente di raccolta eventi da un computer locale. È necessario conoscere il nome della sottoscrizione prima di poterla eliminare. Per altre informazioni su come elencare le sottoscrizioni correnti in un computer locale, vedere [Elenco](listing-event-collector-subscriptions.md)delle sottoscrizioni dell'agente di raccolta eventi oppure digitare il comando seguente al prompt dei comandi:

**wecutil es**

> [!Note]
>
> È possibile usare questo esempio per eliminare una sottoscrizione dell'agente di raccolta eventi oppure digitare il comando seguente al prompt dei comandi:
>
> **wecutil ds** *SubscriptionName*

 

Dopo aver recuperato il nome della sottoscrizione dell'agente di raccolta eventi da eliminare, è possibile specificare il nome della sottoscrizione come parametro per [**EcDeleteSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)

Nell'esempio di codice C++ seguente viene illustrato come eliminare una sottoscrizione dell'agente di raccolta eventi.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco delle sottoscrizioni dell'agente di raccolta eventi](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows Informazioni di riferimento sull'agente di raccolta eventi](windows-event-collector-reference.md)
</dt> </dl>

 

 




