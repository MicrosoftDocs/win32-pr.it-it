---
title: Elenchi
description: Elenchi
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- mixer audio, controlli
- mixer audio, elenchi
- mixer, controlli
- mixer, elenchi
- controlli elenco
- Struttura MIXERCONTROLDETAILS_BOOLEAN
- Struttura MIXERCONTROLDETAILS_LISTTEXT
- controllo a selezione singola
- controllo a selezione multipla
- controllo mixer
- Multiplexer (MUX)
- MUX (Multiplexer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336999"
---
# <a name="lists"></a><span data-ttu-id="aad5e-115">Elenchi</span><span class="sxs-lookup"><span data-stu-id="aad5e-115">Lists</span></span>

<span data-ttu-id="aad5e-116">I controlli elenco forniscono gli Stati a selezione singola o multipla per le linee audio complesse.</span><span class="sxs-lookup"><span data-stu-id="aad5e-116">The list controls provide single-select or multiple-select states for complex audio lines.</span></span> <span data-ttu-id="aad5e-117">Questi controlli utilizzano la [**struttura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) per recuperare e impostare le proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="aad5e-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="aad5e-118">La [**struttura \_ LISTTEXT di MIXERCONTROLDETAILS**](/previous-versions//dd757296(v=vs.85)) viene usata anche per recuperare tutte le descrizioni di testo di un controllo di più elementi.</span><span class="sxs-lookup"><span data-stu-id="aad5e-118">The [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure is also used to retrieve all text descriptions of a multiple-item control.</span></span> <span data-ttu-id="aad5e-119">Nella tabella seguente vengono descritti i tipi di controlli elenco.</span><span class="sxs-lookup"><span data-stu-id="aad5e-119">The following table describes the types of list controls.</span></span>



| <span data-ttu-id="aad5e-120">Controllo</span><span class="sxs-lookup"><span data-stu-id="aad5e-120">Control</span></span>           | <span data-ttu-id="aad5e-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aad5e-121">Description</span></span>                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aad5e-122">Selezione singola</span><span class="sxs-lookup"><span data-stu-id="aad5e-122">Single-select</span></span>     | <span data-ttu-id="aad5e-123">Limita la selezione del controllo a un elemento alla volta.</span><span class="sxs-lookup"><span data-stu-id="aad5e-123">Restricts the control selection to one item at a time.</span></span> <span data-ttu-id="aad5e-124">A differenza del controllo multiplexer, questo controllo può essere usato per controllare più di righe di origine audio.</span><span class="sxs-lookup"><span data-stu-id="aad5e-124">Unlike the multiplexer control, this control can be used to control more than audio source lines.</span></span> <span data-ttu-id="aad5e-125">Ad esempio, è possibile usare questo controllo per selezionare un filtro low-pass da un elenco di filtri supportati da un dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="aad5e-125">For example, you could use this control to select a low-pass filter from a list of filters supported by a mixer device.</span></span> |
| <span data-ttu-id="aad5e-126">Multiplexer (MUX)</span><span class="sxs-lookup"><span data-stu-id="aad5e-126">Multiplexer (MUX)</span></span> | <span data-ttu-id="aad5e-127">Limita la selezione di riga a una riga di origine alla volta.</span><span class="sxs-lookup"><span data-stu-id="aad5e-127">Restricts the line selection to one source line at a time.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="aad5e-128">Selezione multipla</span><span class="sxs-lookup"><span data-stu-id="aad5e-128">Multiple-select</span></span>   | <span data-ttu-id="aad5e-129">Consente all'utente di selezionare più elementi contemporaneamente da un elenco.</span><span class="sxs-lookup"><span data-stu-id="aad5e-129">Allows the user to select multiple items from a list simultaneously.</span></span> <span data-ttu-id="aad5e-130">A differenza del controllo mixer, il controllo a selezione multipla può essere usato per controllare più di righe di origine audio.</span><span class="sxs-lookup"><span data-stu-id="aad5e-130">Unlike the mixer control, the multiple-select control can be used to control more than audio source lines.</span></span>                                                                                                  |
| <span data-ttu-id="aad5e-131">Mixer</span><span class="sxs-lookup"><span data-stu-id="aad5e-131">Mixer</span></span>             | <span data-ttu-id="aad5e-132">Consente all'utente di selezionare le righe di origine da un elenco simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="aad5e-132">Allows the user to select source lines from a list simultaneously.</span></span>                                                                                                                                                                                                               |



 

 

 