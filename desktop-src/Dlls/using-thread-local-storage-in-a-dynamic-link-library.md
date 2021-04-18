---
description: Questa sezione illustra l'uso di una funzione del punto di ingresso della DLL per configurare un indice TLS (thread local storage) per fornire spazio di archiviazione privato per ogni thread di un processo multithread.
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: Uso dell'archiviazione locale di thread in una libreria di Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261ef7482520b4cb6e6c7b630f10ebb456231283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308916"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a><span data-ttu-id="97b7c-103">Uso dell'archiviazione locale di thread in una libreria di Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="97b7c-103">Using Thread Local Storage in a Dynamic-Link Library</span></span>

<span data-ttu-id="97b7c-104">Questa sezione illustra l'uso di una funzione del punto di ingresso della DLL per configurare un indice TLS (thread local storage) per fornire spazio di archiviazione privato per ogni thread di un processo multithread.</span><span class="sxs-lookup"><span data-stu-id="97b7c-104">This section shows the use of a DLL entry-point function to set up a thread local storage (TLS) index to provide private storage for each thread of a multithreaded process.</span></span>

<span data-ttu-id="97b7c-105">L'indice TLS viene archiviato in una variabile globale, rendendolo disponibile a tutte le funzioni DLL.</span><span class="sxs-lookup"><span data-stu-id="97b7c-105">The TLS index is stored in a global variable, making it available to all of the DLL functions.</span></span> <span data-ttu-id="97b7c-106">Questo esempio presuppone che i dati globali della DLL non siano condivisi, perché l'indice TLS non è necessariamente lo stesso per ogni processo che carica la DLL.</span><span class="sxs-lookup"><span data-stu-id="97b7c-106">This example assumes that the DLL's global data is not shared, because the TLS index is not necessarily the same for each process that loads the DLL.</span></span>

<span data-ttu-id="97b7c-107">La funzione del punto di ingresso usa la funzione [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) per allocare un indice TLS ogni volta che un processo carica la dll.</span><span class="sxs-lookup"><span data-stu-id="97b7c-107">The entry-point function uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index whenever a process loads the DLL.</span></span> <span data-ttu-id="97b7c-108">Ogni thread può quindi utilizzare questo indice per archiviare un puntatore al proprio blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="97b7c-108">Each thread can then use this index to store a pointer to its own block of memory.</span></span>

<span data-ttu-id="97b7c-109">Quando la funzione del punto di ingresso viene chiamata con il \_ valore di associazione processo dll \_ , il codice esegue le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="97b7c-109">When the entry-point function is called with the DLL\_PROCESS\_ATTACH value, the code performs the following actions:</span></span>

1.  <span data-ttu-id="97b7c-110">Usa la funzione [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) per allocare un indice TLS.</span><span class="sxs-lookup"><span data-stu-id="97b7c-110">Uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index.</span></span>
2.  <span data-ttu-id="97b7c-111">Alloca un blocco di memoria che deve essere utilizzato esclusivamente dal thread iniziale del processo.</span><span class="sxs-lookup"><span data-stu-id="97b7c-111">Allocates a block of memory to be used exclusively by the initial thread of the process.</span></span>
3.  <span data-ttu-id="97b7c-112">Usa l'indice TLS in una chiamata alla funzione [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) per archiviare l'indirizzo del blocco di memoria nello slot TLS associato all'indice.</span><span class="sxs-lookup"><span data-stu-id="97b7c-112">Uses the TLS index in a call to the [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function to store the address of the memory block in the TLS slot associated with the index.</span></span>

<span data-ttu-id="97b7c-113">Ogni volta che il processo crea un nuovo thread, la funzione del punto di ingresso viene chiamata con il valore di connessione del thread della DLL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="97b7c-113">Each time the process creates a new thread, the entry-point function is called with the DLL\_THREAD\_ATTACH value.</span></span> <span data-ttu-id="97b7c-114">La funzione del punto di ingresso consente quindi di allocare un blocco di memoria per il nuovo thread e di archiviarvi un puntatore usando l'indice TLS.</span><span class="sxs-lookup"><span data-stu-id="97b7c-114">The entry-point function then allocates a block of memory for the new thread and stores a pointer to it by using the TLS index.</span></span>

