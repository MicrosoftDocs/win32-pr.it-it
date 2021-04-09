---
title: Tipo di controllo Slider
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Slider
- Automazione interfaccia utente, tipo di controllo Slider
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Slider
- Automazione interfaccia utente, proprietà per il tipo di controllo Slider
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Slider
- Automazione interfaccia utente, eventi per il tipo di controllo Slider
- strutture ad albero, tipo di controllo Slider
- Proprietà, tipo di controllo Slider
- pattern di controllo, tipo di controllo Slider
- eventi, tipo di controllo Slider
- supporto per il tipo di controllo Slider
- Slider (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Slider
- tipi di controllo, pattern di controllo per il tipo di controllo Slider
- tipi di controllo, supporto per il dispositivo di scorrimento
- tipi di controllo, dispositivo di scorrimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955599"
---
# <a name="slider-control-type"></a><span data-ttu-id="111fe-119">Tipo di controllo Slider</span><span class="sxs-lookup"><span data-stu-id="111fe-119">Slider Control Type</span></span>

<span data-ttu-id="111fe-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Slider** .</span><span class="sxs-lookup"><span data-stu-id="111fe-120">This topic provides information about Microsoft UI Automation support for the **Slider** control type.</span></span>

<span data-ttu-id="111fe-121">Un controllo dispositivo di scorrimento è un controllo composito con pulsanti che consentono a un utente di impostare un intervallo numerico o effettuare una selezione da un set di elementi.</span><span class="sxs-lookup"><span data-stu-id="111fe-121">A slider control is a composite control with buttons that enable a user to set a numerical range or select from a set of items.</span></span>

<span data-ttu-id="111fe-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Slider** .</span><span class="sxs-lookup"><span data-stu-id="111fe-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Slider** control type.</span></span> <span data-ttu-id="111fe-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli dispositivo di scorrimento in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e</span><span class="sxs-lookup"><span data-stu-id="111fe-123">The UI Automation requirements apply to all slider controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="111fe-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="111fe-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="111fe-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="111fe-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="111fe-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="111fe-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="111fe-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="111fe-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="111fe-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="111fe-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="111fe-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="111fe-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="111fe-130">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="111fe-130">Typical Tree Structure</span></span>

<span data-ttu-id="111fe-131">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli dispositivo di scorrimento e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="111fe-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to slider controls and describes what can be contained in each view.</span></span> <span data-ttu-id="111fe-132">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="111fe-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="111fe-133">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="111fe-133">Control View</span></span></th>
<th><span data-ttu-id="111fe-134">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="111fe-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="111fe-135">Slider</span><span class="sxs-lookup"><span data-stu-id="111fe-135">Slider</span></span>
<ul>
<li><span data-ttu-id="111fe-136">Button (2 o 4)</span><span class="sxs-lookup"><span data-stu-id="111fe-136">Button (2 or 4)</span></span></li>
<li><span data-ttu-id="111fe-137">Thumb (1)</span><span class="sxs-lookup"><span data-stu-id="111fe-137">Thumb (1)</span></span></li>
<li><span data-ttu-id="111fe-138">Elemento elenco (0 o più)</span><span class="sxs-lookup"><span data-stu-id="111fe-138">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="111fe-139">Slider</span><span class="sxs-lookup"><span data-stu-id="111fe-139">Slider</span></span>
<ul>
<li><span data-ttu-id="111fe-140">Elemento elenco (0 o più)</span><span class="sxs-lookup"><span data-stu-id="111fe-140">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="111fe-141">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="111fe-141">Relevant Properties</span></span>

<span data-ttu-id="111fe-142">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="111fe-142">The following table lists the UI Automation properties whose value or definition is especially relevant to slider controls.</span></span> <span data-ttu-id="111fe-143">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="111fe-143">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="111fe-144">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="111fe-144">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="111fe-145">Valore</span><span class="sxs-lookup"><span data-stu-id="111fe-145">Value</span></span>      | <span data-ttu-id="111fe-146">Note</span><span class="sxs-lookup"><span data-stu-id="111fe-146">Notes</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="111fe-147">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-147">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="111fe-148">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="111fe-148">See notes.</span></span> | <span data-ttu-id="111fe-149">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="111fe-149">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="111fe-150">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-150">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="111fe-151">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="111fe-151">See notes.</span></span> | <span data-ttu-id="111fe-152">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="111fe-152">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="111fe-153">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-153">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="111fe-154">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="111fe-154">See notes.</span></span> | <span data-ttu-id="111fe-155">La maggior parte dei controlli dispositivo di scorrimento deve restituire l'errore [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) perché l'intero rettangolo di delimitazione del controllo dispositivo di scorrimento è occupato da controlli figlio.</span><span class="sxs-lookup"><span data-stu-id="111fe-155">The majority of slider controls must return the [**UIA\_E\_NOCLICKABLEPOINT**](uiauto-error-codes.md) error because the entire bounding rectangle of the slider control is occupied by child controls.</span></span> |
| [<span data-ttu-id="111fe-156">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="111fe-157">**Dispositivo di scorrimento**</span><span class="sxs-lookup"><span data-stu-id="111fe-157">**Slider**</span></span> | <span data-ttu-id="111fe-158">Questo valore è uguale per tutti i framework.</span><span class="sxs-lookup"><span data-stu-id="111fe-158">This value is the same for all frameworks.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="111fe-159">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="111fe-160">true</span><span class="sxs-lookup"><span data-stu-id="111fe-160">TRUE</span></span>       | <span data-ttu-id="111fe-161">Il controllo dispositivo di scorrimento è sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="111fe-161">The slider control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="111fe-162">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="111fe-163">true</span><span class="sxs-lookup"><span data-stu-id="111fe-163">TRUE</span></span>       | <span data-ttu-id="111fe-164">Il controllo Slider viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="111fe-164">The slider control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="111fe-165">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="111fe-166">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="111fe-166">See notes.</span></span> | <span data-ttu-id="111fe-167">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="111fe-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="111fe-168">Gli elementi figlio (pulsanti e Thumb) di un controllo dispositivo di scorrimento non devono mai prendere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="111fe-168">The children (buttons and thumb) of a slider control should never take the focus.</span></span> <span data-ttu-id="111fe-169">Lo stato attivo deve rimanere sempre sul controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="111fe-169">The focus should always remain on the slider control itself.</span></span>       |
| [<span data-ttu-id="111fe-170">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="111fe-171">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="111fe-171">See notes.</span></span> | <span data-ttu-id="111fe-172">Se è presente un'etichetta di testo statico associata al controllo, questa proprietà deve esporre un riferimento a tale controllo.</span><span class="sxs-lookup"><span data-stu-id="111fe-172">If there is a static text label associated with the control, this property must expose a reference to that control.</span></span> <span data-ttu-id="111fe-173">Se il controllo testo è un sottocomponente di un altro controllo, non avrà una proprietà **LabeledBy** impostata.</span><span class="sxs-lookup"><span data-stu-id="111fe-173">If the text control is a subcomponent of another control, it will not have a **LabeledBy** property set.</span></span>   |
| [<span data-ttu-id="111fe-174">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="111fe-175">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="111fe-175">See notes.</span></span> | <span data-ttu-id="111fe-176">Stringa localizzata corrispondente al tipo di controllo **Slider** .</span><span class="sxs-lookup"><span data-stu-id="111fe-176">Localized string corresponding to the **Slider** control type.</span></span> <span data-ttu-id="111fe-177">Il valore predefinito è "slider" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="111fe-177">The default value is "slider" for en-US or English (United States).</span></span>                                                                                             |
| [<span data-ttu-id="111fe-178">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="111fe-179">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="111fe-179">See notes.</span></span> | <span data-ttu-id="111fe-180">Il nome del controllo dispositivo di scorrimento viene in genere generato da un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="111fe-180">The name of the slider control is typically generated from a static text label.</span></span> <span data-ttu-id="111fe-181">Se non è presente un'etichetta di testo statico, lo sviluppatore dell'applicazione deve assegnare un valore di proprietà per il **nome** .</span><span class="sxs-lookup"><span data-stu-id="111fe-181">If there is not a static text label, a property value for **Name** must be assigned by the application developer.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="111fe-182">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="111fe-182">Required Control Patterns</span></span>

<span data-ttu-id="111fe-183">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="111fe-183">The following table lists the UI Automation control patterns required to be supported by all slider controls.</span></span> <span data-ttu-id="111fe-184">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="111fe-184">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="111fe-185">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="111fe-185">Control Pattern/Pattern Property</span></span>                          | <span data-ttu-id="111fe-186">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="111fe-186">Support/Value</span></span> | <span data-ttu-id="111fe-187">Note</span><span class="sxs-lookup"><span data-stu-id="111fe-187">Notes</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="111fe-188">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="111fe-188">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | <span data-ttu-id="111fe-189">Dipende da</span><span class="sxs-lookup"><span data-stu-id="111fe-189">Depends</span></span>       | <span data-ttu-id="111fe-190">Un dispositivo di scorrimento deve supportare il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) se il contenuto può essere impostato su un valore compreso in un intervallo numerico.</span><span class="sxs-lookup"><span data-stu-id="111fe-190">A slider should support the [RangeValue](uiauto-implementingrangevalue.md) control pattern if the content can be set to a value within a numerical range.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="111fe-191">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="111fe-191">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | <span data-ttu-id="111fe-192">Dipende da</span><span class="sxs-lookup"><span data-stu-id="111fe-192">Depends</span></span>       | <span data-ttu-id="111fe-193">Un dispositivo di scorrimento deve supportare il pattern di controllo [Selection](uiauto-implementingselection.md) se il contenuto rappresenta un valore tra un set discreto di opzioni.</span><span class="sxs-lookup"><span data-stu-id="111fe-193">A slider should support the [Selection](uiauto-implementingselection.md) control pattern if the content represents one value among a discrete set of options.</span></span> <span data-ttu-id="111fe-194">Se il pattern di controllo Selection è supportato, la selezione corrispondente deve essere esposta come uno o più elementi di elenco figlio del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="111fe-194">When the Selection control pattern is supported, the corresponding selection must be exposed as one or more child list items of the slider.</span></span> |
| [<span data-ttu-id="111fe-195">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="111fe-195">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | <span data-ttu-id="111fe-196">Dipende da</span><span class="sxs-lookup"><span data-stu-id="111fe-196">Depends</span></span>       | <span data-ttu-id="111fe-197">Un dispositivo di scorrimento deve supportare il pattern di controllo [value](uiauto-implementingvalue.md) se il contenuto rappresenta un valore tra un set discreto di opzioni.</span><span class="sxs-lookup"><span data-stu-id="111fe-197">A slider should support the [Value](uiauto-implementingvalue.md) control pattern if the content represents one value among a discrete set of options.</span></span>                                                                                                                                                     |



 

## <a name="required-events"></a><span data-ttu-id="111fe-198">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="111fe-198">Required Events</span></span>

<span data-ttu-id="111fe-199">La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="111fe-199">The following table lists the UI Automation events that slider controls are required to support.</span></span> <span data-ttu-id="111fe-200">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="111fe-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="111fe-201">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="111fe-201">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="111fe-202">Note</span><span class="sxs-lookup"><span data-stu-id="111fe-202">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="111fe-203">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="111fe-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="111fe-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="111fe-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="111fe-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="111fe-206">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="111fe-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="111fe-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="111fe-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="111fe-208">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="111fe-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="111fe-209">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà RangeValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="111fe-209">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="111fe-210">Se il controllo supporta il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="111fe-210">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="111fe-211">**\_InvalidatedEventId selezione \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-211">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                       | <span data-ttu-id="111fe-212">Se il controllo supporta il pattern di controllo [Selection](uiauto-implementingselection.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="111fe-212">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="111fe-213">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="111fe-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="111fe-214">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="111fe-214">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="111fe-215">Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="111fe-215">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="111fe-216">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="111fe-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="111fe-217">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="111fe-217">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="111fe-218">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="111fe-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="111fe-219">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="111fe-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




