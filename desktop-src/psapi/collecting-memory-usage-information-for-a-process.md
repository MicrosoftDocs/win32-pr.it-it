---
title: Raccolta di informazioni sull'utilizzo della memoria per un processo
description: Per determinare l'efficienza dell'applicazione, può essere utile esaminare l'utilizzo della memoria. Il codice di esempio seguente usa la funzione GetProcessMemoryInfo per ottenere informazioni sull'utilizzo della memoria di un processo.
ms.assetid: 23641bf8-3653-4cb9-8008-cd99137ca268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead17b8308424be8b959c4043eec606b18292708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399199"
---
# <a name="collecting-memory-usage-information-for-a-process"></a>Raccolta di informazioni sull'utilizzo della memoria per un processo

Per determinare l'efficienza dell'applicazione, può essere utile esaminare l'utilizzo della memoria. Il codice di esempio seguente usa la funzione [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) per ottenere informazioni sull'utilizzo della memoria di un processo.


```C++
#include <windows.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintMemoryInfo( DWORD processID )
{
    HANDLE hProcess;
    PROCESS_MEMORY_COUNTERS pmc;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Print information about the memory usage of the process.

    hProcess = OpenProcess(  PROCESS_QUERY_INFORMATION |
                                    PROCESS_VM_READ,
                                    FALSE, processID );
    if (NULL == hProcess)
        return;

    if ( GetProcessMemoryInfo( hProcess, &pmc, sizeof(pmc)) )
    {
        printf( "\tPageFaultCount: 0x%08X\n", pmc.PageFaultCount );
        printf( "\tPeakWorkingSetSize: 0x%08X\n", 
                  pmc.PeakWorkingSetSize );
        printf( "\tWorkingSetSize: 0x%08X\n", pmc.WorkingSetSize );
        printf( "\tQuotaPeakPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPeakPagedPoolUsage );
        printf( "\tQuotaPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPagedPoolUsage );
        printf( "\tQuotaPeakNonPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPeakNonPagedPoolUsage );
        printf( "\tQuotaNonPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaNonPagedPoolUsage );
        printf( "\tPagefileUsage: 0x%08X\n", pmc.PagefileUsage ); 
        printf( "\tPeakPagefileUsage: 0x%08X\n", 
                  pmc.PeakPagefileUsage );
    }

    CloseHandle( hProcess );
}

int main( void )
{
    // Get the list of process identifiers.

    DWORD aProcesses[1024], cbNeeded, cProcesses;
    unsigned int i;

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
    {
        return 1;
    }

    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the memory usage for each process

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintMemoryInfo( aProcesses[i] );
    }

    return 0;
}
```



La funzione Main ottiene un elenco di processi tramite la funzione [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Per ogni processo, Main chiama la funzione PrintMemoryInfo, passando l'identificatore del processo. PrintMemoryInfo chiama a sua volta la funzione [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) per ottenere l'handle del processo. Se **OpenProcess** ha esito negativo, l'output Mostra solo l'identificatore del processo. Ad esempio, **OpenProcess** non riesce per i processi inattivi e CSRSS perché le relative restrizioni di accesso impediscono l'apertura del codice a livello di utente. Infine, PrintMemoryInfo chiama la funzione [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) per ottenere le informazioni sull'utilizzo della memoria.

 

 