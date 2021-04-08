---
description: Quando si chiama il entryPoints di un assembly, è consigliabile usare lo stesso contesto di attivazione che era attivo durante la ricerca dell'assembly.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Chiamata negli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967724"
---
# <a name="calling-into-assemblies"></a><span data-ttu-id="0cb4a-103">Chiamata negli assembly</span><span class="sxs-lookup"><span data-stu-id="0cb4a-103">Calling Into Assemblies</span></span>

<span data-ttu-id="0cb4a-104">Quando si chiama il entryPoints di un assembly, è consigliabile usare lo stesso contesto di attivazione che era attivo durante la ricerca dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="0cb4a-104">When calling into the entrypoints of an assembly, it is recommended that you use the same activation context that was active when searching for the assembly.</span></span> <span data-ttu-id="0cb4a-105">Assicurarsi almeno che il componente che carica l'assembly non ottenga accidentalmente il contesto di attivazione usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0cb4a-105">At minimum, ensure that the component loading the assembly does not accidentally get the activation context your application is using.</span></span> <span data-ttu-id="0cb4a-106">La perdita del contesto di attivazione tra i limiti DLL può causare dipendenze impreviste.</span><span class="sxs-lookup"><span data-stu-id="0cb4a-106">Leaking activation context across DLL boundaries can lead to unexpected dependencies.</span></span> <span data-ttu-id="0cb4a-107">Questo non è un problema se l'applicazione compila l'isolamento \_ \_ abilitato perché in tal caso non è attivo alcun contesto di attivazione per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0cb4a-107">This is not a problem if your application compiles ISOLATION\_AWARE\_ENABLED because in that case no activation context is active by default.</span></span> <span data-ttu-id="0cb4a-108">Se non si esegue la compilazione con \_ l' \_ Abilitazione dell'isolamento abilitata, è necessario attivare il contesto di attivazione **null** o lo stesso contesto di attivazione usato per caricare l'assembly.</span><span class="sxs-lookup"><span data-stu-id="0cb4a-108">If you do not compile with ISOLATION\_AWARE\_ENABLED defined, you should activate the **NULL** activation context or the same activation context that was used to load the assembly.</span></span>

<span data-ttu-id="0cb4a-109">Nell'esempio seguente si garantisce che la DLL ospitata venga eseguita in un contesto riconosciuto:</span><span class="sxs-lookup"><span data-stu-id="0cb4a-109">The following example ensures that the hosted DLL runs in a context that it recognizes:</span></span>

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



