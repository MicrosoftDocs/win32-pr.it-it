---
title: Allocazione e preparazione di blocchi di dati MIDI
description: Allocazione e preparazione di blocchi di dati MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- MIDI (Musical Instrument Digital Interface), allocazione di blocchi di dati
- MIDI (Musical Instrument Digital Interface), allocazione di blocchi di dati
- Servizi MIDI, allocazione di blocchi di dati
- allocazione di blocchi di dati MIDI
- MIDI (Musical Instrument Digital Interface), preparazione dei blocchi di dati
- MIDI (Musical Instrument Digital Interface), preparazione dei blocchi di dati
- Servizi MIDI, preparazione dei blocchi di dati
- preparazione dei blocchi di dati MIDI
- MIDI (Musical Instrument Digital Interface), blocchi di dati
- MIDI (Musical Instrument Digital Interface), blocchi di dati
- Servizi MIDI, blocchi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299764"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a><span data-ttu-id="ab3a7-114">Allocazione e preparazione di blocchi di dati MIDI</span><span class="sxs-lookup"><span data-stu-id="ab3a7-114">Allocating and Preparing MIDI Data Blocks</span></span>

<span data-ttu-id="ab3a7-115">Le funzioni [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)e [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) richiedono che le applicazioni allochino i blocchi di dati da passare ai driver di dispositivo ai fini della riproduzione o della registrazione.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-115">The [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), and [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) functions require that applications to allocate data blocks to pass to the device drivers for playback or recording purposes.</span></span> <span data-ttu-id="ab3a7-116">Ognuna di queste funzioni utilizza una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) per descrivere il relativo blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-116">Each of these functions uses a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure to describe its data block.</span></span>

<span data-ttu-id="ab3a7-117">Prima di usare una di queste funzioni per passare un blocco di dati a un driver di dispositivo, è necessario allocare memoria per il buffer e la struttura dell'intestazione che descrive il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-117">Before you use one of these functions to pass a data block to a device driver, you must allocate memory for the buffer and the header structure that describes the data block.</span></span>

<span data-ttu-id="ab3a7-118">Windows fornisce le funzioni seguenti per la preparazione e la pulizia dei blocchi di dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-118">Windows provides the following functions for preparing and cleaning up MIDI data blocks.</span></span>



| <span data-ttu-id="ab3a7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ab3a7-119">Value</span></span>                                                    | <span data-ttu-id="ab3a7-120">Significato</span><span class="sxs-lookup"><span data-stu-id="ab3a7-120">Meaning</span></span>                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="ab3a7-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="ab3a7-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | <span data-ttu-id="ab3a7-122">Prepara un blocco di dati di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-122">Prepares a MIDI input data block.</span></span>                      |
| [<span data-ttu-id="ab3a7-123">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="ab3a7-123">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | <span data-ttu-id="ab3a7-124">Pulisce la preparazione di un blocco di dati di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-124">Cleans up the preparation of a MIDI input data block.</span></span>  |
| [<span data-ttu-id="ab3a7-125">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="ab3a7-125">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | <span data-ttu-id="ab3a7-126">Prepara un blocco di dati di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-126">Prepares a MIDI output data block.</span></span>                     |
| [<span data-ttu-id="ab3a7-127">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="ab3a7-127">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | <span data-ttu-id="ab3a7-128">Pulisce la preparazione di un blocco di dati di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-128">Cleans up the preparation of a MIDI output data block.</span></span> |



 

<span data-ttu-id="ab3a7-129">Prima di passare un blocco di dati MIDI a un driver di dispositivo, è necessario preparare il buffer passandolo alla funzione [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) o [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) .</span><span class="sxs-lookup"><span data-stu-id="ab3a7-129">Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) or [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function.</span></span> <span data-ttu-id="ab3a7-130">Quando il driver di dispositivo è terminato con il buffer e lo restituisce, è necessario pulire la preparazione passando il buffer alla funzione [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) o [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) prima di poter liberare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="ab3a7-130">When the device driver is finished with the buffer and returns it, you must clean up this preparation by passing the buffer to the [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) or [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) function before any allocated memory can be freed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab3a7-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab3a7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab3a7-132">Servizi MIDI</span><span class="sxs-lookup"><span data-stu-id="ab3a7-132">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 