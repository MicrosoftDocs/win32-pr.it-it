---
description: Il codice seguente elenca i moduli caricati dalla funzione SymLoadModule64 o SymInitialize.
ms.assetid: 8c7fdfaa-d4d3-42d6-ad19-23e8ffda7bf4
title: Enumerazione dei moduli di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43623a7409116450fccc822bbc0bef1a309fbd2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482725"
---
# <a name="enumerating-symbol-modules"></a><span data-ttu-id="f1043-103">Enumerazione dei moduli di simboli</span><span class="sxs-lookup"><span data-stu-id="f1043-103">Enumerating Symbol Modules</span></span>

<span data-ttu-id="f1043-104">Il codice seguente elenca i moduli caricati dalla funzione [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) o [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="f1043-104">The following code lists the modules that have been loaded by the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="f1043-105">La funzione [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) richiede una funzione di callback, che verrà chiamata una volta per ogni modulo caricato.</span><span class="sxs-lookup"><span data-stu-id="f1043-105">The [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) function requires a callback function, which will be called once for each module loaded.</span></span> <span data-ttu-id="f1043-106">In questo esempio, EnumModules è un'implementazione della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f1043-106">In this example, EnumModules is an implementation of the callback function.</span></span> <span data-ttu-id="f1043-107">Nell'esempio si presuppone che sia stato inizializzato il gestore di simboli utilizzando il codice nell' [inizializzazione del gestore di simboli](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="f1043-107">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
BOOL CALLBACK EnumModules(
    PCTSTR  ModuleName, 
    DWORD64 BaseOfDll,  
    PVOID   UserContext )
{
    UNREFERENCED_PARAMETER(UserContext);
    
    _tprintf(TEXT("%08X %s\n"), BaseOfDll, ModuleName);
    return TRUE;
}


if (SymEnumerateModules64(hProcess, EnumModules, NULL))
{
    // SymEnumerateModules64 returned success
}
else
{
    // SymEnumerateModules64 failed
    error = GetLastError();
    _tprintf(TEXT("SymEnumerateModules64 returned error : %d\n"), error);
}
```



 

 



