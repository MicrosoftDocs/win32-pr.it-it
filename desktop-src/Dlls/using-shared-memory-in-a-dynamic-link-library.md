---
description: Nell'esempio seguente viene illustrato come la funzione del punto di ingresso della DLL può utilizzare un oggetto di mapping dei file per configurare la memoria che può essere condivisa dai processi che caricano la DLL.
ms.assetid: ab751ab1-3b40-4111-b724-9f8676b722a3
title: Uso della memoria condivisa in una libreria di Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978a6fa77964c6404b3f85e9c9bcec6c3644f2ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880017"
---
# <a name="using-shared-memory-in-a-dynamic-link-library"></a>Uso della memoria condivisa in una libreria di Dynamic-Link

Nell'esempio seguente viene illustrato come la funzione del punto di ingresso della DLL può utilizzare un oggetto di mapping dei file per configurare la memoria che può essere condivisa dai processi che caricano la DLL. La memoria della DLL condivisa viene mantenute solo fino a quando la DLL viene caricata. Le applicazioni possono utilizzare le funzioni SetSharedMem e GetSharedMem per accedere alla memoria condivisa.

## <a name="dll-that-implements-the-shared-memory"></a>DLL che implementa la memoria condivisa

Nell'esempio viene usato il mapping dei file per eseguire il mapping di un blocco di memoria condivisa denominata allo spazio degli indirizzi virtuali di ogni processo che carica la DLL. A tale scopo, la funzione del punto di ingresso deve:

1.  Chiamare la funzione [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) per ottenere un handle per un oggetto mapping di file. Il primo processo che carica la DLL crea l'oggetto mapping di file. I processi successivi aprono un handle per l'oggetto esistente. Per ulteriori informazioni, vedere [creazione di un oggetto File-Mapping](/windows/desktop/Memory/creating-a-file-mapping-object).
2.  Chiamare la funzione [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) per eseguire il mapping di una visualizzazione nello spazio degli indirizzi virtuali. Ciò consente al processo di accedere alla memoria condivisa. Per ulteriori informazioni, vedere [creazione di una visualizzazione file](/windows/desktop/Memory/creating-a-file-view).

Si noti che, sebbene sia possibile specificare attributi di sicurezza predefiniti passando un valore NULL per il parametro *lpAttributes* di [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), è possibile scegliere di usare una struttura di [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) per fornire sicurezza aggiuntiva.


```C++
// The DLL code

#include <windows.h> 
#include <memory.h> 
 
#define SHMEMSIZE 4096 
 
static LPVOID lpvMem = NULL;      // pointer to shared memory
static HANDLE hMapObject = NULL;  // handle to file mapping

// The DLL entry-point function sets up shared memory using a 
// named file-mapping object. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL,  // DLL module handle
    DWORD fdwReason,              // reason called 
    LPVOID lpvReserved)           // reserved 
{ 
    BOOL fInit, fIgnore; 
 
    switch (fdwReason) 
    { 
        // DLL load due to process initialization or LoadLibrary
 
          case DLL_PROCESS_ATTACH: 
 
            // Create a named file mapping object
 
            hMapObject = CreateFileMapping( 
                INVALID_HANDLE_VALUE,   // use paging file
                NULL,                   // default security attributes
                PAGE_READWRITE,         // read/write access
                0,                      // size: high 32-bits
                SHMEMSIZE,              // size: low 32-bits
                TEXT("dllmemfilemap")); // name of map object
            if (hMapObject == NULL) 
                return FALSE; 
 
            // The first process to attach initializes memory
 
            fInit = (GetLastError() != ERROR_ALREADY_EXISTS); 
 
            // Get a pointer to the file-mapped shared memory
 
            lpvMem = MapViewOfFile( 
                hMapObject,     // object to map view of
                FILE_MAP_WRITE, // read/write access
                0,              // high offset:  map from
                0,              // low offset:   beginning
                0);             // default: map entire file
            if (lpvMem == NULL) 
                return FALSE; 
 
            // Initialize memory if this is the first process
 
            if (fInit) 
                memset(lpvMem, '\0', SHMEMSIZE); 
 
            break; 
 
        // The attached process creates a new thread
 
        case DLL_THREAD_ATTACH: 
            break; 
 
        // The thread of the attached process terminates
 
        case DLL_THREAD_DETACH: 
            break; 
 
        // DLL unload due to process termination or FreeLibrary
 
        case DLL_PROCESS_DETACH: 
 
            // Unmap shared memory from the process's address space
 
            fIgnore = UnmapViewOfFile(lpvMem); 
 
            // Close the process's handle to the file-mapping object
 
            fIgnore = CloseHandle(hMapObject); 
 
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
 
// SetSharedMem sets the contents of the shared memory 
 
__declspec(dllexport) VOID __cdecl SetSharedMem(LPWSTR lpszBuf) 
{ 
    LPWSTR lpszTmp; 
    DWORD dwCount=1;
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy the null-terminated string into shared memory
 
    while (*lpszBuf && dwCount<SHMEMSIZE) 
    {
        *lpszTmp++ = *lpszBuf++; 
        dwCount++;
    }
    *lpszTmp = '\0'; 
} 
 
// GetSharedMem gets the contents of the shared memory
 
__declspec(dllexport) VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize) 
{ 
    LPWSTR lpszTmp; 
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy from shared memory into the caller's buffer
 
    while (*lpszTmp && --cchSize) 
        *lpszBuf++ = *lpszTmp++; 
    *lpszBuf = '\0'; 
}
#ifdef __cplusplus
}
#endif
```



