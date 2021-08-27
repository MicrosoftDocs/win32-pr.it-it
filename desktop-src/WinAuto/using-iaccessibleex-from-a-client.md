---
title: Uso di IAccessibleEx da un client
description: Questo argomento illustra come i client accedono all'implementazione IAccessibleEx di un server e lo usano per ottenere Automazione interfaccia utente e pattern di controllo per gli elementi dell'interfaccia utente.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f03bd58ec80a29f13e0428de4655aa7200144122b1a1889259844db078aa9dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098101"
---
# <a name="using-iaccessibleex-from-a-client"></a>Uso di IAccessibleEx da un client

Questo argomento illustra il modo in cui i client accedono all'implementazione [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) di un server e lo usano per ottenere Automazione interfaccia utente e pattern di controllo per gli elementi dell'interfaccia utente.

Le procedure e gli esempi in questa sezione presuppongono un client [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) già in-process e un server Microsoft Active Accessibility esistente. Presuppongono anche che il client abbia già ottenuto un oggetto **IAccessible** usando una delle funzioni del framework di accessibilità, ad esempio [**AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a>Recupero di un'interfaccia IAccessibleEx dall'interfaccia IAccessible

Un client con [**un'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un oggetto accessibile può usarla per ottenere l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) corrispondente seguendo questa procedura:

-   Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale con un IID \_ \_ di uuidof(IServiceProvider).
-   Chiamare **IServiceProvider::QueryService per** ottenere [**l'oggetto IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)

### <a name="handling-the-child-id"></a>Gestione dell'ID figlio

I client devono essere preparati per i server con un ID figlio diverso da CHILDID \_ SELF. Dopo aver ottenuto [**un'interfaccia IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) da [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)i client devono chiamare [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) se l'ID figlio non è CHILDID SELF (che indica un \_ oggetto padre).

L'esempio seguente illustra come ottenere un [**oggetto IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per un particolare [**oggetto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e un ID figlio.


```C++
   
HRESULT GetIAccessibleExFromIAccessible(IAccessible * pAcc, long idChild, 
                                           IAccessibleEx ** ppaex)
{
    *ppaex = NULL;

    // First, get IServiceProvider from the IAccessible.
    IServiceProvider * pSp = NULL;
    HRESULT hr = pAcc->QueryInterface(IID_IServiceProvider, (void **) & pSp);
    if(FAILED(hr))
        return hr;
    if(pSp == NULL)
        return E_NOINTERFACE;

    // Next, get the IAccessibleEx for the parent object.
    IAccessibleEx * paex = NULL;
    hr = pSp->QueryService(__uuidof(IAccessibleEx), __uuidof(IAccessibleEx),
                                                                 (void **)&paex);
    pSp->Release();
    if(FAILED(hr))
        return hr;
    if(paex == NULL)
        return E_NOINTERFACE;

    // If this is for CHILDID_SELF, we're done. Otherwise, we have a child ID and 
    // can request the object for child.
    if(idChild == CHILDID_SELF)
    {
        *ppaex = paex;
        return S_OK;
    }
    else
    {
        // Get the IAccessibleEx for the specified child.
        IAccessibleEx * paexChild = NULL;
        hr = paex->GetObjectForChild(idChild, &paexChild);
        paex->Release();
        if(FAILED(hr))
            return hr;
        if(paexChild == NULL)
            return E_NOINTERFACE;
        *ppaex = paexChild;
        return S_OK;
    }
}
```



### <a name="obtaining-the-irawelementprovidersimple-interface"></a>Recupero dell'interfaccia IRawElementProviderSimple

Se un client ha [**un'interfaccia IAccessibleEx,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) può usare QueryInterface per ottenere l'interfaccia [**IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) come illustrato nell'esempio seguente.


```C++
HRESULT GetIRawElementProviderFromIAccessible(IAccessible * pAcc, long idChild,
                                                 IRawElementProviderSimple ** ppEl)
{
    * ppEl = NULL;

    // First, get the IAccessibleEx for the IAccessible and child ID pair.
    IAccessibleEx * paex;
    HRESULT hr = GetIAccessibleExFromIAccessible( pAcc, idChild, &paex );
    if(FAILED(hr))
        return hr;

    // Next, use QueryInterface.
    hr = paex->QueryInterface(__uuidof(IRawElementProviderSimple), (void **)ppEl);
    paex->Release();
    return hr;
}
```



### <a name="retrieving-control-patterns"></a>Recupero di pattern di controllo

Se un client ha accesso [**all'interfaccia IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) può recuperare le interfacce del pattern di controllo implementate dai provider e quindi chiamare metodi su tali interfacce. L'esempio seguente illustra come farlo.


```C++
// Helper function to get a pattern interface from an IAccessible and child ID 
// pair. Gets the IAccessibleEx, then calls GetPatternObject and QueryInterface.
HRESULT GetPatternFromIAccessible(IAccessible * pAcc, long idChild,
                                     PATTERNID patternId, REFIID iid, void ** ppv)
{
    // First, get the IAccesibleEx for this IAccessible and child ID pair.
    IRawElementProviderSimple * pel;
    HRESULT hr = GetIRawElementProviderSimpleFromIAccessible(pAcc, idChild, &pel);
    if(FAILED(hr))
        return hr;
    if(pel == NULL)
        return E_NOINTERFACE;

    // Now get the pattern object.
    IUnknown * pPatternObject = NULL;
    hr = pel->GetPatternProvider(patternId, &pPatternObject);
    pel->Release();
    if(FAILED(hr))
        return hr;
    if(pPatternObject == NULL)
        return E_NOINTERFACE;

    // Finally, use QueryInterface to get the correct interface type.
    hr = pPatternObject->QueryInterface(iid, ppv);
    pPatternObject->Release();
    if(*ppv == NULL)
        return E_NOINTERFACE;
    return hr;
}

HRESULT CallInvokePatternMethod(IAccessible * pAcc, long idChild)
{
    IInvokeProvider * pPattern;
    HRESULT hr = GetPatternFromIAccessible(pAcc, varChild,
                                  UIA_InvokePatternId, __uuidof(IInvokeProvider),
                                  (void **)&pPattern);
    if(FAILED(hr))
        return hr;

    hr = pPattern->Invoke();
    pPattern->Release();
    return hr;
}
```



### <a name="retrieving-property-values"></a>Recupero di valori di proprietà

Se un client ha accesso a [**IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)può recuperare i valori delle proprietà. L'esempio seguente illustra come ottenere i valori per le proprietà AutomationId ed LabeledBy Automazione interfaccia utente Microsoft.


```C++
#include <initguid.h>
#include <uiautomationcoreapi.h> // Includes the UI Automation property GUID definitions.
#include <uiautomationcoreids.h> // Includes definitions of pattern/property IDs.

// Assume we already have a IRawElementProviderSimple * pEl.

VARIANT varValue;

// Get AutomationId property:
varValue.vt = VT_EMPTY;
HRESULT hr = pEl->GetPropertyValue(UIA_AutomationIdPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_BSTR)
    {
        // AutomationId is varValue.bstrVal.
    }
    VariantClear(&varValue);
}


// Get LabeledBy property:
varValue.vt = VT_EMPTY;
hr = pEl->GetPropertyValue(UIA_LabeledByPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_UNKNOWN || varValue.punkVal != NULL)
    {
        // Use QueryInterface to get IRawElementProviderSimple.
        IRawElementProviderSimple * pElLabel = NULL;
        hr = varValue.punkVal->QueryInterface(__uuidof(IRawElementProviderSimple),
                                              (void**)& pElLabel);
        if (SUCCEEDED(hr))
        {
            if(pElLabel != NULL)
            {
            // Use the pElLabel pointer here.
            pElLabel ->Release();
            }
        }
    }
    VariantClear(&varValue);
}
```



L'esempio precedente si applica alle proprietà non associate a un pattern di controllo. Per accedere alle proprietà del pattern di controllo, un client deve ottenere e usare un'interfaccia del pattern di controllo.

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a>Recupero di un'interfaccia IAccessible da un'interfaccia IRawElementProviderSimple

Se un client ottiene [**l'interfaccia IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per un elemento dell'interfaccia utente, il client può usare tale interfaccia per ottenere un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) corrispondente per l'elemento. Ciò è utile se il client deve accedere alle proprietà Microsoft Active Accessibility per l'elemento .

Un client può ottenere l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) come valore della proprietà (ad esempio, chiamando [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) con UIA LabeledByPropertyId) o come elemento recuperato da un metodo (ad esempio \_ chiamando [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) per recuperare una matrice di interfacce **IRawElementProviderSimple** degli elementi selezionati). Dopo aver ottenuto **l'interfaccia IRawElementProviderSimple,** un client può usarla per ottenere un [**oggetto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) corrispondente seguendo questa procedura:

-   Provare a usare QueryInterface per ottenere [**l'interfaccia IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)
-   Se QueryInterface ha esito negativo, chiamare [**IAccessibleEx::ConvertReturnedElement sull'istanza**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) [**di IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) da cui è stata originariamente ottenuta la proprietà.
-   Chiamare il [**metodo GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) sulla nuova istanza [**di IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per ottenere un ID figlio e un interfae [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Il frammento di codice seguente illustra come ottenere [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) da [**un'interfaccia IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ottenuta in precedenza.


```C++
// IRawElementProviderSimple * pVal - an element returned by a property or method
// from another IRawElementProviderSimple.

IAccessible * pAcc = NULL;
long idChild;

// First, try to use QueryInterface to get the IAccessibleEx interface.
IAccessibleEx * pAccEx;
HRESULT hr = pVal->QueryInterface(__uuidof(IAccessibleEx), (void**)&pAccEx);
if (SUCCEEDED(hr)
{
    if (!pAccEx)
    {
        // If QueryInterface fails, and the IRawElementProviderSimple was 
              // obtained as a property or return value from another 
              // IRawElementProviderSimple, pass it to the 
              // IAccessibleEx::ConvertReturnedValue method of the
        // originating element.

        pAccExOrig->ConvertReturnedElement(pVal, &pAccEx);
    }

    if (pAccEx)
    {
        // Call GetIAccessiblePair to get an IAccessible interface and 
              // child ID.
        pAccEx->GetIAccessiblePair(&pAcc, &idChild);
    }

    // Finally, use the IAccessible interface and child ID.
    if (pAcc)
    {
        // Use IAccessible methods to get further information about this UI
              // element, or pass it to existing code that works in terms of 
              // IAccessible.
        ...
    }
}    
```



 

 