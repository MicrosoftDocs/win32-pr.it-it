---
title: Tipo di controllo Button
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Button
- Automazione interfaccia utente, tipo di controllo Button
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Button
- Automazione interfaccia utente, proprietà per il tipo di controllo Button
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Button
- Automazione interfaccia utente, eventi per il tipo di controllo Button
- strutture ad albero, tipo di controllo Button
- Proprietà, tipo di controllo Button
- pattern di controllo, tipo di controllo Button
- eventi, tipo di controllo Button
- supporto per il tipo di controllo Button
- Button (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Button
- tipi di controllo, pattern di controllo per il tipo di controllo Button
- tipi di controllo, supporto per Button
- tipi di controllo, pulsante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222111"
---
# <a name="button-control-type"></a><span data-ttu-id="1929e-119">Tipo di controllo Button</span><span class="sxs-lookup"><span data-stu-id="1929e-119">Button Control Type</span></span>

<span data-ttu-id="1929e-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Button** .</span><span class="sxs-lookup"><span data-stu-id="1929e-120">This topic provides information about Microsoft UI Automation support for the **Button** control type.</span></span>

<span data-ttu-id="1929e-121">Un pulsante è un oggetto che un utente usa per eseguire un'azione, ad esempio i pulsanti OK e Annulla in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1929e-121">A button is an object that a user interacts with to perform an action such as the OK and Cancel buttons on a dialog box.</span></span> <span data-ttu-id="1929e-122">Il controllo Button è un controllo semplice da esporre perché esegue il mapping a un unico comando che l'utente desidera completare.</span><span class="sxs-lookup"><span data-stu-id="1929e-122">The button control is a simple control to expose because it maps to a single command that the user wishes to complete.</span></span>

<span data-ttu-id="1929e-123">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Button** .</span><span class="sxs-lookup"><span data-stu-id="1929e-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Button** control type.</span></span> <span data-ttu-id="1929e-124">I requisiti di automazione interfaccia utente si applicano a tutti i controlli Button in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="1929e-124">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="1929e-125">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1929e-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1929e-126">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="1929e-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="1929e-127">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="1929e-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="1929e-128">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="1929e-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="1929e-129">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="1929e-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="1929e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1929e-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="1929e-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="1929e-131">Typical Tree Structure</span></span>

<span data-ttu-id="1929e-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli Button e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1929e-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="1929e-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="1929e-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1929e-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="1929e-134">Control View</span></span></th>
<th><span data-ttu-id="1929e-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="1929e-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="1929e-136">Pulsante</span><span class="sxs-lookup"><span data-stu-id="1929e-136">Button</span></span>
<ul>
<li><span data-ttu-id="1929e-137">Image (0 o più)</span><span class="sxs-lookup"><span data-stu-id="1929e-137">Image (0 or more)</span></span></li>
<li><span data-ttu-id="1929e-138">Text (0 o più)</span><span class="sxs-lookup"><span data-stu-id="1929e-138">Text (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1929e-139">Pulsante</span><span class="sxs-lookup"><span data-stu-id="1929e-139">Button</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="1929e-140">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="1929e-140">Relevant Properties</span></span>

<span data-ttu-id="1929e-141">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **Button** , ad esempio i controlli Button.</span><span class="sxs-lookup"><span data-stu-id="1929e-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **Button** control type (such as button controls).</span></span> <span data-ttu-id="1929e-142">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="1929e-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="1929e-143">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1929e-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="1929e-144">Valore</span><span class="sxs-lookup"><span data-stu-id="1929e-144">Value</span></span>      | <span data-ttu-id="1929e-145">Note</span><span class="sxs-lookup"><span data-stu-id="1929e-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1929e-146">**\_ACCELERATORKEYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-146">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="1929e-147">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-147">See notes.</span></span> | <span data-ttu-id="1929e-148">Un controllo Button in genere supporta un tasto di scelta rapida per consentire all'utente finale di eseguire rapidamente l'azione rappresentata dal pulsante dalla tastiera.</span><span class="sxs-lookup"><span data-stu-id="1929e-148">A button control typically supports an accelerator key to enable the end user to quickly perform the action represented by the button from the keyboard.</span></span>                                             |
| [<span data-ttu-id="1929e-149">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="1929e-150">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-150">See notes.</span></span> | <span data-ttu-id="1929e-151">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1929e-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="1929e-152">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="1929e-153">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-153">See notes.</span></span> | <span data-ttu-id="1929e-154">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="1929e-154">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="1929e-155">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="1929e-156">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-156">See notes.</span></span> | <span data-ttu-id="1929e-157">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="1929e-157">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="1929e-158">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="1929e-158">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="1929e-159">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-159">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="1929e-160">**Button**</span><span class="sxs-lookup"><span data-stu-id="1929e-160">**Button**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="1929e-161">**\_HELPTEXTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-161">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="1929e-162">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-162">See notes.</span></span> | <span data-ttu-id="1929e-163">Il testo della guida deve indicare quale sarà il risultato finale dell'attivazione del pulsante.</span><span class="sxs-lookup"><span data-stu-id="1929e-163">The help text should indicate what the end result of activating the button will be.</span></span> <span data-ttu-id="1929e-164">Si tratta in genere dello stesso tipo di informazioni visualizzate tramite una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="1929e-164">This is typically the same type of information presented through a tooltip.</span></span>                                      |
| [<span data-ttu-id="1929e-165">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="1929e-166">true</span><span class="sxs-lookup"><span data-stu-id="1929e-166">TRUE</span></span>       | <span data-ttu-id="1929e-167">Il controllo Button deve essere sempre di contenuto.</span><span class="sxs-lookup"><span data-stu-id="1929e-167">The button control must always be content.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="1929e-168">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="1929e-169">true</span><span class="sxs-lookup"><span data-stu-id="1929e-169">TRUE</span></span>       | <span data-ttu-id="1929e-170">Il controllo Button deve essere sempre un controllo.</span><span class="sxs-lookup"><span data-stu-id="1929e-170">The button control must always be a control.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="1929e-171">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="1929e-172">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-172">See notes.</span></span> | <span data-ttu-id="1929e-173">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="1929e-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="1929e-174">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="1929e-175">Null</span><span class="sxs-lookup"><span data-stu-id="1929e-175">Null</span></span>       | <span data-ttu-id="1929e-176">Ai controlli Button viene automaticamente applicata un'etichetta in base al relativo contenuto.</span><span class="sxs-lookup"><span data-stu-id="1929e-176">Button controls are self-labeled by their contents.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="1929e-177">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="1929e-178">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-178">See notes.</span></span> | <span data-ttu-id="1929e-179">Stringa localizzata corrispondente al tipo di controllo **Button** .</span><span class="sxs-lookup"><span data-stu-id="1929e-179">Localized string corresponding to the **Button** control type.</span></span> <span data-ttu-id="1929e-180">Il valore predefinito è "button" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="1929e-180">The default value is "button" for en-US or English (United States).</span></span>                                                                   |
| [<span data-ttu-id="1929e-181">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="1929e-182">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-182">See notes.</span></span> | <span data-ttu-id="1929e-183">Il nome del controllo Button è il testo utilizzato per etichettarlo.</span><span class="sxs-lookup"><span data-stu-id="1929e-183">The name of the button control is the text used to label it.</span></span> <span data-ttu-id="1929e-184">Ogni volta che viene usata un'immagine per etichettare un pulsante, è necessario specificare il testo alternativo per la proprietà **Name** del pulsante.</span><span class="sxs-lookup"><span data-stu-id="1929e-184">Whenever an image is used to label a button, alternate text must be supplied for the button's **Name** property.</span></span>                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="1929e-185">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="1929e-185">Required Control Patterns</span></span>

<span data-ttu-id="1929e-186">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli Button.</span><span class="sxs-lookup"><span data-stu-id="1929e-186">The following table lists the UI Automation control patterns required to be supported by all button controls.</span></span> <span data-ttu-id="1929e-187">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="1929e-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="1929e-188">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="1929e-188">Control Pattern/Pattern Property</span></span>                                  | <span data-ttu-id="1929e-189">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="1929e-189">Support/Value</span></span> | <span data-ttu-id="1929e-190">Note</span><span class="sxs-lookup"><span data-stu-id="1929e-190">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1929e-191">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="1929e-191">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="1929e-192">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-192">See notes.</span></span>    | <span data-ttu-id="1929e-193">Quando un pulsante viene ospitato come figlio di un pulsante di suddivisione, il pulsante figlio può supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) anziché il pattern di controllo [Invoke](uiauto-implementinginvoke.md) o [interruttore](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="1929e-193">When a button is hosted as a child of a split button, the child button can support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern instead of the [Invoke](uiauto-implementinginvoke.md) or [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="1929e-194">Il pattern di controllo ExpandCollapse può essere usato per l'apertura o la chiusura di un menu o di un'altra sottostruttura associata all'elemento Button.</span><span class="sxs-lookup"><span data-stu-id="1929e-194">The ExpandCollapse control pattern can be used for opening or closing a menu or other sub-structure associated with the button element.</span></span> |
| [<span data-ttu-id="1929e-195">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="1929e-195">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="1929e-196">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-196">See notes.</span></span>    | <span data-ttu-id="1929e-197">Tutti i pulsanti devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) o il pattern di controllo di [attivazione/](uiauto-implementingtoggle.md) disattivione, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="1929e-197">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="1929e-198">Il pattern di controllo Invoke deve essere supportato quando il pulsante esegue un comando su richiesta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1929e-198">The Invoke control pattern must be supported when the button performs a command at the request of the user.</span></span> <span data-ttu-id="1929e-199">Questo comando esegue il mapping a una singola operazione, ad esempio Taglia, Copia, Incolla o Elimina.</span><span class="sxs-lookup"><span data-stu-id="1929e-199">This command maps to a single operation such as Cut, Copy, Paste, or Delete.</span></span>                                                              |
| [<span data-ttu-id="1929e-200">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="1929e-200">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="1929e-201">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1929e-201">See notes.</span></span>    | <span data-ttu-id="1929e-202">Tutti i pulsanti devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) o il pattern di controllo di [attivazione/](uiauto-implementingtoggle.md) disattivione, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="1929e-202">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="1929e-203">Il pattern di controllo di attivazione/disattivazione deve essere supportato se il pulsante può scorrere una serie di un massimo di tre stati.</span><span class="sxs-lookup"><span data-stu-id="1929e-203">The Toggle control pattern must be supported if the button can cycle through a series of up to three states.</span></span> <span data-ttu-id="1929e-204">In genere viene interpretato come opzione di attivazione/disattivazione per funzionalità specifiche.</span><span class="sxs-lookup"><span data-stu-id="1929e-204">Typically this is seen as an on/off switch for specific features.</span></span>                                                                        |



 

## <a name="required-events"></a><span data-ttu-id="1929e-205">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="1929e-205">Required Events</span></span>

<span data-ttu-id="1929e-206">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli Button.</span><span class="sxs-lookup"><span data-stu-id="1929e-206">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="1929e-207">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="1929e-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="1929e-208">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1929e-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="1929e-209">Note</span><span class="sxs-lookup"><span data-stu-id="1929e-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1929e-210">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="1929e-211">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="1929e-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="1929e-212">**\_Richiama \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="1929e-212">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="1929e-213">Se il controllo supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1929e-213">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="1929e-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="1929e-214">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="1929e-215">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1929e-215">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="1929e-216">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="1929e-216">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="1929e-217">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1929e-217">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="1929e-218">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="1929e-218">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="1929e-219">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="1929e-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="1929e-220">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="1929e-220">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    | <span data-ttu-id="1929e-221">Se il controllo supporta il pattern di controllo [interruttore](uiauto-implementingtoggle.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1929e-221">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="1929e-222">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1929e-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1929e-223">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1929e-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1929e-224">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1929e-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="1929e-225">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1929e-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




