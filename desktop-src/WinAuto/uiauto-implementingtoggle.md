---
title: Mostra/Nascondi pattern di controllo
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IToggleProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo di alternanza viene usato per supportare i controlli che possono scorrere un insieme di Stati e gestire uno stato una volta impostato.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo di attivazione
- Automazione interfaccia utente, controllo interruttore
- Automazione interfaccia utente, IToggleProvider
- IToggleProvider
- implementazione di pattern di controllo di automazione interfaccia utente
- Imposta/Nascondi pattern di controllo
- pattern di controllo, IToggleProvider
- pattern di controllo, implementazione dell'attivazione di automazione interfaccia utente
- pattern di controllo, interruttore
- interfacce, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395610"
---
# <a name="toggle-control-pattern"></a><span data-ttu-id="177cd-114">Mostra/Nascondi pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="177cd-114">Toggle Control Pattern</span></span>

<span data-ttu-id="177cd-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="177cd-115">Describes guidelines and conventions for implementing [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), including information about properties and methods.</span></span> <span data-ttu-id="177cd-116">Il pattern di controllo di **alternanza** viene usato per supportare i controlli che possono scorrere un insieme di Stati e gestire uno stato una volta impostato.</span><span class="sxs-lookup"><span data-stu-id="177cd-116">The **Toggle** control pattern is used to support controls that can cycle through a set of states and maintain a state once set.</span></span>

<span data-ttu-id="177cd-117">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="177cd-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="177cd-118">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="177cd-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="177cd-119">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="177cd-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="177cd-120">Membri obbligatori per **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="177cd-120">Required Members for **IToggleProvider**</span></span>](#required-members-for-itoggleprovider)
-   [<span data-ttu-id="177cd-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="177cd-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="177cd-122">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="177cd-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="177cd-123">Quando si implementa il pattern di controllo di **attivazione** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="177cd-123">When implementing the **Toggle** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="177cd-124">I controlli che non mantengono lo stato quando vengono attivati, ad esempio pulsanti, pulsanti della barra degli strumenti e collegamenti ipertestuali, devono invece implementare [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .</span><span class="sxs-lookup"><span data-stu-id="177cd-124">Controls that do not maintain state when activated, such as buttons, toolbar buttons, and hyperlinks, must implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) instead.</span></span>
-   <span data-ttu-id="177cd-125">Un controllo deve scorrere i relativi stati di attivazione/disattivazione ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) nell'ordine seguente: **ToggleState \_ on**, **ToggleState \_ off** e, se supportato, **ToggleState \_ indeterminato**.</span><span class="sxs-lookup"><span data-stu-id="177cd-125">A control must cycle through its toggle states ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) in the following order: **ToggleState\_On**, **ToggleState\_Off** and, if supported, **ToggleState\_Indeterminate**.</span></span>
-   <span data-ttu-id="177cd-126">L' **attivazione/disattivazione** non fornisce un metodo di stato set a causa di problemi relativi all'impostazione diretta di una casella di controllo a tre stati senza eseguire il ciclo della sequenza [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) appropriata.</span><span class="sxs-lookup"><span data-stu-id="177cd-126">**Toggle** does not provide a set-state method because of issues surrounding the direct setting of a three-state check box without cycling through its appropriate [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) sequence.</span></span>
-   <span data-ttu-id="177cd-127">Il controllo pulsante di opzione non implementa [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), perché non è in grado di eseguire il Cycling negli stati validi.</span><span class="sxs-lookup"><span data-stu-id="177cd-127">The radio button control does not implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), because it is not capable of cycling through its valid states.</span></span>

## <a name="required-members-for-itoggleprovider"></a><span data-ttu-id="177cd-128">Membri obbligatori per **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="177cd-128">Required Members for **IToggleProvider**</span></span>

<span data-ttu-id="177cd-129">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) .</span><span class="sxs-lookup"><span data-stu-id="177cd-129">The following properties and methods are required for implementing the [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) interface.</span></span>



| <span data-ttu-id="177cd-130">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="177cd-130">Required members</span></span>                                          | <span data-ttu-id="177cd-131">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="177cd-131">Member type</span></span> | <span data-ttu-id="177cd-132">Note</span><span class="sxs-lookup"><span data-stu-id="177cd-132">Notes</span></span> |
|-----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="177cd-133">**Interruttore**</span><span class="sxs-lookup"><span data-stu-id="177cd-133">**Toggle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | <span data-ttu-id="177cd-134">Metodo</span><span class="sxs-lookup"><span data-stu-id="177cd-134">Method</span></span>      | <span data-ttu-id="177cd-135">nessuno</span><span class="sxs-lookup"><span data-stu-id="177cd-135">None</span></span>  |
| [<span data-ttu-id="177cd-136">**ToggleState**</span><span class="sxs-lookup"><span data-stu-id="177cd-136">**ToggleState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | <span data-ttu-id="177cd-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="177cd-137">Property</span></span>    | <span data-ttu-id="177cd-138">nessuno</span><span class="sxs-lookup"><span data-stu-id="177cd-138">None</span></span>  |



 

<span data-ttu-id="177cd-139">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="177cd-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="177cd-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="177cd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="177cd-141">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="177cd-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="177cd-142">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="177cd-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="177cd-143">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="177cd-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




