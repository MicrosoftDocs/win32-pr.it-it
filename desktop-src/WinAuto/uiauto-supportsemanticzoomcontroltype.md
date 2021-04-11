---
title: Tipo di controllo SemanticZoom
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente per il tipo di controllo SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, tipo di controllo SemanticZoom
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, proprietà per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, eventi per il tipo di controllo SemanticZoom
- strutture ad albero, tipo di controllo SemanticZoom
- Proprietà, tipo di controllo SemanticZoom
- pattern di controllo, tipo di controllo SemanticZoom
- eventi, tipo di controllo SemanticZoom
- supporto per il tipo di controllo SemanticZoom
- Tipo di controllo SemanticZoom
- tipi di controllo, struttura ad albero per il tipo di controllo SemanticZoom
- tipi di controllo, pattern di controllo per il tipo di controllo SemanticZoom
- tipi di controllo, supporto per SemanticZoom
- tipi di controllo, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117791"
---
# <a name="semanticzoom-control-type"></a><span data-ttu-id="749c2-119">Tipo di controllo SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="749c2-119">SemanticZoom Control Type</span></span>

<span data-ttu-id="749c2-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente per il tipo di controllo **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="749c2-120">This topic provides information about UI Automation support for the **SemanticZoom** control type.</span></span>

<span data-ttu-id="749c2-121">Lo zoom semantico è una tecnica introdotta in Windows 8 per la presentazione e lo spostamento di grandi set di dati o contenuti correlati in una singola visualizzazione, ad esempio un album di foto, un elenco di app o una rubrica.</span><span class="sxs-lookup"><span data-stu-id="749c2-121">Semantic Zoom is a technique introduced in Windows 8 for presenting and navigating large sets of related data or content within a single view, such as a photo album, app list, or address book.</span></span> <span data-ttu-id="749c2-122">Lo zoom semantico usa due modalità distinte di classificazione o *livelli di zoom* per organizzare e presentare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="749c2-122">Semantic Zoom uses two distinct modes of classification, or *zoom levels*, for organizing and presenting the content.</span></span> <span data-ttu-id="749c2-123">La modalità di basso livello (o *zoom avanti*) Visualizza gli elementi in una struttura Flat, "all-up"; e la modalità di alto livello (o *Zoom* indietro) Visualizza gli elementi in gruppi, consentendo all'utente di spostarsi rapidamente ed esplorare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="749c2-123">The low-level (or *zoomed in*) mode displays items in a flat, "all-up" structure; and the high-level (or *zoomed out*) mode displays items in groups, enabling the user to quickly navigate and browse through the content.</span></span> <span data-ttu-id="749c2-124">Ad esempio, lo zoom di un elenco di città potrebbe cambiare in un elenco di Stati che contengono tali città.</span><span class="sxs-lookup"><span data-stu-id="749c2-124">For example, zooming a list of cities might change to a list of states containing those cities.</span></span> <span data-ttu-id="749c2-125">Lo zoom di un elenco di programmi potrebbe variare in un elenco di gruppi di programmi logici.</span><span class="sxs-lookup"><span data-stu-id="749c2-125">Zooming a list of programs might change to a list of logical program groups.</span></span>

<span data-ttu-id="749c2-126">Per altre informazioni sullo zoom semantico usato per le app di Windows Store, vedere [linee guida per lo zoom semantico](/windows/uwp/controls-and-patterns/semantic-zoom).</span><span class="sxs-lookup"><span data-stu-id="749c2-126">For more information about Semantic Zoom specifically as used for Windows Store apps, see [Guidelines for Semantic Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).</span></span>

<span data-ttu-id="749c2-127">Il modello di utilizzo per il tipo di controllo **SemanticZoom** è insolito perché esiste principalmente per l'accesso a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="749c2-127">The usage model for the **SemanticZoom** control type is unusual in that it exists mainly for programmatic access.</span></span> <span data-ttu-id="749c2-128">I client di automazione interfaccia utente Microsoft possono monitorare e manipolare il controllo zoom semantico per controllare lo stato di ingrandimento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="749c2-128">Microsoft UI Automation clients can monitor and manipulate the Semantic Zoom control to control the zoomed-in state of the list.</span></span> <span data-ttu-id="749c2-129">Gli utenti che non usano la tecnologia per l'accessibilità in genere manipolano il controllo dello zoom semantico direttamente tramite movimenti tocco o tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="749c2-129">Users who are not using assistive technology would typically manipulate the Semantic Zoom control directly through touch gestures or keyboard shortcuts.</span></span>

