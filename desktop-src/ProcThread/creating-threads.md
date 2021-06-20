---
description: Vedere come usare la funzione CreateThread per creare un nuovo thread per un processo. Esaminare un esempio di codice che ne illustra l'utilizzo.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Creazione di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: befd6c00cadb6758d076ad6c4d0fe940cf855f89
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406734"
---
# <a name="creating-threads"></a><span data-ttu-id="0907b-104">Creazione di thread</span><span class="sxs-lookup"><span data-stu-id="0907b-104">Creating Threads</span></span>

<span data-ttu-id="0907b-105">La [**funzione CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuovo thread per un processo.</span><span class="sxs-lookup"><span data-stu-id="0907b-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="0907b-106">Il thread di creazione deve specificare l'indirizzo iniziale del codice che deve essere eseguito dal nuovo thread.</span><span class="sxs-lookup"><span data-stu-id="0907b-106">The creating thread must specify the starting address of the code that the new thread is to execute.</span></span> <span data-ttu-id="0907b-107">In genere, l'indirizzo iniziale è il nome di una funzione definita nel codice del programma (per altre informazioni, vedere [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="0907b-107">Typically, the starting address is the name of a function defined in the program code (for more information, see [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span></span> <span data-ttu-id="0907b-108">Questa funzione accetta un singolo parametro e restituisce un **valore DWORD.**</span><span class="sxs-lookup"><span data-stu-id="0907b-108">This function takes a single parameter and returns a **DWORD** value.</span></span> <span data-ttu-id="0907b-109">Un processo può avere più thread che eseguono contemporaneamente la stessa funzione.</span><span class="sxs-lookup"><span data-stu-id="0907b-109">A process can have multiple threads simultaneously executing the same function.</span></span>

<span data-ttu-id="0907b-110">Di seguito è riportato un semplice esempio che illustra come creare un nuovo thread che esegue la funzione definita in locale, `MyThreadFunction` .</span><span class="sxs-lookup"><span data-stu-id="0907b-110">The following is a simple example that demonstrates how to create a new thread that executes the locally defined function, `MyThreadFunction`.</span></span>

<span data-ttu-id="0907b-111">Il thread chiamante usa la [**funzione WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) per rendere persistenti fino a quando tutti i thread di lavoro non sono terminati.</span><span class="sxs-lookup"><span data-stu-id="0907b-111">The calling thread uses the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to persist until all worker threads have terminated.</span></span> <span data-ttu-id="0907b-112">Il thread chiamante si blocca mentre è in attesa; per continuare l'elaborazione, un thread chiamante usa [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) e attende che ogni thread di lavoro segnali il relativo oggetto di attesa.</span><span class="sxs-lookup"><span data-stu-id="0907b-112">The calling thread blocks while it is waiting; to continue processing, a calling thread would use [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) and wait for each worker thread to signal its wait object.</span></span> <span data-ttu-id="0907b-113">Si noti che se si chiude l'handle a un thread di lavoro prima che venga terminato, il thread di lavoro non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="0907b-113">Note that if you were to close the handle to a worker thread before it terminated, this does not terminate the worker thread.</span></span> <span data-ttu-id="0907b-114">Tuttavia, l'handle non sarà disponibile per l'uso nelle chiamate di funzione successive.</span><span class="sxs-lookup"><span data-stu-id="0907b-114">However, the handle will be unavailable for use in subsequent function calls.</span></span>


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



<span data-ttu-id="0907b-115">La funzione evita l'uso della libreria di runtime C (CRT), poiché molte delle relative funzioni non sono thread-safe, in particolare se non si usa `MyThreadFunction` CRT multithreading.</span><span class="sxs-lookup"><span data-stu-id="0907b-115">The `MyThreadFunction` function avoids the use of the C run-time library (CRT), as many of its functions are not thread-safe, particularly if you are not using the multithreaded CRT.</span></span> <span data-ttu-id="0907b-116">Se si vuole usare CRT in una funzione, usare `ThreadProc` invece la funzione **\_ beginthreadex.**</span><span class="sxs-lookup"><span data-stu-id="0907b-116">If you would like to use the CRT in a `ThreadProc` function, use the **\_beginthreadex** function instead.</span></span>

<span data-ttu-id="0907b-117">È rischioso passare l'indirizzo di una variabile locale se il thread di creazione termina prima del nuovo thread, perché il puntatore diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="0907b-117">It is risky to pass the address of a local variable if the creating thread exits before the new thread, because the pointer becomes invalid.</span></span> <span data-ttu-id="0907b-118">Passare invece un puntatore alla memoria allocata dinamicamente o rendere il thread di creazione in attesa che il nuovo thread venga terminato.</span><span class="sxs-lookup"><span data-stu-id="0907b-118">Instead, either pass a pointer to dynamically allocated memory or make the creating thread wait for the new thread to terminate.</span></span> <span data-ttu-id="0907b-119">I dati possono anche essere passati dal thread di creazione al nuovo thread usando variabili globali.</span><span class="sxs-lookup"><span data-stu-id="0907b-119">Data can also be passed from the creating thread to the new thread using global variables.</span></span> <span data-ttu-id="0907b-120">Con le variabili globali, è in genere necessario sincronizzare l'accesso da parte di più thread.</span><span class="sxs-lookup"><span data-stu-id="0907b-120">With global variables, it is usually necessary to synchronize access by multiple threads.</span></span> <span data-ttu-id="0907b-121">Per altre informazioni sulla sincronizzazione, vedere [Sincronizzazione dell'esecuzione di più thread.](synchronizing-execution-of-multiple-threads.md)</span><span class="sxs-lookup"><span data-stu-id="0907b-121">For more information about synchronization, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

<span data-ttu-id="0907b-122">Il thread di creazione può usare gli argomenti di [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) per specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="0907b-122">The creating thread can use the arguments to [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to specify the following:</span></span>

-   <span data-ttu-id="0907b-123">Attributi di sicurezza per l'handle per il nuovo thread.</span><span class="sxs-lookup"><span data-stu-id="0907b-123">The security attributes for the handle to the new thread.</span></span> <span data-ttu-id="0907b-124">Questi attributi di sicurezza includono un flag di ereditarietà che determina se l'handle può essere ereditato dai processi figlio.</span><span class="sxs-lookup"><span data-stu-id="0907b-124">These security attributes include an inheritance flag that determines whether the handle can be inherited by child processes.</span></span> <span data-ttu-id="0907b-125">Gli attributi di sicurezza includono anche un descrittore di sicurezza, che il sistema usa per eseguire controlli di accesso su tutti gli utilizzi successivi dell'handle del thread prima che venga concesso l'accesso.</span><span class="sxs-lookup"><span data-stu-id="0907b-125">The security attributes also include a security descriptor, which the system uses to perform access checks on all subsequent uses of the thread's handle before access is granted.</span></span>
-   <span data-ttu-id="0907b-126">Dimensione iniziale dello stack del nuovo thread.</span><span class="sxs-lookup"><span data-stu-id="0907b-126">The initial stack size of the new thread.</span></span> <span data-ttu-id="0907b-127">Lo stack del thread viene allocato automaticamente nello spazio di memoria del processo. il sistema aumenta lo stack in base alle esigenze e lo libera quando il thread termina.</span><span class="sxs-lookup"><span data-stu-id="0907b-127">The thread's stack is allocated automatically in the memory space of the process; the system increases the stack as needed and frees it when the thread terminates.</span></span> <span data-ttu-id="0907b-128">Per altre informazioni, vedere [Dimensioni dello stack di thread](thread-stack-size.md).</span><span class="sxs-lookup"><span data-stu-id="0907b-128">For more information, see [Thread Stack Size](thread-stack-size.md).</span></span>
-   <span data-ttu-id="0907b-129">Flag di creazione che consente di creare il thread in uno stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="0907b-129">A creation flag that enables you to create the thread in a suspended state.</span></span> <span data-ttu-id="0907b-130">Quando viene sospeso, il thread non viene eseguito fino a quando non viene chiamata la funzione [**ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)</span><span class="sxs-lookup"><span data-stu-id="0907b-130">When suspended, the thread does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) function is called.</span></span>

<span data-ttu-id="0907b-131">È anche possibile creare un thread chiamando la [**funzione CreateRemoteThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)</span><span class="sxs-lookup"><span data-stu-id="0907b-131">You can also create a thread by calling the [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) function.</span></span> <span data-ttu-id="0907b-132">Questa funzione viene usata dai processi del debugger per creare un thread che viene eseguito nello spazio degli indirizzi del processo di cui viene eseguito il debug.</span><span class="sxs-lookup"><span data-stu-id="0907b-132">This function is used by debugger processes to create a thread that runs in the address space of the process being debugged.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0907b-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0907b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0907b-134">Terminazione di un thread</span><span class="sxs-lookup"><span data-stu-id="0907b-134">Terminating a Thread</span></span>](terminating-a-thread.md)
</dt> </dl>

 

 
