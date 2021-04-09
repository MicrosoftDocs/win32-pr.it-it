---
description: Il codice seguente consente di visualizzare il nome, l'indirizzo e le dimensioni di ogni simbolo caricato nel modulo specificato.
ms.assetid: 6ecdbd1e-406a-453e-9037-707ceb72074a
title: Enumerazione dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33f9a98f37ca5ef2249f68ffa9b8ef73198de242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965887"
---
# <a name="enumerating-symbols"></a><span data-ttu-id="8a134-103">Enumerazione dei simboli</span><span class="sxs-lookup"><span data-stu-id="8a134-103">Enumerating Symbols</span></span>

<span data-ttu-id="8a134-104">Il codice seguente consente di visualizzare il nome, l'indirizzo e le dimensioni di ogni simbolo caricato nel modulo specificato.</span><span class="sxs-lookup"><span data-stu-id="8a134-104">The following code displays the name, address, and size of each loaded symbol in the specified module.</span></span> <span data-ttu-id="8a134-105">La funzione [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) richiede una funzione di callback, che viene chiamata una volta per ogni modulo caricato.</span><span class="sxs-lookup"><span data-stu-id="8a134-105">The [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) function requires a callback function, which is called once for each module loaded.</span></span> <span data-ttu-id="8a134-106">In questo esempio, EnumSymProc è un'implementazione della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="8a134-106">In this example, EnumSymProc is an implementation of the callback function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <dbghelp.h>

BOOL CALLBACK EnumSymProc( 
    PSYMBOL_INFO pSymInfo,   
    ULONG SymbolSize,      
    PVOID UserContext)
{
    UNREFERENCED_PARAMETER(UserContext);
    
    printf("%08X %4u %s\n", 
           pSymInfo->Address, SymbolSize, pSymInfo->Name);
    return TRUE;
}

void main()
{
    HANDLE hProcess = GetCurrentProcess();
    DWORD64 BaseOfDll;
    char *Mask = "*";
    BOOL status;

    status = SymInitialize(hProcess, NULL, FALSE);
    if (status == FALSE)
    {
        return;
    }
    
    BaseOfDll = SymLoadModuleEx(hProcess,
                                NULL,
                                "foo.dll",
                                NULL,
                                0,
                                0,
                                NULL,
                                0);
                                
    if (BaseOfDll == 0)
    {
        SymCleanup(hProcess);
        return;
    }                                
        
    if (SymEnumSymbols(hProcess,     // Process handle from SymInitialize.
                        BaseOfDll,   // Base address of module.
                        Mask,        // Name of symbols to match.
                        EnumSymProc, // Symbol handler procedure.
                        NULL))       // User context.
    {
        // SymEnumSymbols succeeded
    }
    else
    {
        // SymEnumSymbols failed
        printf("SymEnumSymbols failed: %d\n", GetLastError());
    }
    
    SymCleanup(hProcess);
}
```



 

 



