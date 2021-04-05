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
# <a name="deleting-an-event-collector-subscription"></a>Eliminazione di una sottoscrizione di raccolta eventi

È possibile eliminare una sottoscrizione di raccolta eventi da un computer locale. Prima di poter eliminare il nome della sottoscrizione, è necessario conoscerne il nome. Per ulteriori informazioni su come elencare le sottoscrizioni correnti in un computer locale, vedere elenco delle sottoscrizioni degli agenti di [raccolta eventi](listing-event-collector-subscriptions.md)oppure digitare il comando seguente al prompt dei comandi:

**wecutil es**

> [!Note]
>
> È possibile usare questo esempio per eliminare una sottoscrizione di raccolta eventi oppure è possibile digitare il comando seguente al prompt dei comandi:
>
> sottoscrizioni **DS wecutil** 

 

Dopo aver recuperato il nome della sottoscrizione dell'agente di raccolta eventi da eliminare, è possibile specificare il nome della sottoscrizione come parametro per [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).

Nell'esempio di codice C++ riportato di seguito viene illustrato come eliminare una sottoscrizione di raccolta eventi.


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

[Elenco delle sottoscrizioni degli agenti di raccolta eventi](listing-event-collector-subscriptions.md)
</dt> <dt>

[Informazioni di riferimento sull'agente di raccolta eventi Windows](windows-event-collector-reference.md)
</dt> </dl>

 

 




