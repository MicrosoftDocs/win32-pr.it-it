---
title: Invio di singoli messaggi MIDI
description: Invio di singoli messaggi MIDI
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), singoli messaggi
- MIDI (Musical Instrument Digital Interface), singoli messaggi
- riproduzione di file MIDI, singoli messaggi
- singoli messaggi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299656"
---
# <a name="sending-individual-midi-messages"></a><span data-ttu-id="32d15-111">Invio di singoli messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="32d15-111">Sending Individual MIDI Messages</span></span>

<span data-ttu-id="32d15-112">È possibile utilizzare i singoli messaggi MIDI utilizzando le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="32d15-112">You can work with individual MIDI messages by using the following functions.</span></span>



| <span data-ttu-id="32d15-113">Valore</span><span class="sxs-lookup"><span data-stu-id="32d15-113">Value</span></span>                                      | <span data-ttu-id="32d15-114">Significato</span><span class="sxs-lookup"><span data-stu-id="32d15-114">Meaning</span></span>                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32d15-115">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="32d15-115">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | <span data-ttu-id="32d15-116">Invia un buffer di dati MIDI al dispositivo di output MIDI specificato.</span><span class="sxs-lookup"><span data-stu-id="32d15-116">Sends a buffer of MIDI data to the specified MIDI output device.</span></span> <span data-ttu-id="32d15-117">Usare questa funzione per inviare messaggi esclusivi del sistema a un dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="32d15-117">Use this function to send system-exclusive messages to a MIDI device.</span></span>                                              |
| [<span data-ttu-id="32d15-118">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="32d15-118">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | <span data-ttu-id="32d15-119">Disattiva tutte le note in tutti i canali per un dispositivo di output MIDI specificato.</span><span class="sxs-lookup"><span data-stu-id="32d15-119">Turns off all notes on all channels for a specified MIDI output device.</span></span> <span data-ttu-id="32d15-120">I buffer di flusso e i buffer esclusivi del sistema in sospeso sono contrassegnati come done e restituiti all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32d15-120">Any pending system-exclusive buffers and stream buffers are marked as done and returned to the application.</span></span> |
| [<span data-ttu-id="32d15-121">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="32d15-121">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | <span data-ttu-id="32d15-122">Invia un messaggio MIDI a un dispositivo di output MIDI specificato.</span><span class="sxs-lookup"><span data-stu-id="32d15-122">Sends a MIDI message to a specified MIDI output device.</span></span>                                                                                                                             |



 

<span data-ttu-id="32d15-123">Per inviare qualsiasi messaggio MIDI (ad eccezione dei messaggi di sistema esclusivi), usare [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span><span class="sxs-lookup"><span data-stu-id="32d15-123">To send any MIDI message (except for system-exclusive messages), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span></span>

 

 