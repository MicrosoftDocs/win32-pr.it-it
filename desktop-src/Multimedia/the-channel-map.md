---
title: Mappa del canale
description: Mappa del canale
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, mappa canali
- Mappa canali
- Mapper MIDI, messaggi del canale
- Messaggi del canale MIDI
- messaggi del canale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116868"
---
# <a name="the-channel-map"></a><span data-ttu-id="faa74-110">Mappa del canale</span><span class="sxs-lookup"><span data-stu-id="faa74-110">The Channel Map</span></span>

<span data-ttu-id="faa74-111">La mappa del canale influiscono su tutti i messaggi del canale MIDI.</span><span class="sxs-lookup"><span data-stu-id="faa74-111">The channel map affects all MIDI channel messages.</span></span> <span data-ttu-id="faa74-112">I messaggi del canale MIDI includono i messaggi note-on, note-off, polifoniche-Key-aftertouch, CTRL-Change, Program-Change, Channel-aftertouch e Pitch-Bend-Change.</span><span class="sxs-lookup"><span data-stu-id="faa74-112">MIDI channel messages include note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch, and pitch-bend-change messages.</span></span> <span data-ttu-id="faa74-113">Il mapper MIDI usa una singola mappa del canale con una voce per ognuno dei 16 canali MIDI.</span><span class="sxs-lookup"><span data-stu-id="faa74-113">The MIDI Mapper uses a single channel map with an entry for each of the 16 MIDI channels.</span></span> <span data-ttu-id="faa74-114">Ogni voce della mappa del canale specifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="faa74-114">Each channel-map entry specifies the following:</span></span>

-   <span data-ttu-id="faa74-115">Canale di destinazione per il messaggio MIDI</span><span class="sxs-lookup"><span data-stu-id="faa74-115">A destination channel for the MIDI message</span></span>
-   <span data-ttu-id="faa74-116">Un dispositivo di output di destinazione per il messaggio MIDI</span><span class="sxs-lookup"><span data-stu-id="faa74-116">A destination output device for the MIDI message</span></span>
-   <span data-ttu-id="faa74-117">Mappa patch facoltativa che specifica altre possibili modifiche per il messaggio MIDI</span><span class="sxs-lookup"><span data-stu-id="faa74-117">An optional patch map specifying other possible modifications for the MIDI message</span></span>

<span data-ttu-id="faa74-118">Il canale di destinazione è impostato su uno dei 16 canali MIDI.</span><span class="sxs-lookup"><span data-stu-id="faa74-118">The destination channel is set to one of the 16 MIDI channels.</span></span> <span data-ttu-id="faa74-119">I messaggi MIDI vengono modificati in modo da riflettere ogni nuova assegnazione del canale.</span><span class="sxs-lookup"><span data-stu-id="faa74-119">MIDI messages are modified to reflect each new channel assignment.</span></span> <span data-ttu-id="faa74-120">Se, ad esempio, la voce del canale di destinazione per il canale MIDI 4 è impostata su 6, viene eseguito il mapping di tutti i messaggi MIDI inviati a Channel 4 a Channel 6, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="faa74-120">For example, if the destination channel entry for MIDI channel 4 is set to 6, all MIDI messages sent to channel 4 will be mapped to channel 6, as shown in the following illustration.</span></span>

![immagine MIDI mappata](images/mmap-a05.gif)

<span data-ttu-id="faa74-122">In questo esempio il byte di stato MIDI 0x93 viene mappato a 0x95.</span><span class="sxs-lookup"><span data-stu-id="faa74-122">In this example, the MIDI status byte 0x93 is mapped to 0x95.</span></span> <span data-ttu-id="faa74-123">L'ordine inferiore di un byte di stato MIDI specifica il numero del canale.</span><span class="sxs-lookup"><span data-stu-id="faa74-123">The low-order of a MIDI status byte specifies the channel number.</span></span> <span data-ttu-id="faa74-124">I canali di origine sono impostati su attivo o inattivo.</span><span class="sxs-lookup"><span data-stu-id="faa74-124">Source channels are set to either active or inactive.</span></span> <span data-ttu-id="faa74-125">I messaggi inviati ai canali di origine inattivi vengono ignorati, pertanto un canale inattivo viene attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="faa74-125">Messages sent to inactive source channels are ignored, so an inactive channel is in effect muted or turned off.</span></span>

<span data-ttu-id="faa74-126">Il dispositivo di output di destinazione è impostato su uno dei dispositivi di output MIDI disponibili.</span><span class="sxs-lookup"><span data-stu-id="faa74-126">The destination output device is set to one of the available MIDI output devices.</span></span> <span data-ttu-id="faa74-127">Un dispositivo di output MIDI può essere un sintetizzatore interno o una porta di output MIDI fisica.</span><span class="sxs-lookup"><span data-stu-id="faa74-127">A MIDI output device can be an internal synthesizer or a physical MIDI output port.</span></span>

<span data-ttu-id="faa74-128">I messaggi di sistema MIDI sono messaggi MIDI (con byte di stato) da 0xF0 a 0xFF.</span><span class="sxs-lookup"><span data-stu-id="faa74-128">MIDI system messages are MIDI messages (with status bytes) from 0xF0 to 0xFF.</span></span> <span data-ttu-id="faa74-129">Non esiste alcun canale associato ai messaggi di sistema MIDI, pertanto non è possibile eseguirne il mapping.</span><span class="sxs-lookup"><span data-stu-id="faa74-129">There is no channel associated with MIDI system messages, so they cannot be mapped.</span></span> <span data-ttu-id="faa74-130">I messaggi di sistema MIDI vengono inviati a tutti i dispositivi di output MIDI elencati in una mappa canali.</span><span class="sxs-lookup"><span data-stu-id="faa74-130">MIDI system messages are sent to all MIDI output devices listed in a channel map.</span></span>

 

 




