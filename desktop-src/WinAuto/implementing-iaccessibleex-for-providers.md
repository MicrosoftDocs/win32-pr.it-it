---
title: Implementazione di IAccessibleEx per i provider
description: Questa sezione illustra come aggiungere le funzionalità del provider di automazione interfaccia utente Microsoft a un server di Active Accessibility Microsoft implementando l'interfaccia IAccessibleEx.
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299887"
---
# <a name="implementing-iaccessibleex-for-providers"></a>Implementazione di IAccessibleEx per i provider

Questa sezione illustra come aggiungere le funzionalità del provider di automazione interfaccia utente Microsoft a un server di Active Accessibility Microsoft implementando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Prima di implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), considerare i requisiti seguenti:

-   La gerarchia di oggetti di base Microsoft Active Accessibility accessibile deve essere pulita. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) non è in grado di correggere i problemi con le gerarchie degli oggetti accessibili esistenti. Eventuali problemi con la struttura del modello a oggetti devono essere corretti nell'implementazione di Microsoft Active Accessibility prima di implementare **IAccessibleEx**.
-   L'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) deve essere conforme sia alla specifica di Microsoft Active Accessibility sia alla specifica di automazione interfaccia utente. Sono disponibili strumenti per la convalida della conformità in entrambe le specifiche. Per altre informazioni, vedere [strumenti di test](testing-tools.md) e [Framework di automazione di test di automazione interfaccia utente (verifica UIA)](https://www.codeplex.com/UIAutomationVerify/).

Per l'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sono necessari i passaggi principali seguenti:

-   Implementare **IServiceProvider** sull'oggetto accessibile in modo che l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) possa trovarsi in questo oggetto o in un oggetto separato.
-   Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sull'oggetto accessibile.
-   Creare oggetti accessibili per tutti gli elementi figlio di Microsoft Active Accessibility, che in Microsoft Active Accessibility sono rappresentati dall'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nell'oggetto padre (ad esempio, gli elementi dell'elenco). Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) su questi oggetti.
-   Implementare [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) in tutti gli oggetti accessibili.
-   Implementare le interfacce del pattern di controllo appropriate sugli oggetti accessibili.

### <a name="implementing-the-iserviceprovider-interface"></a>Implementazione dell'interfaccia IServiceProvider

Poiché l'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per un controllo può trovarsi in un oggetto separato, le applicazioni client non possono basarsi su [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere questa interfaccia. Al contrario, si prevede che i client chiamino **IServiceProvider:: QueryService**. Nell'implementazione di questo metodo dell'esempio seguente si presuppone che **IAccessibleEx** non sia implementato su un oggetto separato. il metodo chiama quindi semplicemente per **QueryInterface**.


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
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
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a>Implementazione dell'interfaccia IAccessibleEx

In Microsoft Active Accessibility, un elemento dell'interfaccia utente è sempre identificato da un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e da un ID figlio. Una singola istanza di **IAccessible** può rappresentare più elementi dell'interfaccia utente.

Poiché ogni istanza di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) rappresenta solo un singolo elemento dell'interfaccia utente, ogni coppia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e ID figlio deve essere mappata a una singola istanza di **IAccessibleEx** . **IAccessibleEx** include due metodi per gestire questo mapping:

-   [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild): Recupera l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per l'elemento figlio specificato. Questo metodo restituisce **null** se l'implementazione di **IAccessibleEx** non riconosce l'ID figlio specificato, non ha un **IAccessibleEx** per l'elemento figlio specificato o rappresenta un elemento figlio.
-   [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair): Recupera l'interfaccia [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e l'ID figlio per l'elemento [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Per le implementazioni di **IAccessible** che non utilizzano un ID figlio, questo metodo recupera l'oggetto **IACCESSIBLE** corrispondente e CHILDID \_ self.

Nell'esempio seguente viene illustrata l'implementazione dei metodi [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) e [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) per un elemento in una visualizzazione elenco personalizzata. I metodi consentono a automazione interfaccia utente di eseguire il mapping della coppia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e ID figlio a un'istanza di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) corrispondente.


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



Se un'implementazione di un oggetto accessibile non usa un ID figlio, i metodi possono comunque essere implementati, come illustrato nel frammento di codice seguente.


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a>Implementare l'interfaccia IRawElementProviderSimple

I server usano [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per esporre informazioni sulle proprietà e sui pattern di controllo di automazione interfaccia utente. **IRawElementProviderSimple** include i metodi seguenti:

-   [**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider): questo metodo viene usato per esporre le interfacce del pattern di controllo. Restituisce un oggetto che supporta il pattern di controllo specificato o **null** se il pattern di controllo non è supportato.
-   [**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue): questo metodo viene usato per esporre i valori delle proprietà di automazione interfaccia utente.
-   [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider): questo metodo non viene usato con le implementazioni di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .
-   [**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions): questo metodo non viene usato con le implementazioni di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Un server [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) espone i pattern di controllo implementando [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). Questo metodo accetta un parametro integer che specifica il pattern di controllo. Il server restituisce **null** se il modello non è supportato. Se l'interfaccia del pattern di controllo è supportata, i server restituiscono un [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) e il client chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere il pattern di controllo appropriato.

Un server [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) può supportare le proprietà di automazione interfaccia utente (ad esempio, LabeledBy e IsRequiredForForm) implementando [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) e fornendo un intero PROPERTYID che identifica la proprietà come parametro. Questa tecnica si applica solo alle proprietà di automazione interfaccia utente che non sono incluse in un'interfaccia del pattern di controllo. Le proprietà associate a un'interfaccia del pattern di controllo sono esposte tramite il metodo di interfaccia del pattern di controllo. Ad esempio, la proprietà IsSelected del pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) verrebbe esposta con [**ISelectionItemProvider:: Get \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).

 

 