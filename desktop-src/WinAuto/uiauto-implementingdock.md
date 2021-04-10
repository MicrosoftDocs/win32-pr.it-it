---
title: Pattern di controllo Dock
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IDockProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Dock viene usato per esporre le proprietà di ancoraggio di un controllo all'interno di un contenitore di ancoraggio.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Dock
- Automazione interfaccia utente, pattern di controllo Dock
- Automazione interfaccia utente, IDockProvider
- IDockProvider
- implementazione di pattern di controllo Dock di automazione interfaccia utente
- modelli di controllo Dock
- pattern di controllo, IDockProvider
- pattern di controllo, implementazione del dock di automazione interfaccia utente
- pattern di controllo, ancoraggio
- interfacce, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855990"
---
# <a name="dock-control-pattern"></a><span data-ttu-id="c18b8-114">Pattern di controllo Dock</span><span class="sxs-lookup"><span data-stu-id="c18b8-114">Dock Control Pattern</span></span>

<span data-ttu-id="c18b8-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="c18b8-115">Describes guidelines and conventions for implementing [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), including information about properties and methods.</span></span> <span data-ttu-id="c18b8-116">Il pattern di controllo **Dock** viene usato per esporre le proprietà di ancoraggio di un controllo all'interno di un contenitore di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="c18b8-116">The **Dock** control pattern is used to expose the dock properties of a control within a docking container.</span></span>

<span data-ttu-id="c18b8-117">Un contenitore di ancoraggio è un controllo che consente di disporre gli elementi figlio orizzontalmente e verticalmente, uno rispetto all'altro.</span><span class="sxs-lookup"><span data-stu-id="c18b8-117">A docking container is a control that allows you to arrange child elements horizontally and vertically, relative to each other.</span></span> <span data-ttu-id="c18b8-118">La figura seguente mostra un contenitore di ancoraggio con due elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="c18b8-118">The following image shows a docking container with two child elements.</span></span> <span data-ttu-id="c18b8-119">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="c18b8-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![screenshot che mostra il contenitore di ancoraggio con due elementi figlio ancorati](images/dockxmpl.jpg)

<span data-ttu-id="c18b8-121">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c18b8-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c18b8-122">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="c18b8-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c18b8-123">Membri obbligatori per **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="c18b8-123">Required Members for **IDockProvider**</span></span>](#required-members-for-idockprovider)
-   [<span data-ttu-id="c18b8-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c18b8-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c18b8-125">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="c18b8-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c18b8-126">Quando si implementa il pattern di controllo **Dock** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c18b8-126">When implementing the **Dock** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c18b8-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) non espone le proprietà del contenitore di ancoraggio o le proprietà dei controlli ancorati adiacenti al controllo corrente all'interno del contenitore di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="c18b8-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) does not expose any properties of the docking container or any properties of controls that are docked adjacent to the current control within the docking container.</span></span>
-   <span data-ttu-id="c18b8-128">I controlli vengono ancorati reciprocamente in base al relativo ordine z corrente, ovvero più elevata è la posizione nell'ordine z, più lontano verrà inserito il controllo rispetto al bordo specificato del contenitore di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="c18b8-128">Controls are docked relative to each other based on their current z-order; the higher their z-order placement, the farther they are placed from the specified edge of the docking container.</span></span>
-   <span data-ttu-id="c18b8-129">Se il contenitore di ancoraggio viene ridimensionato, i controlli ancorati all'interno del contenitore verranno riposizionati e allineati allo stesso bordo a cui sono stati originariamente ancorati.</span><span class="sxs-lookup"><span data-stu-id="c18b8-129">If the docking container is resized, any docked controls within the container will be repositioned flush to the same edge to which they were originally docked.</span></span> <span data-ttu-id="c18b8-130">Anche i controlli ancorati vengono ridimensionati per riempire lo spazio all'interno del contenitore in base al comportamento di ancoraggio della relativa proprietà [**impostata su DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) .</span><span class="sxs-lookup"><span data-stu-id="c18b8-130">The docked controls will also resize to fill any space within the container according to the docking behavior of their [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) property.</span></span> <span data-ttu-id="c18b8-131">Se, ad esempio, si specifica **impostata su DockPosition \_ Top** , il lato sinistro e destro del controllo si espanderà in modo da riempire lo spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="c18b8-131">For example, if **DockPosition\_Top** is specified, the left and right sides of the control will expand to fill any available space.</span></span> <span data-ttu-id="c18b8-132">Se si specifica **impostata su DockPosition \_ Fill** , tutti e quattro i lati del controllo si espanderanno in modo da riempire lo spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="c18b8-132">If **DockPosition\_Fill** is specified, all four sides of the control will expand to fill any available space.</span></span>
-   <span data-ttu-id="c18b8-133">In un sistema con più monitor i controlli devono essere ancorati al lato sinistro o destro del monitor corrente.</span><span class="sxs-lookup"><span data-stu-id="c18b8-133">On a multi-monitor system, controls should dock to the left or right side of the current monitor.</span></span> <span data-ttu-id="c18b8-134">Se ciò non è possibile, devono essere ancorati al lato sinistro del monitor all'estrema sinistra o al lato destro del monitor all'estrema destra.</span><span class="sxs-lookup"><span data-stu-id="c18b8-134">If that is not possible, they should dock to the left side of the leftmost monitor or the right side of the rightmost monitor.</span></span>

## <a name="required-members-for-idockprovider"></a><span data-ttu-id="c18b8-135">Membri obbligatori per **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="c18b8-135">Required Members for **IDockProvider**</span></span>

<span data-ttu-id="c18b8-136">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) .</span><span class="sxs-lookup"><span data-stu-id="c18b8-136">The following properties and methods are required for implementing the [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) interface.</span></span>



| <span data-ttu-id="c18b8-137">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="c18b8-137">Required members</span></span>                                                | <span data-ttu-id="c18b8-138">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="c18b8-138">Member type</span></span> | <span data-ttu-id="c18b8-139">Note</span><span class="sxs-lookup"><span data-stu-id="c18b8-139">Notes</span></span> |
|-----------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="c18b8-140">**Impostata su DockPosition**</span><span class="sxs-lookup"><span data-stu-id="c18b8-140">**DockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | <span data-ttu-id="c18b8-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c18b8-141">Property</span></span>    | <span data-ttu-id="c18b8-142">nessuno</span><span class="sxs-lookup"><span data-stu-id="c18b8-142">None</span></span>  |
| [<span data-ttu-id="c18b8-143">**SetDockPosition**</span><span class="sxs-lookup"><span data-stu-id="c18b8-143">**SetDockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | <span data-ttu-id="c18b8-144">Metodo</span><span class="sxs-lookup"><span data-stu-id="c18b8-144">Method</span></span>      | <span data-ttu-id="c18b8-145">nessuno</span><span class="sxs-lookup"><span data-stu-id="c18b8-145">None</span></span>  |



 

<span data-ttu-id="c18b8-146">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="c18b8-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c18b8-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c18b8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c18b8-148">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="c18b8-148">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c18b8-149">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c18b8-149">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c18b8-150">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c18b8-150">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




