---
title: Enumerazione di tutti i processi
description: Nell'esempio di codice seguente viene utilizzata la funzione EnumProcesses per enumerare i processi correnti nel sistema.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89798ed3d2d7e44f014d95833302edb5d5be078daf557eed32d3496c863539e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681008"
---
# <a name="enumerating-all-processes"></a>Enumerazione di tutti i processi

Nell'esempio di codice seguente viene [**utilizzata la funzione EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) per recuperare l'identificatore del processo per ogni oggetto processo nel sistema. [EnumProcessModules viene](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) quindi chiamato per ottenere il nome di ogni processo e stamparlo.

>[!NOTE]
> Per i processi a 64 bit, usare la [funzione EnumProcessModulesEx.](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex)

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



La funzione main ottiene un elenco di processi usando la [**funzione EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) Per ogni processo, main chiama la **funzione PrintProcessNameAndID,** passando l'identificatore del processo. **PrintProcessNameAndID** chiama a sua volta la [**funzione OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) per ottenere l'handle del processo. Se **OpenProcess ha** esito negativo, l'output mostra il nome del processo come <unknown> . Ad esempio, **OpenProcess ha** esito negativo per i processi Inattivi e CSRSS perché le restrizioni di accesso impediscono al codice a livello di utente di aprirli. **PrintProcessNameAndID** chiama quindi la [**funzione EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) per ottenere gli handle del modulo. Infine, **PrintProcessNameAndID** chiama la [**funzione GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) per ottenere il nome del file eseguibile e visualizza il nome insieme all'identificatore del processo.

 

 
