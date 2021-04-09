---
title: Pattern di controllo Grid
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IGridProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Grid viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Grid
- Automazione interfaccia utente, pattern di controllo Grid
- Automazione interfaccia utente, IGridProvider
- IGridProvider
- implementazione di pattern di controllo Grid di automazione interfaccia utente
- Pattern di controllo Grid
- pattern di controllo, IGridProvider
- pattern di controllo, implementazione della griglia di automazione interfaccia utente
- pattern di controllo, griglia
- interfacce, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044477"
---
# <a name="grid-control-pattern"></a><span data-ttu-id="f7ce4-114">Pattern di controllo Grid</span><span class="sxs-lookup"><span data-stu-id="f7ce4-114">Grid Control Pattern</span></span>

<span data-ttu-id="f7ce4-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-115">Describes guidelines and conventions for implementing [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), including information about properties and methods.</span></span> <span data-ttu-id="f7ce4-116">Il pattern di controllo **Grid** viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-116">The **Grid** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="f7ce4-117">Gli elementi figlio di questo elemento devono implementare [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) ed essere organizzati in un sistema di coordinate logico bidimensionale che può essere attraversato da righe e colonne.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-117">The children of this element must implement [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="f7ce4-118">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="f7ce4-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="f7ce4-119">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f7ce4-120">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="f7ce4-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f7ce4-121">Membri obbligatori per **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="f7ce4-121">Required Members for **IGridProvider**</span></span>](#required-members-for-igridprovider)
-   [<span data-ttu-id="f7ce4-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7ce4-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f7ce4-123">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="f7ce4-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f7ce4-124">Quando si implementa il pattern di controllo **Grid** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7ce4-124">When implementing the **Grid** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f7ce4-125">Le coordinate della griglia sono in base zero, con la cella in alto a sinistra o in alto a destra, in base alle impostazioni locali, con coordinate (0, 0).</span><span class="sxs-lookup"><span data-stu-id="f7ce4-125">Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).</span></span>
-   <span data-ttu-id="f7ce4-126">Se una cella è vuota, è necessario che venga restituito un elemento di automazione interfaccia utente Microsoft per supportare la proprietà [**IGridItemProvider:: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) per tale cella.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-126">If a cell is empty, a Microsoft UI Automation element must still be returned in order to support the [**IGridItemProvider::ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) property for that cell.</span></span> <span data-ttu-id="f7ce4-127">Ciò è possibile quando il layout degli elementi figlio nella griglia è simile a una matrice irregolare (vedere l'esempio riportato di seguito).</span><span class="sxs-lookup"><span data-stu-id="f7ce4-127">This is possible when the layout of child elements in the grid is similar to a ragged array (see example below).</span></span>

    ![esempio di controllo griglia con coordinate vuote](images/grid.png)

-   <span data-ttu-id="f7ce4-129">Una griglia con un solo elemento è ancora necessaria per implementare [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) se è considerata logicamente una griglia.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-129">A grid with a single item is still required to implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) if it is logically considered to be a grid.</span></span> <span data-ttu-id="f7ce4-130">Il numero di elementi figlio nella griglia non ha importanza.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-130">The number of child items in the grid is immaterial.</span></span>
-   <span data-ttu-id="f7ce4-131">Le righe e le colonne nascoste, a seconda dell'implementazione del provider, possono essere caricate nell'albero di automazione interfaccia utente e pertanto verranno riflesse nelle proprietà [**IGridProvider:: RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) e [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) .</span><span class="sxs-lookup"><span data-stu-id="f7ce4-131">Hidden rows and columns, depending on the provider implementation, may be loaded in the UI Automation tree and will therefore be reflected in the [**IGridProvider::RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) and [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) properties.</span></span> <span data-ttu-id="f7ce4-132">Se le righe e colonne nascoste non sono ancora state caricate, non devono essere contate.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-132">If the hidden rows and columns have not yet been loaded, they should not be counted.</span></span>
-   <span data-ttu-id="f7ce4-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) non consente la modifica attiva di una griglia; Per abilitare questa funzionalità, è necessario implementare [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .</span><span class="sxs-lookup"><span data-stu-id="f7ce4-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not enable active manipulation of a grid; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) must be implemented to enable this functionality.</span></span>
-   <span data-ttu-id="f7ce4-134">Usare un [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) per restare in ascolto delle modifiche strutturali o di layout della griglia, ad esempio le celle che sono state aggiunte, rimosse o unite.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-134">Use a [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) to listen for structural or layout changes to the grid such as cells that have been added, removed, or merged.</span></span>
-   <span data-ttu-id="f7ce4-135">Usare un [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) per tenere traccia dell'attraversamento attraverso gli elementi o le celle di una griglia.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-135">Use a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) to track traversal through the items or cells of a grid.</span></span>

## <a name="required-members-for-igridprovider"></a><span data-ttu-id="f7ce4-136">Membri obbligatori per **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="f7ce4-136">Required Members for **IGridProvider**</span></span>

<span data-ttu-id="f7ce4-137">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) .</span><span class="sxs-lookup"><span data-stu-id="f7ce4-137">The following properties and methods are required for implementing the [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) interface.</span></span>



| <span data-ttu-id="f7ce4-138">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="f7ce4-138">Required members</span></span>                                        | <span data-ttu-id="f7ce4-139">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="f7ce4-139">Member type</span></span> | <span data-ttu-id="f7ce4-140">Note</span><span class="sxs-lookup"><span data-stu-id="f7ce4-140">Notes</span></span> |
|---------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="f7ce4-141">**RowCount**</span><span class="sxs-lookup"><span data-stu-id="f7ce4-141">**RowCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | <span data-ttu-id="f7ce4-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7ce4-142">Property</span></span>    | <span data-ttu-id="f7ce4-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="f7ce4-143">None</span></span>  |
| [<span data-ttu-id="f7ce4-144">**ColumnCount**</span><span class="sxs-lookup"><span data-stu-id="f7ce4-144">**ColumnCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | <span data-ttu-id="f7ce4-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7ce4-145">Property</span></span>    | <span data-ttu-id="f7ce4-146">nessuno</span><span class="sxs-lookup"><span data-stu-id="f7ce4-146">None</span></span>  |
| [<span data-ttu-id="f7ce4-147">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="f7ce4-147">**GetItem**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | <span data-ttu-id="f7ce4-148">Metodo</span><span class="sxs-lookup"><span data-stu-id="f7ce4-148">Method</span></span>      | <span data-ttu-id="f7ce4-149">nessuno</span><span class="sxs-lookup"><span data-stu-id="f7ce4-149">None</span></span>  |



 

<span data-ttu-id="f7ce4-150">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="f7ce4-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7ce4-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7ce4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7ce4-152">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="f7ce4-152">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="f7ce4-153">Pattern di controllo GridItem</span><span class="sxs-lookup"><span data-stu-id="f7ce4-153">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
</dt> <dt>

[<span data-ttu-id="f7ce4-154">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f7ce4-154">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="f7ce4-155">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f7ce4-155">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




