---
title: Architettura (Framework dei servizi di testo)
description: Architettura
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Framework servizi di testo (TSF), architettura
- TSF (Framework di servizi di testo), architettura
- Servizi di testo, architettura
- Applicazioni abilitate per TSF, architettura
- Framework servizi di testo (TSF), componenti
- TSF (Framework di servizi di testo), componenti
- Servizi di testo, componenti
- Applicazioni abilitate per TSF, componenti
- Framework servizi di testo (TSF), applicazioni
- TSF (Framework di servizi di testo), applicazioni
- Servizi di testo, applicazioni
- Applicazioni abilitate per TSF, informazioni
- Framework servizi di testo (TSF), servizi di testo
- TSF (Text Services Framework), servizi di testo
- Servizi di testo, informazioni
- Applicazioni abilitate per TSF, servizi di testo
- Framework servizi di testo (TSF), gestione TSF
- TSF (Text Services Framework), gestione TSF
- Servizi di testo, gestione TSF
- Applicazioni abilitate per TSF, gestione TSF
- Gestione TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104565282"
---
# <a name="architecture-text-services-framework"></a><span data-ttu-id="701d3-124">Architettura (Framework dei servizi di testo)</span><span class="sxs-lookup"><span data-stu-id="701d3-124">Architecture (Text Services Framework)</span></span>

<span data-ttu-id="701d3-125">Il Framework di servizi di testo include tre componenti principali:</span><span class="sxs-lookup"><span data-stu-id="701d3-125">Text Services Framework includes three primary components:</span></span>

-   <span data-ttu-id="701d3-126">**Applicazioni:** Le operazioni dell'applicazione includono in genere la visualizzazione, la modifica diretta e l'archiviazione del testo.</span><span class="sxs-lookup"><span data-stu-id="701d3-126">**Applications:** Application operations typically include display, direct editing, and storage of text.</span></span> <span data-ttu-id="701d3-127">Un'applicazione fornisce l'accesso al testo implementando un server COM che supporta determinate interfacce e comunica con TSF usando le interfacce esposte dal gestore TSF.</span><span class="sxs-lookup"><span data-stu-id="701d3-127">An application provides access to text by implementing a COM server that supports certain interfaces and communicates with TSF using interfaces that the TSF manager exposes.</span></span> <span data-ttu-id="701d3-128">In questa documentazione, il termine applicazione si riferisce a un'applicazione abilitata per TSF, salvo diversa indicazione.</span><span class="sxs-lookup"><span data-stu-id="701d3-128">Throughout this documentation, the term, application, refers to a TSF-enabled application, unless otherwise specified.</span></span>
-   <span data-ttu-id="701d3-129">**Servizi di testo:** Un servizio di testo funziona come provider di testo per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="701d3-129">**Text Services:** A text service functions as a text provider to an application.</span></span> <span data-ttu-id="701d3-130">Un servizio di testo può ottenere testo da e scrivere testo in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="701d3-130">A text service can obtain text from, and write text to, an application.</span></span> <span data-ttu-id="701d3-131">Un servizio di testo può inoltre associare dati e proprietà a un blocco di testo.</span><span class="sxs-lookup"><span data-stu-id="701d3-131">A text service can also associate data and properties with a block of text.</span></span> <span data-ttu-id="701d3-132">Un servizio di testo viene implementato come un server COM in-process che si registra con TSF.</span><span class="sxs-lookup"><span data-stu-id="701d3-132">A text service is implemented as a COM in-proc server that registers itself with TSF.</span></span> <span data-ttu-id="701d3-133">Quando viene registrato, l'utente interagisce con il servizio di testo utilizzando la barra della lingua o i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="701d3-133">When registered, the user interacts with the text service using the language bar or keyboard shortcuts.</span></span> <span data-ttu-id="701d3-134">È possibile installare più servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="701d3-134">Multiple text services can be installed.</span></span>
-   <span data-ttu-id="701d3-135">**Gestione TSF:** Il gestore di TSF funziona come Mediator tra un'applicazione e uno o più servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="701d3-135">**TSF Manager:** The TSF manager functions as a mediator between an application and one or more text services.</span></span> <span data-ttu-id="701d3-136">Un servizio di testo non interagisce mai direttamente con un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="701d3-136">A text service never interacts directly with an application.</span></span> <span data-ttu-id="701d3-137">Tutte le comunicazioni passano attraverso gestione TSF.</span><span class="sxs-lookup"><span data-stu-id="701d3-137">All communication passes through the TSF manager.</span></span> <span data-ttu-id="701d3-138">Il gestore TSF viene implementato dal sistema operativo e non può essere sostituito.</span><span class="sxs-lookup"><span data-stu-id="701d3-138">The TSF manager is implemented by the operating system and cannot be replaced.</span></span> <span data-ttu-id="701d3-139">In questa documentazione, il termine gestione si riferisce al gestore di TSF, salvo diversa indicazione.</span><span class="sxs-lookup"><span data-stu-id="701d3-139">Throughout this documentation, the term, manager, refers to the TSF manager, unless otherwise specified.</span></span>

<span data-ttu-id="701d3-140">La figura seguente Mostra gli elementi architetturali principali di TSF.</span><span class="sxs-lookup"><span data-stu-id="701d3-140">The following illustration shows the primary architectural elements of TSF.</span></span>

![architettura del Framework dei servizi di testo](images/tsf-arch.gif)

<span data-ttu-id="701d3-142">Con questa architettura, gestione TSF fornisce un livello di astrazione tra le applicazioni e i servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="701d3-142">With this architecture, the TSF manager provides an abstraction layer between applications and text services.</span></span> <span data-ttu-id="701d3-143">Questo livello di astrazione consente a un'applicazione e uno o più servizi di testo di condividere il testo e consente al gestore di TSF di gestire i servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="701d3-143">This abstraction layer enables an application and one or more text services to share text, and it enables the TSF manager to manage text services.</span></span>

 

 




