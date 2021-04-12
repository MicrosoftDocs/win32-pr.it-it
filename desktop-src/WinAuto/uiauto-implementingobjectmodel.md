---
title: Pattern di controllo ObjectModel
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IObjectModelProvider, incluse informazioni sui metodi. Il pattern di controllo ObjectModel viene usato per esporre un puntatore al modello a oggetti sottostante di un documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo ObjectModel
- Automazione interfaccia utente, pattern di controllo ObjectModel
- Automazione interfaccia utente, IObjectModelProvider
- IObjectModelProvider
- implementazione del pattern di controllo ObjectModel di automazione interfaccia utente
- Pattern di controllo ObjectModel
- pattern di controllo, IObjectModelProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente ObjectModel
- pattern di controllo, ObjectModel
- interfacce, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338335"
---
# <a name="objectmodel-control-pattern"></a><span data-ttu-id="8f9d8-114">Pattern di controllo ObjectModel</span><span class="sxs-lookup"><span data-stu-id="8f9d8-114">ObjectModel Control Pattern</span></span>

<span data-ttu-id="8f9d8-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), incluse informazioni sui metodi.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-115">Describes guidelines and conventions for implementing [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), including information about methods.</span></span> <span data-ttu-id="8f9d8-116">Il pattern di controllo **ObjectModel** viene usato per esporre un puntatore al modello a oggetti sottostante di un documento.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-116">The **ObjectModel** control pattern is used to expose a pointer to the underlying object model of a document.</span></span>

<span data-ttu-id="8f9d8-117">Molte applicazioni implementano modelli a oggetti avanzati che aggiungono valore oltre a quello fornito da automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-117">Many applications implement rich object models that add value beyond what Microsoft UI Automation provides.</span></span> <span data-ttu-id="8f9d8-118">Questo pattern di controllo consente a un client di passare da un elemento di automazione interfaccia utente al modello a oggetti sottostante.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-118">This control pattern allows a client to navigate from a UI Automation element into the underlying object model.</span></span>

<span data-ttu-id="8f9d8-119">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8f9d8-120">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="8f9d8-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="8f9d8-121">Membri obbligatori per **IObjectModelProvider**</span><span class="sxs-lookup"><span data-stu-id="8f9d8-121">Required Members for **IObjectModelProvider**</span></span>](#required-members-for-iobjectmodelprovider)
-   [<span data-ttu-id="8f9d8-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f9d8-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="8f9d8-123">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="8f9d8-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="8f9d8-124">Quando si implementa il pattern di controllo **ObjectModel** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f9d8-124">When implementing the **ObjectModel** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="8f9d8-125">Il metodo [**IObjectModelProvider:: GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) deve restituire un puntatore all'oggetto che è il più vicino possibile all'elemento dell'interfaccia utente di origine.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-125">The [**IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) method should return a pointer to the object that is as close as possible to the source UI element.</span></span> <span data-ttu-id="8f9d8-126">Ad esempio, in un Web browser, un provider di automazione interfaccia utente per un singolo elemento deve restituire un puntatore del modello a oggetti per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-126">For example, in a web browser, a UI Automation provider for a single element should return an object model pointer for the element.</span></span> <span data-ttu-id="8f9d8-127">La restituzione di un puntatore del modello a oggetti per la radice del documento sarebbe molto meno utile.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-127">Returning an object model pointer for the document root would be far less useful.</span></span>
-   <span data-ttu-id="8f9d8-128">Il client del pattern di controllo **ObjectModel** dovrebbe avere l'IID per l'interfaccia cercata, motivo per cui è sufficiente restituire un semplice puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8f9d8-128">The client of the **ObjectModel** control pattern is expected to have the IID for the interface they are seeking, which is why it is enough to return a simple [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="8f9d8-129">Poiché l'automazione interfaccia utente esegue il marshalling del puntatore al processo client, il provider deve prevedere che il client acceda al modello a oggetti utilizzando le procedure standard Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="8f9d8-129">Because UI Automation marshals the pointer to the client process, the provider should expect the client to access the object model using standard Component Object Model (COM) practices.</span></span>

## <a name="required-members-for-iobjectmodelprovider"></a><span data-ttu-id="8f9d8-130">Membri obbligatori per **IObjectModelProvider**</span><span class="sxs-lookup"><span data-stu-id="8f9d8-130">Required Members for **IObjectModelProvider**</span></span>

<span data-ttu-id="8f9d8-131">Il metodo seguente è necessario per implementare l'interfaccia [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) .</span><span class="sxs-lookup"><span data-stu-id="8f9d8-131">The following method is required for implementing the [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) interface.</span></span>



| <span data-ttu-id="8f9d8-132">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="8f9d8-132">Required members</span></span>                                                                             | <span data-ttu-id="8f9d8-133">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="8f9d8-133">Member type</span></span> | <span data-ttu-id="8f9d8-134">Note</span><span class="sxs-lookup"><span data-stu-id="8f9d8-134">Notes</span></span>                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9d8-135">**GetUnderlyingObjectModel**</span><span class="sxs-lookup"><span data-stu-id="8f9d8-135">**GetUnderlyingObjectModel**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | <span data-ttu-id="8f9d8-136">Metodo</span><span class="sxs-lookup"><span data-stu-id="8f9d8-136">Method</span></span>      | <span data-ttu-id="8f9d8-137">Restituisce un puntatore COM al modello a oggetti sottostante.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-137">Returns a COM pointer to the underlying object model.</span></span> <span data-ttu-id="8f9d8-138">Si prevede che il client chiami il metodo [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per recuperare i puntatori specifici del modello a oggetti.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-138">The client is expected to call the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to retrieve specific object model pointers.</span></span> |



 

<span data-ttu-id="8f9d8-139">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="8f9d8-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f9d8-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f9d8-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f9d8-141">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="8f9d8-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="8f9d8-142">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8f9d8-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="8f9d8-143">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8f9d8-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 