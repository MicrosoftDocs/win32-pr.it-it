---
title: Tipo di controllo HyperLink
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo HyperLink
- Automazione interfaccia utente, tipo di controllo HyperLink
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo HyperLink
- Automazione interfaccia utente, proprietà per il tipo di controllo HyperLink
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo HyperLink
- Automazione interfaccia utente, eventi per il tipo di controllo HyperLink
- strutture ad albero, tipo di controllo HyperLink
- Proprietà, tipo di controllo HyperLink
- pattern di controllo, tipo di controllo HyperLink
- eventi, tipo di controllo HyperLink
- supporto per il tipo di controllo HyperLink
- Hyperlink (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo HyperLink
- tipi di controllo, pattern di controllo per il tipo di controllo HyperLink
- tipi di controllo, supporto per collegamento ipertestuale
- tipi di controllo, collegamento ipertestuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710312"
---
# <a name="hyperlink-control-type"></a><span data-ttu-id="d80ea-119">Tipo di controllo HyperLink</span><span class="sxs-lookup"><span data-stu-id="d80ea-119">Hyperlink Control Type</span></span>

<span data-ttu-id="d80ea-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="d80ea-120">This topic provides information about Microsoft UI Automation support for the **Hyperlink** control type.</span></span>

<span data-ttu-id="d80ea-121">I controlli collegamento ipertestuale creano collegamenti che consentono agli utenti di spostarsi all'interno della stessa pagina o da una pagina all'altra.</span><span class="sxs-lookup"><span data-stu-id="d80ea-121">Hyperlink controls create links that enable users to navigate within the same page, or from one page to another.</span></span>

<span data-ttu-id="d80ea-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="d80ea-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Hyperlink** control type.</span></span> <span data-ttu-id="d80ea-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli collegamento ipertestuale in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e</span><span class="sxs-lookup"><span data-stu-id="d80ea-123">The UI Automation requirements apply to all hyperlink controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="d80ea-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d80ea-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d80ea-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="d80ea-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="d80ea-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="d80ea-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="d80ea-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="d80ea-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="d80ea-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="d80ea-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="d80ea-129">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="d80ea-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="d80ea-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d80ea-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="d80ea-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="d80ea-131">Typical Tree Structure</span></span>

<span data-ttu-id="d80ea-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli collegamento ipertestuale e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d80ea-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to hyperlink controls and describes what can be contained in each view.</span></span> <span data-ttu-id="d80ea-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d80ea-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d80ea-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="d80ea-134">Control View</span></span></th>
<th><span data-ttu-id="d80ea-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="d80ea-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d80ea-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="d80ea-136">Hyperlink</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d80ea-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="d80ea-137">Hyperlink</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="d80ea-138">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="d80ea-138">Relevant Properties</span></span>

<span data-ttu-id="d80ea-139">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="d80ea-139">The following table lists the UI Automation properties whose value or definition is especially relevant to the hyperlink controls.</span></span> <span data-ttu-id="d80ea-140">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="d80ea-140">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="d80ea-141">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d80ea-141">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="d80ea-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d80ea-142">Value</span></span>         | <span data-ttu-id="d80ea-143">Note</span><span class="sxs-lookup"><span data-stu-id="d80ea-143">Notes</span></span>                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d80ea-144">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-144">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="d80ea-145">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d80ea-145">See notes.</span></span>    | <span data-ttu-id="d80ea-146">Il valore di questa proprietà deve essere univoco in tutti i controlli in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d80ea-146">The value of this property must be unique across all controls in an application.</span></span>                                                         |
| [<span data-ttu-id="d80ea-147">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-147">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="d80ea-148">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d80ea-148">See notes.</span></span>    | <span data-ttu-id="d80ea-149">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="d80ea-149">The outermost rectangle that contains the whole control.</span></span>                                                                                 |
| [<span data-ttu-id="d80ea-150">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-150">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="d80ea-151">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d80ea-151">See notes.</span></span>    | <span data-ttu-id="d80ea-152">Il punto selezionabile del controllo collegamento ipertestuale deve essere un punto che avvia il collegamento ipertestuale se viene selezionato con un puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="d80ea-152">The hyperlink control's clickable point must be a point that launches the hyperlink if clicked with a mouse pointer.</span></span>                     |
| [<span data-ttu-id="d80ea-153">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d80ea-154">**Collegamento ipertestuale**</span><span class="sxs-lookup"><span data-stu-id="d80ea-154">**Hyperlink**</span></span> |                                                                                                                                          |
| [<span data-ttu-id="d80ea-155">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-155">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d80ea-156">true</span><span class="sxs-lookup"><span data-stu-id="d80ea-156">TRUE</span></span>          | <span data-ttu-id="d80ea-157">Il controllo HyperLink viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d80ea-157">The hyperlink control is always included in the content view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="d80ea-158">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-158">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d80ea-159">true</span><span class="sxs-lookup"><span data-stu-id="d80ea-159">TRUE</span></span>          | <span data-ttu-id="d80ea-160">Il controllo HyperLink viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d80ea-160">The hyperlink control is always included in the control view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="d80ea-161">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-161">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="d80ea-162">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d80ea-162">See notes.</span></span>    | <span data-ttu-id="d80ea-163">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="d80ea-163">If the control can receive keyboard focus, it must support this property.</span></span>                                                                |
| [<span data-ttu-id="d80ea-164">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="d80ea-165">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d80ea-165">See notes.</span></span>    | <span data-ttu-id="d80ea-166">Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.</span><span class="sxs-lookup"><span data-stu-id="d80ea-166">If there is a static text label, this property must expose a reference to that control.</span></span>                                                  |
| [<span data-ttu-id="d80ea-167">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-167">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="d80ea-168">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d80ea-168">See notes.</span></span>    | <span data-ttu-id="d80ea-169">Stringa localizzata corrispondente al tipo di controllo **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="d80ea-169">Localized string corresponding to the **Hyperlink** control type.</span></span> <span data-ttu-id="d80ea-170">Il valore predefinito è "Hyperlink" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="d80ea-170">The default value is "hyperlink" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="d80ea-171">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-171">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="d80ea-172">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d80ea-172">See notes.</span></span>    | <span data-ttu-id="d80ea-173">Il nome del controllo HyperLink è il testo visualizzato sullo schermo sotto forma di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="d80ea-173">The hyperlink control's name is the text that is displayed on the screen as underlined.</span></span>                                                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="d80ea-174">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="d80ea-174">Required Control Patterns</span></span>

<span data-ttu-id="d80ea-175">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente necessari per supportare i controlli collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="d80ea-175">The following table lists the UI Automation control patterns that hyperlink controls are required to support.</span></span> <span data-ttu-id="d80ea-176">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d80ea-176">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="d80ea-177">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="d80ea-177">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="d80ea-178">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="d80ea-178">Support/Value</span></span>                | <span data-ttu-id="d80ea-179">Note</span><span class="sxs-lookup"><span data-stu-id="d80ea-179">Notes</span></span>                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d80ea-180">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="d80ea-180">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | <span data-ttu-id="d80ea-181">Necessario</span><span class="sxs-lookup"><span data-stu-id="d80ea-181">Required</span></span>                     | <span data-ttu-id="d80ea-182">Tutti i controlli collegamento ipertestuale devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="d80ea-182">All hyperlink controls must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="d80ea-183">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d80ea-183">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="d80ea-184">Dipende da</span><span class="sxs-lookup"><span data-stu-id="d80ea-184">Depends</span></span>                      | <span data-ttu-id="d80ea-185">I controlli collegamento ipertestuale devono supportare il pattern di controllo [value](uiauto-implementingvalue.md) quando il collegamento contiene informazioni utilizzabili e significative per l'utente.</span><span class="sxs-lookup"><span data-stu-id="d80ea-185">Hyperlink controls should support the [Value](uiauto-implementingvalue.md) control pattern when the link contains information that is usable and meaningful to the user.</span></span>                                                                              |
| [<span data-ttu-id="d80ea-186">**Valore**</span><span class="sxs-lookup"><span data-stu-id="d80ea-186">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | <span data-ttu-id="d80ea-187">Ad esempio, "https://www..".</span><span class="sxs-lookup"><span data-stu-id="d80ea-187">For example, "https://www..."</span></span> | <span data-ttu-id="d80ea-188">Un URL per un indirizzo Internet o Intranet è un esempio di collegamento ipertestuale contenente informazioni significative per l'utente.</span><span class="sxs-lookup"><span data-stu-id="d80ea-188">A URL for an Internet or intranet address is an example of a hyperlink that contains information that is meaningful to the user.</span></span> <span data-ttu-id="d80ea-189">Un collegamento a livello di codice, tuttavia, è significativo solo per un'applicazione e non è consigliato per la proprietà **value** .</span><span class="sxs-lookup"><span data-stu-id="d80ea-189">A programmatic link, however, is meaningful only to an application and is not recommended for the **Value** property.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="d80ea-190">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="d80ea-190">Required Events</span></span>

<span data-ttu-id="d80ea-191">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="d80ea-191">The following table lists the UI Automation events that hyperlink controls are required to support.</span></span> <span data-ttu-id="d80ea-192">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d80ea-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="d80ea-193">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d80ea-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="d80ea-194">Note</span><span class="sxs-lookup"><span data-stu-id="d80ea-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d80ea-195">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="d80ea-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d80ea-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="d80ea-197">**\_Richiama \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="d80ea-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     |                                                                                                                            |
| <span data-ttu-id="d80ea-198">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d80ea-198">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="d80ea-199">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="d80ea-199">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="d80ea-200">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d80ea-200">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="d80ea-201">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="d80ea-201">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="d80ea-202">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="d80ea-202">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="d80ea-203">Commenti</span><span class="sxs-lookup"><span data-stu-id="d80ea-203">Remarks</span></span>

<span data-ttu-id="d80ea-204">Il tipo di controllo collegamento ipertestuale deve essere applicato solo a un oggetto che, se selezionato, causa la navigazione; non deve essere applicato al contenitore del collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="d80ea-204">The Hyperlink control type should be applied only to an object that, when clicked, causes navigation to occur; it should not be applied to the container of the hyperlink.</span></span> <span data-ttu-id="d80ea-205">Ad esempio, solo le "aree sensibili" selezionabili all'interno di una mappa immagine dovrebbero avere il tipo di controllo **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="d80ea-205">For example, only the clickable "hot spots" inside an image map should have the **Hyperlink** control type.</span></span> <span data-ttu-id="d80ea-206">Lo stesso vale per i collegamenti ipertestuali in un campo di testo o un contenitore di documenti.</span><span class="sxs-lookup"><span data-stu-id="d80ea-206">The same is true of hyperlinks in a text field or document container.</span></span> <span data-ttu-id="d80ea-207">In questo caso, solo il testo o l'immagine del collegamento ipertestuale deve avere il tipo di controllo **Hyperlink** , non il contenitore.</span><span class="sxs-lookup"><span data-stu-id="d80ea-207">In this case, only the hyperlink text or image should have the **Hyperlink** control type, not the container.</span></span>

<span data-ttu-id="d80ea-208">Il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) è ideale per il supporto di collegamenti ipertestuali incorporati in elementi di testo o documento.</span><span class="sxs-lookup"><span data-stu-id="d80ea-208">The [Text](uiauto-implementingtextandtextrange.md) control pattern is ideal for supporting embedded hyperlinks in text or document elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d80ea-209">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d80ea-209">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d80ea-210">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d80ea-210">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d80ea-211">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d80ea-211">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d80ea-212">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d80ea-212">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




