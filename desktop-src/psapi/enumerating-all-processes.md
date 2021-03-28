---
title: Enumerazione di tutti i processi
description: Il codice di esempio seguente usa la funzione EnumProcesses per enumerare i processi correnti nel sistema.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64e127014910974b881a7ae21e807be9ac19452
ms.sourcegitcommit: d581811a577e00821667dad731710909979dc72d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/08/2021
ms.locfileid: "104530415"
---
# <a name="enumerating-all-processes"></a><span data-ttu-id="774dc-103">Enumerazione di tutti i processi</span><span class="sxs-lookup"><span data-stu-id="774dc-103">Enumerating All Processes</span></span>

<span data-ttu-id="774dc-104">Il codice di esempio seguente usa la funzione [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) per recuperare l'identificatore del processo per ogni oggetto processo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="774dc-104">The following sample code uses the [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) function to retrieve the process identifier for each process object in the system.</span></span> <span data-ttu-id="774dc-105">Viene quindi chiamato [EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) per ottenere ogni nome di processo e stamparlo.</span><span class="sxs-lookup"><span data-stu-id="774dc-105">[EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) is then called to get each process name and print it.</span></span>

>[!NOTE]
> <span data-ttu-id="774dc-106">Per processi a 64 bit, usare la funzione [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) .</span><span class="sxs-lookup"><span data-stu-id="774dc-106">For 64 bit proceses, use the [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) function.</span></span>

```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintProcessNameAndID( DWORD processID )
{
    TCHAR szProcessName[MAX_PATH] = TEXT("<unknown>");

    // Get a handle to the process.

    HANDLE hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                                   PROCESS_VM_READ,
                                   FALSE, processID );

    // Get the process name.

    if (NULL != hProcess )
    {
        HMODULE hMod;
        DWORD cbNeeded;

        if ( EnumProcessModules( hProcess, &hMod, sizeof(hMod), 
             &cbNeeded) )
        {
            GetModuleBaseName( hProcess, hMod, szProcessName, 
                               sizeof(szProcessName)/sizeof(TCHAR) );
        }
    }

    // Print the process name and identifier.

    _tprintf( TEXT("%s  (PID: %u)\n"), szProcessName, processID );

    // Release the handle to the process.

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

    // Print the name and process identifier for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        if( aProcesses[i] != 0 )
        {
            PrintProcessNameAndID( aProcesses[i] );
        }
    }

    return 0;
}
```



<span data-ttu-id="774dc-107">La funzione Main ottiene un elenco di processi tramite la funzione [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="774dc-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="774dc-108">Per ogni processo, Main chiama la funzione **PrintProcessNameAndID** , passando l'identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="774dc-108">For each process, main calls the **PrintProcessNameAndID** function, passing it the process identifier.</span></span> <span data-ttu-id="774dc-109">**PrintProcessNameAndID** chiama a sua volta la funzione [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) per ottenere l'handle del processo.</span><span class="sxs-lookup"><span data-stu-id="774dc-109">**PrintProcessNameAndID** in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="774dc-110">Se **OpenProcess** ha esito negativo, l'output Mostra il nome del processo come <unknown> .</span><span class="sxs-lookup"><span data-stu-id="774dc-110">If **OpenProcess** fails, the output shows the process name as <unknown>.</span></span> <span data-ttu-id="774dc-111">Ad esempio, **OpenProcess** non riesce per i processi inattivi e CSRSS perché le relative restrizioni di accesso impediscono l'apertura del codice a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="774dc-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="774dc-112">**PrintProcessNameAndID** chiama quindi la funzione [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) per ottenere gli handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="774dc-112">Next, **PrintProcessNameAndID** calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles.</span></span> <span data-ttu-id="774dc-113">Infine, **PrintProcessNameAndID** chiama la funzione [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) per ottenere il nome del file eseguibile e visualizza il nome insieme all'identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="774dc-113">Finally, **PrintProcessNameAndID** calls the [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) function to obtain the name of the executable file and displays the name along with the process identifier.</span></span>

 

 
