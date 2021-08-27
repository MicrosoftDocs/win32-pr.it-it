---
description: Vedere come usare la funzione CreateThread per creare un nuovo thread per un processo. Esaminare un esempio di codice che ne illustra l'utilizzo.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Creazione di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dee74cb81c886fe05d07a0970f7d8946d123d92810e6f22dd094e1d8d00466a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081431"
---
# <a name="creating-threads"></a>Creazione di thread

La [**funzione CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuovo thread per un processo. Il thread di creazione deve specificare l'indirizzo iniziale del codice che il nuovo thread deve eseguire. In genere, l'indirizzo iniziale è il nome di una funzione definita nel codice programma . Per altre informazioni, vedere [*ThreadProc.*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) Questa funzione accetta un singolo parametro e restituisce un **valore DWORD.** Un processo può avere più thread che eseguono contemporaneamente la stessa funzione.

Di seguito è riportato un semplice esempio che illustra come creare un nuovo thread che esegue la funzione definita in locale, `MyThreadFunction` .

Il thread chiamante usa la [**funzione WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) per mantenere la persistenza fino al termine di tutti i thread di lavoro. Il thread chiamante si blocca mentre è in attesa; per continuare l'elaborazione, un thread chiamante userà [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) e attenderà che ogni thread di lavoro segnali il relativo oggetto di attesa. Si noti che se si chiude l'handle a un thread di lavoro prima che venga terminato, il thread di lavoro non viene terminato. Tuttavia, l'handle non sarà disponibile per l'uso nelle chiamate di funzione successive.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

#define MAX_THREADS 3
#define BUF_SIZE 255

DWORD WINAPI MyThreadFunction( LPVOID lpParam );
void ErrorHandler(LPTSTR lpszFunction);

// Sample custom data structure for threads to use.
// This is passed by void pointer so it can be any data type
// that can be passed using a single void pointer (LPVOID).
typedef struct MyData {
    int val1;
    int val2;
} MYDATA, *PMYDATA;


int _tmain()
{
    PMYDATA pDataArray[MAX_THREADS];
    DWORD   dwThreadIdArray[MAX_THREADS];
    HANDLE  hThreadArray[MAX_THREADS]; 

    // Create MAX_THREADS worker threads.

    for( int i=0; i<MAX_THREADS; i++ )
    {
        // Allocate memory for thread data.

        pDataArray[i] = (PMYDATA) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY,
                sizeof(MYDATA));

        if( pDataArray[i] == NULL )
        {
           // If the array allocation fails, the system is out of memory
           // so there is no point in trying to print an error message.
           // Just terminate execution.
            ExitProcess(2);
        }

        // Generate unique data for each thread to work with.

        pDataArray[i]->val1 = i;
        pDataArray[i]->val2 = i+100;

        // Create the thread to begin execution on its own.

        hThreadArray[i] = CreateThread( 
            NULL,                   // default security attributes
            0,                      // use default stack size  
            MyThreadFunction,       // thread function name
            pDataArray[i],          // argument to thread function 
            0,                      // use default creation flags 
            &dwThreadIdArray[i]);   // returns the thread identifier 


        // Check the return value for success.
        // If CreateThread fails, terminate execution. 
        // This will automatically clean up threads and memory. 

        if (hThreadArray[i] == NULL) 
        {
           ErrorHandler(TEXT("CreateThread"));
           ExitProcess(3);
        }
    } // End of main thread creation loop.

    // Wait until all threads have terminated.

    WaitForMultipleObjects(MAX_THREADS, hThreadArray, TRUE, INFINITE);

    // Close all thread handles and free memory allocations.

    for(int i=0; i<MAX_THREADS; i++)
    {
        CloseHandle(hThreadArray[i]);
        if(pDataArray[i] != NULL)
        {
            HeapFree(GetProcessHeap(), 0, pDataArray[i]);
            pDataArray[i] = NULL;    // Ensure address is not reused.
        }
    }

    return 0;
}


DWORD WINAPI MyThreadFunction( LPVOID lpParam ) 
{ 
    HANDLE hStdout;
    PMYDATA pDataArray;

    TCHAR msgBuf[BUF_SIZE];
    size_t cchStringSize;
    DWORD dwChars;

    // Make sure there is a console to receive output results. 

    hStdout = GetStdHandle(STD_OUTPUT_HANDLE);
    if( hStdout == INVALID_HANDLE_VALUE )
        return 1;

    // Cast the parameter to the correct data type.
    // The pointer is known to be valid because 
    // it was checked for NULL before the thread was created.
 
    pDataArray = (PMYDATA)lpParam;

    // Print the parameter values using thread-safe functions.

    StringCchPrintf(msgBuf, BUF_SIZE, TEXT("Parameters = %d, %d\n"), 
        pDataArray->val1, pDataArray->val2); 
    StringCchLength(msgBuf, BUF_SIZE, &cchStringSize);
    WriteConsole(hStdout, msgBuf, (DWORD)cchStringSize, &dwChars, NULL);

    return 0; 
} 



void ErrorHandler(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code.

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message.

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR) lpMsgBuf) + lstrlen((LPCTSTR) lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR) lpDisplayBuf, TEXT("Error"), MB_OK); 

    // Free error-handling buffer allocations.

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}
```



La funzione evita l'uso della libreria di runtime C (CRT), poiché molte delle relative funzioni non sono thread-safe, in particolare se non si usa la libreria `MyThreadFunction` CRT multithreading. Se si vuole usare CRT in una funzione, usare `ThreadProc` invece **\_ la funzione beginthreadex.**

È rischioso passare l'indirizzo di una variabile locale se il thread di creazione termina prima del nuovo thread, perché il puntatore diventa non valido. In alternativa, passare un puntatore alla memoria allocata dinamicamente o fare in modo che il thread di creazione attenda il completamento del nuovo thread. I dati possono anche essere passati dal thread di creazione al nuovo thread usando variabili globali. Con le variabili globali, è in genere necessario sincronizzare l'accesso da parte di più thread. Per altre informazioni sulla sincronizzazione, vedere [Sincronizzazione dell'esecuzione di più thread.](synchronizing-execution-of-multiple-threads.md)

Il thread di creazione può usare gli argomenti di [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) per specificare quanto segue:

-   Attributi di sicurezza per l'handle per il nuovo thread. Questi attributi di sicurezza includono un flag di ereditarietà che determina se l'handle può essere ereditato dai processi figlio. Gli attributi di sicurezza includono anche un descrittore di sicurezza, che il sistema usa per eseguire controlli di accesso su tutti gli utilizzi successivi dell'handle del thread prima che venga concesso l'accesso.
-   Dimensione iniziale dello stack del nuovo thread. Lo stack del thread viene allocato automaticamente nello spazio di memoria del processo. il sistema aumenta lo stack in base alle esigenze e lo libera al termine del thread. Per altre informazioni, vedere [Dimensioni dello stack di thread.](thread-stack-size.md)
-   Flag di creazione che consente di creare il thread in uno stato sospeso. Quando viene sospeso, il thread non viene eseguito fino a quando non viene chiamata la funzione [**ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)

È anche possibile creare un thread chiamando la [**funzione CreateRemoteThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) Questa funzione viene usata dai processi del debugger per creare un thread che viene eseguito nello spazio degli indirizzi del processo di cui è in corso il debug.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Terminazione di un thread](terminating-a-thread.md)
</dt> </dl>

 

 
