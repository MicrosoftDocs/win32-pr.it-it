---
title: Tipo di controllo SplitButton
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo SplitButton
- Automazione interfaccia utente, tipo di controllo SplitButton
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo SplitButton
- Automazione interfaccia utente, proprietà per il tipo di controllo SplitButton
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo SplitButton
- Automazione interfaccia utente, eventi per il tipo di controllo SplitButton
- strutture ad albero, tipo di controllo SplitButton
- Proprietà, tipo di controllo SplitButton
- pattern di controllo, tipo di controllo SplitButton
- eventi, tipo di controllo SplitButton
- supporto per il tipo di controllo SplitButton
- Tipo di controllo SplitButton
- tipi di controllo, struttura ad albero per il tipo di controllo SplitButton
- tipi di controllo, pattern di controllo per il tipo di controllo SplitButton
- tipi di controllo, supporto per SplitButton
- tipi di controllo, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712697"
---
# <a name="splitbutton-control-type"></a><span data-ttu-id="59c0e-119">Tipo di controllo SplitButton</span><span class="sxs-lookup"><span data-stu-id="59c0e-119">SplitButton Control Type</span></span>

<span data-ttu-id="59c0e-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="59c0e-120">This topic provides information about Microsoft UI Automation support for the **SplitButton** control type.</span></span>

<span data-ttu-id="59c0e-121">Il controllo pulsante di divisione consente di eseguire un'azione su un controllo ed espandere il controllo per visualizzare un elenco di altre possibili azioni che è possibile eseguire.</span><span class="sxs-lookup"><span data-stu-id="59c0e-121">The split button control enables an action to be performed on a control, and to expand the control to see a list of other possible actions that can be performed.</span></span>

