---
description: È possibile usare un oggetto mutex per proteggere una risorsa condivisa dall'accesso simultaneo da più thread o processi.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Uso di oggetti Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c629d90e1cd811c62f62e1151cee4c3e2af77b84133e142fcfe7f93a35b2e5bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739261"
---
# <a name="using-mutex-objects"></a>Uso di oggetti Mutex

È possibile usare un [oggetto mutex per](mutex-objects.md) proteggere una risorsa condivisa dall'accesso simultaneo da più thread o processi. Ogni thread deve attendere la proprietà del mutex prima di poter eseguire il codice che accede alla risorsa condivisa. Ad esempio, se più thread condividono l'accesso a un database, i thread possono usare un oggetto mutex per consentire la scrittura nel database di un solo thread alla volta.

Nell'esempio seguente viene utilizzata [**la funzione CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) per creare un oggetto mutex e la [**funzione CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) per creare thread di lavoro.

Quando un thread di questo processo scrive nel database, richiede prima la proprietà del mutex usando la [**funzione WaitForSingleObject.**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) Se il thread ottiene la proprietà del mutex, scrive nel database e quindi rilascia la proprietà del mutex usando la [**funzione ReleaseMutex.**](/windows/win32/api/synchapi/nf-synchapi-releasemutex)

In questo esempio viene utilizzata la gestione delle eccezioni strutturata per garantire che il thread rilasci correttamente l'oggetto mutex. Il **\_ \_ blocco di** codice finally viene eseguito indipendentemente dal modo in cui termina il blocco **\_ \_ try** (a meno che il blocco **\_ \_ try** non includa una chiamata alla funzione [**TerminateThread).**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) In questo modo si impedisce che l'oggetto mutex venga abbandonato inavvertitamente.

Se un mutex viene abbandonato, il thread proprietario del mutex non lo ha rilasciato correttamente prima della chiusura. In questo caso, lo stato della risorsa condivisa è indeterminato e continuare a usare il mutex può nascondere un errore potenzialmente grave. Alcune applicazioni potrebbero tentare di ripristinare lo stato coerente della risorsa. Questo esempio restituisce semplicemente un errore e interrompe l'uso del mutex. Per altre informazioni, vedere [Oggetti Mutex](mutex-objects.md).


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



 

 
