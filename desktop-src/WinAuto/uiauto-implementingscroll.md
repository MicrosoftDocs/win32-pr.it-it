---
title: Pattern di controllo Scroll
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IScrollProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Scroll viene usato per supportare un controllo che funge da contenitore scorrevole per una raccolta di oggetti figlio.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Scroll
- Automazione interfaccia utente, pattern di controllo Scroll
- Automazione interfaccia utente, IScrollProvider
- IScrollProvider
- implementazione di pattern di controllo Scroll di automazione interfaccia utente
- Pattern di controllo Scroll
- pattern di controllo, IScrollProvider
- pattern di controllo, implementazione dello scorrimento di automazione interfaccia utente
- pattern di controllo, scorrimento
- interfacce, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712172"
---
# <a name="scroll-control-pattern"></a><span data-ttu-id="2b7c0-114">Pattern di controllo Scroll</span><span class="sxs-lookup"><span data-stu-id="2b7c0-114">Scroll Control Pattern</span></span>

<span data-ttu-id="2b7c0-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-115">Describes guidelines and conventions for implementing [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), including information about properties and methods.</span></span> <span data-ttu-id="2b7c0-116">Il pattern di controllo **Scroll** viene usato per supportare un controllo che funge da contenitore scorrevole per una raccolta di oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-116">The **Scroll** control pattern is used to support a control that acts as a scrollable container for a collection of child objects.</span></span>

<span data-ttu-id="2b7c0-117">Il controllo non è necessario per usare le barre di scorrimento per supportare la funzionalità di scorrimento, sebbene in genere.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-117">The control is not required to use scroll bars to support the scrolling functionality, although it commonly does.</span></span> <span data-ttu-id="2b7c0-118">La figura seguente mostra un controllo scorrevole che non usa barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-118">The following image shows a scrolling control that does not use scroll bars.</span></span> <span data-ttu-id="2b7c0-119">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="2b7c0-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![screenshot che mostra un controllo di scorrimento senza barre di scorrimento](images/uia-scrollpattern-without-scrollbars.jpg)

