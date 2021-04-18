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
# <a name="using-mutex-objects"></a><span data-ttu-id="05e3e-103">Utilizzo di oggetti mutex</span><span class="sxs-lookup"><span data-stu-id="05e3e-103">Using Mutex Objects</span></span>

<span data-ttu-id="05e3e-104">È possibile usare un [oggetto mutex](mutex-objects.md) per proteggere una risorsa condivisa dall'accesso simultaneo da più thread o processi.</span><span class="sxs-lookup"><span data-stu-id="05e3e-104">You can use a [mutex object](mutex-objects.md) to protect a shared resource from simultaneous access by multiple threads or processes.</span></span> <span data-ttu-id="05e3e-105">Ogni thread deve attendere la proprietà del mutex prima di poter eseguire il codice che accede alla risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="05e3e-105">Each thread must wait for ownership of the mutex before it can execute the code that accesses the shared resource.</span></span> <span data-ttu-id="05e3e-106">Se, ad esempio, più thread condividono l'accesso a un database, i thread possono usare un oggetto mutex per consentire a un solo thread alla volta di scrivere nel database.</span><span class="sxs-lookup"><span data-stu-id="05e3e-106">For example, if several threads share access to a database, the threads can use a mutex object to permit only one thread at a time to write to the database.</span></span>

<span data-ttu-id="05e3e-107">Nell'esempio seguente viene usata la funzione [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) per creare un oggetto mutex e la funzione [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) per creare thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="05e3e-107">The following example uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create a mutex object and the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create worker threads.</span></span>

<span data-ttu-id="05e3e-108">Quando un thread di questo processo scrive nel database, richiede prima di tutto la proprietà del mutex usando la funzione [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="05e3e-108">When a thread of this process writes to the database, it first requests ownership of the mutex using the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function.</span></span> <span data-ttu-id="05e3e-109">Se il thread ottiene la proprietà del mutex, scrive nel database e quindi rilascia la relativa proprietà del mutex utilizzando la funzione [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .</span><span class="sxs-lookup"><span data-stu-id="05e3e-109">If the thread obtains ownership of the mutex, it writes to the database and then releases its ownership of the mutex using the [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) function.</span></span>

<span data-ttu-id="05e3e-110">In questo esempio viene utilizzata la gestione strutturata delle eccezioni per garantire che il thread rilasci correttamente l'oggetto mutex.</span><span class="sxs-lookup"><span data-stu-id="05e3e-110">This example uses structured exception handling to ensure that the thread properly releases the mutex object.</span></span> <span data-ttu-id="05e3e-111">Il blocco **\_ \_ finally** del codice viene eseguito indipendentemente dal modo in cui il blocco **\_ \_ try** termina (a meno che il blocco **\_ \_ try** non includa una chiamata alla funzione [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ).</span><span class="sxs-lookup"><span data-stu-id="05e3e-111">The **\_\_finally** block of code is executed no matter how the **\_\_try** block terminates (unless the **\_\_try** block includes a call to the [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) function).</span></span> <span data-ttu-id="05e3e-112">In questo modo si impedisce che l'oggetto mutex venga abbandonato inavvertitamente.</span><span class="sxs-lookup"><span data-stu-id="05e3e-112">This prevents the mutex object from being abandoned inadvertently.</span></span>

<span data-ttu-id="05e3e-113">Se un mutex viene abbandonato, il thread di proprietà del mutex non lo rilascia correttamente prima di terminare.</span><span class="sxs-lookup"><span data-stu-id="05e3e-113">If a mutex is abandoned, the thread that owned the mutex did not properly release it before terminating.</span></span> <span data-ttu-id="05e3e-114">In questo caso, lo stato della risorsa condivisa è indeterminato e la continuazione dell'utilizzo del mutex può nascondere un errore potenzialmente grave.</span><span class="sxs-lookup"><span data-stu-id="05e3e-114">In this case, the status of the shared resource is indeterminate, and continuing to use the mutex can obscure a potentially serious error.</span></span> <span data-ttu-id="05e3e-115">Alcune applicazioni potrebbero tentare di ripristinare lo stato coerente della risorsa; in questo esempio viene semplicemente restituito un errore e viene interrotto l'utilizzo del mutex.</span><span class="sxs-lookup"><span data-stu-id="05e3e-115">Some applications might attempt to restore the resource to a consistent state; this example simply returns an error and stops using the mutex.</span></span> <span data-ttu-id="05e3e-116">Per ulteriori informazioni, vedere [oggetti mutex](mutex-objects.md).</span><span class="sxs-lookup"><span data-stu-id="05e3e-116">For more information, see [Mutex Objects](mutex-objects.md).</span></span>


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



 

 
