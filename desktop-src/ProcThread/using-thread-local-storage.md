---
description: L'archiviazione thread-local (TLS) consente a più thread dello stesso processo di usare un indice allocato dalla funzione TlsAlloc per archiviare e recuperare un valore locale per il thread.
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: Uso di thread locali Archiviazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdac1306a4a2da10e6a24ba2e1b2444f6215fdac39be7b41cc6850c1e5a683d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127991"
---
# <a name="using-thread-local-storage"></a>Uso di thread locali Archiviazione

[L'archiviazione](thread-local-storage.md) thread-local (TLS) consente a più thread dello stesso processo di usare un indice allocato dalla funzione [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) per archiviare e recuperare un valore locale per il thread. In questo esempio viene allocato un indice all'avvio del processo. All'avvio di ogni thread, alloca un blocco di memoria dinamica e archivia un puntatore a questa memoria nello slot TLS usando la [**funzione TlsSetValue.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) La funzione CommonFunc usa la [**funzione TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) per accedere ai dati associati all'indice locale del thread chiamante. Prima che ogni thread termini, rilascia la memoria dinamica. Prima che il processo termini, chiama [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) per rilasciare l'indice.


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
DWORD dwTlsIndex; 
 
VOID ErrorExit (LPCSTR message);
 
VOID CommonFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Retrieve a data pointer for the current thread. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if ((lpvData == 0) && (GetLastError() != ERROR_SUCCESS)) 
      ErrorExit("TlsGetValue error"); 
 
// Use the data stored for the current thread. 
 
   printf("common: thread %d: lpvData=%lx\n", 
      GetCurrentThreadId(), lpvData); 
 
   Sleep(5000); 
} 
 
DWORD WINAPI ThreadFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Initialize the TLS index for this thread. 
 
   lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
   if (! TlsSetValue(dwTlsIndex, lpvData)) 
      ErrorExit("TlsSetValue error"); 
 
   printf("thread %d: lpvData=%lx\n", GetCurrentThreadId(), lpvData); 
 
   CommonFunc(); 
 
// Release the dynamic memory before the thread returns. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData != 0) 
      LocalFree((HLOCAL) lpvData); 
 
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
 
// Allocate a TLS index. 
 
   if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
      ErrorExit("TlsAlloc failed"); 
 
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
 
   for (i = 0; i < THREADCOUNT; i++) 
      WaitForSingleObject(hThread[i], INFINITE); 
 
   TlsFree(dwTlsIndex);

   return 0; 
} 
 
VOID ErrorExit (LPCSTR message)
{ 
   fprintf(stderr, "%s\n", message); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di thread locali Archiviazione in una libreria Dynamic-Link locale](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
