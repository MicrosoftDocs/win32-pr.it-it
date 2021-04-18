---
description: Il codice di esempio seguente apre la porta seriale per le operazioni di I/O sovrapposte, crea una maschera di eventi per monitorare i segnali CTS e DSR e quindi attende che si verifichi un evento.
ms.assetid: 23ebcb04-1571-4e93-a549-46ad6b9d4272
title: Monitoraggio degli eventi di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5eac453b7f864f4f0b5fc756b1ffc6a730e2769
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304850"
---
# <a name="monitoring-communications-events"></a><span data-ttu-id="5d843-103">Monitoraggio degli eventi di comunicazione</span><span class="sxs-lookup"><span data-stu-id="5d843-103">Monitoring Communications Events</span></span>

<span data-ttu-id="5d843-104">Il codice di esempio seguente apre la porta seriale per le operazioni di I/O sovrapposte, crea una maschera di eventi per monitorare i segnali CTS e DSR e quindi attende che si verifichi un evento.</span><span class="sxs-lookup"><span data-stu-id="5d843-104">The following example code opens the serial port for overlapped I/O, creates an event mask to monitor CTS and DSR signals, and then waits for an event to occur.</span></span> <span data-ttu-id="5d843-105">La funzione [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) deve essere eseguita come operazione sovrapposta, in modo che gli altri thread del processo possano eseguire operazioni di I/O durante l'attesa.</span><span class="sxs-lookup"><span data-stu-id="5d843-105">The [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) function should be executed as an overlapped operation so the other threads of the process can perform I/O operations during the wait.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <assert.h>
#include <stdio.h>

void _tmain(
            int argc, 
            TCHAR *argv[]
           )
{
    HANDLE hCom;
    OVERLAPPED o;
    BOOL fSuccess;
    DWORD dwEvtMask;

    hCom = CreateFile( TEXT("\\\\.\\COM1"),
        GENERIC_READ | GENERIC_WRITE,
        0,    // exclusive access 
        NULL, // default security attributes 
        OPEN_EXISTING,
        FILE_FLAG_OVERLAPPED,
        NULL 
        );

    if (hCom == INVALID_HANDLE_VALUE) 
    {
        // Handle the error. 
        printf("CreateFile failed with error %d.\n", GetLastError());
        return;
    }

    // Set the event mask. 

    fSuccess = SetCommMask(hCom, EV_CTS | EV_DSR);

    if (!fSuccess) 
    {
        // Handle the error. 
        printf("SetCommMask failed with error %d.\n", GetLastError());
        return;
    }

    // Create an event object for use by WaitCommEvent. 

    o.hEvent = CreateEvent(
        NULL,   // default security attributes 
        TRUE,   // manual-reset event 
        FALSE,  // not signaled 
        NULL    // no name
         );
    

    // Initialize the rest of the OVERLAPPED structure to zero.
    o.Internal = 0;
    o.InternalHigh = 0;
    o.Offset = 0;
    o.OffsetHigh = 0;

    assert(o.hEvent);

    if (WaitCommEvent(hCom, &dwEvtMask, &o)) 
    {
        if (dwEvtMask & EV_DSR) 
        {
             // To do.
        }

        if (dwEvtMask & EV_CTS) 
        {
            // To do. 
        }
    }
    else
    {
        DWORD dwRet = GetLastError();
        if( ERROR_IO_PENDING == dwRet)
        {
            printf("I/O is pending...\n");

            // To do.
        }
        else 
            printf("Wait failed with error %d.\n", GetLastError());
    }
}
```



 

 