<span data-ttu-id="97b7c-115">Quando una funzione richiede l'accesso ai dati associati a un indice TLS, specificare l'indice in una chiamata alla funzione [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) .</span><span class="sxs-lookup"><span data-stu-id="97b7c-115">When a function requires access to the data associated with a TLS index, specify the index in a call to the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function.</span></span> <span data-ttu-id="97b7c-116">In questo modo viene recuperato il contenuto dello slot TLS per il thread chiamante, che in questo caso è un puntatore al blocco di memoria per i dati.</span><span class="sxs-lookup"><span data-stu-id="97b7c-116">This retrieves the contents of the TLS slot for the calling thread, which in this case is a pointer to the memory block for the data.</span></span> <span data-ttu-id="97b7c-117">Quando un processo usa il collegamento della fase di caricamento con questa DLL, la funzione del punto di ingresso è sufficiente per gestire l'archiviazione locale del thread.</span><span class="sxs-lookup"><span data-stu-id="97b7c-117">When a process uses load-time linking with this DLL, the entry-point function is sufficient to manage the thread local storage.</span></span> <span data-ttu-id="97b7c-118">I problemi possono verificarsi con un processo che utilizza il collegamento di run-time perché la funzione del punto di ingresso non viene chiamata per i thread esistenti prima della chiamata della funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , quindi la memoria TLS non viene allocata per questi thread.</span><span class="sxs-lookup"><span data-stu-id="97b7c-118">Problems can occur with a process that uses run-time linking because the entry-point function is not called for threads that exist before the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is called, so TLS memory is not allocated for these threads.</span></span> <span data-ttu-id="97b7c-119">Questo esempio risolve questo problema controllando il valore restituito dalla funzione [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) e allocando memoria se il valore indica che lo slot TLS per il thread non è impostato.</span><span class="sxs-lookup"><span data-stu-id="97b7c-119">This example solves this problem by checking the value returned by the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function and allocating memory if the value indicates that the TLS slot for this thread is not set.</span></span>

<span data-ttu-id="97b7c-120">Quando ogni thread non deve più usare un indice TLS, deve liberare la memoria il cui puntatore è archiviato nello slot TLS.</span><span class="sxs-lookup"><span data-stu-id="97b7c-120">When each thread no longer needs to use a TLS index, it must free the memory whose pointer is stored in the TLS slot.</span></span> <span data-ttu-id="97b7c-121">Al termine dell'utilizzo di un indice TLS da parte di tutti i thread, utilizzare la funzione [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) per rilasciare l'indice.</span><span class="sxs-lookup"><span data-stu-id="97b7c-121">When all threads have finished using a TLS index, use the [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) function to release the index.</span></span>

<span data-ttu-id="97b7c-122">Quando un thread termina, la funzione del punto di ingresso viene chiamata con il \_ valore di \_ scollegamento del thread dll e la memoria per quel thread viene liberata.</span><span class="sxs-lookup"><span data-stu-id="97b7c-122">When a thread terminates, the entry-point function is called with the DLL\_THREAD\_DETACH value and the memory for that thread is freed.</span></span> <span data-ttu-id="97b7c-123">Al termine di un processo, la funzione del punto di ingresso viene chiamata con il \_ \_ valore di scollegamento del processo dll e la memoria a cui fa riferimento il puntatore nell'indice TLS viene liberata.</span><span class="sxs-lookup"><span data-stu-id="97b7c-123">When a process terminates, the entry-point function is called with the DLL\_PROCESS\_DETACH value and the memory referenced by the pointer in the TLS index is freed.</span></span>


