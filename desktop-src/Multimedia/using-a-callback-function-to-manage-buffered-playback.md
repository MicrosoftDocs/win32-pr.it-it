---
title: Utilizzo di una funzione di callback per gestire la riproduzione memorizzata nel buffer
description: Utilizzo di una funzione di callback per gestire la riproduzione memorizzata nel buffer
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- riproduzione di file MIDI, riproduzione memorizzata nel buffer
- riproduzione memorizzata nel buffer
- Messaggio MOM_CLOSE
- Messaggio MOM_DONE
- Messaggio MOM_OPEN
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), funzioni di callback
- MIDI (Musical Instrument Digital Interface), funzioni di callback
- riproduzione di file MIDI, funzioni di callback
- Funzione di callback MidiOutProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726295"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a><span data-ttu-id="ccf2d-118">Utilizzo di una funzione di callback per gestire la riproduzione memorizzata nel buffer</span><span class="sxs-lookup"><span data-stu-id="ccf2d-118">Using a Callback Function to Manage Buffered Playback</span></span>

<span data-ttu-id="ccf2d-119">È possibile definire una funzione di callback personalizzata per gestire la riproduzione del buffer dei dispositivi di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-119">You can define your own callback function to manage buffered playback of MIDI output devices.</span></span> <span data-ttu-id="ccf2d-120">La funzione di callback è documentata come [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ccf2d-120">The callback function is documented as [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span></span>

<span data-ttu-id="ccf2d-121">I messaggi seguenti possono essere inviati al parametro *wmsg* della funzione di callback **MidiOutProc** .</span><span class="sxs-lookup"><span data-stu-id="ccf2d-121">The following messages can be sent to the *wMsg* parameter of the **MidiOutProc** callback function.</span></span>



| <span data-ttu-id="ccf2d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf2d-122">Value</span></span>                           | <span data-ttu-id="ccf2d-123">Significato</span><span class="sxs-lookup"><span data-stu-id="ccf2d-123">Meaning</span></span>                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccf2d-124">**\_chiusura MOM**</span><span class="sxs-lookup"><span data-stu-id="ccf2d-124">**MOM\_CLOSE**</span></span>](mom-close.md) | <span data-ttu-id="ccf2d-125">Inviato quando il dispositivo viene chiuso tramite la funzione [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="ccf2d-125">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="ccf2d-126">**MOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="ccf2d-126">**MOM\_DONE**</span></span>](mom-done.md)   | <span data-ttu-id="ccf2d-127">Inviato quando il driver di dispositivo viene terminato con un blocco di dati inviato tramite la funzione [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) o [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="ccf2d-127">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="ccf2d-128">**MOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="ccf2d-128">**MOM\_OPEN**</span></span>](mom-open.md)   | <span data-ttu-id="ccf2d-129">Inviato quando il dispositivo viene aperto tramite la funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="ccf2d-129">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="ccf2d-130">Questi messaggi sono simili a quelli inviati alle funzioni di routine della finestra, ma i parametri sono diversi.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-130">These messages are similar to those sent to window procedure functions, but the parameters are different.</span></span> <span data-ttu-id="ccf2d-131">Un handle del dispositivo MIDI aperto viene passato come parametro alla funzione di callback, insieme al parola doppia dei dati dell'istanza passati usando **midiOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-131">A handle of the open MIDI device is passed as a parameter to the callback function, along with the doubleword of instance data passed by using **midiOutOpen**.</span></span>

<span data-ttu-id="ccf2d-132">Al termine del driver, è possibile pulire e liberare il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-132">After the driver is finished with a data block, you can clean up and free the data block.</span></span> <span data-ttu-id="ccf2d-133">A causa delle restrizioni suggerite sulle funzioni di callback, è preferibile non eseguire questa operazione dall'interno della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-133">Because of the suggested restrictions on callback functions, it is better not to do this from within the callback function.</span></span>

 

 