---
title: Ospitare un controllo ActiveX senza finestra di automazione interfaccia utente
description: Informazioni su come creare un contenitore di controlli in grado di ospitare controlli Microsoft ActiveX senza finestra che implementano l'automazione interfaccia utente Microsoft.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- Automazione interfaccia utente, controllo ActiveX senza finestra
- Controllo ActiveX senza finestra, automazione interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337679"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a><span data-ttu-id="605a7-105">Ospitare un controllo ActiveX senza finestra di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="605a7-105">Host a UI Automation Windowless ActiveX Control</span></span>

<span data-ttu-id="605a7-106">Informazioni su come creare un contenitore di controlli in grado di ospitare controlli Microsoft ActiveX senza finestra che implementano l'automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="605a7-106">Learn how to create a control container that can host windowless Microsoft ActiveX controls that implement Microsoft UI Automation.</span></span> <span data-ttu-id="605a7-107">Utilizzando la procedura descritta in questo articolo, è possibile verificare che tutti i controlli senza finestra di automazione interfaccia utente ospitati nel contenitore di controllo siano accessibili alle applicazioni client per l'accessibilità.</span><span class="sxs-lookup"><span data-stu-id="605a7-107">By using the steps described here, you can ensure that any UI Automation windowless controls that are hosted in your control container are accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="605a7-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="605a7-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="605a7-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="605a7-109">Technologies</span></span>

