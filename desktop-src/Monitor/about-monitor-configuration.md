---
title: Informazioni sulla configurazione del monitoraggio
description: Informazioni sulla configurazione del monitoraggio
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- monitoraggio, informazioni
- monitoraggio, calibrazione colore
- monitoraggio, regolazione dell'area di visualizzazione del monitoraggio
- monitorare, salvare le impostazioni di monitoraggio
- monitoraggio, ripristino delle impostazioni di monitoraggio
- monitoraggio, funzionalità fornitore
- calibrazione colore
- regolazione dell'area di visualizzazione del monitoraggio
- salvataggio delle impostazioni di monitoraggio
- ripristino delle impostazioni di monitoraggio
- funzionalità fornitore
- configurazione del monitoraggio, calibrazione del colore
- configurazione del monitoraggio, informazioni
- configurazione del monitoraggio, regolazione dell'area di visualizzazione del monitoraggio
- monitorare la configurazione, salvare le impostazioni di monitoraggio
- configurazione del monitoraggio, ripristino delle impostazioni di monitoraggio
- monitorare la configurazione, le funzionalità del fornitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515682"
---
# <a name="about-monitor-configuration"></a><span data-ttu-id="d50d6-120">Informazioni sulla configurazione del monitoraggio</span><span class="sxs-lookup"><span data-stu-id="d50d6-120">About Monitor Configuration</span></span>

<span data-ttu-id="d50d6-121">Gli utilizzi per le funzioni di configurazione di monitoraggio includono:</span><span class="sxs-lookup"><span data-stu-id="d50d6-121">Uses for the monitor configuration functions include:</span></span>

-   <span data-ttu-id="d50d6-122">Calibrazione del colore.</span><span class="sxs-lookup"><span data-stu-id="d50d6-122">Color calibration.</span></span> <span data-ttu-id="d50d6-123">Un monitoraggio correttamente calibrato riproduce correttamente i colori.</span><span class="sxs-lookup"><span data-stu-id="d50d6-123">A properly calibrated monitor reproduces colors correctly.</span></span> <span data-ttu-id="d50d6-124">In genere, un'applicazione di calibrazione colori Visualizza un criterio di test e dispone di controlli per modificare un'impostazione di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="d50d6-124">Typically, a color calibration application displays a test pattern and has controls to change a monitor setting.</span></span> <span data-ttu-id="d50d6-125">L'utente modifica l'impostazione fino a quando non viene soddisfatta una condizione e ripete questo processo per ogni impostazione di monitoraggio fino a quando non viene calibrato il monitor.</span><span class="sxs-lookup"><span data-stu-id="d50d6-125">The user changes the setting until a condition is met, and repeats this process for each monitor setting until the monitor is calibrated.</span></span>
-   <span data-ttu-id="d50d6-126">Regolazione dell'area di visualizzazione del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="d50d6-126">Adjusting the monitor's display area.</span></span> <span data-ttu-id="d50d6-127">Le funzioni di configurazione del monitoraggio possono essere utilizzate per modificare le dimensioni e la posizione dell'area di visualizzazione di un monitor.</span><span class="sxs-lookup"><span data-stu-id="d50d6-127">The monitor configuration functions can be used to change the size and position of a monitor's display area.</span></span> <span data-ttu-id="d50d6-128">Ad esempio, quando un monitor LCD è connesso a un computer usando un connettore analogico, viene ottenuta la migliore qualità dell'immagine quando è presente un mapping uno-a-uno tra i pixel nel buffer frame della scheda grafica e i pixel sul monitor LCD.</span><span class="sxs-lookup"><span data-stu-id="d50d6-128">For example, when an LCD monitor is connected to a computer by using an analog connector, the best image quality is obtained when there is a one-to-one mapping between pixels in the graphics card's frame buffer and pixels on the LCD monitor.</span></span>
-   <span data-ttu-id="d50d6-129">Salvataggio e ripristino delle impostazioni di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="d50d6-129">Saving and restoring monitor settings.</span></span> <span data-ttu-id="d50d6-130">Alcuni utenti necessitano di più set di impostazioni di monitoraggio, perché diversi scenari richiedono impostazioni di monitoraggio diverse.</span><span class="sxs-lookup"><span data-stu-id="d50d6-130">Some users need multiple sets of monitor settings, because different scenarios require different monitor settings.</span></span> <span data-ttu-id="d50d6-131">Ad esempio, le impostazioni di monitoraggio ottimali per le applicazioni desktop non sono ottimali per la visione della televisione.</span><span class="sxs-lookup"><span data-stu-id="d50d6-131">For example, monitor settings that are optimal for desktop applications are not optimal for watching television.</span></span>
-   <span data-ttu-id="d50d6-132">Utilizzo delle funzionalità di monitoraggio specifiche del fornitore.</span><span class="sxs-lookup"><span data-stu-id="d50d6-132">Using vendor-specific monitor features.</span></span> <span data-ttu-id="d50d6-133">Utilizzando le funzioni di configurazione del monitoraggio, i produttori possono creare applicazioni che utilizzano le funzionalità specifiche del fornitore del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="d50d6-133">Using the monitor configuration functions, manufacturers can create applications that use the vendor-specific features of the monitor.</span></span>

