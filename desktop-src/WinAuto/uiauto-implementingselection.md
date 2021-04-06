---
title: Pattern di controllo Selection
description: Descrive le linee guida e le convenzioni per l'implementazione di ISelectionProvider, incluse informazioni su proprietà, metodi ed eventi.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Selection
- Automazione interfaccia utente, pattern di controllo Selection
- Automazione interfaccia utente, ISelectionProvider
- ISelectionProvider
- implementazione di pattern di controllo Selection di automazione interfaccia utente
- Pattern di controllo Selection
- pattern di controllo, ISelectionProvider
- pattern di controllo, implementazione della selezione di automazione interfaccia utente
- pattern di controllo, selezione
- interfacce, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044773"
---
# <a name="selection-control-pattern"></a><span data-ttu-id="c9cd7-113">Pattern di controllo Selection</span><span class="sxs-lookup"><span data-stu-id="c9cd7-113">Selection Control Pattern</span></span>

<span data-ttu-id="c9cd7-114">Descrive le linee guida e le convenzioni per l'implementazione di [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), incluse informazioni su proprietà, metodi ed eventi.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-114">Describes guidelines and conventions for implementing [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="c9cd7-115">Il pattern di controllo **Selection** viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio selezionabili.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-115">The **Selection** control pattern is used to support controls that act as containers for a collection of selectable child items.</span></span> <span data-ttu-id="c9cd7-116">Gli elementi figlio di questo elemento devono implementare [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="c9cd7-116">The children of this element must implement [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

