---
title: Tipo di controllo Document
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Document.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Document
- Automazione interfaccia utente, tipo di controllo Document
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Document
- Automazione interfaccia utente, proprietà per il tipo di controllo Document
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Document
- Automazione interfaccia utente, eventi per il tipo di controllo Document
- strutture ad albero, tipo di controllo Document
- Proprietà, tipo di controllo Document
- pattern di controllo, tipo di controllo Document
- eventi, tipo di controllo Document
- supporto per il tipo di controllo Document
- Document (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Document
- tipi di controllo, pattern di controllo per il tipo di controllo Document
- tipi di controllo, supporto per documenti
- tipi di controllo, documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044608"
---
# <a name="document-control-type"></a><span data-ttu-id="0205a-119">Tipo di controllo Document</span><span class="sxs-lookup"><span data-stu-id="0205a-119">Document Control Type</span></span>

<span data-ttu-id="0205a-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Document** .</span><span class="sxs-lookup"><span data-stu-id="0205a-120">This topic provides information about Microsoft UI Automation support for the **Document** control type.</span></span>

<span data-ttu-id="0205a-121">I controlli Document consentono a un utente di visualizzare e modificare più pagine di testo.</span><span class="sxs-lookup"><span data-stu-id="0205a-121">Document controls let a user view and manipulate multiple pages of text.</span></span> <span data-ttu-id="0205a-122">A differenza dei controlli di modifica che supportano solo una semplice riga di testo non formattato, i controlli documento possono ospitare testo con stili e formattazione avanzati</span><span class="sxs-lookup"><span data-stu-id="0205a-122">Unlike edit controls which only support a simple line of unformatted text, document controls can host text that is richly styled and formatted</span></span>

<span data-ttu-id="0205a-123">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Document** .</span><span class="sxs-lookup"><span data-stu-id="0205a-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Document** control type.</span></span> <span data-ttu-id="0205a-124">I requisiti di automazione interfaccia utente si applicano a tutti i controlli dei documenti in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern</span><span class="sxs-lookup"><span data-stu-id="0205a-124">The UI Automation requirements apply to all document controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0205a-125">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="0205a-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0205a-126">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="0205a-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0205a-127">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="0205a-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0205a-128">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="0205a-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0205a-129">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="0205a-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0205a-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0205a-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0205a-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="0205a-131">Typical Tree Structure</span></span>

<span data-ttu-id="0205a-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli documento e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0205a-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to document controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0205a-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0205a-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0205a-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="0205a-134">Control View</span></span></th>
<th><span data-ttu-id="0205a-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="0205a-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0205a-136">Documento</span><span class="sxs-lookup"><span data-stu-id="0205a-136">Document</span></span>
<ul>
<li><span data-ttu-id="0205a-137">Varia</span><span class="sxs-lookup"><span data-stu-id="0205a-137">Varies</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0205a-138">Documento</span><span class="sxs-lookup"><span data-stu-id="0205a-138">Document</span></span>
<ul>
<li><span data-ttu-id="0205a-139">Varia</span><span class="sxs-lookup"><span data-stu-id="0205a-139">Varies</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="0205a-140">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="0205a-140">Relevant Properties</span></span>

<span data-ttu-id="0205a-141">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli documento.</span><span class="sxs-lookup"><span data-stu-id="0205a-141">The following table lists the UI Automation properties whose value or definition is especially relevant to document controls.</span></span> <span data-ttu-id="0205a-142">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="0205a-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0205a-143">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0205a-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="0205a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="0205a-144">Value</span></span>        | <span data-ttu-id="0205a-145">Note</span><span class="sxs-lookup"><span data-stu-id="0205a-145">Notes</span></span>                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0205a-146">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="0205a-147">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0205a-147">See notes.</span></span>   | <span data-ttu-id="0205a-148">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0205a-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                      |
| [<span data-ttu-id="0205a-149">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="0205a-150">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0205a-150">See notes.</span></span>   | <span data-ttu-id="0205a-151">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="0205a-151">The outermost rectangle that contains the whole control.</span></span>                                                                                          |
| [<span data-ttu-id="0205a-152">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="0205a-153">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0205a-153">See notes.</span></span>   | <span data-ttu-id="0205a-154">Il documento ha un punto selezionabile che farà passare lo stato attivo sul documento o su uno degli elementi nel documento contenitore.</span><span class="sxs-lookup"><span data-stu-id="0205a-154">The document has a clickable point that will cause the document of one of its elements in the document container to have focus.</span></span>                   |
| [<span data-ttu-id="0205a-155">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0205a-156">**Documento**</span><span class="sxs-lookup"><span data-stu-id="0205a-156">**Document**</span></span> |                                                                                                                                                   |
| [<span data-ttu-id="0205a-157">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0205a-158">true</span><span class="sxs-lookup"><span data-stu-id="0205a-158">TRUE</span></span>         | <span data-ttu-id="0205a-159">Il controllo documento viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0205a-159">The document control is always included in the content view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="0205a-160">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0205a-161">true</span><span class="sxs-lookup"><span data-stu-id="0205a-161">TRUE</span></span>         | <span data-ttu-id="0205a-162">Il controllo documento viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0205a-162">The document control is always included in the control view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="0205a-163">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="0205a-164">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0205a-164">See notes.</span></span>   | <span data-ttu-id="0205a-165">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0205a-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                         |
| [<span data-ttu-id="0205a-166">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="0205a-167">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0205a-167">See notes.</span></span>   | <span data-ttu-id="0205a-168">Il valore di questa proprietà deve essere l'etichetta del controllo documento.</span><span class="sxs-lookup"><span data-stu-id="0205a-168">The value of this property should be the label of the document control.</span></span> <span data-ttu-id="0205a-169">In genere, viene usato il titolo del documento.</span><span class="sxs-lookup"><span data-stu-id="0205a-169">Typically, the title of the document is used.</span></span>                             |
| [<span data-ttu-id="0205a-170">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0205a-171">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0205a-171">See notes.</span></span>   | <span data-ttu-id="0205a-172">Stringa localizzata corrispondente al tipo di controllo **Document** .</span><span class="sxs-lookup"><span data-stu-id="0205a-172">Localized string corresponding to the **Document** control type.</span></span> <span data-ttu-id="0205a-173">Il valore predefinito è "Document" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="0205a-173">The default value is "document" for en-US or English (United States).</span></span>            |
| [<span data-ttu-id="0205a-174">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-174">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="0205a-175">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0205a-175">See notes.</span></span>   | <span data-ttu-id="0205a-176">Il controllo documento in genere ottiene il nome dal nome file da cui viene caricato.</span><span class="sxs-lookup"><span data-stu-id="0205a-176">The document control typically gets its name from the file name it is loaded from.</span></span> <span data-ttu-id="0205a-177">Viene spesso visualizzato nel titolo di una finestra o di un frame contenitore.</span><span class="sxs-lookup"><span data-stu-id="0205a-177">This is often displayed in a containing window or frame title.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0205a-178">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="0205a-178">Required Control Patterns</span></span>

<span data-ttu-id="0205a-179">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli documento.</span><span class="sxs-lookup"><span data-stu-id="0205a-179">The following table lists the UI Automation control patterns required to be supported by document controls.</span></span> <span data-ttu-id="0205a-180">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0205a-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="0205a-181">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="0205a-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="0205a-182">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="0205a-182">Support/Value</span></span> | <span data-ttu-id="0205a-183">Note</span><span class="sxs-lookup"><span data-stu-id="0205a-183">Notes</span></span>                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0205a-184">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="0205a-184">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | <span data-ttu-id="0205a-185">Dipende da</span><span class="sxs-lookup"><span data-stu-id="0205a-185">Depends</span></span>       | <span data-ttu-id="0205a-186">Il controllo documento può estendersi oltre il riquadro di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0205a-186">The document control can span larger than that span of the viewport.</span></span> <span data-ttu-id="0205a-187">Il controllo deve supportare il pattern di controllo [Scroll](uiauto-implementingscroll.md) se il contenuto è scorrevole.</span><span class="sxs-lookup"><span data-stu-id="0205a-187">The control should support the [Scroll](uiauto-implementingscroll.md) control pattern if the content is scrollable.</span></span>                                                                                                                              |
| [<span data-ttu-id="0205a-188">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="0205a-188">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | <span data-ttu-id="0205a-189">Necessario</span><span class="sxs-lookup"><span data-stu-id="0205a-189">Required</span></span>      | <span data-ttu-id="0205a-190">Tutti i controlli documento devono supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="0205a-190">All document controls must support the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="0205a-191">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="0205a-191">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="0205a-192">Dipende da</span><span class="sxs-lookup"><span data-stu-id="0205a-192">Depends</span></span>       | <span data-ttu-id="0205a-193">Sebbene i client di automazione interfaccia utente possano usare [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) per ottenere informazioni di testo su un documento, hanno bisogno del pattern di controllo [value](uiauto-implementingvalue.md) per impostare il valore interno.</span><span class="sxs-lookup"><span data-stu-id="0205a-193">While UI Automation clients can use [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) to obtain text information about a document, they need the [Value](uiauto-implementingvalue.md) control pattern to set the inner value.</span></span> <span data-ttu-id="0205a-194">La voce di testo semplice è possibile solo tramite il pattern di controllo value.</span><span class="sxs-lookup"><span data-stu-id="0205a-194">Simple text entry is possible only through the Value control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="0205a-195">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="0205a-195">Required Events</span></span>

<span data-ttu-id="0205a-196">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli documento.</span><span class="sxs-lookup"><span data-stu-id="0205a-196">The following table lists the UI Automation events that document controls are required to support.</span></span> <span data-ttu-id="0205a-197">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0205a-197">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0205a-198">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0205a-198">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="0205a-199">Note</span><span class="sxs-lookup"><span data-stu-id="0205a-199">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0205a-200">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-200">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="0205a-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-201">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="0205a-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-202">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="0205a-203">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-203">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="0205a-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-204">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="0205a-205">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-205">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="0205a-206">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-206">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| <span data-ttu-id="0205a-207">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-207">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="0205a-208">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-208">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="0205a-209">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-209">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="0205a-210">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-210">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="0205a-211">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-211">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="0205a-212">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-212">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="0205a-213">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-213">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="0205a-214">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-214">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="0205a-215">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-215">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="0205a-216">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-216">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="0205a-217">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-217">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="0205a-218">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-218">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="0205a-219">**\_InvalidatedEventId selezione \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-219">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            | <span data-ttu-id="0205a-220">Se il controllo supporta il pattern di controllo [Selection](uiauto-implementingselection.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-220">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="0205a-221">**\_TextSelectionChangedEventId testo \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-221">**UIA\_Text\_TextSelectionChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [<span data-ttu-id="0205a-222">**\_TextChangedEventId testo \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="0205a-222">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| <span data-ttu-id="0205a-223">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0205a-223">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                       | <span data-ttu-id="0205a-224">Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0205a-224">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="0205a-225">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0205a-225">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0205a-226">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0205a-226">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0205a-227">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0205a-227">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0205a-228">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0205a-228">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