<span data-ttu-id="59c0e-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="59c0e-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SplitButton** control type.</span></span> <span data-ttu-id="59c0e-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli pulsante di divisione in cui il Framework dell'interfaccia utente/piattaforma integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="59c0e-123">The UI Automation requirements apply to all split button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="59c0e-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="59c0e-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="59c0e-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="59c0e-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="59c0e-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="59c0e-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="59c0e-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="59c0e-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="59c0e-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="59c0e-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="59c0e-129">Esempio di tipo di controllo SplitButton</span><span class="sxs-lookup"><span data-stu-id="59c0e-129">SplitButton Control Type Example</span></span>](#splitbutton-control-type-example)
-   [<span data-ttu-id="59c0e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59c0e-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="59c0e-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="59c0e-131">Typical Tree Structure</span></span>

<span data-ttu-id="59c0e-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli pulsante di suddivisione e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="59c0e-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to split button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="59c0e-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="59c0e-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59c0e-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="59c0e-134">Control View</span></span></th>
<th><span data-ttu-id="59c0e-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="59c0e-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="59c0e-136">SplitButton</span><span class="sxs-lookup"><span data-stu-id="59c0e-136">SplitButton</span></span>
<ul>
<li><span data-ttu-id="59c0e-137">Image (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="59c0e-137">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="59c0e-138">Text (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="59c0e-138">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="59c0e-139">Button (1 o 2)</span><span class="sxs-lookup"><span data-stu-id="59c0e-139">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="59c0e-140">Menu (0 o 1; viene visualizzato come elemento figlio di un pulsante secondario che supporta il pattern ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="59c0e-140">Menu (0 or 1; appears as a child of a sub-button that supports the ExpandCollapse pattern)</span></span>
<ul>
<li><span data-ttu-id="59c0e-141">MenuItem (da 1 a molti)</span><span class="sxs-lookup"><span data-stu-id="59c0e-141">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59c0e-142">SplitButton</span><span class="sxs-lookup"><span data-stu-id="59c0e-142">SplitButton</span></span>
<ul>
<li><span data-ttu-id="59c0e-143">Button (1 o 2)</span><span class="sxs-lookup"><span data-stu-id="59c0e-143">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="59c0e-144">MenuItem (da 1 a molti)</span><span class="sxs-lookup"><span data-stu-id="59c0e-144">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="59c0e-145">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="59c0e-145">Relevant Properties</span></span>

<span data-ttu-id="59c0e-146">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="59c0e-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the **SplitButton** control type.</span></span> <span data-ttu-id="59c0e-147">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="59c0e-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="59c0e-148">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="59c0e-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="59c0e-149">Valore</span><span class="sxs-lookup"><span data-stu-id="59c0e-149">Value</span></span>           | <span data-ttu-id="59c0e-150">Note</span><span class="sxs-lookup"><span data-stu-id="59c0e-150">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59c0e-151">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="59c0e-152">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="59c0e-152">See notes.</span></span>      | <span data-ttu-id="59c0e-153">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="59c0e-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="59c0e-154">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="59c0e-155">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="59c0e-155">See notes.</span></span>      | <span data-ttu-id="59c0e-156">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="59c0e-156">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="59c0e-157">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="59c0e-158">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="59c0e-158">See notes.</span></span>      | <span data-ttu-id="59c0e-159">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="59c0e-159">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="59c0e-160">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="59c0e-160">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="59c0e-161">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-161">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="59c0e-162">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="59c0e-162">**SplitButton**</span></span> | <span data-ttu-id="59c0e-163">Questo valore è uguale per tutti i framework dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="59c0e-163">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="59c0e-164">**\_HELPTEXTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="59c0e-165">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="59c0e-165">See notes.</span></span>      | <span data-ttu-id="59c0e-166">Il testo della Guida può indicare il risultato dell'attivazione del pulsante di menu combinato, che in genere è lo stesso tipo di informazioni visualizzate mediante una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="59c0e-166">The help text can indicate the result of activating the split button, which is typically the same type of information presented through a tooltip.</span></span>                                                   |
| [<span data-ttu-id="59c0e-167">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="59c0e-168">true</span><span class="sxs-lookup"><span data-stu-id="59c0e-168">TRUE</span></span>            | <span data-ttu-id="59c0e-169">Il controllo pulsante di menu combinato contiene informazioni per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="59c0e-169">The split button control contains information for the end user.</span></span>                                                                                                                                      |
| [<span data-ttu-id="59c0e-170">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="59c0e-171">true</span><span class="sxs-lookup"><span data-stu-id="59c0e-171">TRUE</span></span>            | <span data-ttu-id="59c0e-172">Il controllo pulsante di menu combinato è visibile all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="59c0e-172">The split button control is visible to the end user.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="59c0e-173">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="59c0e-174">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="59c0e-174">See notes.</span></span>      | <span data-ttu-id="59c0e-175">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="59c0e-175">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="59c0e-176">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="59c0e-177">NULL</span><span class="sxs-lookup"><span data-stu-id="59c0e-177">NULL</span></span>            | <span data-ttu-id="59c0e-178">I controlli pulsante di menu combinato non hanno un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="59c0e-178">Split button controls do not have a static text label.</span></span>                                                                                                                                               |
| [<span data-ttu-id="59c0e-179">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="59c0e-180">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="59c0e-180">See notes.</span></span>      | <span data-ttu-id="59c0e-181">Stringa localizzata corrispondente al tipo di controllo **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="59c0e-181">Localized string corresponding to the **SplitButton** control type.</span></span> <span data-ttu-id="59c0e-182">Il valore predefinito è "Split Button" per en-US o English (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="59c0e-182">The default value is "split button" for en-US or English (United States).</span></span>                                                        |
| [<span data-ttu-id="59c0e-183">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="59c0e-184">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="59c0e-184">See notes.</span></span>      | <span data-ttu-id="59c0e-185">Testo utilizzato per assegnare un'etichetta al pulsante di suddivisione.</span><span class="sxs-lookup"><span data-stu-id="59c0e-185">The text that is used to label the split button.</span></span> <span data-ttu-id="59c0e-186">Ogni volta che viene usata un'immagine per etichettare un pulsante di suddivisione, è necessario specificare il testo alternativo per la proprietà nome pulsante di divisione.</span><span class="sxs-lookup"><span data-stu-id="59c0e-186">Whenever an image is used to label a split button, alternate text must be supplied for the split button Name property.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="59c0e-187">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="59c0e-187">Required Control Patterns</span></span>

<span data-ttu-id="59c0e-188">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli pulsante di comando combinato.</span><span class="sxs-lookup"><span data-stu-id="59c0e-188">The following table lists the UI Automation control patterns required to be supported by all split button controls.</span></span> <span data-ttu-id="59c0e-189">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="59c0e-189">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="59c0e-190">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="59c0e-190">Control Pattern</span></span>                                                   | <span data-ttu-id="59c0e-191">Supporto</span><span class="sxs-lookup"><span data-stu-id="59c0e-191">Support</span></span>  | <span data-ttu-id="59c0e-192">Note</span><span class="sxs-lookup"><span data-stu-id="59c0e-192">Notes</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59c0e-193">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="59c0e-193">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="59c0e-194">Necessario</span><span class="sxs-lookup"><span data-stu-id="59c0e-194">Required</span></span> | <span data-ttu-id="59c0e-195">Poiché i pulsanti Split hanno sempre la possibilità di espandere un elenco di opzioni, devono supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="59c0e-195">Because split buttons always have the ability to expand a list of options, they must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span>                                                      |
| [<span data-ttu-id="59c0e-196">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="59c0e-196">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="59c0e-197">Necessario</span><span class="sxs-lookup"><span data-stu-id="59c0e-197">Required</span></span> | <span data-ttu-id="59c0e-198">Poiché i pulsanti Split hanno sempre un'azione predefinita associata al metodo [**IInvokeProvider:: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="59c0e-198">Because split buttons always have a default action associated with the [**IInvokeProvider::Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) method, they must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="59c0e-199">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="59c0e-199">Required Events</span></span>

<span data-ttu-id="59c0e-200">La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli pulsante di suddivisione.</span><span class="sxs-lookup"><span data-stu-id="59c0e-200">The following table lists the UI Automation events that split button controls are required to support.</span></span> <span data-ttu-id="59c0e-201">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="59c0e-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="59c0e-202">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="59c0e-202">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="59c0e-203">Note</span><span class="sxs-lookup"><span data-stu-id="59c0e-203">Notes</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59c0e-204">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| <span data-ttu-id="59c0e-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="59c0e-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                            |
| <span data-ttu-id="59c0e-206">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="59c0e-206">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="59c0e-207">**\_Richiama \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="59c0e-207">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| <span data-ttu-id="59c0e-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="59c0e-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="59c0e-209">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="59c0e-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="59c0e-210">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="59c0e-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="59c0e-211">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="59c0e-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="59c0e-212">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="59c0e-212">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a><span data-ttu-id="59c0e-213">Esempio di tipo di controllo SplitButton</span><span class="sxs-lookup"><span data-stu-id="59c0e-213">SplitButton Control Type Example</span></span>

<span data-ttu-id="59c0e-214">Nell'immagine seguente viene illustrato un controllo che implementa il tipo di controllo **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="59c0e-214">The following image illustrates a control that implements the **SplitButton** control type.</span></span>

![screenshot che mostra l'esempio di un controllo SplitButton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59c0e-216">Albero di automazione interfaccia utente-visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="59c0e-216">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="59c0e-217">Albero di automazione interfaccia utente-visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="59c0e-217">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="59c0e-218">&quot;Nome SplitButton &quot; (Invoke, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="59c0e-218">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="59c0e-219">&quot;Opzione altro pulsante &quot; (richiama)</span><span class="sxs-lookup"><span data-stu-id="59c0e-219">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="59c0e-220">Menu</span><span class="sxs-lookup"><span data-stu-id="59c0e-220">Menu</span></span>
<ul>
<li><span data-ttu-id="59c0e-221">MenuItem</span><span class="sxs-lookup"><span data-stu-id="59c0e-221">MenuItem</span></span></li>
<li><span data-ttu-id="59c0e-222">...</span><span class="sxs-lookup"><span data-stu-id="59c0e-222">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59c0e-223">&quot;Nome SplitButton &quot; (Invoke, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="59c0e-223">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="59c0e-224">&quot;Opzione altro pulsante &quot; (richiama)</span><span class="sxs-lookup"><span data-stu-id="59c0e-224">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="59c0e-225">Menu</span><span class="sxs-lookup"><span data-stu-id="59c0e-225">Menu</span></span>
<ul>
<li><span data-ttu-id="59c0e-226">MenuItem</span><span class="sxs-lookup"><span data-stu-id="59c0e-226">MenuItem</span></span></li>
<li><span data-ttu-id="59c0e-227">...</span><span class="sxs-lookup"><span data-stu-id="59c0e-227">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="59c0e-228">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59c0e-228">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="59c0e-229">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="59c0e-229">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="59c0e-230">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="59c0e-230">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="59c0e-231">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="59c0e-231">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




