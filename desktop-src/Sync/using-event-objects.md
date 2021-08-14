---
description: Le applicazioni possono usare oggetti evento in diverse situazioni per notificare a un thread in attesa l'occorrenza di un evento.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Uso di oggetti evento (sincronizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8466ca1104a4d8e6ddaaed3e0618bea3db68bd1954aaf3b859f66fb93a3aac79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765332"
---
# <a name="using-event-objects-synchronization"></a>Uso di oggetti evento (sincronizzazione)

Le applicazioni possono [usare oggetti evento](event-objects.md) in diverse situazioni per notificare a un thread in attesa l'occorrenza di un evento. Ad esempio, le operazioni di I/O sovrapposte su file, named pipe e dispositivi di comunicazione usano un oggetto evento per segnalarne il completamento. Per altre informazioni sull'uso di oggetti evento in operazioni di I/O sovrapposte, vedere Sincronizzazione e [input e output sovrapposti.](synchronization-and-overlapped-input-and-output.md)

Nell'esempio seguente vengono utilizzati oggetti evento per impedire a diversi thread di leggere da un buffer di memoria condivisa mentre un thread master sta scrivendo in tale buffer. In primo luogo, il thread master usa la [**funzione CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) per creare un oggetto evento di reimpostazione manuale il cui stato iniziale non è associato a un'assegnazione. Crea quindi diversi thread di lettura. Il thread master esegue un'operazione di scrittura e quindi imposta l'oggetto evento sullo stato segnalato al termine della scrittura.

Prima di avviare un'operazione di lettura, ogni thread di lettura usa [**WaitForSingleObject per**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) attendere la segnalazione dell'oggetto evento di reimpostazione manuale. Quando **viene restituito WaitForSingleObject,** indica che il thread principale è pronto per iniziare l'operazione di lettura.


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 4 

HANDLE ghWriteEvent; 
HANDLE ghThreads[THREADCOUNT];

DWORD WINAPI ThreadProc(LPVOID);

void CreateEventsAndThreads(void) 
{
    int i; 
    DWORD dwThreadID; 

    // Create a manual-reset event object. The write thread sets this
    // object to the signaled state when it finishes writing to a 
    // shared buffer. 

    ghWriteEvent = CreateEvent( 
        NULL,               // default security attributes
        TRUE,               // manual-reset event
        FALSE,              // initial state is nonsignaled
        TEXT("WriteEvent")  // object name
        ); 

    if (ghWriteEvent == NULL) 
    { 
        printf("CreateEvent failed (%d)\n", GetLastError());
        return;
    }

    // Create multiple threads to read from the buffer.

    for(i = 0; i < THREADCOUNT; i++) 
    {
        // TODO: More complex scenarios may require use of a parameter
        //   to the thread procedure, such as an event per thread to  
        //   be used for synchronization.
        ghThreads[i] = CreateThread(
            NULL,              // default security
            0,                 // default stack size
            ThreadProc,        // name of the thread function
            NULL,              // no thread parameters
            0,                 // default startup flags
            &dwThreadID); 

        if (ghThreads[i] == NULL) 
        {
            printf("CreateThread failed (%d)\n", GetLastError());
            return;
        }
    }
}

void WriteToBuffer(VOID) 
{
    // TODO: Write to the shared buffer.
    
    printf("Main thread writing to the shared buffer...\n");

    // Set ghWriteEvent to signaled

    if (! SetEvent(ghWriteEvent) ) 
    {
        printf("SetEvent failed (%d)\n", GetLastError());
        return;
    }
}

void CloseEvents()
{
    // Close all event handles (currently, only one global handle).
    
    CloseHandle(ghWriteEvent);
}

int main( void )
{
    DWORD dwWaitResult;

    // TODO: Create the shared buffer

    // Create events and THREADCOUNT threads to read from the buffer

    CreateEventsAndThreads();

    // At this point, the reader threads have started and are most
    // likely waiting for the global event to be signaled. However, 
    // it is safe to write to the buffer because the event is a 
    // manual-reset event.
    
    WriteToBuffer();

    printf("Main thread waiting for threads to exit...\n");

    // The handle for each thread is signaled when the thread is
    // terminated.
    dwWaitResult = WaitForMultipleObjects(
        THREADCOUNT,   // number of handles in array
        ghThreads,     // array of thread handles
        TRUE,          // wait until all are signaled
        INFINITE);

    switch (dwWaitResult) 
    {
        // All thread objects were signaled
        case WAIT_OBJECT_0: 
            printf("All threads ended, cleaning up for application exit...\n");
            break;

        // An error occurred
        default: 
            printf("WaitForMultipleObjects failed (%d)\n", GetLastError());
            return 1;
    } 
            
    // Close the events to clean up

    CloseEvents();

    return 0;
}

DWORD WINAPI ThreadProc(LPVOID lpParam) 
{
    // lpParam not used in this example.
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult;

    printf("Thread %d waiting for write event...\n", GetCurrentThreadId());
    
    dwWaitResult = WaitForSingleObject( 
        ghWriteEvent, // event handle
        INFINITE);    // indefinite wait

    switch (dwWaitResult) 
    {
        // Event object was signaled
        case WAIT_OBJECT_0: 
            //
            // TODO: Read from the shared buffer
            //
            printf("Thread %d reading from buffer\n", 
                   GetCurrentThreadId());
            break; 

        // An error occurred
        default: 
            printf("Wait error (%d)\n", GetLastError()); 
            return 0; 
    }

    // Now that we are done reading the buffer, we could use another
    // event to signal that this thread is no longer reading. This
    // example simply uses the thread handle for synchronization (the
    // handle is signaled when the thread terminates.)

    printf("Thread %d exiting\n", GetCurrentThreadId());
    return 1;
}

```



 

 
