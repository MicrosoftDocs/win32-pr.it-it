---
title: Buffer di flusso
description: Buffer di flusso
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Multimedia di Windows, buffer di flusso
- Multimedia, buffer di flusso
- audio multimediale, buffer di flusso
- audio, buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- buffer di flusso, informazioni
- Struttura MIDIHDR
- Struttura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725351"
---
# <a name="stream-buffers"></a><span data-ttu-id="784dc-112">Buffer di flusso</span><span class="sxs-lookup"><span data-stu-id="784dc-112">Stream Buffers</span></span>

<span data-ttu-id="784dc-113">Le applicazioni possono usare i buffer di flusso per inviare flussi di eventi MIDI a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="784dc-113">Applications can use stream buffers to send streams of MIDI events to a device.</span></span> <span data-ttu-id="784dc-114">Ogni buffer di flusso è un blocco di memoria a cui punta una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="784dc-114">Each stream buffer is a block of memory pointed to by a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span> <span data-ttu-id="784dc-115">Questo blocco di memoria contiene i dati per uno o più eventi MIDI, ognuno dei quali è definito da una struttura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="784dc-115">This block of memory contains data for one or more MIDI events, each of which is defined by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="784dc-116">Un'applicazione controlla il buffer chiamando le funzioni di manipolazione del flusso, ad esempio [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)e [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span><span class="sxs-lookup"><span data-stu-id="784dc-116">An application controls the buffer by calling the stream-manipulation functions, such as [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout), and [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span></span>

-   [<span data-ttu-id="784dc-117">Formato del buffer del flusso</span><span class="sxs-lookup"><span data-stu-id="784dc-117">Stream Buffer Format</span></span>](stream-buffer-format.md)
-   [<span data-ttu-id="784dc-118">Informazioni sull'intervallo</span><span class="sxs-lookup"><span data-stu-id="784dc-118">Timing Information</span></span>](timing-information.md)
-   [<span data-ttu-id="784dc-119">Tipi di evento MIDI</span><span class="sxs-lookup"><span data-stu-id="784dc-119">MIDI Event Types</span></span>](midi-event-types.md)
-   [<span data-ttu-id="784dc-120">Flussi MIDI</span><span class="sxs-lookup"><span data-stu-id="784dc-120">MIDI Streams</span></span>](midi-streams.md)

 

 