---
title: Usare MSAA per rendere accessibile un controllo ActiveX senza finestra
description: Viene descritto come utilizzare Microsoft Active Accessibility \ 32; API per garantire che il controllo Microsoft ActiveX senza finestra sia accessibile per le applicazioni client di Assistive Technology (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- Controllo ActiveX, accessibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300182"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="75d36-104">Usare MSAA per rendere accessibile un controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="75d36-104">Use MSAA to make a windowless ActiveX control accessible</span></span>

<span data-ttu-id="75d36-105">Viene descritto come utilizzare l'API Microsoft Active Accessibility per garantire che il controllo Microsoft ActiveX senza finestra sia accessibile alle applicazioni client per la tecnologia assistive (AT).</span><span class="sxs-lookup"><span data-stu-id="75d36-105">Describes how to use the Microsoft Active Accessibility API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="75d36-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="75d36-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="75d36-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="75d36-107">Technologies</span></span>

-   [<span data-ttu-id="75d36-108">Controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="75d36-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="75d36-109">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="75d36-109">Microsoft Active Accessibility</span></span>](microsoft-active-accessibility.md)

### <a name="prerequisites"></a><span data-ttu-id="75d36-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="75d36-110">Prerequisites</span></span>

-   <span data-ttu-id="75d36-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="75d36-111">C/C++</span></span>
-   <span data-ttu-id="75d36-112">Programmazione Microsoft Win32 e Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="75d36-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="75d36-113">Controlli ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="75d36-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="75d36-114">Server Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="75d36-114">Microsoft Active Accessibility servers</span></span>

## <a name="instructions"></a><span data-ttu-id="75d36-115">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="75d36-115">Instructions</span></span>

### <a name="step-1-implement-the-iaccessible-interface"></a><span data-ttu-id="75d36-116">Passaggio 1: implementare l'interfaccia IAccessible.</span><span class="sxs-lookup"><span data-stu-id="75d36-116">Step 1: Implement the IAccessible interface.</span></span>

<span data-ttu-id="75d36-117">Per rendere accessibile il controllo ActiveX senza finestra, è necessario implementare l'interfaccia Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , come per un controllo basato su finestra, eccetto come descritto nei passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="75d36-117">To make your windowless ActiveX control accessible, you must implement the Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="75d36-118">Per ulteriori informazioni sull'implementazione di **IAccessible**, vedere [la guida per gli sviluppatori di Active Accessibility server](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="75d36-118">For more information about implementing **IAccessible**, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="75d36-119">Passaggio 2: implementare l'interfaccia IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="75d36-119">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="75d36-120">Quando un client richiede informazioni di accessibilità sul controllo senza finestra, il contenitore chiama il metodo [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) del controllo per recuperare il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="75d36-120">When a client requests accessibility information about your windowless control, the container calls your control's [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method to retrieve the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="75d36-121">Questo esempio illustra come implementare il metodo [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="75d36-121">This example shows how to implement the [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a><span data-ttu-id="75d36-122">Passaggio 3: delegare \_ le chiamate al metodo IAccessible:: get accParent al metodo IAccessibleWindowlessSite:: GetParentAccessible del sito del controllo.</span><span class="sxs-lookup"><span data-stu-id="75d36-122">Step 3: Delegate IAccessible::get\_accParent method calls to the control site's IAccessibleWindowlessSite::GetParentAccessible method.</span></span>

<span data-ttu-id="75d36-123">Quando un client richiede l'oggetto padre del controllo senza finestra, il contenitore chiama il metodo [**IAccessible:: Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del controllo.</span><span class="sxs-lookup"><span data-stu-id="75d36-123">When a client requests the parent object of your windowless control, the container calls your control's [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span> <span data-ttu-id="75d36-124">L'implementazione di **get \_ accParent** deve delegare al metodo [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="75d36-124">Your **get\_accParent** implementation should delegate to the [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method of the container.</span></span>

<span data-ttu-id="75d36-125">Questo esempio illustra come implementare il metodo [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .</span><span class="sxs-lookup"><span data-stu-id="75d36-125">This example shows how to implement the [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span>


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a><span data-ttu-id="75d36-126">Passaggio 4: acquisire un intervallo di ID oggetto da assegnare alle origini eventi nel controllo privo di finestra.</span><span class="sxs-lookup"><span data-stu-id="75d36-126">Step 4: Acquire a range of object IDs to assign to the event sources in your windowless control.</span></span>

<span data-ttu-id="75d36-127">Analogamente ai controlli basati su finestra, un controllo ActiveX senza finestra chiama la funzione [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per notificare ai client eventi importanti.</span><span class="sxs-lookup"><span data-stu-id="75d36-127">Like window-based controls, a windowless ActiveX control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function to notify clients of important events.</span></span> <span data-ttu-id="75d36-128">I parametri della funzione includono l'ID oggetto dell'elemento che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="75d36-128">The function parameters include the object ID of the item that is raising the event.</span></span> <span data-ttu-id="75d36-129">Il controllo senza finestra deve assegnare gli ID oggetto usando un valore di un intervallo acquisito chiamando il metodo [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) del sito del controllo.</span><span class="sxs-lookup"><span data-stu-id="75d36-129">Your windowless control must assign object IDs by using a value from a range acquired by calling the control site’s [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) method.</span></span>

<span data-ttu-id="75d36-130">Questo esempio illustra come acquisire un intervallo di valori ID oggetto dal contenitore di controlli.</span><span class="sxs-lookup"><span data-stu-id="75d36-130">This example shows how to acquire a range of object ID values from the control container.</span></span>


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a><span data-ttu-id="75d36-131">Passaggio 5: implementare l'interfaccia IAccessibleHandler.</span><span class="sxs-lookup"><span data-stu-id="75d36-131">Step 5: Implement the IAccessibleHandler interface.</span></span>

<span data-ttu-id="75d36-132">Quando un controllo senza finestra chiama la funzione [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , il controllo specifica l'ID oggetto dell'elemento dell'interfaccia utente che genera l'evento e specifica il contenitore di controlli come finestra che risponderà ai messaggi [**WM \_ GetObject**](wm-getobject.md) per conto del controllo.</span><span class="sxs-lookup"><span data-stu-id="75d36-132">When a windowless control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function, the control specifies the object ID of the UI item that is raising the event, and specifies the control container as the window that will respond to [**WM\_GETOBJECT**](wm-getobject.md) messages on behalf of the control.</span></span>

<span data-ttu-id="75d36-133">Se un'applicazione client risponde all'evento, il contenitore di controlli riceve un messaggio [**WM \_ GetObject**](wm-getobject.md) che include l'ID oggetto dell'elemento dell'interfaccia utente che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="75d36-133">If a client application responds to the event, the control container receives a [**WM\_GETOBJECT**](wm-getobject.md) message that includes the object ID of the UI item that raised the event.</span></span> <span data-ttu-id="75d36-134">Il contenitore di controlli risponde cercando il controllo senza finestra che "possiede" l'ID oggetto, quindi chiamando il metodo [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) del controllo.</span><span class="sxs-lookup"><span data-stu-id="75d36-134">The control container responds by looking up the windowless control that "owns" the object ID, and then calling that control's [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) method.</span></span> <span data-ttu-id="75d36-135">Il metodo **AccessibleObjectFromID** restituisce il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento dell'interfaccia utente e il contenitore di controlli lo trasmette all'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="75d36-135">The **AccessibleObjectFromID** method returns the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the UI item, and the control container forwards the pointer to the client application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75d36-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75d36-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75d36-137">Usare l'automazione dell'interfaccia utente per rendere accessibile un controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="75d36-137">Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="75d36-138">Accessibilità controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="75d36-138">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 