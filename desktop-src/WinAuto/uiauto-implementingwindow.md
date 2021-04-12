---
title: Pattern di controllo Window
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IWindowProvider, incluse informazioni su proprietà, metodi ed eventi. Il pattern di controllo Window supporta i controlli che forniscono funzionalità fondamentali basate su finestra all'interno di un'interfaccia utente grafica tradizionale.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Window
- Automazione interfaccia utente, pattern di controllo Window
- Automazione interfaccia utente, IWindowProvider
- IWindowProvider
- implementazione di pattern di controllo Window di automazione interfaccia utente
- Pattern di controllo Window
- pattern di controllo, IWindowProvider
- pattern di controllo, implementazione della finestra di automazione interfaccia utente
- pattern di controllo, finestra
- interfacce, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332420"
---
# <a name="window-control-pattern"></a><span data-ttu-id="cef92-114">Pattern di controllo Window</span><span class="sxs-lookup"><span data-stu-id="cef92-114">Window Control Pattern</span></span>

<span data-ttu-id="cef92-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), incluse informazioni su proprietà, metodi ed eventi.</span><span class="sxs-lookup"><span data-stu-id="cef92-115">Describes guidelines and conventions for implementing [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="cef92-116">Il pattern di controllo **Window** supporta i controlli che forniscono funzionalità fondamentali basate su finestra all'interno di un'interfaccia utente grafica tradizionale.</span><span class="sxs-lookup"><span data-stu-id="cef92-116">The **Window** control pattern supports controls that provide fundamental window-based functionality within a traditional GUI.</span></span>