<span data-ttu-id="2b7c0-121">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2b7c0-122">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="2b7c0-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="2b7c0-123">Membri obbligatori per **IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-123">Required Members for **IScrollProvider**</span></span>](#required-members-for-iscrollprovider)
-   [<span data-ttu-id="2b7c0-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b7c0-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="2b7c0-125">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="2b7c0-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="2b7c0-126">Quando si implementa il pattern di controllo **Scroll** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b7c0-126">When implementing the **Scroll** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="2b7c0-127">Gli elementi figlio di questo controllo devono implementare [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span><span class="sxs-lookup"><span data-stu-id="2b7c0-127">The children of this control must implement [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span></span>
-   <span data-ttu-id="2b7c0-128">Le barre di scorrimento di un controllo contenitore non supportano il pattern di controllo **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="2b7c0-128">The scroll bars of a container control do not support the **Scroll** control pattern.</span></span> <span data-ttu-id="2b7c0-129">Devono invece supportare il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="2b7c0-129">They must support the [RangeValue](uiauto-implementingrangevalue.md) control pattern instead.</span></span>
-   <span data-ttu-id="2b7c0-130">Quando lo scorrimento è misurato in percentuali, tutti i valori o gli importi relativi alla scala di scorrimento devono essere normalizzati in base a un intervallo compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-130">When scrolling is measured in percentages, all values or amounts related to scroll graduation must be normalized to a range of 0 to 100.</span></span>
-   <span data-ttu-id="2b7c0-131">La proprietà [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) e la proprietà [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) sono indipendenti dalla proprietà **IsEnabled** .</span><span class="sxs-lookup"><span data-stu-id="2b7c0-131">The [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property and [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property are independent of the **IsEnabled** property.</span></span>
-   <span data-ttu-id="2b7c0-132">Se la proprietà [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) è **false**, la proprietà [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) deve essere impostata su 100 (100%) e la proprietà [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) deve essere impostata su **UIA \_ ScrollPatternNoScroll** (-1).</span><span class="sxs-lookup"><span data-stu-id="2b7c0-132">If the [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property is **FALSE**, the [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) property should be set to 100 (100%) and [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="2b7c0-133">Analogamente, se la proprietà [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) è **false**, la proprietà [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) deve essere impostata su 100 (100%) e la proprietà [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) deve essere impostata su **UIA \_ ScrollPatternNoScroll** (-1).</span><span class="sxs-lookup"><span data-stu-id="2b7c0-133">Likewise, if the [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property is **FALSE**, the [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) property should be set to 100 (100%) and [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="2b7c0-134">In questo modo un client di automazione interfaccia utente Microsoft può usare questi valori di proprietà all'interno del metodo [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) , evitando una race condition se una direzione che il client non è interessata allo scorrimento viene attivata.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-134">This allows a Microsoft UI Automation client to use these property values within the [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) method while avoiding a race condition if a direction the client is not interested in scrolling becomes activated.</span></span>
-   <span data-ttu-id="2b7c0-135">La proprietà [**IScrollProvider:: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) è specifica delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-135">The [**IScrollProvider::HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property is locale-specific.</span></span> <span data-ttu-id="2b7c0-136">Impostando **HorizontalScrollPercent** su 100 è necessario impostare la posizione di scorrimento del controllo sull'equivalente della posizione all'estrema destra per le lingue, ad esempio l'inglese, lette da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-136">Setting **HorizontalScrollPercent** to 100 must set the scrolling location of the control to the equivalent of its rightmost position for languages such as English that read left to right.</span></span> <span data-ttu-id="2b7c0-137">In alternativa, per lingue quali l'arabo che legge da destra a sinistra, impostando **HorizontalScrollPercent** su 100 è necessario impostare la posizione di scorrimento sulla posizione più a sinistra.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-137">Alternately, for languages such as Arabic that read right to left, setting **HorizontalScrollPercent** to 100 must set the scroll location to the leftmost position.</span></span>

## <a name="required-members-for-iscrollprovider"></a><span data-ttu-id="2b7c0-138">Membri obbligatori per **IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-138">Required Members for **IScrollProvider**</span></span>

<span data-ttu-id="2b7c0-139">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) .</span><span class="sxs-lookup"><span data-stu-id="2b7c0-139">The following properties and methods are required for implementing the [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) interface.</span></span>



| <span data-ttu-id="2b7c0-140">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="2b7c0-140">Required members</span></span>                                                                  | <span data-ttu-id="2b7c0-141">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="2b7c0-141">Member type</span></span> | <span data-ttu-id="2b7c0-142">Note</span><span class="sxs-lookup"><span data-stu-id="2b7c0-142">Notes</span></span> |
|-----------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="2b7c0-143">**HorizontalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-143">**HorizontalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | <span data-ttu-id="2b7c0-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b7c0-144">Property</span></span>    | <span data-ttu-id="2b7c0-145">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7c0-145">None</span></span>  |
| [<span data-ttu-id="2b7c0-146">**VerticalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-146">**VerticalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | <span data-ttu-id="2b7c0-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b7c0-147">Property</span></span>    | <span data-ttu-id="2b7c0-148">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7c0-148">None</span></span>  |
| [<span data-ttu-id="2b7c0-149">**HorizontalViewSize**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-149">**HorizontalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | <span data-ttu-id="2b7c0-150">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b7c0-150">Property</span></span>    | <span data-ttu-id="2b7c0-151">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7c0-151">None</span></span>  |
| [<span data-ttu-id="2b7c0-152">**VerticalViewSize**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-152">**VerticalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | <span data-ttu-id="2b7c0-153">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b7c0-153">Property</span></span>    | <span data-ttu-id="2b7c0-154">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7c0-154">None</span></span>  |
| [<span data-ttu-id="2b7c0-155">**HorizontallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-155">**HorizontallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | <span data-ttu-id="2b7c0-156">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b7c0-156">Property</span></span>    | <span data-ttu-id="2b7c0-157">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7c0-157">None</span></span>  |
| [<span data-ttu-id="2b7c0-158">**VerticallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-158">**VerticallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | <span data-ttu-id="2b7c0-159">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b7c0-159">Property</span></span>    | <span data-ttu-id="2b7c0-160">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7c0-160">None</span></span>  |
| [<span data-ttu-id="2b7c0-161">**Scorrimento**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-161">**Scroll**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | <span data-ttu-id="2b7c0-162">Metodo</span><span class="sxs-lookup"><span data-stu-id="2b7c0-162">Method</span></span>      | <span data-ttu-id="2b7c0-163">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7c0-163">None</span></span>  |
| [<span data-ttu-id="2b7c0-164">**SetScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="2b7c0-164">**SetScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | <span data-ttu-id="2b7c0-165">Metodo</span><span class="sxs-lookup"><span data-stu-id="2b7c0-165">Method</span></span>      | <span data-ttu-id="2b7c0-166">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7c0-166">None</span></span>  |



 

<span data-ttu-id="2b7c0-167">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="2b7c0-167">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b7c0-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b7c0-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b7c0-169">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="2b7c0-169">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="2b7c0-170">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="2b7c0-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="2b7c0-171">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="2b7c0-171">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




