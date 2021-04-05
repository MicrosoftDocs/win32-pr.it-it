---
title: Pattern di controllo GridItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IGridItemProvider, incluse le informazioni sulle proprietà. Il pattern di controllo GridItem viene usato per supportare singoli controlli figlio di contenitori che implementano IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo GridItem
- Automazione interfaccia utente, pattern di controllo GridItem
- Automazione interfaccia utente, IGridItemProvider
- IGridItemProvider
- implementazione di pattern di controllo GridItem di automazione interfaccia utente
- Pattern di controllo GridItem
- pattern di controllo, IGridItemProvider
- pattern di controllo, implementazione di GridItem di automazione interfaccia utente
- pattern di controllo, GridItem
- interfacce, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709694"
---
# <a name="griditem-control-pattern"></a><span data-ttu-id="ada52-114">Pattern di controllo GridItem</span><span class="sxs-lookup"><span data-stu-id="ada52-114">GridItem Control Pattern</span></span>

<span data-ttu-id="ada52-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), incluse le informazioni sulle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ada52-115">Describes guidelines and conventions for implementing [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), including information about properties.</span></span> <span data-ttu-id="ada52-116">Il pattern di controllo **GridItem** viene usato per supportare singoli controlli figlio di contenitori che implementano [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="ada52-116">The **GridItem** control pattern is used to support individual child controls of containers that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>

<span data-ttu-id="ada52-117">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="ada52-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="ada52-118">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ada52-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ada52-119">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="ada52-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ada52-120">Membri obbligatori per **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ada52-120">Required Members for **IGridItemProvider**</span></span>](#required-members-for-igriditemprovider)
-   [<span data-ttu-id="ada52-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ada52-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ada52-122">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="ada52-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ada52-123">Quando si implementa il pattern di controllo **GridItem** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ada52-123">When implementing the **GridItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ada52-124">Le coordinate della griglia sono in base zero. Le coordinate della cella in alto a sinistra sono infatti (0, 0).</span><span class="sxs-lookup"><span data-stu-id="ada52-124">Grid coordinates are zero-based with the upper left cell having coordinates (0, 0).</span></span>
-   <span data-ttu-id="ada52-125">Le celle unite segnaleranno le proprietà di [**riga**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) e [**colonna**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) in base alla cella di ancoraggio sottostante, come definito dal provider di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ada52-125">Merged cells will report their [**Row**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) and [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) properties based on their underlying anchor cell as defined by the Microsoft UI Automation provider.</span></span> <span data-ttu-id="ada52-126">In genere si tratterà della riga o della colonna più in alto e più a sinistra.</span><span class="sxs-lookup"><span data-stu-id="ada52-126">Typically, it will be the topmost and leftmost row or column.</span></span>
-   <span data-ttu-id="ada52-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) non fornisce la manipolazione attiva della griglia, ad esempio l'Unione o la suddivisione di celle.</span><span class="sxs-lookup"><span data-stu-id="ada52-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not provide for active manipulation of the grid such as merging or splitting cells.</span></span>
-   <span data-ttu-id="ada52-128">I controlli che implementano [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) possono in genere essere attraversati, ovvero un client di automazione interfaccia utente può spostarsi sui controlli adiacenti usando la tastiera.</span><span class="sxs-lookup"><span data-stu-id="ada52-128">Controls that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) can typically be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.</span></span>

## <a name="required-members-for-igriditemprovider"></a><span data-ttu-id="ada52-129">Membri obbligatori per **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ada52-129">Required Members for **IGridItemProvider**</span></span>

<span data-ttu-id="ada52-130">Per l'implementazione dell'interfaccia [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) sono necessarie le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ada52-130">The following properties are required for implementing the [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) interface.</span></span>



| <span data-ttu-id="ada52-131">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="ada52-131">Required members</span></span>                                                  | <span data-ttu-id="ada52-132">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="ada52-132">Member type</span></span> | <span data-ttu-id="ada52-133">Note</span><span class="sxs-lookup"><span data-stu-id="ada52-133">Notes</span></span> |
|-------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ada52-134">**Riga**</span><span class="sxs-lookup"><span data-stu-id="ada52-134">**Row**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | <span data-ttu-id="ada52-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ada52-135">Property</span></span>    | <span data-ttu-id="ada52-136">nessuno</span><span class="sxs-lookup"><span data-stu-id="ada52-136">None</span></span>  |
| [<span data-ttu-id="ada52-137">**Colonna**</span><span class="sxs-lookup"><span data-stu-id="ada52-137">**Column**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | <span data-ttu-id="ada52-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ada52-138">Property</span></span>    | <span data-ttu-id="ada52-139">nessuno</span><span class="sxs-lookup"><span data-stu-id="ada52-139">None</span></span>  |
| [<span data-ttu-id="ada52-140">**RowSpan**</span><span class="sxs-lookup"><span data-stu-id="ada52-140">**RowSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | <span data-ttu-id="ada52-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ada52-141">Property</span></span>    | <span data-ttu-id="ada52-142">nessuno</span><span class="sxs-lookup"><span data-stu-id="ada52-142">None</span></span>  |
| [<span data-ttu-id="ada52-143">**ColumnSpan**</span><span class="sxs-lookup"><span data-stu-id="ada52-143">**ColumnSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | <span data-ttu-id="ada52-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ada52-144">Property</span></span>    | <span data-ttu-id="ada52-145">nessuno</span><span class="sxs-lookup"><span data-stu-id="ada52-145">None</span></span>  |
| [<span data-ttu-id="ada52-146">**ContainingGrid**</span><span class="sxs-lookup"><span data-stu-id="ada52-146">**ContainingGrid**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | <span data-ttu-id="ada52-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ada52-147">Property</span></span>    | <span data-ttu-id="ada52-148">nessuno</span><span class="sxs-lookup"><span data-stu-id="ada52-148">None</span></span>  |



 

<span data-ttu-id="ada52-149">Questo pattern di controllo non è associato a metodi o eventi.</span><span class="sxs-lookup"><span data-stu-id="ada52-149">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ada52-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ada52-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ada52-151">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="ada52-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="ada52-152">Pattern di controllo Grid</span><span class="sxs-lookup"><span data-stu-id="ada52-152">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
</dt> <dt>

[<span data-ttu-id="ada52-153">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ada52-153">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ada52-154">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ada52-154">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




