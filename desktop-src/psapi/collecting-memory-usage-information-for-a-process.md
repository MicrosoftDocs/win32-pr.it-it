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
# <a name="collecting-memory-usage-information-for-a-process"></a><span data-ttu-id="b9cb9-104">Raccolta di informazioni sull'utilizzo della memoria per un processo</span><span class="sxs-lookup"><span data-stu-id="b9cb9-104">Collecting Memory Usage Information For a Process</span></span>

<span data-ttu-id="b9cb9-105">Per determinare l'efficienza dell'applicazione, può essere utile esaminare l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="b9cb9-105">To determine the efficiency of your application, you may want to examine its memory usage.</span></span> <span data-ttu-id="b9cb9-106">Il codice di esempio seguente usa la funzione [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) per ottenere informazioni sull'utilizzo della memoria di un processo.</span><span class="sxs-lookup"><span data-stu-id="b9cb9-106">The following sample code uses the [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function to obtain information about the memory usage of a process.</span></span>


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



<span data-ttu-id="b9cb9-107">La funzione Main ottiene un elenco di processi tramite la funzione [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="b9cb9-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="b9cb9-108">Per ogni processo, Main chiama la funzione PrintMemoryInfo, passando l'identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="b9cb9-108">For each process, main calls the PrintMemoryInfo function, passing the process identifier.</span></span> <span data-ttu-id="b9cb9-109">PrintMemoryInfo chiama a sua volta la funzione [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) per ottenere l'handle del processo.</span><span class="sxs-lookup"><span data-stu-id="b9cb9-109">PrintMemoryInfo in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="b9cb9-110">Se **OpenProcess** ha esito negativo, l'output Mostra solo l'identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="b9cb9-110">If **OpenProcess** fails, the output shows only the process identifier.</span></span> <span data-ttu-id="b9cb9-111">Ad esempio, **OpenProcess** non riesce per i processi inattivi e CSRSS perché le relative restrizioni di accesso impediscono l'apertura del codice a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="b9cb9-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="b9cb9-112">Infine, PrintMemoryInfo chiama la funzione [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) per ottenere le informazioni sull'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="b9cb9-112">Finally, PrintMemoryInfo calls the [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function to obtain the memory usage information.</span></span>

 

 