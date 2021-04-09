---
description: Nel codice seguente viene illustrato come inizializzare il gestore di simboli.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Inizializzazione del gestore di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965945"
---
# <a name="initializing-the-symbol-handler"></a><span data-ttu-id="f64b6-103">Inizializzazione del gestore di simboli</span><span class="sxs-lookup"><span data-stu-id="f64b6-103">Initializing the Symbol Handler</span></span>

<span data-ttu-id="f64b6-104">Nel codice seguente viene illustrato come inizializzare il gestore di simboli.</span><span class="sxs-lookup"><span data-stu-id="f64b6-104">The following code demonstrates how to initialize the symbol handler.</span></span> <span data-ttu-id="f64b6-105">La funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) rinvia il caricamento dei simboli fino a quando non vengono richieste informazioni sui simboli.</span><span class="sxs-lookup"><span data-stu-id="f64b6-105">The [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function defers symbol loading until symbol information is requested.</span></span> <span data-ttu-id="f64b6-106">Il codice carica i simboli per ogni modulo nel processo specificato passando il valore **true** per il parametro *BInvade* della funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="f64b6-106">The code loads the symbols for each module in the specified process by passing a value of **TRUE** for the *bInvade* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="f64b6-107">Questa funzione chiama la funzione [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) per ogni modulo a cui è stato eseguito il mapping del processo nello spazio degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="f64b6-107">(This function calls the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) function for each module the process has mapped into its address space.)</span></span>

<span data-ttu-id="f64b6-108">Se il processo specificato non è il processo che ha chiamato [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), il codice passa un identificatore di processo come primo parametro di **SymInitialize**.</span><span class="sxs-lookup"><span data-stu-id="f64b6-108">If the specified process is not the process that called [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), the code passes a process identifier as the first parameter of **SymInitialize**.</span></span>

<span data-ttu-id="f64b6-109">Se si specifica **null** come secondo parametro di [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) , il gestore di simboli deve utilizzare il percorso di ricerca predefinito per individuare i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="f64b6-109">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="f64b6-110">Per informazioni dettagliate sul modo in cui il gestore di simboli individua i file di simboli o su come un'applicazione può specificare un percorso di ricerca dei simboli, vedere [percorsi](symbol-paths.md)dei simboli.</span><span class="sxs-lookup"><span data-stu-id="f64b6-110">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



