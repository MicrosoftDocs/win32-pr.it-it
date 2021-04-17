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
# <a name="implementing-iaccessibleex-for-providers"></a><span data-ttu-id="dab9c-103">Implementazione di IAccessibleEx per i provider</span><span class="sxs-lookup"><span data-stu-id="dab9c-103">Implementing IAccessibleEx for Providers</span></span>

<span data-ttu-id="dab9c-104">Questa sezione illustra come aggiungere le funzionalità del provider di automazione interfaccia utente Microsoft a un server di Active Accessibility Microsoft implementando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="dab9c-104">This section explains how to add Microsoft UI Automation provider capabilities to a Microsoft Active Accessibility server by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>

<span data-ttu-id="dab9c-105">Prima di implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), considerare i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="dab9c-105">Before implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), consider the following requirements:</span></span>

-   <span data-ttu-id="dab9c-106">La gerarchia di oggetti di base Microsoft Active Accessibility accessibile deve essere pulita.</span><span class="sxs-lookup"><span data-stu-id="dab9c-106">The baseline Microsoft Active Accessibility accessible object hierarchy must be clean.</span></span> <span data-ttu-id="dab9c-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) non è in grado di correggere i problemi con le gerarchie degli oggetti accessibili esistenti.</span><span class="sxs-lookup"><span data-stu-id="dab9c-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) cannot correct problems with existing accessible object hierarchies.</span></span> <span data-ttu-id="dab9c-108">Eventuali problemi con la struttura del modello a oggetti devono essere corretti nell'implementazione di Microsoft Active Accessibility prima di implementare **IAccessibleEx**.</span><span class="sxs-lookup"><span data-stu-id="dab9c-108">Any problems with the object model structure must be corrected in the Microsoft Active Accessibility implementation before implementing **IAccessibleEx**.</span></span>
-   <span data-ttu-id="dab9c-109">L'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) deve essere conforme sia alla specifica di Microsoft Active Accessibility sia alla specifica di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="dab9c-109">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation must comply with both the Microsoft Active Accessibility specification and the UI Automation specification.</span></span> <span data-ttu-id="dab9c-110">Sono disponibili strumenti per la convalida della conformità in entrambe le specifiche.</span><span class="sxs-lookup"><span data-stu-id="dab9c-110">Tools are available to validate compliance under both specifications.</span></span> <span data-ttu-id="dab9c-111">Per altre informazioni, vedere [strumenti di test](testing-tools.md) e [Framework di automazione di test di automazione interfaccia utente (verifica UIA)](https://www.codeplex.com/UIAutomationVerify/).</span><span class="sxs-lookup"><span data-stu-id="dab9c-111">For more information, see [Testing Tools](testing-tools.md) and [UI Automation Verify (UIA Verify) Test Automation Framework](https://www.codeplex.com/UIAutomationVerify/).</span></span>

<span data-ttu-id="dab9c-112">Per l'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sono necessari i passaggi principali seguenti:</span><span class="sxs-lookup"><span data-stu-id="dab9c-112">Implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requires these main steps:</span></span>

