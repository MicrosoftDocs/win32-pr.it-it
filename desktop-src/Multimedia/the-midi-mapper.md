---
title: Mapper MIDI
description: Mapper MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows Multimedia, Mapper MIDI
- Multimedia, Mapper MIDI
- audio multimediale, Mapper MIDI
- audio, Mapper MIDI
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, informazioni
- Mapper MIDI, origine
- Mapper MIDI, destinazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044540"
---
# <a name="the-midi-mapper"></a><span data-ttu-id="0a781-112">Mapper MIDI</span><span class="sxs-lookup"><span data-stu-id="0a781-112">The MIDI Mapper</span></span>

<span data-ttu-id="0a781-113">I servizi patch standard del mapper MIDI forniscono la riproduzione dei file MIDI indipendenti dal dispositivo per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0a781-113">The MIDI Mapper's standard patch services provide device-independent MIDI file playback for applications.</span></span> <span data-ttu-id="0a781-114">Il mapper MIDI può essere usato con il sequencer MIDI di MCI o con servizi di output MIDI di basso livello.</span><span class="sxs-lookup"><span data-stu-id="0a781-114">The MIDI Mapper can be used with the MCI MIDI sequencer or with low-level MIDI output services.</span></span>

<span data-ttu-id="0a781-115">Se non specificato diversamente, tutti i riferimenti ai numeri di canale MIDI utilizzano i numeri di canale logico da 1 a 16.</span><span class="sxs-lookup"><span data-stu-id="0a781-115">Unless stated otherwise, all references to MIDI channel numbers use the logical channel numbers 1 through 16.</span></span> <span data-ttu-id="0a781-116">Questi numeri di canale logico corrispondono ai numeri di canale fisico da 0 a 15 che fanno effettivamente parte del messaggio MIDI.</span><span class="sxs-lookup"><span data-stu-id="0a781-116">These logical channel numbers correspond to the physical channel numbers 0 through 15 that are actually part of the MIDI message.</span></span> <span data-ttu-id="0a781-117">Tutti i riferimenti ai valori delle chiavi e delle modifiche dei programmi MIDI usano i valori fisici da 0 a 127.</span><span class="sxs-lookup"><span data-stu-id="0a781-117">All references to MIDI program-change and key values use the physical values 0 through 127.</span></span> <span data-ttu-id="0a781-118">Tutti i numeri sono decimali, a meno che non siano preceduti dal prefisso "0x", nel qual caso sono esadecimali.</span><span class="sxs-lookup"><span data-stu-id="0a781-118">All numbers are decimal unless preceded by "0x" prefix, in which case they are hexadecimal.</span></span>

<span data-ttu-id="0a781-119">Nella discussione del mapper MIDI, il termine *origine* si riferisce al lato di input del mapper MIDI.</span><span class="sxs-lookup"><span data-stu-id="0a781-119">In the discussion of the MIDI Mapper, the term *source* refers to the input side of the MIDI Mapper.</span></span> <span data-ttu-id="0a781-120">Il termine *destinazione* si riferisce al lato output del mapper MIDI.</span><span class="sxs-lookup"><span data-stu-id="0a781-120">The term *destination* refers to the output side of the MIDI Mapper.</span></span> <span data-ttu-id="0a781-121">Un canale di origine, ad esempio, è il canale MIDI di un messaggio inviato al mapper MIDI e un canale di destinazione è il canale MIDI di un messaggio inviato dal mapper MIDI a un dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="0a781-121">For example, a source channel is the MIDI channel of a message sent to the MIDI Mapper, and a destination channel is the MIDI channel of a message sent from the MIDI Mapper to an output device.</span></span>

-   [<span data-ttu-id="0a781-122">Il mapper MIDI e Windows</span><span class="sxs-lookup"><span data-stu-id="0a781-122">The MIDI Mapper and Windows</span></span>](the-midi-mapper-and-windows.md)
-   [<span data-ttu-id="0a781-123">Architettura del mapper MIDI</span><span class="sxs-lookup"><span data-stu-id="0a781-123">The MIDI Mapper Architecture</span></span>](the-midi-mapper-architecture.md)
-   [<span data-ttu-id="0a781-124">Mappa del canale</span><span class="sxs-lookup"><span data-stu-id="0a781-124">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="0a781-125">Mappe patch</span><span class="sxs-lookup"><span data-stu-id="0a781-125">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="0a781-126">Volume scalare</span><span class="sxs-lookup"><span data-stu-id="0a781-126">The Volume Scalar</span></span>](the-volume-scalar.md)
-   [<span data-ttu-id="0a781-127">Mappe chiave</span><span class="sxs-lookup"><span data-stu-id="0a781-127">Key Maps</span></span>](key-maps.md)
-   [<span data-ttu-id="0a781-128">Riepilogo delle mappe e dei messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="0a781-128">Summary of Maps and MIDI Messages</span></span>](summary-of-maps-and-midi-messages.md)

 

 