-   [<span data-ttu-id="605a7-110">Controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="605a7-110">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="605a7-111">Automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="605a7-111">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="605a7-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="605a7-112">Prerequisites</span></span>

-   <span data-ttu-id="605a7-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="605a7-113">C/C++</span></span>
-   <span data-ttu-id="605a7-114">Programmazione Microsoft Win32 e Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="605a7-114">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="605a7-115">Controlli ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="605a7-115">Windowless ActiveX controls</span></span>
-   <span data-ttu-id="605a7-116">Provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="605a7-116">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="605a7-117">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="605a7-117">Instructions</span></span>

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a><span data-ttu-id="605a7-118">Passaggio 1: fornire l'interfaccia IRawElementProviderSimple per conto del controllo privo di finestra.</span><span class="sxs-lookup"><span data-stu-id="605a7-118">Step 1: Provide the IRawElementProviderSimple interface on behalf of the windowless control.</span></span>

<span data-ttu-id="605a7-119">Quando il sistema richiede il puntatore [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per la radice di un controllo senza finestra, il sistema esegue una query sul contenitore di controlli.</span><span class="sxs-lookup"><span data-stu-id="605a7-119">Whenever the system needs the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer for the root of a windowless control, the system queries the control container.</span></span> <span data-ttu-id="605a7-120">Per recuperare il puntatore, il contenitore chiama l'implementazione del controllo senza finestra del metodo [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="605a7-120">To retrieve the pointer, the container calls the windowless control's implementation of the [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>

<span data-ttu-id="605a7-121">Se il contenitore di controlli ha un'implementazione di automazione interfaccia utente, può restituire il puntatore [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del controllo senza finestra al sistema.</span><span class="sxs-lookup"><span data-stu-id="605a7-121">If the control container has a UI Automation implementation, it can return the windowless control's [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer to the system.</span></span>

<span data-ttu-id="605a7-122">Se il contenitore di controlli ha un'implementazione di Microsoft Active Accessibility, chiamare la funzione [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) per ottenere un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) che rappresenta il controllo, quindi restituire il puntatore di interfaccia **IAccessible** al sistema.</span><span class="sxs-lookup"><span data-stu-id="605a7-122">If the control container has a Microsoft Active Accessibility implementation, call the [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) function to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer that represents the control, and then return the **IAccessible** interface pointer to the system.</span></span>

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a><span data-ttu-id="605a7-123">Passaggio 2: implementare l'interfaccia IRawElementProviderWindowlessSite.</span><span class="sxs-lookup"><span data-stu-id="605a7-123">Step 2: Implement the IRawElementProviderWindowlessSite interface.</span></span>

<span data-ttu-id="605a7-124">Un contenitore di controlli implementa l'interfaccia [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) Abilita un controllo senza finestra basato sull'automazione dell'interfaccia utente per comunicare le informazioni di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="605a7-124">A control container implements the [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) interface enable a windowless control that is based on UI Automation to communicate its accessibility information.</span></span>

1.  <span data-ttu-id="605a7-125">Implementare [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span><span class="sxs-lookup"><span data-stu-id="605a7-125">Implement [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span></span>

    <span data-ttu-id="605a7-126">Un frammento di controllo senza finestra deve creare un ID Runtime univoco per se stesso.</span><span class="sxs-lookup"><span data-stu-id="605a7-126">A windowless control fragment must create a unique runtime ID for itself.</span></span> <span data-ttu-id="605a7-127">Per creare il relativo ID di runtime, un frammento di controllo senza finestra Recupera un valore di prefisso chiamando il metodo [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) del sito del controllo e quindi aggiunge al prefisso un valore integer univoco rispetto a tutti gli altri frammenti nel controllo senza finestra.</span><span class="sxs-lookup"><span data-stu-id="605a7-127">To create its runtime ID, a windowless control fragment retrieves a prefix value by calling the control site's [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method, and then appends to the prefix an integer value that is unique relative to all other fragments in the windowless control.</span></span>

    <span data-ttu-id="605a7-128">Il sito di controllo per un controllo senza finestra deve implementare il metodo [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) formando un **SAFEARRAY** che contiene la costante **UiaAppendRuntimeId**, seguito da un valore integer univoco per il sito.</span><span class="sxs-lookup"><span data-stu-id="605a7-128">The control site for a windowless control should implement the [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method by forming a **SAFEARRAY** that contains the constant **UiaAppendRuntimeId**, followed by an integer value that is unique to the site.</span></span>

    <span data-ttu-id="605a7-129">Questo esempio Mostra come restituire un prefisso dell'ID di runtime per un controllo senza finestra.</span><span class="sxs-lookup"><span data-stu-id="605a7-129">This example shows how to return a runtime ID prefix for a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  <span data-ttu-id="605a7-130">Implementare il metodo [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .</span><span class="sxs-lookup"><span data-stu-id="605a7-130">Implement the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method.</span></span>

    <span data-ttu-id="605a7-131">Un controllo che implementa l'automazione dell'interfaccia utente deve restituire un puntatore al provider di frammenti padre del controllo.</span><span class="sxs-lookup"><span data-stu-id="605a7-131">A control that implements UI Automation must return a pointer to the control's parent fragment provider.</span></span>

    <span data-ttu-id="605a7-132">Per restituire l'elemento padre del frammento, un oggetto che implementa l'interfaccia [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) deve essere in grado di implementare il metodo [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="605a7-132">To return the parent of the fragment, an object that implements the [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) interface must be able to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span> <span data-ttu-id="605a7-133">L'implementazione di **Navigate** è difficile per un controllo senza finestra perché il controllo potrebbe non essere in grado di determinarne la posizione nell'albero accessibile dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="605a7-133">Implementing **Navigate** is difficult for a windowless control because the control might be unable to determine its location in the accessible tree of the parent object.</span></span> <span data-ttu-id="605a7-134">Il metodo [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) consente al controllo senza finestra di eseguire una query sul relativo sito per il frammento adiacente, quindi restituisce il frammento al client che ha chiamato **Navigate**.</span><span class="sxs-lookup"><span data-stu-id="605a7-134">The [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method enables the windowless control to query its site for the adjacent fragment, and then return that fragment to the client that called **Navigate**.</span></span>

    <span data-ttu-id="605a7-135">Questo esempio Mostra come un contenitore di controlli Recupera il frammento padre di un controllo senza finestra.</span><span class="sxs-lookup"><span data-stu-id="605a7-135">This example shows how a control container retrieves the parent fragment of a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a><span data-ttu-id="605a7-136">Passaggio 3: facoltativo: implementare l'interfaccia IRawElementProviderHostingAccessibles.</span><span class="sxs-lookup"><span data-stu-id="605a7-136">Step 3: Optional: Implement the IRawElementProviderHostingAccessibles interface.</span></span>

<span data-ttu-id="605a7-137">Implementare l'interfaccia [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) se il contenitore di controlli ha un'implementazione del provider di automazione interfaccia utente che è la radice di un albero di accessibilità che include controlli ActiveX senza finestra che supportano Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="605a7-137">Implement the [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) interface if your control container has a UI Automation provider implementation that is the root of an accessibility tree that includes windowless ActiveX controls that support Microsoft Active Accessibility.</span></span> <span data-ttu-id="605a7-138">L'interfaccia **IRawElementProviderHostingAccessibles** ha un singolo metodo, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), che recupera i puntatori dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di tutti i controlli ActiveX senza finestra basati su Microsoft Active Accessibility ospitati dal contenitore di controlli.</span><span class="sxs-lookup"><span data-stu-id="605a7-138">The **IRawElementProviderHostingAccessibles** interface has a single method, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), which retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers of all Microsoft Active Accessibility-based windowless ActiveX controls that are hosted by your control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="605a7-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="605a7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="605a7-140">Come ospitare un controllo ActiveX senza finestra MSAA</span><span class="sxs-lookup"><span data-stu-id="605a7-140">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[<span data-ttu-id="605a7-141">Accessibilità controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="605a7-141">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 