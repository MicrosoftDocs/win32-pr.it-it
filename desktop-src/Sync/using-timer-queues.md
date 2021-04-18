---
description: Nell'esempio seguente viene creata una routine timer che verrà eseguita da un thread da una coda timer dopo un ritardo di 10 secondi.
ms.assetid: 779156fe-f825-452b-acbe-e2cb189e24d2
title: Uso delle code timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13f7afd18a22c42e3af8cffd8b2b148f68b9d99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316063"
---
# <a name="using-timer-queues"></a><span data-ttu-id="0c7a1-103">Uso delle code timer</span><span class="sxs-lookup"><span data-stu-id="0c7a1-103">Using Timer Queues</span></span>

<span data-ttu-id="0c7a1-104">Nell'esempio seguente viene creata una routine timer che verrà eseguita da un thread da una [coda timer](timer-queues.md) dopo un ritardo di 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="0c7a1-104">The following example creates a timer routine that will be executed by a thread from a [timer queue](timer-queues.md) after a 10 second delay.</span></span> <span data-ttu-id="0c7a1-105">Innanzitutto, il codice usa la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) per creare un oggetto evento che viene segnalato al completamento del thread della coda del timer.</span><span class="sxs-lookup"><span data-stu-id="0c7a1-105">First, the code uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create an event object that is signaled when the timer-queue thread completes.</span></span> <span data-ttu-id="0c7a1-106">Crea quindi una coda timer e un timer coda timer, usando rispettivamente le funzioni [**CreateTimerQueue ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) e [**CreateTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="0c7a1-106">Then it creates a timer queue and a timer-queue timer, using the [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) and [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) functions, respectively.</span></span> <span data-ttu-id="0c7a1-107">Il codice usa la funzione [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) per determinare quando la routine del timer è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0c7a1-107">The code uses the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function to determine when the timer routine has completed.</span></span> <span data-ttu-id="0c7a1-108">Infine, il codice chiama [**deletetimerqueue ha provocato**](/windows/desktop/api/WinBase/nf-winbase-deletetimerqueue) per eseguire la pulizia.</span><span class="sxs-lookup"><span data-stu-id="0c7a1-108">Finally, the code calls [**DeleteTimerQueue**](/windows/desktop/api/WinBase/nf-winbase-deletetimerqueue) to clean up.</span></span>

<span data-ttu-id="0c7a1-109">Per ulteriori informazioni sulla routine del timer, vedere [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c7a1-109">For more information on the timer routine, see [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

HANDLE gDoneEvent;

VOID CALLBACK TimerRoutine(PVOID lpParam, BOOLEAN TimerOrWaitFired)
{
    if (lpParam == NULL)
    {
        printf("TimerRoutine lpParam is NULL\n");
    }
    else
    {
        // lpParam points to the argument; in this case it is an int

        printf("Timer routine called. Parameter is %d.\n", 
                *(int*)lpParam);
        if(TimerOrWaitFired)
        {
            printf("The wait timed out.\n");
        }
        else
        {
            printf("The wait event was signaled.\n");
        }
    }

    SetEvent(gDoneEvent);
}

int main()
{
    HANDLE hTimer = NULL;
    HANDLE hTimerQueue = NULL;
    int arg = 123;

    // Use an event object to track the TimerRoutine execution
    gDoneEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == gDoneEvent)
    {
        printf("CreateEvent failed (%d)\n", GetLastError());
        return 1;
    }

    // Create the timer queue.
    hTimerQueue = CreateTimerQueue();
    if (NULL == hTimerQueue)
    {
        printf("CreateTimerQueue failed (%d)\n", GetLastError());
        return 2;
    }

    // Set a timer to call the timer routine in 10 seconds.
    if (!CreateTimerQueueTimer( &hTimer, hTimerQueue, 
            (WAITORTIMERCALLBACK)TimerRoutine, &arg , 10000, 0, 0))
    {
        printf("CreateTimerQueueTimer failed (%d)\n", GetLastError());
        return 3;
    }

    // TODO: Do other useful work here 

    printf("Call timer routine in 10 seconds...\n");

    // Wait for the timer-queue thread to complete using an event 
    // object. The thread will signal the event at that time.

    if (WaitForSingleObject(gDoneEvent, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());

    CloseHandle(gDoneEvent);

    // Delete all timers in the timer queue.
    if (!DeleteTimerQueue(hTimerQueue))
        printf("DeleteTimerQueue failed (%d)\n", GetLastError());

    return 0;
}
```



 

 
