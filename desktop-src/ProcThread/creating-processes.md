---
description: La funzione CreateProcess crea un nuovo processo, che viene eseguito indipendentemente dal processo di creazione. Per semplicità, tuttavia, la relazione viene definita relazione padre-figlio.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Creazione di processi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8e5e4340f5c956e964b74ab134a7618a4c4bf0fa44eee1989a0457741d7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143104"
---
# <a name="creating-processes"></a>Creazione di processi

La [**funzione CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) crea un nuovo processo, che viene eseguito indipendentemente dal processo di creazione. Per semplicità, tuttavia, la relazione viene definita relazione padre-figlio.

Nel codice seguente viene illustrato come creare un processo.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```



Se [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ha esito positivo, restituisce una [**struttura PROCESS \_ INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) contenente handle e identificatori per il nuovo processo e il relativo thread primario. Gli handle di thread e processi vengono creati con diritti di accesso completi, anche se l'accesso può essere limitato se si specificano descrittori di sicurezza. Quando questi handle non sono più necessari, chiuderli usando la [**funzione CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

È anche possibile creare un processo usando [**la funzione CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) [**o CreateProcessWithLogonW.**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) In questo modo è possibile specificare il contesto di sicurezza dell'account utente in cui verrà eseguito il processo.

 

 
