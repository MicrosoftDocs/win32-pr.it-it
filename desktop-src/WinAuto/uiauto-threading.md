---
title: Informazioni sui problemi di threading
description: Questo argomento descrive gli scenari di threading comuni per le implementazioni client di automazione interfaccia utente Microsoft e spiega come evitare i problemi che possono verificarsi se un client usa il threading in modo errato.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- client, problemi di threading di automazione interfaccia utente
- client, problemi di threading
- client, modello di threading del gestore eventi
- client, modello di threading del gestore eventi di automazione interfaccia utente
- client, affinità di automazione interfaccia utente
- client, affinità
- Automazione interfaccia utente, problemi di threading
- Automazione interfaccia utente, modello di threading del gestore eventi
- Automazione interfaccia utente, affinità
- problemi relativi al threading
- modello di threading del gestore eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046797"
---
# <a name="understanding-threading-issues"></a><span data-ttu-id="fbe09-114">Informazioni sui problemi di threading</span><span class="sxs-lookup"><span data-stu-id="fbe09-114">Understanding Threading Issues</span></span>

<span data-ttu-id="fbe09-115">Questo argomento descrive gli scenari di threading comuni per le implementazioni client di automazione interfaccia utente Microsoft e spiega come evitare i problemi che possono verificarsi se un client usa il threading in modo errato.</span><span class="sxs-lookup"><span data-stu-id="fbe09-115">This topic describes common threading scenarios for Microsoft UI Automation client implementations and explains how to avoid problems that can occur if a client uses threading incorrectly.</span></span>