<span data-ttu-id="749c2-130">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="749c2-130">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SemanticZoom** control type.</span></span> <span data-ttu-id="749c2-131">I requisiti di automazione interfaccia utente si applicano a tutti i controlli zoom semantici in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="749c2-131">The UI Automation requirements apply to all Semantic Zoom controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="749c2-132">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="749c2-132">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="749c2-133">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="749c2-133">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="749c2-134">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="749c2-134">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="749c2-135">Pattern di controllo e proprietà obbligatori</span><span class="sxs-lookup"><span data-stu-id="749c2-135">Required Control Patterns and Properties</span></span>](#required-control-patterns-and-properties)
-   [<span data-ttu-id="749c2-136">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="749c2-136">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="749c2-137">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="749c2-137">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="749c2-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="749c2-138">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="749c2-139">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="749c2-139">Typical Tree Structure</span></span>

<span data-ttu-id="749c2-140">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto della struttura ad albero di automazione interfaccia utente relativa al tipo di controllo **SemanticZoom** e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="749c2-140">The following table depicts a typical control and content view of the UI Automation tree that pertains to the **SemanticZoom** control type and describes what can be contained in each view.</span></span> <span data-ttu-id="749c2-141">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="749c2-141">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="749c2-142">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="749c2-142">Control View</span></span></th>
<th><span data-ttu-id="749c2-143">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="749c2-143">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="749c2-144">Elenco</span><span class="sxs-lookup"><span data-stu-id="749c2-144">List</span></span>
<ul>
<li><span data-ttu-id="749c2-145">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="749c2-145">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="749c2-146">ListItem (0 o più)</span><span class="sxs-lookup"><span data-stu-id="749c2-146">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="749c2-147">Elenco</span><span class="sxs-lookup"><span data-stu-id="749c2-147">List</span></span>
<ul>
<li><span data-ttu-id="749c2-148">ListItem (0 o più)</span><span class="sxs-lookup"><span data-stu-id="749c2-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="749c2-149">Oppure:</span><span class="sxs-lookup"><span data-stu-id="749c2-149">Or:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="749c2-150">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="749c2-150">Control View</span></span></th>
<th><span data-ttu-id="749c2-151">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="749c2-151">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="749c2-152">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="749c2-152">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="749c2-153">Elenco</span><span class="sxs-lookup"><span data-stu-id="749c2-153">List</span></span>
<ul>
<li><span data-ttu-id="749c2-154">ListItem (0 o più)</span><span class="sxs-lookup"><span data-stu-id="749c2-154">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="749c2-155">Elenco</span><span class="sxs-lookup"><span data-stu-id="749c2-155">List</span></span>
<ul>
<li><span data-ttu-id="749c2-156">ListItem (0 o più)</span><span class="sxs-lookup"><span data-stu-id="749c2-156">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="749c2-157">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="749c2-157">Relevant Properties</span></span>

<span data-ttu-id="749c2-158">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="749c2-158">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **SemanticZoom** control type.</span></span> <span data-ttu-id="749c2-159">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="749c2-159">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="749c2-160">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="749c2-160">UI Automation Property</span></span></th>
<th><span data-ttu-id="749c2-161">Valore</span><span class="sxs-lookup"><span data-stu-id="749c2-161">Value</span></span></th>
<th><span data-ttu-id="749c2-162">Note</span><span class="sxs-lookup"><span data-stu-id="749c2-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="749c2-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-164">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="749c2-164">See notes.</span></span></td>
<td><span data-ttu-id="749c2-165">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="749c2-165">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="749c2-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-167">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="749c2-167">See notes.</span></span></td>
<td><span data-ttu-id="749c2-168">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="749c2-168">The outermost rectangle that contains the whole control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="749c2-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-170">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="749c2-170">See notes.</span></span></td>
<td><span data-ttu-id="749c2-171">Se il controllo elenco ha un punto selezionabile, ovvero un punto su cui è possibile fare clic per fare in modo che l'elenco abbia lo stato attivo, tale punto deve essere esposto tramite questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="749c2-171">If the list control has a clickable point (a point that can be clicked to cause the list to take focus), that point must be exposed through this property.</span></span> <span data-ttu-id="749c2-172">Se il valore della proprietà <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> è <strong>true</strong>, il tentativo di recuperare questa proprietà comporta l'errore <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="749c2-172">If the value of the <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> property is <strong>TRUE</strong>, attempting to retrieve this property results in the <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> error.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="749c2-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-174"><strong>SemanticZoom</strong></span><span class="sxs-lookup"><span data-stu-id="749c2-174"><strong>SemanticZoom</strong></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="749c2-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-176">true</span><span class="sxs-lookup"><span data-stu-id="749c2-176">TRUE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="749c2-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-178">true</span><span class="sxs-lookup"><span data-stu-id="749c2-178">TRUE</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="749c2-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="749c2-180">FALSE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="749c2-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-182">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="749c2-182">See notes.</span></span></td>
<td><span data-ttu-id="749c2-183">Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.</span><span class="sxs-lookup"><span data-stu-id="749c2-183">If there is a static text label, this property must expose a reference to that control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="749c2-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-185">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="749c2-185">See notes.</span></span></td>
<td><span data-ttu-id="749c2-186">Stringa localizzata corrispondente al tipo di controllo <strong>SemanticZoom</strong> .</span><span class="sxs-lookup"><span data-stu-id="749c2-186">A localized string corresponding to the <strong>SemanticZoom</strong> control type.</span></span> <span data-ttu-id="749c2-187">Il valore predefinito è &quot; zoom semantico &quot; per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="749c2-187">The default value is &quot;semantic zoom&quot; for en-US or English (United States).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="749c2-188">Alcuni Framework sono stati concatenati come &quot; SemanticZoom &quot; .</span><span class="sxs-lookup"><span data-stu-id="749c2-188">Some frameworks concatenated this as &quot;semanticzoom&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="749c2-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="749c2-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="749c2-190">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="749c2-190">See notes.</span></span></td>
<td><span data-ttu-id="749c2-191">Una stringa vuota è accettabile, oppure è possibile specificare un nome più utile, purché non contenga il termine zoom semantico, che renderebbe la combinazione di tipo di controllo e nome confuso.</span><span class="sxs-lookup"><span data-stu-id="749c2-191">An empty string is acceptable, or a more useful name could be provided, as long as it does not contain the term  semantic zoom , which would make the combination of control type and name confusing.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a><span data-ttu-id="749c2-192">Pattern di controllo e proprietà obbligatori</span><span class="sxs-lookup"><span data-stu-id="749c2-192">Required Control Patterns and Properties</span></span>

<span data-ttu-id="749c2-193">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli zoom semantici.</span><span class="sxs-lookup"><span data-stu-id="749c2-193">The following table lists the UI Automation control patterns required to be supported by all Semantic Zoom controls.</span></span> <span data-ttu-id="749c2-194">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="749c2-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="749c2-195">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="749c2-195">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="749c2-196">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="749c2-196">Support/Value</span></span> | <span data-ttu-id="749c2-197">Note</span><span class="sxs-lookup"><span data-stu-id="749c2-197">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="749c2-198">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="749c2-198">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="749c2-199">Dipende da</span><span class="sxs-lookup"><span data-stu-id="749c2-199">Depends</span></span>       | <span data-ttu-id="749c2-200">I controlli zoom semantico supportano il pattern di controllo di [attivazione/](uiauto-implementingtoggle.md) disattivazione per consentire l'abilitazione o la disabilitazione dello zoom.</span><span class="sxs-lookup"><span data-stu-id="749c2-200">Semantic Zoom controls support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the zoom to be enabled or disabled.</span></span> <span data-ttu-id="749c2-201">[**ToggleState \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corrisponde allo stato Flat, all-up e [**ToggleState \_ on**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corrisponde alla vista di alto livello, con zoom indietro.</span><span class="sxs-lookup"><span data-stu-id="749c2-201">[**ToggleState\_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the flat, all-up state, and [**ToggleState\_On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the high level, zoomed-out view.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="749c2-202">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="749c2-202">Required Events</span></span>

<span data-ttu-id="749c2-203">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli zoom semantici.</span><span class="sxs-lookup"><span data-stu-id="749c2-203">The following table lists the UI Automation events that Semantic Zoom controls are required to support.</span></span> <span data-ttu-id="749c2-204">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="749c2-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="749c2-205">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="749c2-205">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="749c2-206">Note</span><span class="sxs-lookup"><span data-stu-id="749c2-206">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="749c2-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="749c2-207">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="749c2-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="749c2-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="749c2-209">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="749c2-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="749c2-210">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="749c2-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="749c2-211">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="749c2-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="749c2-212">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="749c2-212">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="749c2-213">Commenti</span><span class="sxs-lookup"><span data-stu-id="749c2-213">Remarks</span></span>

<span data-ttu-id="749c2-214">Se un'interfaccia utente dispone di un pulsante visibile per impostare il comportamento del controllo zoom semantico, questo pulsante non deve avere un tipo di controllo **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="749c2-214">If a UI has a visible button to toggle Semantic Zoom control behavior, this button should not have a **SemanticZoom** control type.</span></span> <span data-ttu-id="749c2-215">Si tratta di un valore non intuitivo, ma il tipo di controllo **SemanticZoom** caratterizza il contenitore del contenuto di zoom, non un pulsante che controlla lo zoom.</span><span class="sxs-lookup"><span data-stu-id="749c2-215">This is counter-intuitive, but the **SemanticZoom** control type characterizes the container of the zooming content, not a button that controls the zoom.</span></span> <span data-ttu-id="749c2-216">Un pulsante di questo tipo può essere rappresentato semplicemente come un tipo di controllo [Button](uiauto-supportbuttoncontroltype.md) con il pattern di controllo dell' [interruttore](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="749c2-216">(Such a button could be represented simply as a [Button](uiauto-supportbuttoncontroltype.md) control type with the [Toggle](uiauto-implementingtoggle.md) control pattern.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="749c2-217">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="749c2-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="749c2-218">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="749c2-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="749c2-219">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="749c2-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

