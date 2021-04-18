---
title: Pattern di controllo SynchronizedInput
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISynchronizedInputProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo SynchronizedInput
- Automazione interfaccia utente, pattern di controllo SynchronizedInput
- Automazione interfaccia utente, ISynchronizedInputProvider
- ISynchronizedInputProvider
- implementazione di pattern di controllo SynchronizedInput di automazione interfaccia utente
- Pattern di controllo SynchronizedInput
- pattern di controllo, ISynchronizedInputProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente SynchronizedInput
- pattern di controllo, SynchronizedInput
- interfacce, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298615"
---
# <a name="synchronizedinput-control-pattern"></a><span data-ttu-id="5412b-113">Pattern di controllo SynchronizedInput</span><span class="sxs-lookup"><span data-stu-id="5412b-113">SynchronizedInput Control Pattern</span></span>

<span data-ttu-id="5412b-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="5412b-114">Describes guidelines and conventions for implementing [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), including information about properties and methods.</span></span> <span data-ttu-id="5412b-115">Il pattern di controllo **SynchronizedInput** consente alle applicazioni client di automazione interfaccia utente Microsoft di indirizzare l'input del mouse o della tastiera a un elemento specifico dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5412b-115">The **SynchronizedInput** control pattern enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element.</span></span>

<span data-ttu-id="5412b-116">Questo pattern di controllo viene in genere usato negli script di test automatizzati per inviare l'input del mouse o della tastiera a un elemento dell'interfaccia utente specifico e quindi verificare che l'elemento abbia ricevuto l'input.</span><span class="sxs-lookup"><span data-stu-id="5412b-116">This control pattern is typically used in automated test scripts to send mouse or keyboard input to a specific user-interface element, and then verify that the element received the input.</span></span>

<span data-ttu-id="5412b-117">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="5412b-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5412b-118">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="5412b-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="5412b-119">Membri obbligatori per **ISynchronizedInputProvider**</span><span class="sxs-lookup"><span data-stu-id="5412b-119">Required Members for **ISynchronizedInputProvider**</span></span>](#required-members-for-isynchronizedinputprovider)
-   [<span data-ttu-id="5412b-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5412b-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="5412b-121">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="5412b-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="5412b-122">Quando si implementa il pattern di controllo **SynchronizedInput** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5412b-122">When implementing the **SynchronizedInput** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="5412b-123">Quando viene chiamato il metodo [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) , il provider di automazione interfaccia utente deve iniziare a controllare l'input del tipo specificato e quindi eseguire una delle azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5412b-123">When the [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) method is called, the UI Automation provider should start checking for input of the specified type, and then take one of the following actions:</span></span>
    -   <span data-ttu-id="5412b-124">Quando viene trovato un input corrispondente per l'elemento, il provider deve generare l'evento [**\_ InputReachedTargetEventId di UIA**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="5412b-124">When matching input is found for the element, the provider should raise the [**UIA\_InputReachedTargetEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="5412b-125">Quando viene trovato un input corrispondente, ma è stato raggiunto un elemento diverso, il provider deve generare l'evento [**\_ InputReachedOtherElementEventId di UIA**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="5412b-125">When matching input is found, but it reached a different element, the provider should raise the [**UIA\_InputReachedOtherElementEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="5412b-126">Quando viene trovato un input non corrispondente, il provider deve eliminare l'input e generare l' [**evento \_ InputDiscardedEventId**](uiauto-event-ids.md) di gestione dei servizi.</span><span class="sxs-lookup"><span data-stu-id="5412b-126">When mismatched input is found, the provider should discard the input and raise the [**UIA\_InputDiscardedEventId**](uiauto-event-ids.md) event.</span></span>
-   <span data-ttu-id="5412b-127">Il provider di automazione interfaccia utente deve eliminare l'input se è per un elemento diverso dall'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="5412b-127">The UI Automation provider must discard the input if it is for an element other than the current element.</span></span>
-   <span data-ttu-id="5412b-128">Quando l'elemento riceve l'input o quando viene chiamato il metodo [**ISynchronizedInputProvider:: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) , il provider interrompe il controllo dell'input e continua normalmente.</span><span class="sxs-lookup"><span data-stu-id="5412b-128">When the element receives the input, or when the [**ISynchronizedInputProvider::Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) method is called, the provider stops checking input and continues as normal.</span></span>
-   <span data-ttu-id="5412b-129">Se [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) viene chiamato quando il provider è già in ascolto per l'input, il provider deve restituire l'oggetto [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5412b-129">If [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) is called when the provider is already listening for input, the provider should return [**UIA\_E\_INVALIDOPERATION**](uiauto-error-codes.md).</span></span>

## <a name="required-members-for-isynchronizedinputprovider"></a><span data-ttu-id="5412b-130">Membri obbligatori per **ISynchronizedInputProvider**</span><span class="sxs-lookup"><span data-stu-id="5412b-130">Required Members for **ISynchronizedInputProvider**</span></span>

<span data-ttu-id="5412b-131">Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) .</span><span class="sxs-lookup"><span data-stu-id="5412b-131">The following properties, methods, and events are required for implementing the [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) interface.</span></span>



| <span data-ttu-id="5412b-132">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="5412b-132">Required members</span></span>                                                                         | <span data-ttu-id="5412b-133">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="5412b-133">Member type</span></span> | <span data-ttu-id="5412b-134">Note</span><span class="sxs-lookup"><span data-stu-id="5412b-134">Notes</span></span> |
|------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="5412b-135">**StartListening**</span><span class="sxs-lookup"><span data-stu-id="5412b-135">**StartListening**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | <span data-ttu-id="5412b-136">Metodo</span><span class="sxs-lookup"><span data-stu-id="5412b-136">Method</span></span>      | <span data-ttu-id="5412b-137">nessuno</span><span class="sxs-lookup"><span data-stu-id="5412b-137">None</span></span>  |
| [<span data-ttu-id="5412b-138">**Annulla**</span><span class="sxs-lookup"><span data-stu-id="5412b-138">**Cancel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | <span data-ttu-id="5412b-139">Metodo</span><span class="sxs-lookup"><span data-stu-id="5412b-139">Method</span></span>      | <span data-ttu-id="5412b-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="5412b-140">None</span></span>  |
| [<span data-ttu-id="5412b-141">**\_INPUTREACHEDTARGETEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="5412b-141">**UIA\_InputReachedTargetEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="5412b-142">Evento</span><span class="sxs-lookup"><span data-stu-id="5412b-142">Event</span></span>       | <span data-ttu-id="5412b-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="5412b-143">None</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="5412b-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5412b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5412b-145">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="5412b-145">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




