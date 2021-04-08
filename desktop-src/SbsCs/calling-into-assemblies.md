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
# <a name="calling-into-assemblies"></a>Chiamata negli assembly

Quando si chiama il entryPoints di un assembly, è consigliabile usare lo stesso contesto di attivazione che era attivo durante la ricerca dell'assembly. Assicurarsi almeno che il componente che carica l'assembly non ottenga accidentalmente il contesto di attivazione usato dall'applicazione. La perdita del contesto di attivazione tra i limiti DLL può causare dipendenze impreviste. Questo non è un problema se l'applicazione compila l'isolamento \_ \_ abilitato perché in tal caso non è attivo alcun contesto di attivazione per impostazione predefinita. Se non si esegue la compilazione con \_ l' \_ Abilitazione dell'isolamento abilitata, è necessario attivare il contesto di attivazione **null** o lo stesso contesto di attivazione usato per caricare l'assembly.

Nell'esempio seguente si garantisce che la DLL ospitata venga eseguita in un contesto riconosciuto:

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

 

 



