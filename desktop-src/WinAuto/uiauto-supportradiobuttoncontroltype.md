---
title: RadioButton (tipo di controllo)
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo RadioButton
- Automazione interfaccia utente, tipo di controllo RadioButton
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo RadioButton
- Automazione interfaccia utente, proprietà per il tipo di controllo RadioButton
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo RadioButton
- Automazione interfaccia utente, eventi per il tipo di controllo RadioButton
- strutture ad albero, tipo di controllo RadioButton
- Proprietà, tipo di controllo RadioButton
- pattern di controllo, tipo di controllo RadioButton
- eventi, tipo di controllo RadioButton
- supporto per il tipo di controllo RadioButton
- RadioButton (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo RadioButton
- tipi di controllo, pattern di controllo per il tipo di controllo RadioButton
- tipi di controllo, supporto per RadioButton
- tipi di controllo, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712703"
---
# <a name="radiobutton-control-type"></a><span data-ttu-id="82b3d-119">RadioButton (tipo di controllo)</span><span class="sxs-lookup"><span data-stu-id="82b3d-119">RadioButton Control Type</span></span>

<span data-ttu-id="82b3d-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="82b3d-120">This topic provides information about Microsoft UI Automation support for the **RadioButton** control type.</span></span>

<span data-ttu-id="82b3d-121">Un pulsante di opzione è composto da un pulsante circolare e testo definito dall'applicazione (etichetta), un'icona o una bitmap che indica una scelta che l'utente può effettuare selezionando il pulsante.</span><span class="sxs-lookup"><span data-stu-id="82b3d-121">A radio button consists of a round button and application-defined text (a label), an icon, or a bitmap that indicates a choice the user can make by selecting the button.</span></span> <span data-ttu-id="82b3d-122">Un'applicazione usa in genere i pulsanti di opzione in una casella di gruppo per consentire all'utente di effettuare la scelta da un set di opzioni correlate che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="82b3d-122">An application typically uses radio buttons in a group box to permit the user to choose from a set of related, but mutually exclusive options.</span></span> <span data-ttu-id="82b3d-123">Ad esempio, l'applicazione potrebbe visualizzare un gruppo di pulsanti di opzione da cui l'utente può selezionare una preferenza di formato per il testo selezionato nell'area client.</span><span class="sxs-lookup"><span data-stu-id="82b3d-123">For example, the application might present a group of radio buttons from which the user can select a format preference for text selected in the client area.</span></span> <span data-ttu-id="82b3d-124">L'utente può selezionare un formato allineato a sinistra, a destra oppure centrato selezionando il pulsante di opzione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="82b3d-124">The user could select a left-aligned, right-aligned, or centered format by selecting the corresponding radio button.</span></span> <span data-ttu-id="82b3d-125">In genere, l'utente può selezionare una sola opzione alla volta da un set di pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="82b3d-125">Typically, the user can select only one option at a time from a set of radio buttons.</span></span>

> [!Note]  
> <span data-ttu-id="82b3d-126">Un'altra generalizzazione del controllo per i pulsanti in cui è possibile selezionare solo un gruppo è il contenuto di un interruttore.</span><span class="sxs-lookup"><span data-stu-id="82b3d-126">Another control generalization for buttons where only one in a group can be selected is the content of a toggle button.</span></span> <span data-ttu-id="82b3d-127">Alcuni framework dell'interfaccia utente considerano un pulsante di opzione come interruttore specializzato.</span><span class="sxs-lookup"><span data-stu-id="82b3d-127">Some UI frameworks consider a radio button to be a specialized toggle button.</span></span>

 

<span data-ttu-id="82b3d-128">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="82b3d-128">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **RadioButton** control type.</span></span> <span data-ttu-id="82b3d-129">I requisiti di automazione interfaccia utente si applicano a tutti i controlli Button in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="82b3d-129">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="82b3d-130">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="82b3d-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="82b3d-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="82b3d-131">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="82b3d-132">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="82b3d-132">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="82b3d-133">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="82b3d-133">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="82b3d-134">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="82b3d-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="82b3d-135">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="82b3d-135">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="82b3d-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82b3d-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="82b3d-137">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="82b3d-137">Typical Tree Structure</span></span>

<span data-ttu-id="82b3d-138">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli pulsante di opzione e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="82b3d-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to radio button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="82b3d-139">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="82b3d-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82b3d-140">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="82b3d-140">Control View</span></span></th>
<th><span data-ttu-id="82b3d-141">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="82b3d-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="82b3d-142">RadioButton</span><span class="sxs-lookup"><span data-stu-id="82b3d-142">RadioButton</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="82b3d-143">RadioButton</span><span class="sxs-lookup"><span data-stu-id="82b3d-143">RadioButton</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="82b3d-144">Non sono presenti elementi figli nella visualizzazione controlli o nella visualizzazione contenuto.</span><span class="sxs-lookup"><span data-stu-id="82b3d-144">There are no children in the control view or the content view.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="82b3d-145">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="82b3d-145">Relevant Properties</span></span>

<span data-ttu-id="82b3d-146">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **RadioButton** , ad esempio i controlli Button.</span><span class="sxs-lookup"><span data-stu-id="82b3d-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **RadioButton** control type (such as button controls).</span></span> <span data-ttu-id="82b3d-147">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="82b3d-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="82b3d-148">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="82b3d-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="82b3d-149">Valore</span><span class="sxs-lookup"><span data-stu-id="82b3d-149">Value</span></span>           | <span data-ttu-id="82b3d-150">Note</span><span class="sxs-lookup"><span data-stu-id="82b3d-150">Notes</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82b3d-151">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="82b3d-152">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="82b3d-152">See notes.</span></span>      | <span data-ttu-id="82b3d-153">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="82b3d-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                  |
| [<span data-ttu-id="82b3d-154">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="82b3d-155">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="82b3d-155">See notes.</span></span>      | <span data-ttu-id="82b3d-156">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="82b3d-156">The outermost rectangle that contains the whole control.</span></span>                                                                                      |
| [<span data-ttu-id="82b3d-157">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="82b3d-158">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="82b3d-158">See notes.</span></span>      | <span data-ttu-id="82b3d-159">Il punto selezionabile deve essere un punto che, quando selezionato, seleziona il pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="82b3d-159">The clickable point must be a point that, when clicked, selects the radio button.</span></span>                                                             |
| [<span data-ttu-id="82b3d-160">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="82b3d-161">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="82b3d-161">**RadioButton**</span></span> |                                                                                                                                               |
| [<span data-ttu-id="82b3d-162">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="82b3d-163">true</span><span class="sxs-lookup"><span data-stu-id="82b3d-163">TRUE</span></span>            | <span data-ttu-id="82b3d-164">Il controllo pulsante di opzione viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="82b3d-164">The radio button control is always included in the content view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="82b3d-165">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-165">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="82b3d-166">true</span><span class="sxs-lookup"><span data-stu-id="82b3d-166">TRUE</span></span>            | <span data-ttu-id="82b3d-167">Il controllo pulsante di opzione viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="82b3d-167">The radio button control is always included in the control view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="82b3d-168">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-168">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="82b3d-169">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="82b3d-169">See notes.</span></span>      | <span data-ttu-id="82b3d-170">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="82b3d-170">If the control can receive keyboard focus, it must support this property.</span></span>                                                                     |
| [<span data-ttu-id="82b3d-171">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="82b3d-172">NULL</span><span class="sxs-lookup"><span data-stu-id="82b3d-172">NULL</span></span>            | <span data-ttu-id="82b3d-173">I controlli pulsante di opzione hanno un'etichetta automatica in base al relativo contenuto.</span><span class="sxs-lookup"><span data-stu-id="82b3d-173">Radio button controls are self-labeled by their contents.</span></span>                                                                                     |
| [<span data-ttu-id="82b3d-174">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="82b3d-175">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="82b3d-175">See notes.</span></span>      | <span data-ttu-id="82b3d-176">Stringa localizzata corrispondente al tipo di controllo **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="82b3d-176">Localized string corresponding to the **RadioButton** control type.</span></span> <span data-ttu-id="82b3d-177">Il valore predefinito è "pulsante di opzione" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="82b3d-177">The default value is "radio button" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="82b3d-178">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="82b3d-179">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="82b3d-179">See notes.</span></span>      | <span data-ttu-id="82b3d-180">Il nome del controllo pulsante di opzione è il testo visualizzato accanto al pulsante che mantiene lo stato di selezione.</span><span class="sxs-lookup"><span data-stu-id="82b3d-180">The name of the radio button control is the text that is displayed beside the button that maintains the selection state.</span></span>                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="82b3d-181">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="82b3d-181">Required Control Patterns</span></span>

<span data-ttu-id="82b3d-182">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="82b3d-182">The following table lists the UI Automation control patterns required to be supported by all radio button controls.</span></span> <span data-ttu-id="82b3d-183">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="82b3d-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="82b3d-184">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="82b3d-184">Control Pattern/Pattern Property</span></span>                                               | <span data-ttu-id="82b3d-185">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="82b3d-185">Support/Value</span></span> | <span data-ttu-id="82b3d-186">Note</span><span class="sxs-lookup"><span data-stu-id="82b3d-186">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82b3d-187">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="82b3d-187">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | <span data-ttu-id="82b3d-188">Necessario</span><span class="sxs-lookup"><span data-stu-id="82b3d-188">Required</span></span>      | <span data-ttu-id="82b3d-189">Tutti i controlli pulsante di opzione devono supportare il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) per abilitarne la selezione.</span><span class="sxs-lookup"><span data-stu-id="82b3d-189">All radio button controls must support the [SelectionItem](uiauto-implementingselectionitem.md) control pattern to enable themselves to be selected.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="82b3d-190">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="82b3d-190">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | <span data-ttu-id="82b3d-191">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="82b3d-191">See notes.</span></span>    | <span data-ttu-id="82b3d-192">La proprietà [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) deve sempre essere completata in modo che un client di automazione interfaccia utente possa determinare quali altri pulsanti di opzione in un contesto specifico sono correlati tra loro.</span><span class="sxs-lookup"><span data-stu-id="82b3d-192">The [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) property must always be completed so that a UI Automation client can determine what other radio buttons within a specific context relate to one another.</span></span> <span data-ttu-id="82b3d-193">Per la versione Microsoft Win32 del pulsante di opzione, questa proprietà non è supportata perché non è possibile ottenere queste informazioni da tale framework legacy.</span><span class="sxs-lookup"><span data-stu-id="82b3d-193">For the Microsoft Win32 version of the radio button, this property is not supported because it is not possible to obtain this information from that legacy framework.</span></span> |
| [<span data-ttu-id="82b3d-194">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="82b3d-194">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | <span data-ttu-id="82b3d-195">Mai</span><span class="sxs-lookup"><span data-stu-id="82b3d-195">Never</span></span>         | <span data-ttu-id="82b3d-196">Dopo aver impostato questa proprietà, il pulsante di opzione non può scorrere tra i propri stati.</span><span class="sxs-lookup"><span data-stu-id="82b3d-196">The radio button cannot cycle through its state once it has been set.</span></span> <span data-ttu-id="82b3d-197">Il pattern di controllo di [attivazione/disattivazione](uiauto-implementingtoggle.md) non deve mai essere supportato su un pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="82b3d-197">The [Toggle](uiauto-implementingtoggle.md) control pattern must never be supported on a radio button.</span></span>                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="82b3d-198">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="82b3d-198">Required Events</span></span>

<span data-ttu-id="82b3d-199">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli Button.</span><span class="sxs-lookup"><span data-stu-id="82b3d-199">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="82b3d-200">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="82b3d-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="82b3d-201">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="82b3d-201">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="82b3d-202">Note</span><span class="sxs-lookup"><span data-stu-id="82b3d-202">Notes</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82b3d-203">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                                |
| <span data-ttu-id="82b3d-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="82b3d-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                                |
| <span data-ttu-id="82b3d-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="82b3d-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="82b3d-206">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="82b3d-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="82b3d-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="82b3d-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="82b3d-208">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="82b3d-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>     |
| [<span data-ttu-id="82b3d-209">**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="82b3d-209">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="82b3d-210">Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="82b3d-210">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="82b3d-211">**\_ElementSelectedEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="82b3d-211">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="82b3d-212">Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="82b3d-212">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="82b3d-213">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="82b3d-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="82b3d-214">Commenti</span><span class="sxs-lookup"><span data-stu-id="82b3d-214">Remarks</span></span>

<span data-ttu-id="82b3d-215">Un pulsante di opzione rappresenta una singola opzione selezionabile tra un gruppo di pulsanti di opzione peer.</span><span class="sxs-lookup"><span data-stu-id="82b3d-215">A radio button represents a single selectable option among a group of peer radio buttons.</span></span> <span data-ttu-id="82b3d-216">Idealmente, i pulsanti di opzione devono avere un elemento Grouping che chiarisca i limiti dei pulsanti di opzione peer.</span><span class="sxs-lookup"><span data-stu-id="82b3d-216">Ideally, radio buttons should have a grouping element that clarifies the boundaries of the peer radio buttons.</span></span> <span data-ttu-id="82b3d-217">Spesso, tuttavia, il limite è implicito nella struttura degli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="82b3d-217">Often, however, the boundary is implied by the UI element structure.</span></span> <span data-ttu-id="82b3d-218">Un menu, ad esempio, può contenere un set di pulsanti di opzione consecutivi anziché voci di menu o un set di pulsanti di opzione che si verificano dopo un'etichetta di gruppo, ma prima di un elemento di cui è possibile eseguire l'azione, ad esempio un pulsante.</span><span class="sxs-lookup"><span data-stu-id="82b3d-218">For example, a menu might contain a set of consecutive radio buttons instead of menu items, or a set of radio buttons that occur after a group label, but before an actionable element such as button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82b3d-219">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82b3d-219">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="82b3d-220">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="82b3d-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="82b3d-221">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="82b3d-221">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="82b3d-222">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="82b3d-222">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




