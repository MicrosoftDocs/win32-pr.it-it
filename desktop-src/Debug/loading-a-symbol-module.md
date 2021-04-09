---
description: Se un'applicazione non chiama la funzione SymInitialize con il parametro fInvadeProcess impostato su TRUE, deve caricare i simboli per un modulo quando sono necessari.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Caricamento di un modulo dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125973"
---
# <a name="loading-a-symbol-module"></a><span data-ttu-id="51c53-103">Caricamento di un modulo dei simboli</span><span class="sxs-lookup"><span data-stu-id="51c53-103">Loading a Symbol Module</span></span>

<span data-ttu-id="51c53-104">Se un'applicazione non chiama la funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) con il parametro *FInvadeProcess* impostato su **true**, deve caricare i simboli per un modulo quando sono necessari.</span><span class="sxs-lookup"><span data-stu-id="51c53-104">If an application does not call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function with the *fInvadeProcess* parameter set to **TRUE**, it must load symbols for a module when they are required.</span></span> <span data-ttu-id="51c53-105">Per caricare un modulo di simboli su richiesta, l'applicazione può chiamare la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) con il percorso completo di un nome di modulo.</span><span class="sxs-lookup"><span data-stu-id="51c53-105">To load a symbol module on demand, the application can call the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function with a full path to a module name.</span></span> <span data-ttu-id="51c53-106">Quando il modulo viene caricato, il gestore di simboli caricherà immediatamente i simboli o rinvia il carico, a seconda delle opzioni impostate mediante la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="51c53-106">When the module is loaded, the symbol handler will either load the symbols immediately or defer the load, depending on the options set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span>

<span data-ttu-id="51c53-107">Il codice seguente carica un modulo dei simboli.</span><span class="sxs-lookup"><span data-stu-id="51c53-107">The following code loads a symbol module.</span></span> <span data-ttu-id="51c53-108">Si noti che si presuppone che sia stato inizializzato il gestore di simboli utilizzando il codice nell' [inizializzazione del gestore di simboli](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="51c53-108">Note that it assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



<span data-ttu-id="51c53-109">Si noti che *szImageName* può essere un percorso di qualsiasi modulo eseguibile con informazioni di debug (. exe,. dll,. drv,. sys,. SCR,. cpl,. com).</span><span class="sxs-lookup"><span data-stu-id="51c53-109">Note that *szImageName* can be a path to any executable module that has debugging information (.exe, .dll, .drv, .sys, .scr, .cpl, .com).</span></span> <span data-ttu-id="51c53-110">Inoltre, *dwBaseAddr* è l'indirizzo di base del modulo dei simboli da caricare.</span><span class="sxs-lookup"><span data-stu-id="51c53-110">Also, *dwBaseAddr* is the base address of the symbol module to be loaded.</span></span> <span data-ttu-id="51c53-111">Se questo valore è 0, il gestore di simboli otterrà l'indirizzo di base dal modulo dei simboli specificato.</span><span class="sxs-lookup"><span data-stu-id="51c53-111">If this value is 0, the symbol handler will obtain the base address from the specified symbol module.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51c53-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51c53-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51c53-113">Scaricamento di un modulo di simboli</span><span class="sxs-lookup"><span data-stu-id="51c53-113">Unloading a Symbol Module</span></span>](unloading-a-symbol-module.md)
</dt> </dl>

 

 