È possibile eseguire il mapping della memoria condivisa a un indirizzo diverso in ogni processo. Per questo motivo, ogni processo dispone di una propria istanza di lpvMem, che viene dichiarata come variabile globale in modo che sia disponibile per tutte le funzioni DLL. Nell'esempio si presuppone che i dati globali della DLL non siano condivisi, in modo che ogni processo che carica la DLL disponga di una propria istanza di lpvMem.

Si noti che la memoria condivisa viene rilasciata quando l'ultimo handle per l'oggetto di mapping dei file viene chiuso. Per creare una memoria condivisa persistente, è necessario assicurarsi che un processo abbia sempre un handle aperto per l'oggetto mapping di file.

## <a name="processes-that-use-the-shared-memory"></a>Processi che utilizzano la memoria condivisa

Nei processi seguenti viene utilizzata la memoria condivisa fornita dalla DLL definita in precedenza. Il primo processo chiama SetSharedMem per scrivere una stringa mentre il secondo processo chiama GetSharedMem per recuperare questa stringa.

Questo processo usa la funzione SetSharedMem implementata dalla DLL per scrivere la stringa "This is a test String" nella memoria condivisa. Avvia anche un processo figlio che leggerà la stringa dalla memoria condivisa.


```C++
// Parent process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl SetSharedMem(LPWSTR lpszBuf);

HANDLE CreateChildProcess(LPTSTR szCmdline) 
{ 
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bFuncRetn = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
 
// Create the child process. 
    
   bFuncRetn = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   if (bFuncRetn == 0) 
   {
      printf("CreateProcess failed (%)\n", GetLastError());
      return INVALID_HANDLE_VALUE;
   }
   else 
   {
      CloseHandle(piProcInfo.hThread);
      return piProcInfo.hProcess;
   }
}

int _tmain(int argc, TCHAR *argv[])
{
   HANDLE hProcess;

   if (argc == 1) 
   {
      printf("Please specify an input file");
      ExitProcess(0);
   }

   // Call the DLL function
   printf("\nProcess is writing to shared memory...\n\n");
   SetSharedMem(L"This is a test string");

   // Start the child process that will read the memory
   hProcess = CreateChildProcess(argv[1]);

   // Ensure this process is around until the child process terminates
   if (INVALID_HANDLE_VALUE != hProcess) 
   {
      WaitForSingleObject(hProcess, INFINITE);
      CloseHandle(hProcess);
   }
   return 0;
}

```



Questo processo usa la funzione GetSharedMem implementata dalla DLL per leggere una stringa dalla memoria condivisa. Viene avviato dal processo padre sopra riportato.


```C++
// Child process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize);

int _tmain( void )
{
    WCHAR cBuf[MAX_PATH];

    GetSharedMem(cBuf, MAX_PATH);
 
    printf("Child process read from shared memory: %S\n", cBuf);
    
    return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dati della libreria a collegamento dinamico](dynamic-link-library-data.md)
</dt> </dl>

 

 
