---
description: È possibile usare un oggetto mutex per proteggere una risorsa condivisa dall'accesso simultaneo da più thread o processi.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Utilizzo di oggetti mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd68f41319125613e8569e7b343c0b1601a7735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312741"
---
# <a name="using-mutex-objects"></a>Utilizzo di oggetti mutex

È possibile usare un [oggetto mutex](mutex-objects.md) per proteggere una risorsa condivisa dall'accesso simultaneo da più thread o processi. Ogni thread deve attendere la proprietà del mutex prima di poter eseguire il codice che accede alla risorsa condivisa. Se, ad esempio, più thread condividono l'accesso a un database, i thread possono usare un oggetto mutex per consentire a un solo thread alla volta di scrivere nel database.

Nell'esempio seguente viene usata la funzione [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) per creare un oggetto mutex e la funzione [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) per creare thread di lavoro.

Quando un thread di questo processo scrive nel database, richiede prima di tutto la proprietà del mutex usando la funzione [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) . Se il thread ottiene la proprietà del mutex, scrive nel database e quindi rilascia la relativa proprietà del mutex utilizzando la funzione [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .

In questo esempio viene utilizzata la gestione strutturata delle eccezioni per garantire che il thread rilasci correttamente l'oggetto mutex. Il blocco **\_ \_ finally** del codice viene eseguito indipendentemente dal modo in cui il blocco **\_ \_ try** termina (a meno che il blocco **\_ \_ try** non includa una chiamata alla funzione [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ). In questo modo si impedisce che l'oggetto mutex venga abbandonato inavvertitamente.

Se un mutex viene abbandonato, il thread di proprietà del mutex non lo rilascia correttamente prima di terminare. In questo caso, lo stato della risorsa condivisa è indeterminato e la continuazione dell'utilizzo del mutex può nascondere un errore potenzialmente grave. Alcune applicazioni potrebbero tentare di ripristinare lo stato coerente della risorsa; in questo esempio viene semplicemente restituito un errore e viene interrotto l'utilizzo del mutex. Per ulteriori informazioni, vedere [oggetti mutex](mutex-objects.md).


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 2

HANDLE ghMutex; 

DWORD WINAPI WriteToDatabase( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a mutex with no initial owner

    ghMutex = CreateMutex( 
        NULL,              // default security attributes
        FALSE,             // initially not owned
        NULL);             // unnamed mutex

    if (ghMutex == NULL) 
    {
        printf("CreateMutex error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) WriteToDatabase, 
                     NULL,       // no thread function arguments
                     0,          // default creation flags
                     &ThreadID); // receive thread identifier

        if( aThread[i] == NULL )
        {
            printf("CreateThread error: %d\n", GetLastError());
            return 1;
        }
    }

    // Wait for all threads to terminate

    WaitForMultipleObjects(THREADCOUNT, aThread, TRUE, INFINITE);

    // Close thread and mutex handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghMutex);

    return 0;
}

DWORD WINAPI WriteToDatabase( LPVOID lpParam )
{ 
    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwCount=0, dwWaitResult; 

    // Request ownership of mutex.

    while( dwCount < 20 )
    { 
        dwWaitResult = WaitForSingleObject( 
            ghMutex,    // handle to mutex
            INFINITE);  // no time-out interval
 
        switch (dwWaitResult) 
        {
            // The thread got ownership of the mutex
            case WAIT_OBJECT_0: 
                __try { 
                    // TODO: Write to the database
                    printf("Thread %d writing to database...\n", 
                            GetCurrentThreadId());
                    dwCount++;
                } 

                __finally { 
                    // Release ownership of the mutex object
                    if (! ReleaseMutex(ghMutex)) 
                    { 
                        // Handle error.
                    } 
                } 
                break; 

            // The thread got ownership of an abandoned mutex
            // The database is in an indeterminate state
            case WAIT_ABANDONED: 
                return FALSE; 
        }
    }
    return TRUE; 
}
```



 

 
