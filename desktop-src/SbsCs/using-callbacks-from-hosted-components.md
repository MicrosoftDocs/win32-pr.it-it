---
description: I callback dai componenti ospitati sono ciò che rende possibile l'hosting. Tuttavia, è possibile che il componente che si sta ospitando abbia attivato un altro contesto di attivazione che usa per accedere a plug-in o componenti propri.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Uso di callback da componenti ospitati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb13e61b83ba52f0f8dd5265b11585e8366c0e8558d45c5738f179d43df2eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884601"
---
# <a name="using-callbacks-from-hosted-components"></a>Uso di callback da componenti ospitati

I callback dai componenti ospitati sono ciò che rende possibile l'hosting. Tuttavia, è possibile che il componente che si sta ospitando abbia attivato un altro contesto di attivazione che usa per accedere a plug-in o componenti propri. In questo caso, se il componente ospitato lascia nello stack un contesto di attivazione che fa riferimento al proprio oggetto COM, l'applicazione host potrebbe chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto che prevede di essere la propria implementazione e ricevere invece l'oggetto del componente ospitato. Per evitare questa ereditarietà dei contesti di attivazione, una buona applicazione di hosting deve attivare prima il proprio contesto di attivazione noto durante un callback.

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

In questo modo si garantisce che venga impostato un contesto di attivazione appropriato prima di passare la richiesta a un'implementazione interna di **Funct**. La propria implementazione può avere l'implementazione effettiva inline, ma il metodo precedente garantisce una maggiore interoperabilità semplicemente creando wrapper delegati. È consigliabile usare un metodo simile quando si espongono callback normali (non COM).

 

 
