---
description: Quando si chiama nei punti di ingresso di un assembly, è consigliabile usare lo stesso contesto di attivazione attivo durante la ricerca dell'assembly.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Chiamata agli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6f785c9d68aa0dbf4bec24927d9f2a1443aed1fb7fe65ec9244616fce8feec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142424"
---
# <a name="calling-into-assemblies"></a>Chiamata agli assembly

Quando si chiama nei punti di ingresso di un assembly, è consigliabile usare lo stesso contesto di attivazione attivo durante la ricerca dell'assembly. Assicurarsi almeno che il componente che carica l'assembly non otterrà accidentalmente il contesto di attivazione utilizzato dall'applicazione. La perdita del contesto di attivazione attraverso i limiti della DLL può causare dipendenze impreviste. Questo non è un problema se l'applicazione compila ISOLATION AWARE ENABLED perché in questo caso non è attivo alcun contesto di attivazione \_ \_ per impostazione predefinita. Se non si esegue la compilazione con l'opzione ISOLATION AWARE ENABLED definita, è necessario attivare il contesto di attivazione NULL o lo stesso contesto di attivazione utilizzato per \_ \_ caricare l'assembly. 

L'esempio seguente assicura che la DLL ospitata venga eseguita in un contesto riconosciuto:

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

 

 