<span data-ttu-id="fbe09-116">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fbe09-116">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="fbe09-117">Automazione interfaccia utente e thread UI</span><span class="sxs-lookup"><span data-stu-id="fbe09-117">UI Automation and the UI Thread</span></span>](#ui-automation-and-the-ui-thread)
-   [<span data-ttu-id="fbe09-118">Modello di threading per i gestori eventi</span><span class="sxs-lookup"><span data-stu-id="fbe09-118">Threading Model for Event Handlers</span></span>](#threading-model-for-event-handlers)
-   [<span data-ttu-id="fbe09-119">Affinità di apartment COM in Windows a 64 bit</span><span class="sxs-lookup"><span data-stu-id="fbe09-119">COM Apartment Affinity on 64-bit Windows</span></span>](#com-apartment-affinity-on-64-bit-windows)
-   [<span data-ttu-id="fbe09-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fbe09-120">Related topics</span></span>](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a><span data-ttu-id="fbe09-121">Automazione interfaccia utente e thread UI</span><span class="sxs-lookup"><span data-stu-id="fbe09-121">UI Automation and the UI Thread</span></span>

<span data-ttu-id="fbe09-122">A causa del modo in cui automazione interfaccia utente usa i messaggi di Windows, i conflitti possono verificarsi quando un'applicazione client tenta di interagire con la propria interfaccia utente nel thread dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fbe09-122">Because of the way UI Automation uses Windows messages, conflicts can occur when a client application attempts to interact with its own UI on the UI thread.</span></span> <span data-ttu-id="fbe09-123">Questi conflitti possono comportare prestazioni molto lente o addirittura causare l'interruzione della risposta da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fbe09-123">These conflicts can lead to very slow performance, or even cause the application to stop responding.</span></span>

<span data-ttu-id="fbe09-124">Se l'applicazione client è progettata per interagire con tutti gli elementi sul desktop, inclusa la propria interfaccia utente, è necessario effettuare tutte le chiamate di automazione interfaccia utente da un thread separato.</span><span class="sxs-lookup"><span data-stu-id="fbe09-124">If your client application is intended to interact with all elements on the desktop, including its own UI, you should make all UI Automation calls from a separate thread.</span></span> <span data-ttu-id="fbe09-125">Ciò include l'individuazione di elementi, ad esempio, tramite [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) o il metodo [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) e l'uso dei pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="fbe09-125">This includes locating elements, for example, by using [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) or the [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) method and using control patterns.</span></span> <span data-ttu-id="fbe09-126">Questo thread non deve essere proprietario di alcuna finestra e deve essere un thread del modello di Component Object Model (COM) multithreading Apartment (MTA) (uno che inizializza COM chiamando [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con il flag **COinit \_ multithreading** ).</span><span class="sxs-lookup"><span data-stu-id="fbe09-126">This thread should not own any windows, and should be a Component Object Model (COM) Multithreaded Apartment (MTA) model thread (one that initializes COM by calling [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.)</span></span>

<span data-ttu-id="fbe09-127">È possibile eseguire chiamate di automazione interfaccia utente in un gestore eventi di automazione interfaccia utente, poiché il gestore eventi viene sempre chiamato su un thread non dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fbe09-127">It is safe to make UI Automation calls in a UI Automation event handler, because the event handler is always called on a non-UI thread.</span></span> <span data-ttu-id="fbe09-128">Tuttavia, quando si sottoscrive eventi che possono provenire dall'interfaccia utente dell'applicazione client, è necessario effettuare la chiamata a [**IUIAutomation:: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)o a un metodo correlato su un thread non dell'interfaccia utente (che deve essere anche un thread MTA).</span><span class="sxs-lookup"><span data-stu-id="fbe09-128">However, when subscribing to events that may originate from your client application UI, you must make the call to [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), or a related method, on a non-UI thread (which should also be an MTA thread).</span></span> <span data-ttu-id="fbe09-129">Rimuovere i gestori eventi sullo stesso thread.</span><span class="sxs-lookup"><span data-stu-id="fbe09-129">Remove event handlers on the same thread.</span></span>

<span data-ttu-id="fbe09-130">Un client di automazione interfaccia utente non deve usare più thread per aggiungere o rimuovere i gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="fbe09-130">A UI Automation client should not use multiple threads to add or remove event handlers.</span></span> <span data-ttu-id="fbe09-131">Un comportamento imprevisto può verificarsi se un gestore eventi viene aggiunto o rimosso mentre un altro viene aggiunto o rimosso nello stesso processo client.</span><span class="sxs-lookup"><span data-stu-id="fbe09-131">Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.</span></span>

## <a name="threading-model-for-event-handlers"></a><span data-ttu-id="fbe09-132">Modello di threading per i gestori eventi</span><span class="sxs-lookup"><span data-stu-id="fbe09-132">Threading Model for Event Handlers</span></span>

<span data-ttu-id="fbe09-133">Un client di automazione interfaccia utente deve utilizzare il modello di threading MTA COM per i thread che implementano i gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="fbe09-133">A UI Automation client should use the COM MTA threading model for threads that implement event handlers.</span></span> <span data-ttu-id="fbe09-134">L'uso del modello STA (Single-Threaded Apartment) può causare problemi, ad esempio impedire ai client di rimuovere i gestori eventi dal thread.</span><span class="sxs-lookup"><span data-stu-id="fbe09-134">Using the Single-threaded Apartment (STA) model can cause problems such as preventing clients from removing event handlers from the thread.</span></span>

## <a name="com-apartment-affinity-on-64-bit-windows"></a><span data-ttu-id="fbe09-135">Affinità di apartment COM in Windows a 64 bit</span><span class="sxs-lookup"><span data-stu-id="fbe09-135">COM Apartment Affinity on 64-bit Windows</span></span>

<span data-ttu-id="fbe09-136">In base alla specifica COM, la durata di un oggetto remoto è regolata dalla durata dell'Apartment in cui viene chiamata la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fbe09-136">According to the COM specification, the lifetime of a remote object is governed by the lifetime of the apartment where the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function is called to create the object.</span></span> <span data-ttu-id="fbe09-137">Quando l'Apartment originale viene arrestato, viene rilasciato anche l'oggetto remoto.</span><span class="sxs-lookup"><span data-stu-id="fbe09-137">When the original apartment shuts down, the remote object is also released.</span></span>

<span data-ttu-id="fbe09-138">Per i client di automazione interfaccia utente, questo comportamento COM può indicare che la durata dell'helper 32/64 remoto (creata da UIAutomationCore.dll) usata da un elemento a 32 bit è regolata dalla durata dell'Apartment del thread che ha creato l'elemento.</span><span class="sxs-lookup"><span data-stu-id="fbe09-138">For UI Automation clients, this COM behavior can mean that the lifetime of the remote 32/64 helper (created by UIAutomationCore.dll) used by a 32-bit element is governed by the apartment lifetime of the thread that created the element.</span></span> <span data-ttu-id="fbe09-139">Se il client di automazione interfaccia utente esegue il marshalling dell'elemento in un altro thread, l'elemento può essere invalidato quando l'Apartment di origine si arresta.</span><span class="sxs-lookup"><span data-stu-id="fbe09-139">If the UI Automation client marshals the element to another thread, the element can become invalidated when the originating apartment shuts down.</span></span> <span data-ttu-id="fbe09-140">Il client di automazione interfaccia utente deve gestire correttamente questi problemi intercettando gli errori quando si usano gli elementi di automazione sottoposti a marshalling.</span><span class="sxs-lookup"><span data-stu-id="fbe09-140">The UI Automation client should handle these issues gracefully by catching errors while using marshaled automation elements.</span></span>

<span data-ttu-id="fbe09-141">Lo stesso problema può verificarsi con un client di automazione interfaccia utente a 32 bit che contiene elementi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fbe09-141">The same issue can occur with a 32-bit UI Automation client that has 64-bit elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbe09-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fbe09-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fbe09-143">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="fbe09-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fbe09-144">Ottenere elementi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fbe09-144">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="fbe09-145">Sottoscrizione degli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fbe09-145">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="fbe09-146">Cenni preliminari sugli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fbe09-146">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

<span data-ttu-id="fbe09-147">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="fbe09-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fbe09-148">INFORMAZIONI: descrizioni e funzioni dei modelli di threading OLE</span><span class="sxs-lookup"><span data-stu-id="fbe09-148">INFO: Descriptions and Workings of OLE Threading Models</span></span>](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 