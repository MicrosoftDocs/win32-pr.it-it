---
title: Pattern di controllo VirtualizedItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IVirtualizedItemProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo VirtualizedItem
- Automazione interfaccia utente, pattern di controllo VirtualizedItem
- Automazione interfaccia utente, IVirtualizedItemProvider
- IVirtualizedItemProvider
- implementazione di pattern di controllo VirtualizedItem di automazione interfaccia utente
- Pattern di controllo VirtualizedItem
- pattern di controllo, IVirtualizedItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente VirtualizedItem
- pattern di controllo, VirtualizedItem
- interfacce, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222097"
---
# <a name="virtualizeditem-control-pattern"></a><span data-ttu-id="caaac-113">Pattern di controllo VirtualizedItem</span><span class="sxs-lookup"><span data-stu-id="caaac-113">VirtualizedItem Control Pattern</span></span>

<span data-ttu-id="caaac-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="caaac-114">Describes guidelines and conventions for implementing [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), including information about properties and methods.</span></span> <span data-ttu-id="caaac-115">Il pattern di controllo **VirtualizedItem** viene usato per supportare elementi virtualizzati, ovvero elementi rappresentati da elementi di automazione segnaposto nell'albero di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="caaac-115">The **VirtualizedItem** control pattern is used to support virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.</span></span>

<span data-ttu-id="caaac-116">Gli elementi virtualizzati possono includere elementi recuperati da un controllo che supporta il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) o un oggetto incorporato virtualizzato recuperato da un controllo che supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="caaac-116">Virtualized items can include items retrieved from a control that supports the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern, or a virtualized embedded object retrieved from a control that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span> <span data-ttu-id="caaac-117">Il segnaposto di un elemento virtualizzato potrebbe non avere caricato i dati per tutte le proprietà di automazione interfaccia utente e può restituire l' [**\_ \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) e la restituzione in risposta a query per le proprietà che non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="caaac-117">The placeholder for a virtualized item might not have loaded data for all UI Automation properties, and may return [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) in response to queries for properties that are not available.</span></span> <span data-ttu-id="caaac-118">Il pattern di controllo **VirtualizedItem** fornisce un metodo per la realizzazione di un elemento virtuale in modo da rendere disponibili le informazioni complete per l'elemento ed è possibile creare un elemento di automazione completo per l'elemento nell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="caaac-118">The **VirtualizedItem** control pattern provides a method for realizing a virtual item so that full information is made available for the item, and a full automation element can be created for the item in the UI Automation tree.</span></span>

<span data-ttu-id="caaac-119">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="caaac-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="caaac-120">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="caaac-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="caaac-121">Membri obbligatori per **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="caaac-121">Required Members for **IVirtualizedItemProvider**</span></span>](#required-members-for-ivirtualizeditemprovider)
-   [<span data-ttu-id="caaac-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="caaac-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="caaac-123">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="caaac-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="caaac-124">Quando si implementa il pattern di controllo **VirtualizedItem** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="caaac-124">When implementing the **VirtualizedItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="caaac-125">Qualsiasi elemento segnaposto di automazione interfaccia utente che può essere virtualizzato deve supportare il pattern di controllo **VirtualizedItem** esponendo l'interfaccia [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="caaac-125">Any UI Automation placeholder element that can be virtualized must support the **VirtualizedItem** control pattern by exposing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>
-   <span data-ttu-id="caaac-126">Quando viene chiamato [**IVirtualizedItemProvider:: realizzate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , l'oggetto segnaposto deve essere aggiornato con implementazioni complete delle proprietà e dei pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="caaac-126">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the placeholder object must be updated with full implementations of its properties and control patterns.</span></span>
-   <span data-ttu-id="caaac-127">Quando viene chiamato [**IVirtualizedItemProvider:: réalisateur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , il provider può modificare il viewport in modo da visualizzare l'elemento virtualizzato.</span><span class="sxs-lookup"><span data-stu-id="caaac-127">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the provider can change the viewport so that the virtualized item comes into view.</span></span> <span data-ttu-id="caaac-128">Non è necessario portare l'elemento nella visualizzazione. gli elementi non virtualizzati, tuttavia, devono supportare il metodo [**IScrollItemProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .</span><span class="sxs-lookup"><span data-stu-id="caaac-128">Bringing the item into view is not required; however, off-screen, non-virtualized items should support the [**IScrollItemProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) method.</span></span>

## <a name="required-members-for-ivirtualizeditemprovider"></a><span data-ttu-id="caaac-129">Membri obbligatori per **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="caaac-129">Required Members for **IVirtualizedItemProvider**</span></span>

<span data-ttu-id="caaac-130">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="caaac-130">The following properties and methods are required for implementing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>



| <span data-ttu-id="caaac-131">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="caaac-131">Required members</span></span>                                           | <span data-ttu-id="caaac-132">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="caaac-132">Member type</span></span> | <span data-ttu-id="caaac-133">Note</span><span class="sxs-lookup"><span data-stu-id="caaac-133">Notes</span></span> |
|------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="caaac-134">**Tenere presente**</span><span class="sxs-lookup"><span data-stu-id="caaac-134">**Realize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | <span data-ttu-id="caaac-135">Metodo</span><span class="sxs-lookup"><span data-stu-id="caaac-135">Method</span></span>      | <span data-ttu-id="caaac-136">nessuno</span><span class="sxs-lookup"><span data-stu-id="caaac-136">None</span></span>  |



 

<span data-ttu-id="caaac-137">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="caaac-137">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="caaac-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="caaac-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caaac-139">Implementazione del pattern di controllo ItemContainer di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="caaac-139">Implementing the UI Automation ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
</dt> <dt>

[<span data-ttu-id="caaac-140">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="caaac-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="caaac-141">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="caaac-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="caaac-142">Utilizzo degli elementi virtualizzati</span><span class="sxs-lookup"><span data-stu-id="caaac-142">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




