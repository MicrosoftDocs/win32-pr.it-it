---
title: Riepilogo delle mappe e dei messaggi MIDI
description: Riepilogo delle mappe e dei messaggi MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, mappa canali
- Mapper MIDI, mappe patch
- Mapper MIDI, mappe chiave
- Mappa canali
- Mappe patch
- Mappe chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713303"
---
# <a name="summary-of-maps-and-midi-messages"></a><span data-ttu-id="d782a-111">Riepilogo delle mappe e dei messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="d782a-111">Summary of Maps and MIDI Messages</span></span>

<span data-ttu-id="d782a-112">Di seguito sono riportati i byte di stato per i messaggi MIDI e i tipi di mappa che interessano ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="d782a-112">Following are the status bytes for MIDI messages and the map types that affect each message.</span></span>



| <span data-ttu-id="d782a-113">Stato MIDI</span><span class="sxs-lookup"><span data-stu-id="d782a-113">MIDI status</span></span> | <span data-ttu-id="d782a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d782a-114">Description</span></span>               | <span data-ttu-id="d782a-115">Tipi di mappa</span><span class="sxs-lookup"><span data-stu-id="d782a-115">Map types</span></span>                |
|-------------|---------------------------|--------------------------|
| <span data-ttu-id="d782a-116">0x80-0x8F</span><span class="sxs-lookup"><span data-stu-id="d782a-116">0x80-0x8F</span></span>   | <span data-ttu-id="d782a-117">Nota disattivato</span><span class="sxs-lookup"><span data-stu-id="d782a-117">Note off</span></span>                  | <span data-ttu-id="d782a-118">Mappe canali, mappe chiave</span><span class="sxs-lookup"><span data-stu-id="d782a-118">Channel maps, key maps</span></span>   |
| <span data-ttu-id="d782a-119">0x90-0x9F</span><span class="sxs-lookup"><span data-stu-id="d782a-119">0x90-0x9F</span></span>   | <span data-ttu-id="d782a-120">Nota su </span><span class="sxs-lookup"><span data-stu-id="d782a-120">Note on</span></span>                   | <span data-ttu-id="d782a-121">Mappe canali, mappe chiave</span><span class="sxs-lookup"><span data-stu-id="d782a-121">Channel maps, key maps</span></span>   |
| <span data-ttu-id="d782a-122">Messaggi 0XA0-0xAF</span><span class="sxs-lookup"><span data-stu-id="d782a-122">0xA0-0xAF</span></span>   | <span data-ttu-id="d782a-123">Aftertouch chiave polifonica</span><span class="sxs-lookup"><span data-stu-id="d782a-123">Polyphonic-key aftertouch</span></span> | <span data-ttu-id="d782a-124">Mappe canali, mappe chiave</span><span class="sxs-lookup"><span data-stu-id="d782a-124">Channel maps, key maps</span></span>   |
| <span data-ttu-id="d782a-125">0xB0-0xBF</span><span class="sxs-lookup"><span data-stu-id="d782a-125">0xB0-0xBF</span></span>   | <span data-ttu-id="d782a-126">Modifica controllo</span><span class="sxs-lookup"><span data-stu-id="d782a-126">Control change</span></span>            | <span data-ttu-id="d782a-127">Mappe del canale, mappe delle patch</span><span class="sxs-lookup"><span data-stu-id="d782a-127">Channel maps, patch maps</span></span> |
| <span data-ttu-id="d782a-128">0xC0-0xCF</span><span class="sxs-lookup"><span data-stu-id="d782a-128">0xC0-0xCF</span></span>   | <span data-ttu-id="d782a-129">Modifica del programma</span><span class="sxs-lookup"><span data-stu-id="d782a-129">Program change</span></span>            | <span data-ttu-id="d782a-130">Mappe del canale, mappe delle patch</span><span class="sxs-lookup"><span data-stu-id="d782a-130">Channel maps, patch maps</span></span> |
| <span data-ttu-id="d782a-131">0xD0-0xDF</span><span class="sxs-lookup"><span data-stu-id="d782a-131">0xD0-0xDF</span></span>   | <span data-ttu-id="d782a-132">Canale aftertouch</span><span class="sxs-lookup"><span data-stu-id="d782a-132">Channel aftertouch</span></span>        | <span data-ttu-id="d782a-133">Mappe del canale</span><span class="sxs-lookup"><span data-stu-id="d782a-133">Channel maps</span></span>             |
| <span data-ttu-id="d782a-134">0xE0-0xEF</span><span class="sxs-lookup"><span data-stu-id="d782a-134">0xE0-0xEF</span></span>   | <span data-ttu-id="d782a-135">Modifica Pitch-Bend</span><span class="sxs-lookup"><span data-stu-id="d782a-135">Pitch-bend change</span></span>         | <span data-ttu-id="d782a-136">Mappe del canale</span><span class="sxs-lookup"><span data-stu-id="d782a-136">Channel maps</span></span>             |
| <span data-ttu-id="d782a-137">0xF0-0xFF</span><span class="sxs-lookup"><span data-stu-id="d782a-137">0xF0-0xFF</span></span>   | <span data-ttu-id="d782a-138">Sistema</span><span class="sxs-lookup"><span data-stu-id="d782a-138">System</span></span>                    | <span data-ttu-id="d782a-139">Non mappata</span><span class="sxs-lookup"><span data-stu-id="d782a-139">Not mapped</span></span>               |



 

-   <span data-ttu-id="d782a-140">I quattro bit più significativi rappresentano il valore dello stato.</span><span class="sxs-lookup"><span data-stu-id="d782a-140">The high-order four bits represent the status value.</span></span> <span data-ttu-id="d782a-141">I quattro bit di ordine inferiore rappresentano le informazioni sul canale.</span><span class="sxs-lookup"><span data-stu-id="d782a-141">The low-order four bits represent the channel information.</span></span>
-   <span data-ttu-id="d782a-142">Le mappe delle patch hanno effetto solo sul controller 7 (volume principale).</span><span class="sxs-lookup"><span data-stu-id="d782a-142">Patch maps affect only controller 7 (main volume).</span></span>
-   <span data-ttu-id="d782a-143">I messaggi di sistema vengono inviati a tutti i dispositivi elencati in una mappa canali.</span><span class="sxs-lookup"><span data-stu-id="d782a-143">System messages are sent to all devices listed in a channel map.</span></span>

 

 