<span data-ttu-id="c9cd7-117">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="c9cd7-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="c9cd7-118">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c9cd7-119">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="c9cd7-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c9cd7-120">Membri obbligatori per **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="c9cd7-120">Required Members for **ISelectionProvider**</span></span>](#required-members-for-iselectionprovider)
-   [<span data-ttu-id="c9cd7-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9cd7-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c9cd7-122">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="c9cd7-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c9cd7-123">Quando si implementa il pattern di controllo **Selection** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9cd7-123">When implementing the **Selection** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c9cd7-124">I controlli che implementano [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) consentono la selezione di uno o più elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-124">Controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) allow either single or multiple child items to be selected.</span></span> <span data-ttu-id="c9cd7-125">Ad esempio, le caselle di riepilogo, le visualizzazioni elenco e le visualizzazioni ad albero supportano selezioni multiple, mentre le caselle combinate, i dispositivi di scorrimento e i gruppi di pulsanti di opzione supportano la selezione singola.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-125">For example, list boxes, list views, and tree views support multiple selections, whereas combo boxes, sliders, and radio button groups support single selection.</span></span>
-   <span data-ttu-id="c9cd7-126">I controlli che hanno un intervallo minimo, massimo e continuo, ad esempio il controllo dispositivo di scorrimento del **volume** di un lettore multimediale, devono implementare [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) anziché [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="c9cd7-126">Controls that have a minimum, maximum, and continuous range, such as the **Volume** slider control of a media player, should implement [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) instead of [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>
-   <span data-ttu-id="c9cd7-127">I controlli a selezione singola che gestiscono i controlli figlio che implementano [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), ad esempio il dispositivo di scorrimento **risoluzione schermo** nella finestra di dialogo **proprietà di visualizzazione** per Windows o il controllo selezione selezione **colori** da Microsoft Word (vedere l'immagine seguente), devono implementare [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); i relativi elementi figlio devono implementare sia [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) che [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="c9cd7-127">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, or the **Color Picker** selection control from Microsoft Word (see the following image), should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

    ![immagine che mostra un esempio di mapping delle stringhe dei campioni colore](images/uia-valuepattern-colorpicker.jpg)

-   <span data-ttu-id="c9cd7-129">I menu non supportano il pattern di controllo **Selection** .</span><span class="sxs-lookup"><span data-stu-id="c9cd7-129">Menus do not support the **Selection** control pattern.</span></span> <span data-ttu-id="c9cd7-130">Se si usano voci di menu che includono sia grafica che testo (ad esempio gli elementi del **riquadro di anteprima** nel menu **Visualizza** in Microsoft Outlook) ed è necessario indicare lo stato, è necessario implementare [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span><span class="sxs-lookup"><span data-stu-id="c9cd7-130">If you are working with menu items that include both graphics and text (such as the **Preview Pane** items in the **View** menu in Microsoft Outlook) and need to convey state, you should implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span></span>

## <a name="required-members-for-iselectionprovider"></a><span data-ttu-id="c9cd7-131">Membri obbligatori per **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="c9cd7-131">Required Members for **ISelectionProvider**</span></span>

<span data-ttu-id="c9cd7-132">Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="c9cd7-132">The following properties, methods, and events are required for implementing the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>



| <span data-ttu-id="c9cd7-133">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="c9cd7-133">Required members</span></span>                                                                                | <span data-ttu-id="c9cd7-134">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="c9cd7-134">Member type</span></span> | <span data-ttu-id="c9cd7-135">Note</span><span class="sxs-lookup"><span data-stu-id="c9cd7-135">Notes</span></span>                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="c9cd7-136">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="c9cd7-136">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | <span data-ttu-id="c9cd7-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c9cd7-137">Property</span></span>    | <span data-ttu-id="c9cd7-138">nessuno</span><span class="sxs-lookup"><span data-stu-id="c9cd7-138">None</span></span>                                                                        |
| [<span data-ttu-id="c9cd7-139">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="c9cd7-139">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | <span data-ttu-id="c9cd7-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c9cd7-140">Property</span></span>    | <span data-ttu-id="c9cd7-141">nessuno</span><span class="sxs-lookup"><span data-stu-id="c9cd7-141">None</span></span>                                                                        |
| [<span data-ttu-id="c9cd7-142">**GetSelection**</span><span class="sxs-lookup"><span data-stu-id="c9cd7-142">**GetSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | <span data-ttu-id="c9cd7-143">Metodo</span><span class="sxs-lookup"><span data-stu-id="c9cd7-143">Method</span></span>      | <span data-ttu-id="c9cd7-144">nessuno</span><span class="sxs-lookup"><span data-stu-id="c9cd7-144">None</span></span>                                                                        |
| [<span data-ttu-id="c9cd7-145">**\_InvalidatedEventId selezione \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="c9cd7-145">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="c9cd7-146">Evento</span><span class="sxs-lookup"><span data-stu-id="c9cd7-146">Event</span></span>       | <span data-ttu-id="c9cd7-147">Generare questo evento quando una selezione in un contenitore è cambiata in modo significativo.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-147">Raise this event when a selection in a container has changed significantly.</span></span> |



 

<span data-ttu-id="c9cd7-148">Le proprietà [**ISelectionProvider:: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) e [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) possono essere dinamiche.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-148">The [**ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) and [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) properties can be dynamic.</span></span> <span data-ttu-id="c9cd7-149">Ad esempio, lo stato iniziale di un controllo potrebbe non includere elementi selezionati per impostazione predefinita, a indicare che **IsSelectionRequired** è false.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-149">For example, the initial state of a control might not have any items selected by default, indicating that **IsSelectionRequired** is false.</span></span> <span data-ttu-id="c9cd7-150">Tuttavia, dopo aver selezionato un elemento, il controllo deve sempre avere almeno un elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-150">However, after an item is selected, the control must always have at least one item selected.</span></span> <span data-ttu-id="c9cd7-151">Analogamente, in casi rari, un controllo potrebbe consentire la selezione di più elementi durante l'inizializzazione e successivamente consentire solo selezioni singole.</span><span class="sxs-lookup"><span data-stu-id="c9cd7-151">Similarly, in rare cases, a control might allow multiple items to be selected on initialization, but subsequently allow only single selections to be made.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9cd7-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9cd7-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9cd7-153">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="c9cd7-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c9cd7-154">Pattern di controllo SelectionItem</span><span class="sxs-lookup"><span data-stu-id="c9cd7-154">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
</dt> <dt>

[<span data-ttu-id="c9cd7-155">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c9cd7-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c9cd7-156">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c9cd7-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




