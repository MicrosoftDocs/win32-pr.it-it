---
title: Come abilitare la navigazione in un provider di frammenti di automazione interfaccia utente
description: Questo argomento contiene codice di esempio che illustra come abilitare la navigazione in un provider di automazione interfaccia utente Microsoft per un elemento in un frammento.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044189"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a>Come abilitare la navigazione in un provider di frammenti di automazione interfaccia utente

Questo argomento contiene codice di esempio che illustra come abilitare la navigazione in un provider di automazione interfaccia utente Microsoft per un elemento in un frammento.

Il codice di esempio seguente implementa il metodo [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) per una voce di elenco in un controllo elenco personalizzato. L'elemento padre è il controllo elenco personalizzato, mentre gli elementi di pari livello sono altri elementi dell'elenco. Il metodo imposta il parametro *pRetVal* su **null** se non è presente alcun elemento nella direzione specificata.


```C++
// Implementation of IRawElementProviderFragment::Navigate.
// Enables UI Automation to locate the element in the tree.
HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*) m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*) m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*) m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag->AddRef();
    }
    return S_OK;
}              
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di un provider di automazione interfaccia utente Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Procedure per i provider di automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




