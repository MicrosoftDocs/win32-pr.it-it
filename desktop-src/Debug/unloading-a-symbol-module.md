---
description: Il codice seguente Scarica un modulo di simboli a cui fa riferimento l'indirizzo del modulo BaseOfDll usando SymUnloadModule64.
ms.assetid: f185ae64-1de9-4139-acd5-7c3a108e1eba
title: Scaricamento di un modulo di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b6fad0177fce36865e90dadf04bd563130789
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877782"
---
# <a name="unloading-a-symbol-module"></a><span data-ttu-id="38cb1-103">Scaricamento di un modulo di simboli</span><span class="sxs-lookup"><span data-stu-id="38cb1-103">Unloading a Symbol Module</span></span>

<span data-ttu-id="38cb1-104">Il codice seguente Scarica un modulo di simboli a cui fa riferimento l'indirizzo del modulo BaseOfDll usando [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule).</span><span class="sxs-lookup"><span data-stu-id="38cb1-104">The following code unloads a symbol module referred to by the BaseOfDll module address using [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule).</span></span>


```C++
if (SymUnloadModule64(hProcess, BaseOfDll))
{
    // SymUnloadModule64 returned success
}
else
{
    // SymUnloadModule64 failed
    DWORD error = GetLastError();
    printf("SymUnloadModule64 returned error : %d\n", error);
}
```



## <a name="related-topics"></a><span data-ttu-id="38cb1-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38cb1-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38cb1-106">Caricamento di un modulo dei simboli</span><span class="sxs-lookup"><span data-stu-id="38cb1-106">Loading a Symbol Module</span></span>](loading-a-symbol-module.md)
</dt> </dl>

 

 



