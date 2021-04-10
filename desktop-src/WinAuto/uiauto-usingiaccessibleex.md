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
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a><span data-ttu-id="fd1c7-115">Aggiunta della funzionalità di automazione interfaccia utente ai server Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="fd1c7-115">Adding UI Automation Functionality to Active Accessibility Servers</span></span>

<span data-ttu-id="fd1c7-116">I controlli che non dispongono di un provider di automazione interfaccia utente Microsoft ma che implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) possono essere facilmente aggiornati per fornire alcune funzionalità di automazione interfaccia utente, implementando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="fd1c7-116">Controls that do not have a Microsoft UI Automation provider but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) can easily be upgraded to provide some UI Automation functionality, by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="fd1c7-117">Questa interfaccia consente al controllo di esporre le proprietà e i pattern di controllo di automazione interfaccia utente senza la necessità di un'implementazione completa delle interfacce del provider di automazione interfaccia utente, ad esempio [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="fd1c7-117">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="fd1c7-118">Per implementare **IAccessibleEx**, la gerarchia di oggetti Microsoft Active Accessibility di base non deve contenere errori o incoerenze (ad esempio un oggetto figlio il cui oggetto padre non lo elenca come figlio) e non deve essere in conflitto con le specifiche di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-118">To implement **IAccessibleEx**, the baseline Microsoft Active Accessibility object hierarchy must contain no errors or inconsistencies (such as a child object whose parent object does not list it as a child), and must not conflict with UI Automation specifications.</span></span> <span data-ttu-id="fd1c7-119">Se la gerarchia di oggetti di Microsoft Active Accessibility soddisfa questi requisiti, è un buon candidato per l'aggiunta di funzionalità tramite **IAccessibleEx**; in caso contrario, è necessario implementare l'automazione dell'interfaccia utente autonomamente o insieme all'implementazione di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-119">If the Microsoft Active Accessibility object hierarchy meets these requirements, it is a good candidate for adding functionality by using **IAccessibleEx**; otherwise, you must implement UI Automation alone or alongside the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="fd1c7-120">Prendere il caso di un controllo personalizzato con un valore di intervallo.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-120">Take the case of a custom control that has a range value.</span></span> <span data-ttu-id="fd1c7-121">Il server Microsoft Active Accessibility per il controllo definisce il proprio ruolo ed è in grado di restituire il valore corrente, ma non ha i mezzi per restituire i valori minimo e massimo del controllo, perché queste proprietà non sono definite in Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-121">The Microsoft Active Accessibility server for the control defines its role, and is able to return its current value, but lacks the means to return the minimum and maximum values of the control, because these properties are not defined in Microsoft Active Accessibility.</span></span> <span data-ttu-id="fd1c7-122">Un client di automazione interfaccia utente è in grado di recuperare il ruolo del controllo, il valore corrente e altre proprietà di Active Accessibility Microsoft, perché il nucleo di automazione interfaccia utente può ottenere tali proprietà tramite [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="fd1c7-122">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="fd1c7-123">Tuttavia, senza l'accesso a un'interfaccia [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sull'oggetto, l'automazione dell'interfaccia utente non è in grado di recuperare i valori massimi e minimi.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-123">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="fd1c7-124">Lo sviluppatore del controllo può fornire un provider di automazione interfaccia utente completo per il controllo, ma ciò comporta la duplicazione di gran parte delle funzionalità esistenti dell'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , ad esempio la navigazione e le proprietà comuni.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-124">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="fd1c7-125">Lo sviluppatore può invece continuare a basarsi su **IAccessible** per fornire questa funzionalità, aggiungendo il supporto per le proprietà specifiche del controllo tramite [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="fd1c7-125">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

<span data-ttu-id="fd1c7-126">Per aggiornare il controllo personalizzato sono necessari i passaggi principali seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd1c7-126">Updating the custom control requires these main steps:</span></span>

-   <span data-ttu-id="fd1c7-127">Implementare [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) sull'oggetto accessibile in modo che l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) possa trovarsi in questo oggetto o in un oggetto separato.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-127">Implement [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="fd1c7-128">Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sull'oggetto accessibile.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-128">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="fd1c7-129">Creare oggetti distinti accessibili per tutti gli elementi figlio di Microsoft Active Accessibility, che in Microsoft Active Accessibility potrebbero essere stati rappresentati dall'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nell'oggetto padre (ad esempio, gli elementi dell'elenco).</span><span class="sxs-lookup"><span data-stu-id="fd1c7-129">Create distinct accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility might have been represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="fd1c7-130">Implementare [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) su questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-130">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="fd1c7-131">Implementare [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) in tutti gli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-131">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="fd1c7-132">Implementare le interfacce del pattern di controllo appropriate sugli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-132">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

<span data-ttu-id="fd1c7-133">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-133">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fd1c7-134">Esposizione di IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="fd1c7-134">Exposing IAccessibleEx</span></span>](#exposing-iaccessibleex)
-   [<span data-ttu-id="fd1c7-135">Implementazione di IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="fd1c7-135">Implementing IAccessibleEx</span></span>](#implementing-iaccessibleex)
-   [<span data-ttu-id="fd1c7-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd1c7-136">Related topics</span></span>](#related-topics)

## <a name="exposing-iaccessibleex"></a><span data-ttu-id="fd1c7-137">Esposizione di IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="fd1c7-137">Exposing IAccessibleEx</span></span>

<span data-ttu-id="fd1c7-138">Poiché l'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per un controllo può trovarsi in un oggetto separato, le applicazioni client non possono basarsi su [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-138">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="fd1c7-139">Al contrario, si prevede che i client chiamino [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fd1c7-139">Instead, clients are expected to call [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span></span> <span data-ttu-id="fd1c7-140">Nell'implementazione di questo metodo dell'esempio seguente si presuppone che **IAccessibleEx** non sia implementato su un oggetto separato. il metodo chiama quindi semplicemente per **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-140">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


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



## <a name="implementing-iaccessibleex"></a><span data-ttu-id="fd1c7-141">Implementazione di IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="fd1c7-141">Implementing IAccessibleEx</span></span>

<span data-ttu-id="fd1c7-142">Il metodo di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) di maggiore interesse è [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span><span class="sxs-lookup"><span data-stu-id="fd1c7-142">The method of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) that is of most interest is [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span></span> <span data-ttu-id="fd1c7-143">Questo metodo fornisce al server Microsoft Active Accessibility la possibilità di creare un oggetto accessibile (uno che espone, come minimo, **IAccessibleEx**) per un elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-143">This method gives the Microsoft Active Accessibility server an opportunity to create an accessible object (one that exposes, at a minimum, **IAccessibleEx**) for a child item.</span></span> <span data-ttu-id="fd1c7-144">In Microsoft Active Accessibility gli elementi figlio non sono in genere rappresentati come oggetti accessibili, ma come elementi figlio di un oggetto accessibile.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-144">In Microsoft Active Accessibility, child items typically are not represented as accessible objects but as children of an accessible object.</span></span> <span data-ttu-id="fd1c7-145">Tuttavia, poiché l'automazione dell'interfaccia utente richiede che ogni elemento sia rappresentato da un oggetto accessibile separato, **GetObjectForChild** deve creare un oggetto separato per ogni elemento figlio su richiesta.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-145">However, because UI Automation requires that each element be represented by a separate accessible object, **GetObjectForChild** must create a separate object for each child on demand.</span></span>

<span data-ttu-id="fd1c7-146">Nell'implementazione di esempio seguente viene restituito un oggetto accessibile per un elemento in una visualizzazione elenco personalizzata.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-146">The following example implementation returns an accessible object for an item in a custom list view.</span></span>


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



<span data-ttu-id="fd1c7-147">Per un'implementazione di esempio completa, vedere [rendere accessibili i controlli personalizzati, parte 5: uso di IAccessibleEx per aggiungere il supporto di automazione interfaccia utente a un controllo personalizzato](/previous-versions/msdn10/cc307850(v=msdn.10)) in MSDN.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-147">For a complete sample implementation, see [Making Custom Controls Accessible, Part 5: Using IAccessibleEx to Add UI Automation Support to a Custom Control](/previous-versions/msdn10/cc307850(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd1c7-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd1c7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd1c7-149">Guida per programmatori del provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fd1c7-149">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 