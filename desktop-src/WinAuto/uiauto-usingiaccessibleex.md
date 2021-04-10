---
title: Aggiunta della funzionalità di automazione interfaccia utente ai server Active Accessibility
description: I controlli che non dispongono di un provider di automazione interfaccia utente Microsoft ma che implementano IAccessible possono essere facilmente aggiornati per fornire alcune funzionalità di automazione interfaccia utente, implementando l'interfaccia IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Automazione interfaccia utente, server Active Accessibility
- Automazione interfaccia utente, server Microsoft Active Accessibility
- Automazione interfaccia utente, IAccessible
- Automazione interfaccia utente, IAccessibleEx
- Automazione interfaccia utente, esposizione di IAccessibleEx
- Automazione interfaccia utente, implementazione di IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- esposizione di IAccessibleEx
- implementazione di IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963139"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>Aggiunta della funzionalità di automazione interfaccia utente ai server Active Accessibility

I controlli che non dispongono di un provider di automazione interfaccia utente Microsoft ma che implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) possono essere facilmente aggiornati per fornire alcune funzionalità di automazione interfaccia utente, implementando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Questa interfaccia consente al controllo di esporre le proprietà e i pattern di controllo di automazione interfaccia utente senza la necessità di un'implementazione completa delle interfacce del provider di automazione interfaccia utente, ad esempio [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Per implementare **IAccessibleEx**, la gerarchia di oggetti Microsoft Active Accessibility di base non deve contenere errori o incoerenze (ad esempio un oggetto figlio il cui oggetto padre non lo elenca come figlio) e non deve essere in conflitto con le specifiche di automazione interfaccia utente. Se la gerarchia di oggetti di Microsoft Active Accessibility soddisfa questi requisiti, è un buon candidato per l'aggiunta di funzionalità tramite **IAccessibleEx**; in caso contrario, è necessario implementare l'automazione dell'interfaccia utente autonomamente o insieme all'implementazione di Microsoft Active Accessibility.

Prendere il caso di un controllo personalizzato con un valore di intervallo. Il server Microsoft Active Accessibility per il controllo definisce il proprio ruolo ed è in grado di restituire il valore corrente, ma non ha i mezzi per restituire i valori minimo e massimo del controllo, perché queste proprietà non sono definite in Microsoft Active Accessibility. Un client di automazione interfaccia utente è in grado di recuperare il ruolo del controllo, il valore corrente e altre proprietà di Active Accessibility Microsoft, perché il nucleo di automazione interfaccia utente può ottenere tali proprietà tramite [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Tuttavia, senza l'accesso a un'interfaccia [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sull'oggetto, l'automazione dell'interfaccia utente non è in grado di recuperare i valori massimi e minimi.

Lo sviluppatore del controllo può fornire un provider di automazione interfaccia utente completo per il controllo, ma ciò comporta la duplicazione di gran parte delle funzionalità esistenti dell'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , ad esempio la navigazione e le proprietà comuni. Lo sviluppatore può invece continuare a basarsi su **IAccessible** per fornire questa funzionalità, aggiungendo il supporto per le proprietà specifiche del controllo tramite [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

Per aggiornare il controllo personalizzato sono necessari i passaggi principali seguenti:

-   Implementare [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) sull'oggetto accessibile in modo che l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) possa trovarsi in questo oggetto o in un oggetto separato.
-   Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sull'oggetto accessibile.
-   Creare oggetti distinti accessibili per tutti gli elementi figlio di Microsoft Active Accessibility, che in Microsoft Active Accessibility potrebbero essere stati rappresentati dall'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nell'oggetto padre (ad esempio, gli elementi dell'elenco). Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) su questi oggetti.
-   Implementare [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) in tutti gli oggetti accessibili.
-   Implementare le interfacce del pattern di controllo appropriate sugli oggetti accessibili.

In questo argomento sono contenute le sezioni seguenti.

-   [Esposizione di IAccessibleEx](#exposing-iaccessibleex)
-   [Implementazione di IAccessibleEx](#implementing-iaccessibleex)
-   [Argomenti correlati](#related-topics)

## <a name="exposing-iaccessibleex"></a>Esposizione di IAccessibleEx

Poiché l'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per un controllo può trovarsi in un oggetto separato, le applicazioni client non possono basarsi su [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere questa interfaccia. Al contrario, si prevede che i client chiamino [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)). Nell'implementazione di questo metodo dell'esempio seguente si presuppone che **IAccessibleEx** non sia implementato su un oggetto separato. il metodo chiama quindi semplicemente per **QueryInterface**.


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

Il metodo di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) di maggiore interesse è [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild). Questo metodo fornisce al server Microsoft Active Accessibility la possibilità di creare un oggetto accessibile (uno che espone, come minimo, **IAccessibleEx**) per un elemento figlio. In Microsoft Active Accessibility gli elementi figlio non sono in genere rappresentati come oggetti accessibili, ma come elementi figlio di un oggetto accessibile. Tuttavia, poiché l'automazione dell'interfaccia utente richiede che ogni elemento sia rappresentato da un oggetto accessibile separato, **GetObjectForChild** deve creare un oggetto separato per ogni elemento figlio su richiesta.

Nell'implementazione di esempio seguente viene restituito un oggetto accessibile per un elemento in una visualizzazione elenco personalizzata.


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



Per un'implementazione di esempio completa, vedere [rendere accessibili i controlli personalizzati, parte 5: uso di IAccessibleEx per aggiungere il supporto di automazione interfaccia utente a un controllo personalizzato](/previous-versions/msdn10/cc307850(v=msdn.10)) in MSDN.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori del provider di automazione interfaccia utente](uiauto-providerportal.md)
</dt> </dl>

 

 