-   <span data-ttu-id="dab9c-113">Implementare **IServiceProvider** sull'oggetto accessibile in modo che l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) possa trovarsi in questo oggetto o in un oggetto separato.</span><span class="sxs-lookup"><span data-stu-id="dab9c-113">Implement **IServiceProvider** on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="dab9c-114">Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sull'oggetto accessibile.</span><span class="sxs-lookup"><span data-stu-id="dab9c-114">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="dab9c-115">Creare oggetti accessibili per tutti gli elementi figlio di Microsoft Active Accessibility, che in Microsoft Active Accessibility sono rappresentati dall'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nell'oggetto padre (ad esempio, gli elementi dell'elenco).</span><span class="sxs-lookup"><span data-stu-id="dab9c-115">Create accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility are represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="dab9c-116">Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) su questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="dab9c-116">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="dab9c-117">Implementare [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) in tutti gli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="dab9c-117">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="dab9c-118">Implementare le interfacce del pattern di controllo appropriate sugli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="dab9c-118">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

### <a name="implementing-the-iserviceprovider-interface"></a><span data-ttu-id="dab9c-119">Implementazione dell'interfaccia IServiceProvider</span><span class="sxs-lookup"><span data-stu-id="dab9c-119">Implementing the IServiceProvider Interface</span></span>

<span data-ttu-id="dab9c-120">Poiché l'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per un controllo può trovarsi in un oggetto separato, le applicazioni client non possono basarsi su [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="dab9c-120">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="dab9c-121">Al contrario, si prevede che i client chiamino **IServiceProvider:: QueryService**.</span><span class="sxs-lookup"><span data-stu-id="dab9c-121">Instead, clients are expected to call **IServiceProvider::QueryService**.</span></span> <span data-ttu-id="dab9c-122">Nell'implementazione di questo metodo dell'esempio seguente si presuppone che **IAccessibleEx** non sia implementato su un oggetto separato. il metodo chiama quindi semplicemente per **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="dab9c-122">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


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



### <a name="implementing-the-iaccessibleex-interface"></a><span data-ttu-id="dab9c-123">Implementazione dell'interfaccia IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="dab9c-123">Implementing the IAccessibleEx Interface</span></span>

<span data-ttu-id="dab9c-124">In Microsoft Active Accessibility, un elemento dell'interfaccia utente è sempre identificato da un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e da un ID figlio.</span><span class="sxs-lookup"><span data-stu-id="dab9c-124">In Microsoft Active Accessibility, a UI element is always identified by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and a child ID.</span></span> <span data-ttu-id="dab9c-125">Una singola istanza di **IAccessible** può rappresentare più elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="dab9c-125">A single instance of **IAccessible** can represent multiple UI elements.</span></span>

<span data-ttu-id="dab9c-126">Poiché ogni istanza di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) rappresenta solo un singolo elemento dell'interfaccia utente, ogni coppia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e ID figlio deve essere mappata a una singola istanza di **IAccessibleEx** .</span><span class="sxs-lookup"><span data-stu-id="dab9c-126">Because each [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance represents only a single UI element, each [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair must be mapped to a single **IAccessibleEx** instance.</span></span> <span data-ttu-id="dab9c-127">**IAccessibleEx** include due metodi per gestire questo mapping:</span><span class="sxs-lookup"><span data-stu-id="dab9c-127">**IAccessibleEx** includes two methods to handle this mapping:</span></span>

-   <span data-ttu-id="dab9c-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild): Recupera l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per l'elemento figlio specificato.</span><span class="sxs-lookup"><span data-stu-id="dab9c-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)—Retrieves the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface for the specified child.</span></span> <span data-ttu-id="dab9c-129">Questo metodo restituisce **null** se l'implementazione di **IAccessibleEx** non riconosce l'ID figlio specificato, non ha un **IAccessibleEx** per l'elemento figlio specificato o rappresenta un elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="dab9c-129">This method returns **NULL** if the **IAccessibleEx** implementation does not recognize the specified child ID, does not have an **IAccessibleEx** for the specified child, or represents a child element.</span></span>
-   <span data-ttu-id="dab9c-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair): Recupera l'interfaccia [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e l'ID figlio per l'elemento [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="dab9c-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)—Retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and child ID for the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) element.</span></span> <span data-ttu-id="dab9c-131">Per le implementazioni di **IAccessible** che non utilizzano un ID figlio, questo metodo recupera l'oggetto **IACCESSIBLE** corrispondente e CHILDID \_ self.</span><span class="sxs-lookup"><span data-stu-id="dab9c-131">For **IAccessible** implementations that do not use a child ID, this method retrieves the corresponding **IAccessible** object and CHILDID\_SELF.</span></span>

<span data-ttu-id="dab9c-132">Nell'esempio seguente viene illustrata l'implementazione dei metodi [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) e [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) per un elemento in una visualizzazione elenco personalizzata.</span><span class="sxs-lookup"><span data-stu-id="dab9c-132">The following example shows the implementation of the [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) and [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) methods for an item in a custom list view.</span></span> <span data-ttu-id="dab9c-133">I metodi consentono a automazione interfaccia utente di eseguire il mapping della coppia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e ID figlio a un'istanza di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="dab9c-133">The methods enable UI Automation to map the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair to a corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance.</span></span>


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