<span data-ttu-id="cef92-117">Esempi di controlli che devono implementare questo pattern di controllo sono le finestre dell'applicazione di primo livello, le finestre figlio dell'interfaccia a documenti multipli (MDI), i controlli del riquadro suddiviso ridimensionabili, le finestre di dialogo modali e le finestre della guida del fumetto.</span><span class="sxs-lookup"><span data-stu-id="cef92-117">Examples of controls that must implement this control pattern include top-level application windows, multiple-document interface (MDI) child windows, resizable split pane controls, modal dialogs and balloon help windows.</span></span> <span data-ttu-id="cef92-118">Per esempi di controlli che implementano questo pattern di controllo, vedere [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="cef92-118">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="cef92-119">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="cef92-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cef92-120">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="cef92-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="cef92-121">Membri obbligatori per **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="cef92-121">Required Members for **IWindowProvider**</span></span>](#required-members-for-iwindowprovider)
-   [<span data-ttu-id="cef92-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cef92-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="cef92-123">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="cef92-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="cef92-124">Quando si implementa il pattern di controllo **Window** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cef92-124">When implementing the **Window** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="cef92-125">Per supportare la possibilità di modificare le dimensioni della finestra e la posizione dello schermo usando l'automazione interfaccia utente Microsoft, un controllo deve implementare [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) oltre a [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="cef92-125">To support the ability to modify both window size and screen position using Microsoft UI Automation, a control must implement [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) in addition to [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="cef92-126">I controlli che contengono barre del titolo ed elementi della barra del titolo che consentono di spostare, ridimensionare, ingrandire, ridurre a icona o chiudere il controllo sono in genere necessari per implementare [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="cef92-126">Controls that contain title bars, and title bar elements that enable the control to be moved, resized, maximized, minimized, or closed, are typically required to implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="cef92-127">I controlli quali popup della descrizione comando e elenchi a discesa della casella combinata o dei menu non implementano in genere [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="cef92-127">Controls such as tooltip pop-ups and combo-box or menu drop-downs do not typically implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="cef92-128">Le finestre della Guida per i fumetti si differenziano dai popup di descrizione comando di base tramite il provisioning di un pulsante **Chiudi** simile a una finestra.</span><span class="sxs-lookup"><span data-stu-id="cef92-128">Balloon help windows are differentiated from basic tooltip pop-ups by the provision of a window-like **Close** button.</span></span>
-   <span data-ttu-id="cef92-129">La modalità schermo intero non è supportata da [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) perché è specifica della funzionalità per un'applicazione e non è un comportamento tipico delle finestre.</span><span class="sxs-lookup"><span data-stu-id="cef92-129">Full-screen mode is not supported by [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) as it is feature-specific to an application and is not typical window behavior.</span></span>

## <a name="required-members-for-iwindowprovider"></a><span data-ttu-id="cef92-130">Membri obbligatori per **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="cef92-130">Required Members for **IWindowProvider**</span></span>

<span data-ttu-id="cef92-131">Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) .</span><span class="sxs-lookup"><span data-stu-id="cef92-131">The following properties, methods, and events are required for implementing the [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) interface.</span></span>



| <span data-ttu-id="cef92-132">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="cef92-132">Required members</span></span>                                                                            | <span data-ttu-id="cef92-133">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="cef92-133">Member type</span></span> | <span data-ttu-id="cef92-134">Note</span><span class="sxs-lookup"><span data-stu-id="cef92-134">Notes</span></span>                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="cef92-135">**WindowInteractionState**</span><span class="sxs-lookup"><span data-stu-id="cef92-135">**WindowInteractionState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | <span data-ttu-id="cef92-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cef92-136">Property</span></span>    | <span data-ttu-id="cef92-137">Non è garantito che sia **WindowInteractionState \_ ReadyForUserInteraction**</span><span class="sxs-lookup"><span data-stu-id="cef92-137">Is not guaranteed to be **WindowInteractionState\_ReadyForUserInteraction**</span></span> |
| [<span data-ttu-id="cef92-138">**IsModal**</span><span class="sxs-lookup"><span data-stu-id="cef92-138">**IsModal**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | <span data-ttu-id="cef92-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cef92-139">Property</span></span>    | <span data-ttu-id="cef92-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-140">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-141">**IsTopmost**</span><span class="sxs-lookup"><span data-stu-id="cef92-141">**IsTopmost**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | <span data-ttu-id="cef92-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cef92-142">Property</span></span>    | <span data-ttu-id="cef92-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-143">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-144">**CanMaximize**</span><span class="sxs-lookup"><span data-stu-id="cef92-144">**CanMaximize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | <span data-ttu-id="cef92-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cef92-145">Property</span></span>    | <span data-ttu-id="cef92-146">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-146">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-147">**CanMinimize**</span><span class="sxs-lookup"><span data-stu-id="cef92-147">**CanMinimize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | <span data-ttu-id="cef92-148">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cef92-148">Property</span></span>    | <span data-ttu-id="cef92-149">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-149">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-150">**WindowVisualState**</span><span class="sxs-lookup"><span data-stu-id="cef92-150">**WindowVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | <span data-ttu-id="cef92-151">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cef92-151">Property</span></span>    | <span data-ttu-id="cef92-152">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-152">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-153">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="cef92-153">**Close**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | <span data-ttu-id="cef92-154">Metodo</span><span class="sxs-lookup"><span data-stu-id="cef92-154">Method</span></span>      | <span data-ttu-id="cef92-155">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-155">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-156">**SetVisualState**</span><span class="sxs-lookup"><span data-stu-id="cef92-156">**SetVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | <span data-ttu-id="cef92-157">Metodo</span><span class="sxs-lookup"><span data-stu-id="cef92-157">Method</span></span>      | <span data-ttu-id="cef92-158">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-158">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-159">**WaitForInputIdle**</span><span class="sxs-lookup"><span data-stu-id="cef92-159">**WaitForInputIdle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | <span data-ttu-id="cef92-160">Metodo</span><span class="sxs-lookup"><span data-stu-id="cef92-160">Method</span></span>      | <span data-ttu-id="cef92-161">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-161">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-162">**\_WindowClosedEventId finestra \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="cef92-162">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="cef92-163">Evento</span><span class="sxs-lookup"><span data-stu-id="cef92-163">Event</span></span>       | <span data-ttu-id="cef92-164">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-164">None</span></span>                                                                        |
| [<span data-ttu-id="cef92-165">**\_WindowOpenedEventId finestra \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="cef92-165">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="cef92-166">Evento</span><span class="sxs-lookup"><span data-stu-id="cef92-166">Event</span></span>       | <span data-ttu-id="cef92-167">nessuno</span><span class="sxs-lookup"><span data-stu-id="cef92-167">None</span></span>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="cef92-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cef92-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cef92-169">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="cef92-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cef92-170">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="cef92-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="cef92-171">Mapping dei pattern di controllo per i client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="cef92-171">Control Pattern Mapping for UI Automation Clients</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="cef92-172">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="cef92-172">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




