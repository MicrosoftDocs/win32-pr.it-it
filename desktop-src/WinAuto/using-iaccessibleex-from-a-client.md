---
title: Uso di IAccessibleEx da un client
description: In questo argomento viene illustrato come i client accedono all'implementazione IAccessibleEx di un server e lo usano per ottenere le proprietà e i pattern di controllo di automazione interfaccia utente per gli elementi dell'interfaccia utente
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b14b935bd7ed432ea4d378034763635309213f
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399918"
---
# <a name="using-iaccessibleex-from-a-client"></a><span data-ttu-id="dde3d-103">Uso di IAccessibleEx da un client</span><span class="sxs-lookup"><span data-stu-id="dde3d-103">Using IAccessibleEx from a Client</span></span>

<span data-ttu-id="dde3d-104">In questo argomento viene illustrato come i client accedono all'implementazione [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) di un server e lo usano per ottenere le proprietà e i pattern di controllo di automazione interfaccia utente per gli elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="dde3d-104">This topic explains how clients access the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation of a server and use it to get UI Automation properties and control patterns for UI elements.</span></span>

<span data-ttu-id="dde3d-105">Le procedure e gli esempi in questa sezione presuppongono un client [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) già in-process e un server Microsoft Active Accessibility esistente.</span><span class="sxs-lookup"><span data-stu-id="dde3d-105">The procedures and examples in this section assume an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) client that is already in-process, and an existing Microsoft Active Accessibility server.</span></span> <span data-ttu-id="dde3d-106">Si presuppone inoltre che il client abbia già ottenuto un oggetto **IAccessible** utilizzando una delle funzioni del Framework di accessibilità, ad esempio [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="dde3d-106">They also assume that the client has already obtained an **IAccessible** object by using one of the accessibility framework functions such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a><span data-ttu-id="dde3d-107">Acquisizione di un'interfaccia IAccessibleEx dall'interfaccia IAccessible</span><span class="sxs-lookup"><span data-stu-id="dde3d-107">Obtaining an IAccessibleEx Interface from the IAccessible Interface</span></span>

<span data-ttu-id="dde3d-108">Un client che dispone di un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un oggetto accessibile può utilizzarlo per ottenere l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) corrispondente attenendosi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="dde3d-108">A client that has an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for an accessible object can use it to obtain the corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface by following these steps:</span></span>

-   <span data-ttu-id="dde3d-109">Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale con un IID di \_ \_ uuidof (IServiceProvider).</span><span class="sxs-lookup"><span data-stu-id="dde3d-109">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with an IID of \_\_uuidof(IServiceProvider).</span></span>
-   <span data-ttu-id="dde3d-110">Chiamare **IServiceProvider:: QueryService** per ottenere il [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span><span class="sxs-lookup"><span data-stu-id="dde3d-110">Call **IServiceProvider::QueryService** to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span></span>

### <a name="handling-the-child-id"></a><span data-ttu-id="dde3d-111">Gestione dell'ID figlio</span><span class="sxs-lookup"><span data-stu-id="dde3d-111">Handling the Child ID</span></span>

<span data-ttu-id="dde3d-112">I client devono essere preparati per i server con un ID figlio diverso da CHILDID \_ self.</span><span class="sxs-lookup"><span data-stu-id="dde3d-112">Clients must be prepared for servers with a child ID other than CHILDID\_SELF.</span></span> <span data-ttu-id="dde3d-113">Dopo avere ottenuto un'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) da un [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), i client devono chiamare [**IAccessibleEx:: GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) se l'ID figlio non è CHILDID \_ self (che indica un oggetto padre).</span><span class="sxs-lookup"><span data-stu-id="dde3d-113">After obtaining an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface from an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), clients must call [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) if the child ID is not CHILDID\_SELF (indicating a parent object).</span></span>

<span data-ttu-id="dde3d-114">Nell'esempio seguente viene illustrato come ottenere un [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per un determinato oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e ID figlio.</span><span class="sxs-lookup"><span data-stu-id="dde3d-114">The following example shows how to get an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a particular [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span>


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



### <a name="obtaining-the-irawelementprovidersimple-interface"></a><span data-ttu-id="dde3d-115">Ottenere l'interfaccia IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="dde3d-115">Obtaining the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="dde3d-116">Se un client dispone di un'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , può usare QueryInterface per ottenere l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="dde3d-116">If a client has an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, it can use QueryInterface to get to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, as the following example shows.</span></span>


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



