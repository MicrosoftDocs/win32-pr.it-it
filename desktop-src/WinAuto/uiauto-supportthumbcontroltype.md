---
title: Tipo di controllo Thumb
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Thumb
- Automazione interfaccia utente, tipo di controllo Thumb
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Thumb
- Automazione interfaccia utente, proprietà per il tipo di controllo Thumb
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Thumb
- Automazione interfaccia utente, eventi per il tipo di controllo Thumb
- strutture ad albero, tipo di controllo Thumb
- Proprietà, tipo di controllo Thumb
- pattern di controllo, tipo di controllo Thumb
- eventi, tipo di controllo Thumb
- supporto per il tipo di controllo Thumb
- Thumb (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Thumb
- tipi di controllo, pattern di controllo per il tipo di controllo Thumb
- tipi di controllo, supporto per Thumb
- tipi di controllo, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396743"
---
# <a name="thumb-control-type"></a><span data-ttu-id="4090a-119">Tipo di controllo Thumb</span><span class="sxs-lookup"><span data-stu-id="4090a-119">Thumb Control Type</span></span>

<span data-ttu-id="4090a-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="4090a-120">This topic provides information about Microsoft UI Automation support for the **Thumb** control type.</span></span>

<span data-ttu-id="4090a-121">I controlli Thumb forniscono la funzionalità che consente lo spostamento o il trascinamento di un controllo, ad esempio un pulsante della barra di scorrimento, oppure il ridimensionato, ad esempio un widget per il ridimensionamento della finestra.</span><span class="sxs-lookup"><span data-stu-id="4090a-121">Thumb controls provide the functionality that enables a control to be moved (or dragged), such as a scroll bar button, or resized, such as a window resizing widget.</span></span> <span data-ttu-id="4090a-122">Si noti che un controllo Thumb non fornisce funzionalità di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="4090a-122">Note that a thumb control does not provide drag-and-drop functionality.</span></span> <span data-ttu-id="4090a-123">I controlli Thumb possono ricevere lo stato attivo del mouse ma non lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="4090a-123">Thumb controls can receive mouse focus but not keyboard focus.</span></span> <span data-ttu-id="4090a-124">Lo sviluppatore del controllo deve implementare il controllo in modo che funzioni nel modo appropriato, ovvero possa essere trascinato o ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="4090a-124">The control developer must implement the control so that it acts appropriately (can be dragged or resized).</span></span>

<span data-ttu-id="4090a-125">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="4090a-125">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Thumb** control type.</span></span> <span data-ttu-id="4090a-126">I requisiti di automazione interfaccia utente applicano tutti i controlli Thumb in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="4090a-126">The UI Automation requirements apply all thumb controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4090a-127">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="4090a-127">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4090a-128">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="4090a-128">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4090a-129">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="4090a-129">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4090a-130">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="4090a-130">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4090a-131">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="4090a-131">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4090a-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4090a-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4090a-133">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="4090a-133">Typical Tree Structure</span></span>

<span data-ttu-id="4090a-134">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli Thumb e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4090a-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to thumb controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4090a-135">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4090a-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4090a-136">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="4090a-136">Control View</span></span></th>
<th><span data-ttu-id="4090a-137">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="4090a-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4090a-138">Thumb</span><span class="sxs-lookup"><span data-stu-id="4090a-138">Thumb</span></span></li>
</ul></td>
<td><span data-ttu-id="4090a-139">(Non applicabile)</span><span class="sxs-lookup"><span data-stu-id="4090a-139">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4090a-140">I controlli Thumb non vengono mai visualizzati nella visualizzazione contenuto perché esistono solo per essere modificati con il mouse.</span><span class="sxs-lookup"><span data-stu-id="4090a-140">Thumb controls never appear in the content view because they exist only to be manipulated with a mouse.</span></span> <span data-ttu-id="4090a-141">Sono esposti anche se un altro pattern di controllo, ad esempio il pattern di controllo [Scroll](uiauto-implementingscroll.md) , il pattern di controllo [Transform](uiauto-implementingtransform.md) o il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , è supportato nel contenitore del controllo Thumb.</span><span class="sxs-lookup"><span data-stu-id="4090a-141">They are exposed though another control pattern, such as the [Scroll](uiauto-implementingscroll.md) control pattern, [Transform](uiauto-implementingtransform.md) control pattern, or [RangeValue](uiauto-implementingrangevalue.md) control pattern, being supported on the thumb control's container.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="4090a-142">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="4090a-142">Relevant Properties</span></span>

<span data-ttu-id="4090a-143">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli Thumb.</span><span class="sxs-lookup"><span data-stu-id="4090a-143">The following table lists the UI Automation properties whose value or definition is especially relevant to thumb controls.</span></span> <span data-ttu-id="4090a-144">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="4090a-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4090a-145">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4090a-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4090a-146">Valore</span><span class="sxs-lookup"><span data-stu-id="4090a-146">Value</span></span>      | <span data-ttu-id="4090a-147">Note</span><span class="sxs-lookup"><span data-stu-id="4090a-147">Notes</span></span>                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4090a-148">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4090a-149">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="4090a-149">See notes.</span></span> | <span data-ttu-id="4090a-150">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4090a-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="4090a-151">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4090a-152">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="4090a-152">See notes.</span></span> | <span data-ttu-id="4090a-153">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="4090a-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="4090a-154">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4090a-155">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="4090a-155">See notes.</span></span> | <span data-ttu-id="4090a-156">Punto all'interno dell'area client visibile del controllo Thumb.</span><span class="sxs-lookup"><span data-stu-id="4090a-156">A point within the visible client area of the thumb control.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="4090a-157">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-157">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4090a-158">**Thumb**</span><span class="sxs-lookup"><span data-stu-id="4090a-158">**Thumb**</span></span>  |                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="4090a-159">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4090a-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="4090a-160">FALSE</span></span>      | <span data-ttu-id="4090a-161">Il controllo Thumb non è mai incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4090a-161">The thumb control is never included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="4090a-162">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4090a-163">true</span><span class="sxs-lookup"><span data-stu-id="4090a-163">TRUE</span></span>       | <span data-ttu-id="4090a-164">Il controllo Thumb viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4090a-164">The thumb control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="4090a-165">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4090a-166">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="4090a-166">See notes.</span></span> | <span data-ttu-id="4090a-167">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="4090a-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="4090a-168">Un controllo Thumb può ricevere lo stato attivo se viene usato come oggetto "pinza" per dimensionare una finestra o un riquadro.</span><span class="sxs-lookup"><span data-stu-id="4090a-168">A thumb control can receive the focus if it is used as a "gripper" object for sizing a window or a pane.</span></span> <span data-ttu-id="4090a-169">Un controllo Thumb in un dispositivo di scorrimento o una barra di scorrimento non deve mai ricevere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="4090a-169">A thumb control in a slider or scroll bar should never receive the focus.</span></span> |
| [<span data-ttu-id="4090a-170">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4090a-171">NULL</span><span class="sxs-lookup"><span data-stu-id="4090a-171">NULL</span></span>       | <span data-ttu-id="4090a-172">I controlli Thumb non includono mai un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="4090a-172">Thumb controls never have a label.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="4090a-173">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4090a-174">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="4090a-174">See notes.</span></span> | <span data-ttu-id="4090a-175">Stringa localizzata corrispondente al tipo di controllo **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="4090a-175">Localized string corresponding to the **Thumb** control type.</span></span> <span data-ttu-id="4090a-176">Il valore predefinito è "thumb" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="4090a-176">The default value is "thumb" for en-US or English (United States).</span></span>                                                                                                                             |
| [<span data-ttu-id="4090a-177">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4090a-178">NULL</span><span class="sxs-lookup"><span data-stu-id="4090a-178">NULL</span></span>       | <span data-ttu-id="4090a-179">Poiché il controllo Thumb non è disponibile nella visualizzazione contenuto dell'albero di automazione interfaccia utente, non richiede un nome.</span><span class="sxs-lookup"><span data-stu-id="4090a-179">Because the thumb control is not available in the content view of the UI Automation tree, it does not require a name.</span></span>                                                                                                                                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4090a-180">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="4090a-180">Required Control Patterns</span></span>

<span data-ttu-id="4090a-181">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli Thumb.</span><span class="sxs-lookup"><span data-stu-id="4090a-181">The following table lists the UI Automation control patterns required to be supported by thumb controls.</span></span> <span data-ttu-id="4090a-182">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4090a-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4090a-183">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="4090a-183">Control Pattern</span></span>                                         | <span data-ttu-id="4090a-184">Supporto</span><span class="sxs-lookup"><span data-stu-id="4090a-184">Support</span></span>  | <span data-ttu-id="4090a-185">Note</span><span class="sxs-lookup"><span data-stu-id="4090a-185">Notes</span></span>                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4090a-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="4090a-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="4090a-187">Necessario</span><span class="sxs-lookup"><span data-stu-id="4090a-187">Required</span></span> | <span data-ttu-id="4090a-188">Consente lo spostamento del controllo Thumb sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="4090a-188">Enables the thumb control to be moved on the screen.</span></span> <span data-ttu-id="4090a-189">Poiché non è in genere possibile ridimensionare o ruotare il controllo Thumb, il pattern di controllo [Transform](uiauto-implementingtransform.md) supporta principalmente la funzione [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) .</span><span class="sxs-lookup"><span data-stu-id="4090a-189">Because the thumb control typically cannot be resized or rotated, the [Transform](uiauto-implementingtransform.md) control pattern primarily supports the [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) function.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="4090a-190">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="4090a-190">Required Events</span></span>

<span data-ttu-id="4090a-191">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli Thumb.</span><span class="sxs-lookup"><span data-stu-id="4090a-191">The following table lists the UI Automation events that thumb controls are required to support.</span></span> <span data-ttu-id="4090a-192">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4090a-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4090a-193">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4090a-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="4090a-194">Note</span><span class="sxs-lookup"><span data-stu-id="4090a-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4090a-195">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="4090a-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4090a-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="4090a-197">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4090a-197">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="4090a-198">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="4090a-198">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="4090a-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4090a-199">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="4090a-200">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="4090a-200">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="4090a-201">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="4090a-201">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="4090a-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4090a-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4090a-203">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4090a-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4090a-204">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4090a-204">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4090a-205">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4090a-205">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




