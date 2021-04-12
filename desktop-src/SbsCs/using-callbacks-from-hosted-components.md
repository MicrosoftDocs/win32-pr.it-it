---
description: I callback dai componenti ospitati sono elementi che rendono possibile l'hosting. Tuttavia, è possibile che il componente che si sta ospitando abbia attivato un altro contesto di attivazione che usa per accedere ai plug-in o ai componenti propri.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Utilizzo di callback da componenti ospitati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef302601985bc7e56a296bc8f494e48e18d785e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128814"
---
# <a name="using-callbacks-from-hosted-components"></a>Utilizzo di callback da componenti ospitati

I callback dai componenti ospitati sono elementi che rendono possibile l'hosting. Tuttavia, è possibile che il componente che si sta ospitando abbia attivato un altro contesto di attivazione che usa per accedere ai plug-in o ai componenti propri. In questo caso, se il componente hosted lascia un contesto di attivazione nello stack che fa riferimento al relativo oggetto COM, l'applicazione host potrebbe chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto che si prevede sia la propria implementazione e ricevere invece l'oggetto del componente ospitato. Per evitare questa ereditarietà dei contesti di attivazione, è consigliabile che una buona applicazione host attivi il proprio contesto di attivazione noto prima durante un callback.

Si consideri l'esempio seguente che protegge il codice dell'applicazione host:

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

In questo modo si garantisce che venga impostato un contesto di attivazione appropriato prima di passare la richiesta a un'implementazione interna di **Funct**. La tua implementazione può avere l'implementazione effettiva inline, ma il metodo precedente garantisce una maggiore interoperabilità semplicemente creando wrapper delegati. È consigliabile usare un metodo simile quando si espongono callback normali (non COM).

 

 
