---
title: Enumerazione di tutti i moduli per un processo
description: Per determinare i processi che hanno caricato una determinata DLL, è necessario enumerare i moduli per ogni processo. Il codice di esempio seguente usa la funzione EnumProcessModules per enumerare i moduli dei processi correnti nel sistema.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf09d02d4ae9dc7e55177653e05e3d19df4ab7b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337502"
---
# <a name="enumerating-all-modules-for-a-process"></a><span data-ttu-id="1813a-104">Enumerazione di tutti i moduli per un processo</span><span class="sxs-lookup"><span data-stu-id="1813a-104">Enumerating All Modules For a Process</span></span>

<span data-ttu-id="1813a-105">Per determinare i processi che hanno caricato una determinata DLL, è necessario enumerare i moduli per ogni processo.</span><span class="sxs-lookup"><span data-stu-id="1813a-105">To determine which processes have loaded a particular DLL, you must enumerate the modules for each process.</span></span> <span data-ttu-id="1813a-106">Il codice di esempio seguente usa la funzione [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) per enumerare i moduli dei processi correnti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1813a-106">The following sample code uses the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to enumerate the modules of current processes in the system.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

int PrintModules( DWORD processID )
{
    HMODULE hMods[1024];
    HANDLE hProcess;
    DWORD cbNeeded;
    unsigned int i;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Get a handle to the process.

    hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                            PROCESS_VM_READ,
                            FALSE, processID );
    if (NULL == hProcess)
        return 1;

   // Get a list of all the modules in this process.

    if( EnumProcessModules(hProcess, hMods, sizeof(hMods), &cbNeeded))
    {
        for ( i = 0; i < (cbNeeded / sizeof(HMODULE)); i++ )
        {
            TCHAR szModName[MAX_PATH];

            // Get the full path to the module's file.

            if ( GetModuleFileNameEx( hProcess, hMods[i], szModName,
                                      sizeof(szModName) / sizeof(TCHAR)))
            {
                // Print the module name and handle value.

                _tprintf( TEXT("\t%s (0x%08X)\n"), szModName, hMods[i] );
            }
        }
    }
    
    // Release the handle to the process.

    CloseHandle( hProcess );

    return 0;
}

int main( void )
{

    DWORD aProcesses[1024]; 
    DWORD cbNeeded; 
    DWORD cProcesses;
    unsigned int i;

    // Get the list of process identifiers.

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
        return 1;

    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the names of the modules for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintModules( aProcesses[i] );
    }

    return 0;
}
```



<span data-ttu-id="1813a-107">La funzione Main ottiene un elenco di processi tramite la funzione [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="1813a-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="1813a-108">Per ogni processo, la funzione Main chiama la funzione PrintModules, passando l'identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="1813a-108">For each process, the main function calls the PrintModules function, passing it the process identifier.</span></span> <span data-ttu-id="1813a-109">PrintModules chiama a sua volta la funzione [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) per ottenere l'handle del processo.</span><span class="sxs-lookup"><span data-stu-id="1813a-109">PrintModules in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="1813a-110">Se **OpenProcess** ha esito negativo, l'output Mostra solo l'identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="1813a-110">If **OpenProcess** fails, the output shows only the process identifier.</span></span> <span data-ttu-id="1813a-111">Ad esempio, **OpenProcess** non riesce per i processi inattivi e CSRSS perché le relative restrizioni di accesso impediscono l'apertura del codice a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="1813a-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="1813a-112">PrintModules chiama quindi la funzione [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) per ottenere la funzione di gestione dei moduli.</span><span class="sxs-lookup"><span data-stu-id="1813a-112">Next, PrintModules calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles function.</span></span> <span data-ttu-id="1813a-113">Infine, PrintModules chiama la funzione [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) , una volta per ogni modulo, per ottenere i nomi dei moduli.</span><span class="sxs-lookup"><span data-stu-id="1813a-113">Finally, PrintModules calls the [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) function, once for each module, to obtain the module names.</span></span>

 

 