```C++
// The DLL code

#include <windows.h>

static DWORD dwTlsIndex; // address of shared memory
 
// DllMain() is the entry-point function for this DLL. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL, // DLL module handle
    DWORD fdwReason,                    // reason called
    LPVOID lpvReserved)                 // reserved
{ 
    LPVOID lpvData; 
    BOOL fIgnore; 
 
    switch (fdwReason) 
    { 
        // The DLL is loading due to process 
        // initialization or a call to LoadLibrary. 
 
        case DLL_PROCESS_ATTACH: 
 
            // Allocate a TLS index.
 
            if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
                return FALSE; 
 
            // No break: Initialize the index for first thread.
 
        // The attached process creates a new thread. 
 
        case DLL_THREAD_ATTACH: 
 
            // Initialize the TLS index for this thread.
 
            lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
            if (lpvData != NULL) 
                fIgnore = TlsSetValue(dwTlsIndex, lpvData); 
 
            break; 
 
        // The thread of the attached process terminates.
 
        case DLL_THREAD_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            break; 
 
        // DLL unload due to process termination or FreeLibrary. 
 
        case DLL_PROCESS_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            // Release the TLS index.
 
            TlsFree(dwTlsIndex); 
            break; 
 
        default: 
            break; 
    } 
 
    return TRUE; 
    UNREFERENCED_PARAMETER(hinstDLL); 
    UNREFERENCED_PARAMETER(lpvReserved); 
}

// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.

#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif

__declspec(dllexport)
BOOL WINAPI StoreData(DWORD dw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
   {
      lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
      if (lpvData == NULL) 
         return FALSE;
      if (!TlsSetValue(dwTlsIndex, lpvData))
         return FALSE;
   }

   pData = (DWORD *) lpvData; // Cast to my data type.
   // In this example, it is only a pointer to a DWORD
   // but it can be a structure pointer to contain more complicated data.

   (*pData) = dw;
   return TRUE;
}

__declspec(dllexport)
BOOL WINAPI GetData(DWORD *pdw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
      return FALSE;

   pData = (DWORD *) lpvData;
   (*pdw) = (*pData);
   return TRUE;
}
#ifdef __cplusplus
}
#endif
```



<span data-ttu-id="97b7c-124">Il codice seguente illustra l'uso delle funzioni DLL definite nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="97b7c-124">The following code demonstrates the use of the DLL functions defined in the previous example.</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
#define DLL_NAME TEXT("testdll")

VOID ErrorExit(LPSTR); 

extern "C" BOOL WINAPI StoreData(DWORD dw);
extern "C" BOOL WINAPI GetData(DWORD *pdw);
 
DWORD WINAPI ThreadFunc(VOID) 
{   
   int i;

   if(!StoreData(GetCurrentThreadId()))
      ErrorExit("StoreData error");

   for(i=0; i<THREADCOUNT; i++)
   {
      DWORD dwOut;
      if(!GetData(&dwOut))
         ErrorExit("GetData error");
      if( dwOut != GetCurrentThreadId())
         printf("thread %d: data is incorrect (%d)\n", GetCurrentThreadId(), dwOut);
      else printf("thread %d: data is correct\n", GetCurrentThreadId());
      Sleep(0);
   }
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
   HMODULE hm;
 
// Load the DLL

   hm = LoadLibrary(DLL_NAME);
   if(!hm)
   {
      ErrorExit("DLL failed to load");
   }

// Create multiple threads. 
 
   for (i = 0; i < THREADCOUNT; i++) 
   { 
      hThread[i] = CreateThread(NULL, // default security attributes 
         0,                           // use default stack size 
         (LPTHREAD_START_ROUTINE) ThreadFunc, // thread function 
         NULL,                    // no thread function argument 
         0,                       // use default creation flags 
         &IDThread);              // returns thread identifier 
 
   // Check the return value for success. 
      if (hThread[i] == NULL) 
         ErrorExit("CreateThread error\n"); 
   } 
 
   WaitForMultipleObjects(THREADCOUNT, hThread, TRUE, INFINITE); 

   FreeLibrary(hm);
 
   return 0; 
} 
 
VOID ErrorExit (LPSTR lpszMessage) 
{ 
   fprintf(stderr, "%s\n", lpszMessage); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a><span data-ttu-id="97b7c-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97b7c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b7c-126">Dati della libreria a collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="97b7c-126">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> <dt>

[<span data-ttu-id="97b7c-127">Uso dell'archiviazione locale di thread</span><span class="sxs-lookup"><span data-stu-id="97b7c-127">Using Thread Local Storage</span></span>](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