<span data-ttu-id="dab9c-134">Se un'implementazione di un oggetto accessibile non usa un ID figlio, i metodi possono comunque essere implementati, come illustrato nel frammento di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="dab9c-134">If an accessible object implementation does not use a child ID, the methods can still be implemented as shown in the following code snippet.</span></span>


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



### <a name="implement-the-irawelementprovidersimple-interface"></a><span data-ttu-id="dab9c-135">Implementare l'interfaccia IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="dab9c-135">Implement the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="dab9c-136">I server usano [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per esporre informazioni sulle proprietà e sui pattern di controllo di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="dab9c-136">Servers use [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) to expose information about UI Automation properties and control patterns.</span></span> <span data-ttu-id="dab9c-137">**IRawElementProviderSimple** include i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="dab9c-137">**IRawElementProviderSimple** includes the following methods:</span></span>

-   <span data-ttu-id="dab9c-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider): questo metodo viene usato per esporre le interfacce del pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="dab9c-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)—This method is used to expose control pattern interfaces.</span></span> <span data-ttu-id="dab9c-139">Restituisce un oggetto che supporta il pattern di controllo specificato o **null** se il pattern di controllo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dab9c-139">It returns an object that supports the specified control pattern, or **NULL** if the control pattern is not supported.</span></span>
-   <span data-ttu-id="dab9c-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue): questo metodo viene usato per esporre i valori delle proprietà di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="dab9c-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)—This method is used to expose UI Automation property values.</span></span>
-   <span data-ttu-id="dab9c-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider): questo metodo non viene usato con le implementazioni di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="dab9c-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>
-   <span data-ttu-id="dab9c-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions): questo metodo non viene usato con le implementazioni di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="dab9c-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>

<span data-ttu-id="dab9c-143">Un server [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) espone i pattern di controllo implementando [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span><span class="sxs-lookup"><span data-stu-id="dab9c-143">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server exposes control patterns by implementing [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span></span> <span data-ttu-id="dab9c-144">Questo metodo accetta un parametro integer che specifica il pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="dab9c-144">This method takes an integer parameter that specifies the control pattern.</span></span> <span data-ttu-id="dab9c-145">Il server restituisce **null** se il modello non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dab9c-145">The server returns **NULL** if the pattern is not supported.</span></span> <span data-ttu-id="dab9c-146">Se l'interfaccia del pattern di controllo è supportata, i server restituiscono un [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) e il client chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere il pattern di controllo appropriato.</span><span class="sxs-lookup"><span data-stu-id="dab9c-146">If the control pattern interface is supported, servers return an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) and the client then calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the appropriate control pattern.</span></span>

<span data-ttu-id="dab9c-147">Un server [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) può supportare le proprietà di automazione interfaccia utente (ad esempio, LabeledBy e IsRequiredForForm) implementando [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) e fornendo un intero PROPERTYID che identifica la proprietà come parametro.</span><span class="sxs-lookup"><span data-stu-id="dab9c-147">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server can support UI Automation properties (such as LabeledBy, and IsRequiredForForm) by implementing [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) and supplying an integer PROPERTYID identifying the property as a parameter.</span></span> <span data-ttu-id="dab9c-148">Questa tecnica si applica solo alle proprietà di automazione interfaccia utente che non sono incluse in un'interfaccia del pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="dab9c-148">This technique applies only to UI Automation properties that are not included in a control pattern interface.</span></span> <span data-ttu-id="dab9c-149">Le proprietà associate a un'interfaccia del pattern di controllo sono esposte tramite il metodo di interfaccia del pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="dab9c-149">Properties associated with a control pattern interface are exposed through the control pattern interface method.</span></span> <span data-ttu-id="dab9c-150">Ad esempio, la proprietà IsSelected del pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) verrebbe esposta con [**ISelectionItemProvider:: Get \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span><span class="sxs-lookup"><span data-stu-id="dab9c-150">For example, the IsSelected property from the [SelectionItem](uiauto-implementingselectionitem.md) control pattern would be exposed with [**ISelectionItemProvider::get\_IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span></span>

 

 