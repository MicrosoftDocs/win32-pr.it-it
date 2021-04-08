---
description: La funzione CreateProcess crea un nuovo processo, che viene eseguito indipendentemente dal processo di creazione. Per semplicità, tuttavia, la relazione viene definita relazione padre-figlio.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Creazione di processi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75606a3006bf63359b3e52cf2172b8bc2d77ed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967482"
---
# <a name="creating-processes"></a><span data-ttu-id="ff69b-104">Creazione di processi</span><span class="sxs-lookup"><span data-stu-id="ff69b-104">Creating Processes</span></span>

<span data-ttu-id="ff69b-105">La funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) crea un nuovo processo, che viene eseguito indipendentemente dal processo di creazione.</span><span class="sxs-lookup"><span data-stu-id="ff69b-105">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function creates a new process, which runs independently of the creating process.</span></span> <span data-ttu-id="ff69b-106">Per semplicità, tuttavia, la relazione viene definita relazione padre-figlio.</span><span class="sxs-lookup"><span data-stu-id="ff69b-106">However, for simplicity, the relationship is referred to as a parent-child relationship.</span></span>

<span data-ttu-id="ff69b-107">Nel codice seguente viene illustrato come creare un processo.</span><span class="sxs-lookup"><span data-stu-id="ff69b-107">The following code demonstrates how to create a process.</span></span>


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



<span data-ttu-id="ff69b-108">Se [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ha esito positivo, restituisce una struttura di [**\_ informazioni sul processo**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) contenente handle e identificatori per il nuovo processo e il relativo thread primario.</span><span class="sxs-lookup"><span data-stu-id="ff69b-108">If [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) succeeds, it returns a [**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) structure containing handles and identifiers for the new process and its primary thread.</span></span> <span data-ttu-id="ff69b-109">Gli handle di thread e di processo vengono creati con diritti di accesso completi, sebbene l'accesso possa essere limitato se si specificano descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ff69b-109">The thread and process handles are created with full access rights, although access can be restricted if you specify security descriptors.</span></span> <span data-ttu-id="ff69b-110">Quando questi handle non sono più necessari, chiuderli usando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="ff69b-110">When you no longer need these handles, close them by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="ff69b-111">È anche possibile creare un processo usando la funzione [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) .</span><span class="sxs-lookup"><span data-stu-id="ff69b-111">You can also create a process using the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) function.</span></span> <span data-ttu-id="ff69b-112">In questo modo è possibile specificare il contesto di sicurezza dell'account utente in cui verrà eseguito il processo.</span><span class="sxs-lookup"><span data-stu-id="ff69b-112">This allows you to specify the security context of the user account in which the process will execute.</span></span>

 

 
