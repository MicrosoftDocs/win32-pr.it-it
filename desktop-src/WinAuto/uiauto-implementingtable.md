---
title: Pattern di controllo Table
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ITableProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Table viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Table
- Automazione interfaccia utente, pattern di controllo Table
- Automazione interfaccia utente, ITableProvider
- ITableProvider
- implementazione di pattern di controllo Table di automazione interfaccia utente
- Pattern di controllo Table
- pattern di controllo, ITableProvider
- pattern di controllo, implementazione della tabella di automazione interfaccia utente
- pattern di controllo, tabella
- interfacce, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104554478"
---
# <a name="table-control-pattern"></a><span data-ttu-id="8599f-114">Pattern di controllo Table</span><span class="sxs-lookup"><span data-stu-id="8599f-114">Table Control Pattern</span></span>

<span data-ttu-id="8599f-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="8599f-115">Describes guidelines and conventions for implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), including information about properties and methods.</span></span> <span data-ttu-id="8599f-116">Il pattern di controllo **Table** viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="8599f-116">The **Table** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="8599f-117">Gli elementi figlio dell'elemento contenitore devono implementare [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) ed essere organizzati in un sistema di coordinate logico bidimensionale che può essere attraversato da righe e colonne.</span><span class="sxs-lookup"><span data-stu-id="8599f-117">The children of the container element must implement [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="8599f-118">Questo pattern di controllo è analogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , con la differenza che qualsiasi controllo che implementa [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) deve esporre anche una relazione di intestazione di riga e/o di colonna per ogni elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="8599f-118">This control pattern is analogous to [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) with the distinction that any control implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) must also expose a column and/or row header relationship for each child element.</span></span> <span data-ttu-id="8599f-119">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="8599f-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="8599f-120">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8599f-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8599f-121">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="8599f-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="8599f-122">Membri obbligatori per **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="8599f-122">Required Members for **ITableProvider**</span></span>](#required-members-for-itableprovider)
-   [<span data-ttu-id="8599f-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8599f-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="8599f-124">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="8599f-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="8599f-125">Quando si implementa il pattern di controllo **Table** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8599f-125">When implementing the **Table** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="8599f-126">L'accesso al contenuto delle singole celle avviene tramite un sistema di coordinate logico bidimensionale o una matrice fornita dall'implementazione simultanea richiesta di [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="8599f-126">Access to the content of individual cells is through a two-dimensional logical coordinate system or array provided by the required, concurrent implementation of [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>
-   <span data-ttu-id="8599f-127">Un'intestazione di riga o colonna può essere contenuta all'interno di un oggetto tabella oppure essere un oggetto intestazione distinto associato a un oggetto tabella.</span><span class="sxs-lookup"><span data-stu-id="8599f-127">A column or row header can be contained within a table object or be a separate header object that is associated with a table object.</span></span>
-   <span data-ttu-id="8599f-128">Le intestazioni di riga e colonna possono includere un'intestazione principale nonché intestazioni di supporto.</span><span class="sxs-lookup"><span data-stu-id="8599f-128">Column and row headers may include both a primary header as well as any supporting headers.</span></span>
    > [!Note]  
    > <span data-ttu-id="8599f-129">Questo concetto diventa evidente in un foglio di calcolo di Microsoft Excel in cui un utente ha definito una colonna con **nome** .</span><span class="sxs-lookup"><span data-stu-id="8599f-129">This concept becomes evident in a Microsoft Excel spreadsheet where a user has defined a **First name** column.</span></span> <span data-ttu-id="8599f-130">Questa colonna include ora due intestazioni, tra cui l'intestazione del **nome** definito dall'utente e la designazione alfanumerica per la colonna assegnata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8599f-130">This column now has two headers, including the **First name** header defined by the user, and the alphanumeric designation for that column assigned by the application.</span></span>

     

-   <span data-ttu-id="8599f-131">Vedere [pattern di controllo Grid](uiauto-implementinggrid.md) per la funzionalità della griglia correlata.</span><span class="sxs-lookup"><span data-stu-id="8599f-131">See [Grid Control Pattern](uiauto-implementinggrid.md) for related grid functionality.</span></span>

    <span data-ttu-id="8599f-132">Nell'immagine seguente viene illustrata una tabella con intestazioni di colonna complesse.</span><span class="sxs-lookup"><span data-stu-id="8599f-132">The following image shows a table with complex column headers.</span></span>

    ![tabella con intestazioni di colonna complesse](images/uia-valuepattern-colorpicker.jpg)

    <span data-ttu-id="8599f-134">Nell'immagine seguente viene illustrata una tabella con una proprietà [**ITableProvider:: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambigua.</span><span class="sxs-lookup"><span data-stu-id="8599f-134">The following image shows a table with an ambiguous [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) property.</span></span>

    ![tabella con una proprietà RowOrColumnMajor ambigua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a><span data-ttu-id="8599f-136">Membri obbligatori per **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="8599f-136">Required Members for **ITableProvider**</span></span>

<span data-ttu-id="8599f-137">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) .</span><span class="sxs-lookup"><span data-stu-id="8599f-137">The following properties and methods are required for implementing the [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) interface.</span></span>



| <span data-ttu-id="8599f-138">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="8599f-138">Required members</span></span>                                                   | <span data-ttu-id="8599f-139">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="8599f-139">Member type</span></span> | <span data-ttu-id="8599f-140">Note</span><span class="sxs-lookup"><span data-stu-id="8599f-140">Notes</span></span> |
|--------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="8599f-141">**RowOrColumnMajor**</span><span class="sxs-lookup"><span data-stu-id="8599f-141">**RowOrColumnMajor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | <span data-ttu-id="8599f-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8599f-142">Property</span></span>    | <span data-ttu-id="8599f-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="8599f-143">None</span></span>  |
| [<span data-ttu-id="8599f-144">**GetColumnHeaders**</span><span class="sxs-lookup"><span data-stu-id="8599f-144">**GetColumnHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | <span data-ttu-id="8599f-145">Metodo</span><span class="sxs-lookup"><span data-stu-id="8599f-145">Method</span></span>      | <span data-ttu-id="8599f-146">nessuno</span><span class="sxs-lookup"><span data-stu-id="8599f-146">None</span></span>  |
| [<span data-ttu-id="8599f-147">**GetRowHeaders**</span><span class="sxs-lookup"><span data-stu-id="8599f-147">**GetRowHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | <span data-ttu-id="8599f-148">Metodo</span><span class="sxs-lookup"><span data-stu-id="8599f-148">Method</span></span>      | <span data-ttu-id="8599f-149">nessuno</span><span class="sxs-lookup"><span data-stu-id="8599f-149">None</span></span>  |



 

<span data-ttu-id="8599f-150">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="8599f-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8599f-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8599f-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8599f-152">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8599f-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8599f-153">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="8599f-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="8599f-154">Pattern di controllo TableItem</span><span class="sxs-lookup"><span data-stu-id="8599f-154">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
</dt> <dt>

[<span data-ttu-id="8599f-155">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8599f-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="8599f-156">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8599f-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




