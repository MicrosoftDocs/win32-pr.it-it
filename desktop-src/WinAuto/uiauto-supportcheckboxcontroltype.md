---
title: Tipo di controllo CheckBox
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo CheckBox
- Automazione interfaccia utente, tipo di controllo CheckBox
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo CheckBox
- Automazione interfaccia utente, proprietà per il tipo di controllo CheckBox
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo CheckBox
- Automazione interfaccia utente, eventi per il tipo di controllo CheckBox
- strutture ad albero, tipo di controllo CheckBox
- Proprietà, tipo di controllo CheckBox
- pattern di controllo, tipo di controllo CheckBox
- eventi, tipo di controllo CheckBox
- supporto per il tipo di controllo CheckBox
- CheckBox (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo CheckBox
- tipi di controllo, pattern di controllo per il tipo di controllo CheckBox
- tipi di controllo, supporto per CheckBox
- tipi di controllo, casella di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856085"
---
# <a name="checkbox-control-type"></a><span data-ttu-id="586eb-119">Tipo di controllo CheckBox</span><span class="sxs-lookup"><span data-stu-id="586eb-119">CheckBox Control Type</span></span>

<span data-ttu-id="586eb-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="586eb-120">This topic provides information about Microsoft UI Automation support for the **CheckBox** control type.</span></span>

<span data-ttu-id="586eb-121">Una casella di controllo è un oggetto usato per indicare uno stato con cui gli utenti possono interagire per scorrere tale stato.</span><span class="sxs-lookup"><span data-stu-id="586eb-121">A check box is an object used to indicate a state that users can interact with to cycle through that state.</span></span> <span data-ttu-id="586eb-122">Le caselle di controllo presentano all'utente un'opzione binaria (Yes/No), (On/Off) o terziaria (On, Off, Indeterminate).</span><span class="sxs-lookup"><span data-stu-id="586eb-122">Check boxes either present a binary (Yes/No), (On/Off), or tertiary (On, Off, Indeterminate) option to the user.</span></span>

<span data-ttu-id="586eb-123">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="586eb-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **CheckBox** control type.</span></span> <span data-ttu-id="586eb-124">I requisiti di automazione interfaccia utente si applicano a tutti i controlli casella di controllo in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="586eb-124">The UI Automation requirements apply to all check box controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="586eb-125">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="586eb-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="586eb-126">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="586eb-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="586eb-127">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="586eb-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="586eb-128">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="586eb-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="586eb-129">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="586eb-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="586eb-130">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="586eb-130">DefaultAction</span></span>](#defaultaction)
-   [<span data-ttu-id="586eb-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="586eb-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="586eb-132">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="586eb-132">Typical Tree Structure</span></span>

<span data-ttu-id="586eb-133">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli casella di controllo e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="586eb-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to check box controls and describes what can be contained in each view.</span></span> <span data-ttu-id="586eb-134">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="586eb-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="586eb-135">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="586eb-135">Control View</span></span></th>
<th><span data-ttu-id="586eb-136">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="586eb-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="586eb-137">CheckBox</span><span class="sxs-lookup"><span data-stu-id="586eb-137">CheckBox</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="586eb-138">CheckBox</span><span class="sxs-lookup"><span data-stu-id="586eb-138">CheckBox</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="586eb-139">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="586eb-139">Relevant Properties</span></span>

<span data-ttu-id="586eb-140">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="586eb-140">The following table lists the UI Automation properties whose value or definition is especially relevant to the **CheckBox** control type.</span></span> <span data-ttu-id="586eb-141">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="586eb-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="586eb-142">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="586eb-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="586eb-143">Valore</span><span class="sxs-lookup"><span data-stu-id="586eb-143">Value</span></span>        | <span data-ttu-id="586eb-144">Note</span><span class="sxs-lookup"><span data-stu-id="586eb-144">Notes</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="586eb-145">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="586eb-146">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="586eb-146">See notes.</span></span>   | <span data-ttu-id="586eb-147">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="586eb-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="586eb-148">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="586eb-149">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="586eb-149">See notes.</span></span>   | <span data-ttu-id="586eb-150">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="586eb-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="586eb-151">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="586eb-152">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="586eb-152">See notes.</span></span>   | <span data-ttu-id="586eb-153">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="586eb-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="586eb-154">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="586eb-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                               |
| [<span data-ttu-id="586eb-155">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="586eb-156">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="586eb-156">**CheckBox**</span></span> |                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="586eb-157">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="586eb-158">true</span><span class="sxs-lookup"><span data-stu-id="586eb-158">TRUE</span></span>         | <span data-ttu-id="586eb-159">Il valore di questa proprietà deve essere sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="586eb-159">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="586eb-160">Questo significa che il controllo casella di controllo deve essere sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="586eb-160">This means that the check box control must always be included in the content view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="586eb-161">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="586eb-162">true</span><span class="sxs-lookup"><span data-stu-id="586eb-162">TRUE</span></span>         | <span data-ttu-id="586eb-163">Il valore di questa proprietà deve essere sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="586eb-163">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="586eb-164">Questo significa che il controllo casella di controllo deve essere sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="586eb-164">This means that the check box control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="586eb-165">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="586eb-166">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="586eb-166">See notes.</span></span>   | <span data-ttu-id="586eb-167">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="586eb-167">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="586eb-168">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="586eb-169">Null</span><span class="sxs-lookup"><span data-stu-id="586eb-169">Null</span></span>         | <span data-ttu-id="586eb-170">I controlli casella di controllo sono con etichetta automatica.</span><span class="sxs-lookup"><span data-stu-id="586eb-170">Check box controls are self-labeling.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="586eb-171">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="586eb-172">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="586eb-172">See notes.</span></span>   | <span data-ttu-id="586eb-173">Stringa localizzata corrispondente al tipo di controllo **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="586eb-173">Localized string corresponding to the **CheckBox** control type.</span></span> <span data-ttu-id="586eb-174">Il valore predefinito è "casella di controllo" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="586eb-174">The default value is "check box" for en-US or English (United States).</span></span>                                                                                                                                            |
| [<span data-ttu-id="586eb-175">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="586eb-176">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="586eb-176">See notes.</span></span>   | <span data-ttu-id="586eb-177">Il valore della proprietà [**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (o [**CacheName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) del controllo casella di controllo è il testo visualizzato accanto alla casella che mantiene lo stato dell'interruttore.</span><span class="sxs-lookup"><span data-stu-id="586eb-177">The value of the check box control's [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (or [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) property is the text that is displayed beside the box that maintains the toggle state.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="586eb-178">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="586eb-178">Required Control Patterns</span></span>

<span data-ttu-id="586eb-179">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="586eb-179">The following table lists the UI Automation control patterns required to be supported by all check box controls.</span></span> <span data-ttu-id="586eb-180">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="586eb-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="586eb-181">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="586eb-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="586eb-182">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="586eb-182">Support/Value</span></span> | <span data-ttu-id="586eb-183">Note</span><span class="sxs-lookup"><span data-stu-id="586eb-183">Notes</span></span>                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="586eb-184">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="586eb-184">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="586eb-185">Necessario</span><span class="sxs-lookup"><span data-stu-id="586eb-185">Required</span></span>      | <span data-ttu-id="586eb-186">Le caselle di controllo supportano il pattern di controllo di [attivazione/disattivazione](uiauto-implementingtoggle.md) per consentire la visualizzazione della casella di controllo a livello di programmazione tramite gli Stati interni.</span><span class="sxs-lookup"><span data-stu-id="586eb-186">Check boxes support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the check box to be programmatically cycled through its internal states.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="586eb-187">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="586eb-187">Required Events</span></span>

<span data-ttu-id="586eb-188">La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="586eb-188">The following table lists the UI Automation events that check box controls are required to support.</span></span> <span data-ttu-id="586eb-189">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="586eb-189">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="586eb-190">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="586eb-190">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="586eb-191">Note</span><span class="sxs-lookup"><span data-stu-id="586eb-191">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="586eb-192">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-192">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="586eb-193">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="586eb-193">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="586eb-194">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="586eb-194">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="586eb-195">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="586eb-195">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="586eb-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="586eb-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="586eb-197">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="586eb-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| [<span data-ttu-id="586eb-198">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="586eb-198">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="586eb-199">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="586eb-199">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="defaultaction"></a><span data-ttu-id="586eb-200">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="586eb-200">DefaultAction</span></span>

<span data-ttu-id="586eb-201">L'azione predefinita della casella di controllo è fare sì che un pulsante di opzione assuma lo stato attivo e attivarne/disattivarne lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="586eb-201">The default action of the check box is to cause a radio button to become focused and toggle its current state.</span></span> <span data-ttu-id="586eb-202">Come indicato in precedenza, le caselle di controllo presentano una decisione binaria (Yes/No o on/off) per l'utente o terziaria (on, off, Indeterminate).</span><span class="sxs-lookup"><span data-stu-id="586eb-202">As mentioned previously, check boxes either present a binary (Yes/No or On/Off) decision to the user or a tertiary (On, Off, Indeterminate).</span></span> <span data-ttu-id="586eb-203">Se la casella di controllo è binaria, l'azione predefinita fa sì che lo stato "on" diventi "off" o che lo stato "off" diventi "on".</span><span class="sxs-lookup"><span data-stu-id="586eb-203">If the check box is binary the default action causes the "on" state to become "off" or the "off" state to become "on".</span></span> <span data-ttu-id="586eb-204">In una casella di controllo terziario l'azione predefinita scorre gli Stati della casella di controllo nello stesso ordine in cui l'utente ha inviato i clic del mouse successivi al controllo.</span><span class="sxs-lookup"><span data-stu-id="586eb-204">In a tertiary check box the default action cycles through the states of the check box in the same order as if the user had sent successive mouse clicks to the control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="586eb-205">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="586eb-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="586eb-206">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="586eb-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="586eb-207">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="586eb-207">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="586eb-208">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="586eb-208">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




