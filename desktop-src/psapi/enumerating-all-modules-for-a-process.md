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
# <a name="enumerating-all-modules-for-a-process"></a>Enumerazione di tutti i moduli per un processo

Per determinare i processi che hanno caricato una determinata DLL, è necessario enumerare i moduli per ogni processo. Il codice di esempio seguente usa la funzione [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) per enumerare i moduli dei processi correnti nel sistema.


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



La funzione Main ottiene un elenco di processi tramite la funzione [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Per ogni processo, la funzione Main chiama la funzione PrintModules, passando l'identificatore di processo. PrintModules chiama a sua volta la funzione [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) per ottenere l'handle del processo. Se **OpenProcess** ha esito negativo, l'output Mostra solo l'identificatore del processo. Ad esempio, **OpenProcess** non riesce per i processi inattivi e CSRSS perché le relative restrizioni di accesso impediscono l'apertura del codice a livello di utente. PrintModules chiama quindi la funzione [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) per ottenere la funzione di gestione dei moduli. Infine, PrintModules chiama la funzione [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) , una volta per ogni modulo, per ottenere i nomi dei moduli.

 

 