<span data-ttu-id="d50d6-134">Le funzioni di configurazione del monitoraggio sono divise in funzioni di alto livello e di basso livello.</span><span class="sxs-lookup"><span data-stu-id="d50d6-134">The monitor configuration functions are divided into high-level and low-level functions.</span></span> <span data-ttu-id="d50d6-135">Le funzioni di alto livello sono più facili da utilizzare rispetto alle funzioni di basso livello.</span><span class="sxs-lookup"><span data-stu-id="d50d6-135">The high-level functions are easier to use than the low-level functions.</span></span> <span data-ttu-id="d50d6-136">Per utilizzare le funzioni di alto livello, non è necessario conoscere l'interfaccia del comando Visualizza canale dati (DDC/CI).</span><span class="sxs-lookup"><span data-stu-id="d50d6-136">To use the high-level functions, you do not need to know anything about the Display Data Channel Command Interface (DDC/CI).</span></span> <span data-ttu-id="d50d6-137">Tuttavia, le funzioni di alto livello non consentono di accedere alle funzionalità specifiche del fornitore del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="d50d6-137">However, the high-level functions do not give you access to vendor-specific features of the monitor.</span></span>

<span data-ttu-id="d50d6-138">Le funzioni di basso livello sono un wrapper sottile intorno ai comandi DDC/CI.</span><span class="sxs-lookup"><span data-stu-id="d50d6-138">The low-level functions are a thin wrapper around the DDC/CI commands.</span></span> <span data-ttu-id="d50d6-139">Per usare le funzioni di basso livello, è necessario avere familiarità con lo standard DDC/CI e anche con lo standard MCCS (VESA Monitor Control Command Set).</span><span class="sxs-lookup"><span data-stu-id="d50d6-139">To use the low-level functions, you must be familiar with the DDC/CI standard and also with the VESA Monitor Control Command Set (MCCS) standard.</span></span> <span data-ttu-id="d50d6-140">In genere, è consigliabile utilizzare le funzioni di alto livello, a meno che non sia necessario utilizzare funzionalità disponibili solo nelle funzioni di basso livello.</span><span class="sxs-lookup"><span data-stu-id="d50d6-140">Generally, you should use the high-level functions unless you need to use features that are available only in the low-level functions.</span></span>

<span data-ttu-id="d50d6-141">Le funzioni di configurazione di monitoraggio di alto livello sono progettate in modo che un'applicazione non possa mettere un monitoraggio in uno stato inutilizzabile.</span><span class="sxs-lookup"><span data-stu-id="d50d6-141">The high-level monitor configuration functions are designed so that an application cannot put a monitor into an unusable state.</span></span> <span data-ttu-id="d50d6-142">È possibile utilizzare le funzioni di basso livello per inviare codici VCP al monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="d50d6-142">The low-level functions can be used to send VCP codes to the monitor.</span></span> <span data-ttu-id="d50d6-143">Tuttavia, tenere presente che alcuni codici VCP possono disabilitare funzionalità importanti o impostare il monitoraggio in uno stato in cui l'utente non è in grado di visualizzare l'immagine di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d50d6-143">However, be aware that some VCP codes can disable important functionality or put the monitor into a state where the user cannot see the display image.</span></span> <span data-ttu-id="d50d6-144">Per ulteriori informazioni, vedere lo standard MCCS (VESA Monitor Control Command Set).</span><span class="sxs-lookup"><span data-stu-id="d50d6-144">For more information, see the VESA Monitor Control Command Set (MCCS) standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d50d6-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d50d6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d50d6-146">Configurazione del monitoraggio</span><span class="sxs-lookup"><span data-stu-id="d50d6-146">Monitor Configuration</span></span>](monitor-configuration.md)
</dt> </dl>

 

 




