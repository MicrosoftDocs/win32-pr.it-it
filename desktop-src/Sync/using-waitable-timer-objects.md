---
description: Nell'esempio seguente viene creato un timer che verrà segnalato dopo un ritardo di 10 secondi.
ms.assetid: 3c84c2ad-6bac-4f14-a633-51d4529314af
title: Uso di oggetti timer waitable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cb6c9e049e10a43b854b8d3c937eef513ea6ad5cf4feff8efcf5b9c0486e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959140"
---
# <a name="using-waitable-timer-objects"></a>Uso di oggetti timer waitable

Nell'esempio seguente viene creato un timer che verrà segnalato dopo un ritardo di 10 secondi. In primo luogo, il codice usa [**la funzione CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) per creare un [oggetto timer waitable.](waitable-timer-objects.md) Usa quindi la [**funzione SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) per impostare il timer. Il codice usa la [**funzione WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) per determinare quando il timer è stato segnalato.


```C++
#include <windows.h>
#include <stdio.h>

int main()
{
    HANDLE hTimer = NULL;
    LARGE_INTEGER liDueTime;

    liDueTime.QuadPart = -100000000LL;

    // Create an unnamed waitable timer.
    hTimer = CreateWaitableTimer(NULL, TRUE, NULL);
    if (NULL == hTimer)
    {
        printf("CreateWaitableTimer failed (%d)\n", GetLastError());
        return 1;
    }

    printf("Waiting for 10 seconds...\n");

    // Set a timer to wait for 10 seconds.
    if (!SetWaitableTimer(hTimer, &liDueTime, 0, NULL, NULL, 0))
    {
        printf("SetWaitableTimer failed (%d)\n", GetLastError());
        return 2;
    }

    // Wait for the timer.

    if (WaitForSingleObject(hTimer, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());
    else printf("Timer was signaled.\n");

    return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di timer waitable con una chiamata di procedura asincrona](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
