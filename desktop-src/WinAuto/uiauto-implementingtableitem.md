---
title: Pattern di controllo TableItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ITableItemProvider, incluse informazioni sui metodi. Il pattern di controllo TableItem viene usato per supportare i controlli figlio di contenitori che implementano ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo TableItem
- Automazione interfaccia utente, pattern di controllo TableItem
- Automazione interfaccia utente, ITableItemProvider
- ITableItemProvider
- implementazione di pattern di controllo TableItem di automazione interfaccia utente
- Pattern di controllo TableItem
- pattern di controllo, ITableItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente TableItem
- pattern di controllo, TableItem
- interfacce, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709277"
---
# <a name="tableitem-control-pattern"></a><span data-ttu-id="8b816-114">Pattern di controllo TableItem</span><span class="sxs-lookup"><span data-stu-id="8b816-114">TableItem Control Pattern</span></span>

<span data-ttu-id="8b816-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), incluse informazioni sui metodi.</span><span class="sxs-lookup"><span data-stu-id="8b816-115">Describes guidelines and conventions for implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), including information about methods.</span></span> <span data-ttu-id="8b816-116">Il pattern di controllo **TableItem** viene usato per supportare i controlli figlio di contenitori che implementano [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span><span class="sxs-lookup"><span data-stu-id="8b816-116">The **TableItem** control pattern is used to support child controls of containers that implement [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span></span>

<span data-ttu-id="8b816-117">L'accesso alle singole funzionalità delle celle viene fornito dall'implementazione simultanea obbligatoria di [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span><span class="sxs-lookup"><span data-stu-id="8b816-117">Access to individual cell functionality is provided by the required, concurrent implementation of [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span></span> <span data-ttu-id="8b816-118">Questo pattern di controllo è analogo a **IGridItemProvider** con la differenza che qualsiasi controllo che implementa [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) deve esporre a livello di codice la relazione tra la singola cella e le relative informazioni di riga e colonna.</span><span class="sxs-lookup"><span data-stu-id="8b816-118">This control pattern is analogous to **IGridItemProvider** with the distinction that any control implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) must programmatically expose the relationship between the individual cell and its row and column information.</span></span> <span data-ttu-id="8b816-119">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="8b816-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="8b816-120">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8b816-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8b816-121">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="8b816-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="8b816-122">Membri obbligatori per **ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="8b816-122">Required Members for **ITableItemProvider**</span></span>](#required-members-for-itableitemprovider)
-   [<span data-ttu-id="8b816-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b816-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="8b816-124">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="8b816-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="8b816-125">Quando si implementa il pattern di controllo **TableItem** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b816-125">When implementing the **TableItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="8b816-126">Per la funzionalità degli elementi della griglia correlata, vedere [pattern di controllo GridItem](uiauto-implementinggriditem.md).</span><span class="sxs-lookup"><span data-stu-id="8b816-126">For related grid item functionality, see [GridItem Control Pattern](uiauto-implementinggriditem.md).</span></span>

## <a name="required-members-for-itableitemprovider"></a><span data-ttu-id="8b816-127">Membri obbligatori per **ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="8b816-127">Required Members for **ITableItemProvider**</span></span>

<span data-ttu-id="8b816-128">I metodi seguenti sono necessari per implementare l'interfaccia [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="8b816-128">The following methods are required for implementing the [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) interface.</span></span>



| <span data-ttu-id="8b816-129">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="8b816-129">Required members</span></span>                                                               | <span data-ttu-id="8b816-130">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="8b816-130">Member type</span></span> | <span data-ttu-id="8b816-131">Note</span><span class="sxs-lookup"><span data-stu-id="8b816-131">Notes</span></span> |
|--------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="8b816-132">**GetColumnHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="8b816-132">**GetColumnHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | <span data-ttu-id="8b816-133">Metodo</span><span class="sxs-lookup"><span data-stu-id="8b816-133">Method</span></span>      | <span data-ttu-id="8b816-134">nessuno</span><span class="sxs-lookup"><span data-stu-id="8b816-134">None</span></span>  |
| [<span data-ttu-id="8b816-135">**GetRowHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="8b816-135">**GetRowHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | <span data-ttu-id="8b816-136">Metodo</span><span class="sxs-lookup"><span data-stu-id="8b816-136">Method</span></span>      | <span data-ttu-id="8b816-137">nessuno</span><span class="sxs-lookup"><span data-stu-id="8b816-137">None</span></span>  |



 

<span data-ttu-id="8b816-138">Questo pattern di controllo non è associato a proprietà o eventi.</span><span class="sxs-lookup"><span data-stu-id="8b816-138">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b816-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b816-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8b816-140">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8b816-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8b816-141">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="8b816-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="8b816-142">Pattern di controllo Table</span><span class="sxs-lookup"><span data-stu-id="8b816-142">Table Control Pattern</span></span>](uiauto-implementingtable.md)
</dt> <dt>

[<span data-ttu-id="8b816-143">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8b816-143">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="8b816-144">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8b816-144">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




