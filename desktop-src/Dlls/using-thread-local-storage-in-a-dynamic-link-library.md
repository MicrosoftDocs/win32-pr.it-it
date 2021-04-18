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
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a>Uso dell'archiviazione locale di thread in una libreria di Dynamic-Link

Questa sezione illustra l'uso di una funzione del punto di ingresso della DLL per configurare un indice TLS (thread local storage) per fornire spazio di archiviazione privato per ogni thread di un processo multithread.

L'indice TLS viene archiviato in una variabile globale, rendendolo disponibile a tutte le funzioni DLL. Questo esempio presuppone che i dati globali della DLL non siano condivisi, perché l'indice TLS non è necessariamente lo stesso per ogni processo che carica la DLL.

La funzione del punto di ingresso usa la funzione [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) per allocare un indice TLS ogni volta che un processo carica la dll. Ogni thread può quindi utilizzare questo indice per archiviare un puntatore al proprio blocco di memoria.

Quando la funzione del punto di ingresso viene chiamata con il \_ valore di associazione processo dll \_ , il codice esegue le azioni seguenti:

1.  Usa la funzione [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) per allocare un indice TLS.
2.  Alloca un blocco di memoria che deve essere utilizzato esclusivamente dal thread iniziale del processo.
3.  Usa l'indice TLS in una chiamata alla funzione [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) per archiviare l'indirizzo del blocco di memoria nello slot TLS associato all'indice.

Ogni volta che il processo crea un nuovo thread, la funzione del punto di ingresso viene chiamata con il valore di connessione del thread della DLL \_ \_ . La funzione del punto di ingresso consente quindi di allocare un blocco di memoria per il nuovo thread e di archiviarvi un puntatore usando l'indice TLS.

Quando una funzione richiede l'accesso ai dati associati a un indice TLS, specificare l'indice in una chiamata alla funzione [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) . In questo modo viene recuperato il contenuto dello slot TLS per il thread chiamante, che in questo caso è un puntatore al blocco di memoria per i dati. Quando un processo usa il collegamento della fase di caricamento con questa DLL, la funzione del punto di ingresso è sufficiente per gestire l'archiviazione locale del thread. I problemi possono verificarsi con un processo che utilizza il collegamento di run-time perché la funzione del punto di ingresso non viene chiamata per i thread esistenti prima della chiamata della funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , quindi la memoria TLS non viene allocata per questi thread. Questo esempio risolve questo problema controllando il valore restituito dalla funzione [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) e allocando memoria se il valore indica che lo slot TLS per il thread non è impostato.

Quando ogni thread non deve più usare un indice TLS, deve liberare la memoria il cui puntatore è archiviato nello slot TLS. Al termine dell'utilizzo di un indice TLS da parte di tutti i thread, utilizzare la funzione [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) per rilasciare l'indice.

Quando un thread termina, la funzione del punto di ingresso viene chiamata con il \_ valore di \_ scollegamento del thread dll e la memoria per quel thread viene liberata. Al termine di un processo, la funzione del punto di ingresso viene chiamata con il \_ \_ valore di scollegamento del processo dll e la memoria a cui fa riferimento il puntatore nell'indice TLS viene liberata.


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



Il codice seguente illustra l'uso delle funzioni DLL definite nell'esempio precedente.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dati della libreria a collegamento dinamico](dynamic-link-library-data.md)
</dt> <dt>

[Uso dell'archiviazione locale di thread](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