### <a name="retrieving-control-patterns"></a><span data-ttu-id="dde3d-117">Recupero dei pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="dde3d-117">Retrieving Control Patterns</span></span>

<span data-ttu-id="dde3d-118">Se un client ha accesso all'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , può recuperare le interfacce del pattern di controllo implementate dai provider e quindi chiamare i metodi su tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="dde3d-118">If a client has access to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, it can retrieve control pattern interfaces that have been implemented by providers, and can then call methods on those interfaces.</span></span> <span data-ttu-id="dde3d-119">L'esempio seguente illustra come farlo.</span><span class="sxs-lookup"><span data-stu-id="dde3d-119">The following example shows how to do this.</span></span>


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



### <a name="retrieving-property-values"></a><span data-ttu-id="dde3d-120">Recupero dei valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="dde3d-120">Retrieving Property Values</span></span>

<span data-ttu-id="dde3d-121">Se un client ha accesso a [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), può recuperare i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="dde3d-121">If a client has access to [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), it can retrieve property values.</span></span> <span data-ttu-id="dde3d-122">Nell'esempio seguente viene illustrato come ottenere i valori per le proprietà di automazione interfaccia utente Microsoft AutomationId e LabeledBy.</span><span class="sxs-lookup"><span data-stu-id="dde3d-122">The following example shows how to get values for the AutomationId and LabeledBy Microsoft UI Automation properties.</span></span>


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



<span data-ttu-id="dde3d-123">L'esempio precedente si applica alle proprietà non associate a un pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="dde3d-123">The preceding example applies to properties that are not associated with a control pattern.</span></span> <span data-ttu-id="dde3d-124">Per accedere alle proprietà del pattern di controllo, un client deve ottenere e usare un'interfaccia del pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="dde3d-124">To access control pattern properties, a client must obtain and use a control pattern interface.</span></span>

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a><span data-ttu-id="dde3d-125">Recupero di un'interfaccia IAccessible da un'interfaccia IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="dde3d-125">Retrieving an IAccessible Interface from an IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="dde3d-126">Se un client ottiene l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per un elemento dell'interfaccia utente, il client può utilizzare tale interfaccia per ottenere un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) corrispondente per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="dde3d-126">If a client obtains the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface for a UI element, the client can use that interface to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="dde3d-127">Questa operazione è utile se il client deve accedere alle proprietà di Microsoft Active Accessibility per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="dde3d-127">This is useful if the client needs to access the Microsoft Active Accessibility properties for the element.</span></span>

<span data-ttu-id="dde3d-128">Un client può ottenere l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) come valore della proprietà (ad esempio, chiamando [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) con UIA \_ LabeledByPropertyId) o come elemento recuperato da un metodo (ad esempio, chiamando [**ISelectionProvider:: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) per recuperare una matrice di interfacce **IRawElementProviderSimple** degli elementi selezionati).</span><span class="sxs-lookup"><span data-stu-id="dde3d-128">A client can obtain the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface as a property value (for example, by calling [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) with UIA\_LabeledByPropertyId), or as an item retrieved by a method (for example, by calling [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) to retrieve an array of **IRawElementProviderSimple** interfaces of selected elements).</span></span> <span data-ttu-id="dde3d-129">Dopo aver ottenuto l'interfaccia **IRawElementProviderSimple** , un client può usarlo per ottenere un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) corrispondente attenendosi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="dde3d-129">After obtaining the **IRawElementProviderSimple** interface, a client can use it to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) by following these steps:</span></span>

-   <span data-ttu-id="dde3d-130">Tentativo di utilizzare QueryInterface per ottenere l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="dde3d-130">Attempt to use QueryInterface to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>
-   <span data-ttu-id="dde3d-131">Se QueryInterface ha esito negativo, chiamare [**IAccessibleEx:: ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) sull'istanza di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) dalla quale è stata originariamente ottenuta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="dde3d-131">If QueryInterface fails, call [**IAccessibleEx::ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) on the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance from which the property was originally obtained.</span></span>
-   <span data-ttu-id="dde3d-132">Chiamare il metodo [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) sulla nuova istanza di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per ottenere un elemento [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfae e un ID figlio.</span><span class="sxs-lookup"><span data-stu-id="dde3d-132">Call the [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) method on the new [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfae and child ID.</span></span>

<span data-ttu-id="dde3d-133">Nel frammento di codice seguente viene illustrato come ottenere l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) da un'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ottenuta in precedenza.</span><span class="sxs-lookup"><span data-stu-id="dde3d-133">The following code snippet demonstrates how to obtain the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface from a previously-obtained [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface.</span></span>


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



 

 