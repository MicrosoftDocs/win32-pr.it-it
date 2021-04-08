---
title: Come usare l'automazione dell'interfaccia utente per rendere accessibile un controllo ActiveX senza finestra
description: Viene descritto come usare l'automazione interfaccia utente Microsoft \ 32; API per garantire che il controllo Microsoft ActiveX senza finestra sia accessibile per le applicazioni client di Assistive Technology (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Controllo ActiveX senza finestra, accessibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ada1d26463b0654c1808f6e4fd43f571687d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728418"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="9c6f8-104">Come usare l'automazione dell'interfaccia utente per rendere accessibile un controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="9c6f8-104">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>

<span data-ttu-id="9c6f8-105">Viene descritto come utilizzare l'API di automazione interfaccia utente Microsoft per assicurarsi che il controllo Microsoft ActiveX senza finestra sia accessibile per le applicazioni client di Assistive Technology (AT).</span><span class="sxs-lookup"><span data-stu-id="9c6f8-105">Describes how to use the Microsoft UI Automation API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9c6f8-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="9c6f8-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9c6f8-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="9c6f8-107">Technologies</span></span>

-   [<span data-ttu-id="9c6f8-108">Controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="9c6f8-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="9c6f8-109">Automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9c6f8-109">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="9c6f8-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9c6f8-110">Prerequisites</span></span>

-   <span data-ttu-id="9c6f8-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="9c6f8-111">C/C++</span></span>
-   <span data-ttu-id="9c6f8-112">Programmazione Microsoft Win32 e Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="9c6f8-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="9c6f8-113">Controlli ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="9c6f8-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="9c6f8-114">Provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9c6f8-114">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="9c6f8-115">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="9c6f8-115">Instructions</span></span>

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a><span data-ttu-id="9c6f8-116">Passaggio 1: implementare le interfacce del provider di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-116">Step 1: Implement the UI Automation provider interfaces.</span></span>

<span data-ttu-id="9c6f8-117">Per rendere accessibile l'applicazione, è necessario implementare le interfacce del provider di automazione interfaccia utente per il controllo ActiveX senza finestra, tra cui [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)e [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span><span class="sxs-lookup"><span data-stu-id="9c6f8-117">To make your application accessible, you must implement the UI Automation provider interfaces for your windowless ActiveX control, including [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), and [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span></span> <span data-ttu-id="9c6f8-118">È necessario implementare queste interfacce esattamente come per un controllo basato su finestra, tranne come descritto nei passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-118">You should implement these interfaces just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="9c6f8-119">Per ulteriori informazioni sull'implementazione delle interfacce del provider UIA, vedere [UI Automation provider Programmer ' s Guide](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="9c6f8-119">For more information about implementing UIA provider interfaces, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="9c6f8-120">Passaggio 2: implementare l'interfaccia IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-120">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="9c6f8-121">Quando un client richiede informazioni sull'accessibilità sul controllo senza finestra, il contenitore di controlli chiama il metodo **IServiceProvider:: QueryService** del controllo per recuperare il puntatore all'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per il controllo.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-121">When a client needs accessibility information about your windowless control, the control container calls your control's **IServiceProvider::QueryService** method to retrieve the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface pointer for your control.</span></span>

<span data-ttu-id="9c6f8-122">Nell'esempio seguente viene illustrato come implementare il metodo **QueryService** .</span><span class="sxs-lookup"><span data-stu-id="9c6f8-122">The following example shows how to implement the **QueryService** method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a><span data-ttu-id="9c6f8-123">Passaggio 3: implementare il Metodo IRawElementProviderFragment:: Navigate.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-123">Step 3: Implement the IRawElementProviderFragment::Navigate method.</span></span>

<span data-ttu-id="9c6f8-124">Quando il metodo [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) del controllo senza finestra viene chiamato per passare al padre o a un elemento di pari livello del provider radice del controllo senza finestra, il metodo **Navigate** deve delegare al metodo [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) del contenitore di controlli.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-124">When your windowless control’s [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method is called to navigate to the parent or a sibling of the windowless control's root provider, your **Navigate** method should delegate to the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method of the control container.</span></span>

<span data-ttu-id="9c6f8-125">Nell'esempio seguente viene illustrato come implementare il metodo [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="9c6f8-125">The following example shows how to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a><span data-ttu-id="9c6f8-126">Passaggio 4: implementare il Metodo IRawElementProviderFragment:: GetRuntimeId.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-126">Step 4: Implement the IRawElementProviderFragment::GetRuntimeId method.</span></span>

<span data-ttu-id="9c6f8-127">Quando il controllo senza finestra riceve una chiamata al metodo [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , il controllo deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c6f8-127">When your windowless control receives a call to its [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) method, the control must do the following:</span></span>

1.  <span data-ttu-id="9c6f8-128">Recuperare un prefisso dell'ID di runtime chiamando il metodo [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) del sito del controllo.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-128">Retrieve a runtime ID prefix by calling the control site's [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>
2.  <span data-ttu-id="9c6f8-129">Creare un ID di runtime univoco per il controllo aggiungendo un intero al prefisso dell'ID di Runtime.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-129">Create a unique runtime ID for the control by appending an integer to the runtime ID prefix.</span></span>
3.  <span data-ttu-id="9c6f8-130">Restituisce l'ID di runtime al chiamante.</span><span class="sxs-lookup"><span data-stu-id="9c6f8-130">Return the runtime ID to the caller.</span></span>

<span data-ttu-id="9c6f8-131">Nell'esempio seguente viene illustrato come implementare il metodo [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .</span><span class="sxs-lookup"><span data-stu-id="9c6f8-131">The following example shows how to implement the [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a><span data-ttu-id="9c6f8-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c6f8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c6f8-133">Usare MSAA per rendere accessibile un controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="9c6f8-133">Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="9c6f8-134">Accessibilità controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="9c6f8-134">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 