---
description: Nell'esempio seguente viene creato un timer che verrà segnalato dopo un ritardo di 10 secondi.
ms.assetid: 3c84c2ad-6bac-4f14-a633-51d4529314af
title: Uso di oggetti timer waitable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a23b0d9f6ab74df325be81eb9236bffe6a0c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316062"
---
# <a name="using-waitable-timer-objects"></a>Uso di oggetti timer waitable

Nell'esempio seguente viene creato un timer che verrà segnalato dopo un ritardo di 10 secondi. Per prima cosa, il codice usa la funzione [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) per creare un [oggetto timer in attesa](waitable-timer-objects.md). USA quindi la funzione [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) per impostare il timer. Il codice usa la funzione [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) per determinare quando il timer è stato segnalato.


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

 

 
