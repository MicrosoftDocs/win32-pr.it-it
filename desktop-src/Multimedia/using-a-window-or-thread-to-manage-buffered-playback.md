---
title: Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer
description: Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- riproduzione di file MIDI, riproduzione memorizzata nel buffer
- riproduzione memorizzata nel buffer
- Messaggio MM_MOM_CLOSE
- Messaggio MM_MOM_DONE
- Messaggio MM_MOM_OPEN
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337311"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a><span data-ttu-id="210c8-114">Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer</span><span class="sxs-lookup"><span data-stu-id="210c8-114">Using a Window or Thread to Manage Buffered Playback</span></span>

<span data-ttu-id="210c8-115">I messaggi seguenti possono essere inviati a una finestra o a un thread per la gestione della riproduzione dei messaggi esclusivi del sistema MIDI o dei buffer di flusso.</span><span class="sxs-lookup"><span data-stu-id="210c8-115">The following messages can be sent to a window or thread for managing playback of MIDI system-exclusive messages or stream buffers.</span></span>



| <span data-ttu-id="210c8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="210c8-116">Value</span></span>                                  | <span data-ttu-id="210c8-117">Significato</span><span class="sxs-lookup"><span data-stu-id="210c8-117">Meaning</span></span>                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="210c8-118">**MM \_ \_ chiusura MOM**</span><span class="sxs-lookup"><span data-stu-id="210c8-118">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md) | <span data-ttu-id="210c8-119">Inviato quando il dispositivo viene chiuso tramite la funzione [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="210c8-119">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="210c8-120">**MM \_ MOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="210c8-120">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)   | <span data-ttu-id="210c8-121">Inviato quando il driver di dispositivo viene terminato con un blocco di dati inviato tramite la funzione [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) o [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="210c8-121">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="210c8-122">**MM- \_ MOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="210c8-122">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)   | <span data-ttu-id="210c8-123">Inviato quando il dispositivo viene aperto tramite la funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="210c8-123">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="210c8-124">Un parametro *wParam* e un parametro *lParam* sono associati a ognuno di questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="210c8-124">A *wParam* parameter and an *lParam* parameter are associated with each of these messages.</span></span> <span data-ttu-id="210c8-125">Il parametro *wParam* specifica sempre l'handle di un dispositivo MIDI aperto.</span><span class="sxs-lookup"><span data-stu-id="210c8-125">The *wParam* parameter always specifies the handle of an open MIDI device.</span></span> <span data-ttu-id="210c8-126">Per [**\_ MOM mm \_ done**](mm-mom-done.md), *lParam* specifica un indirizzo di una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il blocco di dati completato.</span><span class="sxs-lookup"><span data-stu-id="210c8-126">For [**MM\_MOM\_DONE**](mm-mom-done.md), *lParam* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the completed data block.</span></span> <span data-ttu-id="210c8-127">Il parametro *lParam* non è usato per [**la \_ \_ chiusura MOM di mm**](mm-mom-close.md) e la [**\_ MOM \_ aperta**](mm-mom-open.md).</span><span class="sxs-lookup"><span data-stu-id="210c8-127">The *lParam* parameter is unused for [**MM\_MOM\_CLOSE**](mm-mom-close.md) and [**MM\_MOM\_OPEN**](mm-mom-open.md).</span></span>

<span data-ttu-id="210c8-128">Il messaggio più utile è probabilmente MM \_ MOM \_ done.</span><span class="sxs-lookup"><span data-stu-id="210c8-128">The most useful message is probably MM\_MOM\_DONE.</span></span> <span data-ttu-id="210c8-129">A meno che non sia necessario allocare memoria o inizializzare variabili, è probabile che non sia necessario elaborare MM \_ MOM \_ Open e mm \_ MOM \_ Close.</span><span class="sxs-lookup"><span data-stu-id="210c8-129">Unless you need to allocate memory or initialize variables, you probably do not need to process MM\_MOM\_OPEN and MM\_MOM\_CLOSE.</span></span> <span data-ttu-id="210c8-130">Quando viene completata la riproduzione di un blocco di dati, è possibile pulire e liberare il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="210c8-130">When playback of a data block is complete, you can clean up and free the data block.</span></span>

 

 