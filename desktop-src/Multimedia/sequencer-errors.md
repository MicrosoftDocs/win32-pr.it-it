---
title: Errori del sequencer
description: Errori del sequencer
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR valori restituiti, errori del sequencer
- riferimento multimediale, errori del sequencer
- informazioni di riferimento per gli errori di Sequencer e multimediali
- Media Control Interface (MCI), errori del sequencer
- MCI (interfaccia di controllo multimediale), errori del sequencer
- informazioni di riferimento per MCI, errori del sequencer
- Riferimento a MCI, errori del sequencer
- Interfaccia di controllo multimediale (MCI), errori
- MCI (interfaccia di controllo multimediale), errori
- informazioni di riferimento per MCI, errori
- Riferimento a MCI, errori
- errori del sequencer
- Errori del sequencer MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710441"
---
# <a name="sequencer-errors"></a><span data-ttu-id="be666-116">Errori del sequencer</span><span class="sxs-lookup"><span data-stu-id="be666-116">Sequencer Errors</span></span>

<span data-ttu-id="be666-117">Per i sequencer MCI sono definiti i seguenti valori restituiti aggiuntivi:</span><span class="sxs-lookup"><span data-stu-id="be666-117">The following additional return values are defined for MCI sequencers:</span></span>



| <span data-ttu-id="be666-118">Valore</span><span class="sxs-lookup"><span data-stu-id="be666-118">Value</span></span>                          | <span data-ttu-id="be666-119">Significato</span><span class="sxs-lookup"><span data-stu-id="be666-119">Meaning</span></span>                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be666-120">MCIERR \_ seq \_ div \_ incompatibile</span><span class="sxs-lookup"><span data-stu-id="be666-120">MCIERR\_SEQ\_DIV\_INCOMPATIBLE</span></span> | <span data-ttu-id="be666-121">I formati di ora del "puntatore del brano" e del SMPTE sono singolari.</span><span class="sxs-lookup"><span data-stu-id="be666-121">The time formats of the "song pointer" and SMPTE are singular.</span></span> <span data-ttu-id="be666-122">Non è possibile usarle insieme.</span><span class="sxs-lookup"><span data-stu-id="be666-122">You can't use them together.</span></span>                                                              |
| <span data-ttu-id="be666-123">MCIERR \_ seq \_ NOMIDIPRESENT</span><span class="sxs-lookup"><span data-stu-id="be666-123">MCIERR\_SEQ\_NOMIDIPRESENT</span></span>     | <span data-ttu-id="be666-124">Nessun dispositivo MIDI installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="be666-124">This system has no installed MIDI devices.</span></span> <span data-ttu-id="be666-125">Usare l'opzione drivers nel pannello di controllo per installare un driver MIDI.</span><span class="sxs-lookup"><span data-stu-id="be666-125">Use the Drivers option from the Control Panel to install a MIDI driver.</span></span>                                       |
| <span data-ttu-id="be666-126">MCIERR \_ seq \_ porta \_ InUse</span><span class="sxs-lookup"><span data-stu-id="be666-126">MCIERR\_SEQ\_PORT\_INUSE</span></span>       | <span data-ttu-id="be666-127">La porta MIDI specificata è già in uso.</span><span class="sxs-lookup"><span data-stu-id="be666-127">The specified MIDI port is already in use.</span></span> <span data-ttu-id="be666-128">Attendere fino a quando non è disponibile; quindi, riprovare.</span><span class="sxs-lookup"><span data-stu-id="be666-128">Wait until it is free; then, try again.</span></span>                                                                       |
| <span data-ttu-id="be666-129">MCIERR \_ seq \_ porta \_ MAPNODEVICE</span><span class="sxs-lookup"><span data-stu-id="be666-129">MCIERR\_SEQ\_PORT\_MAPNODEVICE</span></span> | <span data-ttu-id="be666-130">Il programma di installazione di MIDI Mapper corrente fa riferimento a un dispositivo MIDI non installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="be666-130">The current MIDI Mapper setup refers to a MIDI device that is not installed on the system.</span></span> <span data-ttu-id="be666-131">Usare il mapper MIDI dal pannello di controllo per modificare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="be666-131">Use the MIDI Mapper from the Control Panel to edit the setup.</span></span> |
| <span data-ttu-id="be666-132">MCIERR \_ seq \_ Port \_ uncerror</span><span class="sxs-lookup"><span data-stu-id="be666-132">MCIERR\_SEQ\_PORT\_MISCERROR</span></span>   | <span data-ttu-id="be666-133">Si è verificato un errore con la porta specificata.</span><span class="sxs-lookup"><span data-stu-id="be666-133">An error occurred with specified port.</span></span>                                                                                                                   |
| <span data-ttu-id="be666-134">MCIERR \_ seq \_ porta non \_ esistente</span><span class="sxs-lookup"><span data-stu-id="be666-134">MCIERR\_SEQ\_PORT\_NONEXISTENT</span></span> | <span data-ttu-id="be666-135">Il dispositivo MIDI specificato non è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="be666-135">The specified MIDI device is not installed on the system.</span></span> <span data-ttu-id="be666-136">Usare l'opzione drivers nel pannello di controllo per installare un dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="be666-136">Use the Drivers option from the Control Panel to install a MIDI device.</span></span>                        |
| <span data-ttu-id="be666-137">MCIERR \_ seq \_ PORTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="be666-137">MCIERR\_SEQ\_PORTUNSPECIFIED</span></span>   | <span data-ttu-id="be666-138">Per il sistema non è stata specificata una porta MIDI corrente.</span><span class="sxs-lookup"><span data-stu-id="be666-138">The system does not have a current MIDI port specified.</span></span>                                                                                                  |
| <span data-ttu-id="be666-139">\_timer seq \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="be666-139">MCIERR\_SEQ\_TIMER</span></span>             | <span data-ttu-id="be666-140">Tutti i timer multimediali vengono utilizzati da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="be666-140">All multimedia timers are being used by other applications.</span></span> <span data-ttu-id="be666-141">Uscire da una di queste applicazioni; quindi, riprovare.</span><span class="sxs-lookup"><span data-stu-id="be666-141">Quit one of these applications; then, try again.</span></span>                                             |



 

 

 




