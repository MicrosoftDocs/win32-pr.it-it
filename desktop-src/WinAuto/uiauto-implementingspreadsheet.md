---
title: Pattern di controllo foglio di calcolo
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISpreadsheetProvider, incluse informazioni sui metodi.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Spreadsheet
- Automazione interfaccia utente, pattern di controllo foglio di calcolo
- Automazione interfaccia utente, ISpreadsheetProvider
- ISpreadsheetProvider
- implementazione del pattern di controllo Spreadsheet di automazione interfaccia utente
- pattern di controllo foglio di calcolo
- pattern di controllo, ISpreadsheetProvider
- pattern di controllo, implementazione del foglio di calcolo di automazione
- pattern di controllo, foglio di calcolo
- interfacce, ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338327"
---
# <a name="spreadsheet-control-pattern"></a><span data-ttu-id="4ec0e-113">Pattern di controllo foglio di calcolo</span><span class="sxs-lookup"><span data-stu-id="4ec0e-113">Spreadsheet Control Pattern</span></span>

<span data-ttu-id="4ec0e-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), incluse informazioni sui metodi.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-114">Describes guidelines and conventions for implementing [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), including information about methods.</span></span> <span data-ttu-id="4ec0e-115">Alla fine della panoramica sono elencati collegamenti ad altro materiale di riferimento.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="4ec0e-116">Il pattern di controllo **Spreadsheet** viene usato per esporre il contenuto di un foglio di calcolo o di un altro documento basato su griglia.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-116">The **Spreadsheet** control pattern is used to expose the contents of a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="4ec0e-117">Il pattern di controllo del **foglio di calcolo** è strettamente correlato al pattern di controllo [Grid](uiauto-implementinggrid.md) ; i controlli che implementano il pattern di controllo del **foglio di calcolo** devono implementare anche il pattern di controllo Grid.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-117">The **Spreadsheet** control pattern is closely related to the [Grid](uiauto-implementinggrid.md) control pattern; controls that implement the **Spreadsheet** control pattern should also implement the Grid control pattern.</span></span> <span data-ttu-id="4ec0e-118">I controlli possono anche implementare il pattern di controllo [Table](uiauto-implementingtable.md) , se appropriato.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-118">Controls can also implement the [Table](uiauto-implementingtable.md) control pattern, if appropriate.</span></span> <span data-ttu-id="4ec0e-119">Per esempi di controlli che implementano questi pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="4ec0e-119">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="4ec0e-120">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="4ec0e-120">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="4ec0e-121">Quando si implementa il pattern di controllo **Spreadsheet** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ec0e-121">When implementing the **Spreadsheet** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="4ec0e-122">Se un foglio di calcolo implementa l'interfaccia [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , le relative celle devono implementare l'interfaccia [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="4ec0e-122">If a spreadsheet implements the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface, its cells must implement the [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>
-   <span data-ttu-id="4ec0e-123">Il metodo [**ISpreadsheetProvider:: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) ha lo scopo di fornire lo stesso tipo di spostamento che un'applicazione può fornire con una funzionalità **di salto all'etichetta** .</span><span class="sxs-lookup"><span data-stu-id="4ec0e-123">The [**ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) method is intended to provide the same kind of navigation that an application might supply with a **Jump to Label** feature.</span></span> <span data-ttu-id="4ec0e-124">Molti programmi di fogli di calcolo consentono a determinate celle di assegnare un nome descrittivo o un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-124">Many spreadsheet programs let specific cells be given a friendly name or label.</span></span> <span data-ttu-id="4ec0e-125">**GetItemByName** consente al client di cercare una cella in base al nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-125">**GetItemByName** enables the client to look up a cell based on its friendly name.</span></span> <span data-ttu-id="4ec0e-126">Questo metodo non deve recuperare le celle che contengono il testo del nome perché i risultati possono essere estremamente ambigui.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-126">This method should not retrieve any cells that contain the name text because the results can be highly ambiguous.</span></span> <span data-ttu-id="4ec0e-127">Se il programma di foglio di calcolo consente a più celle nello stesso foglio di calcolo di avere lo stesso nome descrittivo o etichetta, il comportamento di automazione interfaccia utente Microsoft non è definito.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-127">If the spreadsheet program allows multiple cells in the same a spreadsheet to have the same friendly name or label, the Microsoft UI Automation behavior is undefined.</span></span>

## <a name="required-members-for-ispreadsheetprovider"></a><span data-ttu-id="4ec0e-128">Membri obbligatori per **ISpreadsheetProvider**</span><span class="sxs-lookup"><span data-stu-id="4ec0e-128">Required Members for **ISpreadsheetProvider**</span></span>

<span data-ttu-id="4ec0e-129">Il metodo seguente è necessario per implementare l'interfaccia [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) .</span><span class="sxs-lookup"><span data-stu-id="4ec0e-129">The following method is required for implementing the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface.</span></span>



| <span data-ttu-id="4ec0e-130">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="4ec0e-130">Required members</span></span>                                                       | <span data-ttu-id="4ec0e-131">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="4ec0e-131">Member type</span></span> | <span data-ttu-id="4ec0e-132">Note</span><span class="sxs-lookup"><span data-stu-id="4ec0e-132">Notes</span></span> |
|------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="4ec0e-133">**GetItemByName**</span><span class="sxs-lookup"><span data-stu-id="4ec0e-133">**GetItemByName**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | <span data-ttu-id="4ec0e-134">Metodo</span><span class="sxs-lookup"><span data-stu-id="4ec0e-134">Method</span></span>      | <span data-ttu-id="4ec0e-135">nessuno</span><span class="sxs-lookup"><span data-stu-id="4ec0e-135">None</span></span>  |



 

<span data-ttu-id="4ec0e-136">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="4ec0e-136">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ec0e-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ec0e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ec0e-138">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="4ec0e-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="4ec0e-139">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4ec0e-139">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="4ec0e-140">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4ec0e-140">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 