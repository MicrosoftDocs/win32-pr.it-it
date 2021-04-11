---
title: Messaggio WM_GETOBJECT (winuser. h)
description: Inviato da Microsoft Active Accessibility e dall'automazione interfaccia utente Microsoft per ottenere informazioni su un oggetto accessibile contenuto in un'applicazione server.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- Accessibilità Windows del messaggio WM_GETOBJECT
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121627"
---
# <a name="wm_getobject-message"></a><span data-ttu-id="97514-104">\_Messaggio WM GETobject</span><span class="sxs-lookup"><span data-stu-id="97514-104">WM\_GETOBJECT message</span></span>

<span data-ttu-id="97514-105">Inviato da Microsoft Active Accessibility e dall'automazione interfaccia utente Microsoft per ottenere informazioni su un oggetto accessibile contenuto in un'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="97514-105">Sent by both Microsoft Active Accessibility and Microsoft UI Automation to obtain information about an accessible object contained in a server application.</span></span>

<span data-ttu-id="97514-106">Le applicazioni non inviano mai direttamente questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="97514-106">Applications never send this message directly.</span></span> <span data-ttu-id="97514-107">Microsoft Active Accessibility Invia questo messaggio in risposta alle chiamate a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="97514-107">Microsoft Active Accessibility sends this message in response to calls to [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span> <span data-ttu-id="97514-108">Tuttavia, le applicazioni server gestiscono questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="97514-108">However, server applications handle this message.</span></span> <span data-ttu-id="97514-109">Automazione interfaccia utente invia questo messaggio in risposta alle chiamate a [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e quando gestisce gli eventi per i quali un client ha effettuato la registrazione.</span><span class="sxs-lookup"><span data-stu-id="97514-109">UI Automation sends this message in response to calls to [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which a client has registered.</span></span>


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a><span data-ttu-id="97514-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="97514-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97514-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="97514-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="97514-112">Fornisce informazioni aggiuntive sul messaggio e viene utilizzato solo dal sistema.</span><span class="sxs-lookup"><span data-stu-id="97514-112">Provides additional information about the message and is used only by the system.</span></span> <span data-ttu-id="97514-113">I server passano *dwFlags* come parametro *wParam* nella chiamata a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) durante la gestione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="97514-113">Servers pass *dwFlags* as the *wParam* parameter in the call to [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) when handling the message.</span></span>

</dd> <dt>

<span data-ttu-id="97514-114">*dwObjId*</span><span class="sxs-lookup"><span data-stu-id="97514-114">*dwObjId*</span></span> 
</dt> <dd>

<span data-ttu-id="97514-115">Identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="97514-115">Object identifier.</span></span> <span data-ttu-id="97514-116">Questo valore è una delle costanti [identificatore di oggetto](object-identifiers.md) o un identificatore di oggetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="97514-116">This value is one of the [object identifier](object-identifiers.md) constants or a custom object identifier.</span></span> <span data-ttu-id="97514-117">Un'applicazione server deve verificare questo valore per identificare il tipo di informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="97514-117">A server application must check this value to identify the type of information being requested.</span></span> <span data-ttu-id="97514-118">Prima di confrontare questo valore con i \_ valori ObjID, il server deve eseguire il cast a **DWORD**; in caso contrario, in Windows a 64 bit, l'estensione del segno di *lParam* può interferire con il confronto.</span><span class="sxs-lookup"><span data-stu-id="97514-118">Before comparing this value against the OBJID\_ values, the server must cast it to **DWORD**; otherwise, on 64-bit Windows, the sign extension of the *lParam* can interfere with the comparison.</span></span>

-   <span data-ttu-id="97514-119">Se *dwObjId* è uno dei valori di objid \_ , ad esempio [**objid \_ client**](object-identifiers.md), la richiesta è relativa a un oggetto Active Accessibility Microsoft che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="97514-119">If *dwObjId* is one of the OBJID\_ values such as [**OBJID\_CLIENT**](object-identifiers.md), the request is for a Microsoft Active Accessibility object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>
-   <span data-ttu-id="97514-120">Se *dwObjId* è uguale a **UiaRootObjectId**, la richiesta è per un provider di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="97514-120">If *dwObjId* is equal to **UiaRootObjectId**, the request is for a UI Automation provider.</span></span> <span data-ttu-id="97514-121">Se il server implementa l'automazione dell'interfaccia utente, deve restituire un provider utilizzando la funzione [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="97514-121">If the server is implementing UI Automation, it should return a provider using the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="97514-122">Se *dwObjId* è [**objid \_ NATIVEOM**](object-identifiers.md), la richiesta è per il modello a oggetti sottostante del controllo.</span><span class="sxs-lookup"><span data-stu-id="97514-122">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md), the request is for the control's underlying object model.</span></span> <span data-ttu-id="97514-123">Se il controllo supporta questa richiesta, deve restituire un'interfaccia COM appropriata chiamando la funzione [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="97514-123">If the control supports this request, it should return an appropriate COM interface by calling the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="97514-124">Se *dwObjId* è [**objid \_ QUERYCLASSNAMEIDX**](object-identifiers.md), la richiesta è che il controllo si identifichi come un controllo Windows standard o un controllo comune implementato dalla libreria di controlli comuni (ComCtrl.dll).</span><span class="sxs-lookup"><span data-stu-id="97514-124">If *dwObjId* is [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md), the request is for the control to identify itself as a standard Windows control or a common control implemented by the common control library (ComCtrl.dll).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97514-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97514-125">Return value</span></span>

<span data-ttu-id="97514-126">Se la finestra o il controllo non deve rispondere a questo messaggio, deve passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . in caso contrario, la finestra o il controllo deve restituire un valore che corrisponde alla richiesta specificata da *dwObjId*:</span><span class="sxs-lookup"><span data-stu-id="97514-126">If the window or control does not need to respond to this message, it should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function; otherwise, the window or control should return a value that corresponds to the request specified by *dwObjId*:</span></span>

-   <span data-ttu-id="97514-127">Se la finestra o il controllo implementa l'automazione dell'interfaccia utente, la finestra o il controllo deve restituire il valore ottenuto da una chiamata alla funzione [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="97514-127">If the window or control implements UI Automation, the window or control should return the value obtained by a call to the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="97514-128">Se *dwObjId* è [**objid \_ NATIVEOM**](object-identifiers.md) e la finestra espone un modello a oggetti nativo, Windows deve restituire il valore ottenuto da una chiamata alla funzione [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="97514-128">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md) and the window exposes a native Object Model, the windows should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="97514-129">Se *dwObjId* è [**objid \_ client**](object-identifiers.md) e la finestra implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la finestra deve restituire il valore ottenuto da una chiamata alla funzione [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="97514-129">If *dwObjId* is [**OBJID\_CLIENT**](object-identifiers.md) and the window implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), the window should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="97514-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="97514-130">Remarks</span></span>

<span data-ttu-id="97514-131">Quando un client chiama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o qualsiasi altra funzione **AccessibleObjectFrom**_X_ che recupera un'interfaccia a un oggetto, Microsoft Active ACCESSIBILITY invia il messaggio **WM \_ GetObject** alla routine della finestra appropriata all'interno dell'applicazione server appropriata.</span><span class="sxs-lookup"><span data-stu-id="97514-131">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other **AccessibleObjectFrom**_X_ functions that retrieve an interface to an object, Microsoft Active Accessibility sends the **WM\_GETOBJECT** message to the appropriate window procedure within the appropriate server application.</span></span> <span data-ttu-id="97514-132">Durante l'elaborazione di **WM \_ GetObject**, le applicazioni server chiamano [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) e usano il valore restituito di questa funzione come valore restituito per il messaggio.</span><span class="sxs-lookup"><span data-stu-id="97514-132">While processing **WM\_GETOBJECT**, server applications call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) and use the return value of this function as the return value for the message.</span></span> <span data-ttu-id="97514-133">Microsoft Active Accessibility, in combinazione con la libreria COM, esegue il marshalling appropriato e passa di nuovo il puntatore di interfaccia dal server al client.</span><span class="sxs-lookup"><span data-stu-id="97514-133">Microsoft Active Accessibility, in conjunction with the COM library, performs the appropriate marshaling and passes the interface pointer from the server back to the client.</span></span>

<span data-ttu-id="97514-134">I server non rispondono a **WM \_ GetObject** prima che l'oggetto venga inizializzato completamente o dopo l'inizio della chiusura.</span><span class="sxs-lookup"><span data-stu-id="97514-134">Servers do not respond to **WM\_GETOBJECT** before the object is fully initialized or after it begins to close down.</span></span> <span data-ttu-id="97514-135">Quando un'applicazione crea una nuova finestra, il sistema invia [**l' \_ oggetto evento \_ creato**](event-constants.md) per notificare ai client prima di inviare il messaggio [WM \_ create](../winmsg/wm-create.md) alla routine della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97514-135">When an application creates a new window, the system sends [**EVENT\_OBJECT\_CREATE**](event-constants.md) to notify clients before it sends the [WM\_CREATE](../winmsg/wm-create.md) message to the application's window procedure.</span></span> <span data-ttu-id="97514-136">Poiché molte applicazioni usano WM \_ create per avviare il processo di inizializzazione, i server non rispondono al messaggio **WM \_ GetObject** fino al termine dell'elaborazione del messaggio **WM \_ create** .</span><span class="sxs-lookup"><span data-stu-id="97514-136">Because many applications use WM\_CREATE to start their initialization process, servers do not respond to the **WM\_GETOBJECT** message until finished processing the **WM\_CREATE** message.</span></span>

<span data-ttu-id="97514-137">Un server usa **WM \_ GetObject** per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="97514-137">A server uses **WM\_GETOBJECT** to perform the following tasks:</span></span>

-   [<span data-ttu-id="97514-138">Creare nuovi oggetti accessibili</span><span class="sxs-lookup"><span data-stu-id="97514-138">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="97514-139">Riutilizza puntatori esistenti a oggetti</span><span class="sxs-lookup"><span data-stu-id="97514-139">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="97514-140">Crea nuove interfacce per lo stesso oggetto</span><span class="sxs-lookup"><span data-stu-id="97514-140">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

<span data-ttu-id="97514-141">Per i client, ciò significa che potrebbero ricevere puntatori di interfaccia distinti per lo stesso elemento dell'interfaccia utente, a seconda dell'azione del server.</span><span class="sxs-lookup"><span data-stu-id="97514-141">For clients, this means that they might receive distinct interface pointers for the same user interface element, depending on the server's action.</span></span> <span data-ttu-id="97514-142">Per determinare se due puntatori di interfaccia puntano allo stesso elemento dell'interfaccia utente, i client confrontano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="97514-142">To determine if two interface pointers point to the same user interface element, clients compare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties of the object.</span></span> <span data-ttu-id="97514-143">Il confronto tra puntatori non funziona.</span><span class="sxs-lookup"><span data-stu-id="97514-143">Comparing pointers does not work.</span></span>

## <a name="requirements"></a><span data-ttu-id="97514-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97514-144">Requirements</span></span>



| <span data-ttu-id="97514-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="97514-145">Requirement</span></span> | <span data-ttu-id="97514-146">Valore</span><span class="sxs-lookup"><span data-stu-id="97514-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97514-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97514-147">Minimum supported client</span></span><br/> | <span data-ttu-id="97514-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97514-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="97514-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97514-149">Minimum supported server</span></span><br/> | <span data-ttu-id="97514-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97514-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97514-151">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="97514-151">Redistributable</span></span><br/>          | <span data-ttu-id="97514-152">Active Accessibility 1,3 RDK in Windows NT 4,0 con SP6 e versioni successive e Windows 95</span><span class="sxs-lookup"><span data-stu-id="97514-152">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>              |
| <span data-ttu-id="97514-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97514-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="97514-154"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97514-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97514-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97514-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97514-156">Come gestire WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="97514-156">How to Handle WM\_GETOBJECT</span></span>](how-to-handle-wm-getobject.md)
</dt> <dt>

[<span data-ttu-id="97514-157">Funzionamento di WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="97514-157">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
</dt> <dt>

[<span data-ttu-id="97514-158">**LresultFromObject**</span><span class="sxs-lookup"><span data-stu-id="97514-158">**LresultFromObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

