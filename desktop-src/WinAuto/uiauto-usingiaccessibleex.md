---
title: Aggiunta Automazione interfaccia utente funzionalità ai Active Accessibility server
description: I controlli che non dispongono di un provider microsoft Automazione interfaccia utente ma che implementano IAccessible possono essere facilmente aggiornati per fornire alcune funzionalità Automazione interfaccia utente, implementando l'interfaccia IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Automazione interfaccia utente,Active Accessibility server
- Automazione interfaccia utente,Microsoft Active Accessibility server
- Automazione interfaccia utente,IAccessible
- Automazione interfaccia utente,IAccessibleEx
- Automazione interfaccia utente,esposizione di IAccessibleEx
- Automazione interfaccia utente,implementazione di IAccessibleEx
- Iaccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- esposizione di IAccessibleEx
- Implementazione di IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb313205a69f6b69d07a377b006365837ee2a1410c51962000ea4ccff8b9037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823891"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>Aggiunta Automazione interfaccia utente funzionalità ai Active Accessibility server

I controlli che non dispongono di un provider microsoft Automazione interfaccia utente ma che implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) possono essere facilmente aggiornati per fornire alcune funzionalità Automazione interfaccia utente, implementando [**l'interfaccia IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) Questa interfaccia consente al controllo di esporre Automazione interfaccia utente proprietà e pattern di controllo, senza la necessità di un'implementazione completa delle interfacce Automazione interfaccia utente provider, ad esempio [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Per implementare **IAccessibleEx,** la gerarchia di oggetti Microsoft Active Accessibility di base non deve contenere errori o incoerenze (ad esempio un oggetto figlio il cui oggetto padre non lo elenca come figlio) e non deve essere in conflitto con le specifiche Automazione interfaccia utente. Se la Microsoft Active Accessibility gerarchia di oggetti soddisfa questi requisiti, è un buon candidato per l'aggiunta di funzionalità tramite **IAccessibleEx**. In caso contrario, è necessario implementare Automazione interfaccia utente da solo o insieme all'Microsoft Active Accessibility di installazione.

Si prenda il caso di un controllo personalizzato con un valore di intervallo. Il server Microsoft Active Accessibility per il controllo ne definisce il ruolo ed è in grado di restituire il valore corrente, ma non ha i mezzi per restituire i valori minimo e massimo del controllo, perché queste proprietà non sono definite in Microsoft Active Accessibility. Un Automazione interfaccia utente client è in grado di recuperare il ruolo del controllo, il valore corrente e altre proprietà Microsoft Active Accessibility, perché il core Automazione interfaccia utente può ottenerlo tramite [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Tuttavia, senza l'accesso a [**un'interfaccia IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sull'oggetto, Automazione interfaccia utente non è in grado di recuperare i valori massimo e minimo.

Lo sviluppatore del controllo può fornire un provider Automazione interfaccia utente completo per il controllo, ma ciò significa duplicare gran parte delle funzionalità esistenti dell'implementazione [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ad esempio la navigazione e le proprietà comuni. Lo sviluppatore può invece continuare a fare affidamento su **IAccessible** per fornire questa funzionalità, aggiungendo al tempo stesso il supporto per le proprietà specifiche del controllo tramite [**IRangeValueProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)

L'aggiornamento del controllo personalizzato richiede i passaggi principali seguenti:

-   Implementare [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) nell'oggetto accessibile in modo che l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sia disponibile in questo oggetto o in un oggetto separato.
-   Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sull'oggetto accessibile.
-   Creare oggetti accessibili distinti per Microsoft Active Accessibility elementi figlio, che in Microsoft Active Accessibility potrebbero essere stati rappresentati dall'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nell'oggetto padre (ad esempio, elementi elenco). Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) su questi oggetti.
-   Implementare [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) in tutti gli oggetti accessibili.
-   Implementare le interfacce del pattern di controllo appropriate sugli oggetti accessibili.

In questo argomento sono contenute le sezioni seguenti.

-   [Esposizione di IAccessibleEx](#exposing-iaccessibleex)
-   [Implementazione di IAccessibleEx](#implementing-iaccessibleex)
-   [Argomenti correlati](#related-topics)

## <a name="exposing-iaccessibleex"></a>Esposizione di IAccessibleEx

Poiché l'implementazione [**di IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per un controllo può risiedere in un oggetto separato, le applicazioni client non possono basarsi [**su QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere questa interfaccia. È invece previsto che i client [**chiamino IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)). Nell'implementazione di esempio seguente di questo metodo si presuppone che **IAccessibleEx** non sia implementato in un oggetto separato. pertanto il metodo chiama semplicemente tramite a **QueryInterface**.


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a>Implementazione di IAccessibleEx

Il metodo [**di IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) di maggior interesse è [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild). Questo metodo offre al server Microsoft Active Accessibility la possibilità di creare un oggetto accessibile (che espone almeno **IAccessibleEx)** per un elemento figlio. In Microsoft Active Accessibility, gli elementi figlio in genere non sono rappresentati come oggetti accessibili, ma come elementi figlio di un oggetto accessibile. Tuttavia, poiché Automazione interfaccia utente ogni elemento deve essere rappresentato da un oggetto accessibile separato, **GetObjectForChild** deve creare un oggetto separato per ogni elemento figlio su richiesta.

L'implementazione di esempio seguente restituisce un oggetto accessibile per un elemento in una visualizzazione elenco personalizzata.


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



Per un'implementazione di esempio completa, vedere Rendere accessibili i controlli [personalizzati, Parte 5: Uso di IAccessibleEx](/previous-versions/msdn10/cc307850(v=msdn.10)) per aggiungere il supporto Automazione interfaccia utente a un controllo personalizzato in MSDN.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Automazione interfaccia utente guida per programmatori del provider](uiauto-providerportal.md)
</dt> </dl>

 

 