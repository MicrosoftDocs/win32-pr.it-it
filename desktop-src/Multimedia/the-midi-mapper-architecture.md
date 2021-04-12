---
title: Architettura del mapper MIDI
description: Architettura del mapper MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, architettura
- Mapper MIDI, mappa di installazione
- Mappa di installazione MIDI
- Mapper MIDI, mappa canali
- Mapper MIDI, mappe patch
- Mapper MIDI, mappe chiave
- Mappa canali
- Mappe patch
- Mappe chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331567"
---
# <a name="the-midi-mapper-architecture"></a><span data-ttu-id="ea118-114">Architettura del mapper MIDI</span><span class="sxs-lookup"><span data-stu-id="ea118-114">The MIDI Mapper Architecture</span></span>

<span data-ttu-id="ea118-115">Il mapper MIDI usa una mappa di installazione MIDI per determinare come tradurre e reindirizzare i messaggi ricevuti.</span><span class="sxs-lookup"><span data-stu-id="ea118-115">The MIDI Mapper uses a MIDI setup map to determine how to translate and redirect the messages it receives.</span></span> <span data-ttu-id="ea118-116">Una mappa di installazione MIDI è costituita dai tipi di mappe seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea118-116">A MIDI setup map consists of the following types of maps.</span></span>

-   [<span data-ttu-id="ea118-117">Mappa del canale</span><span class="sxs-lookup"><span data-stu-id="ea118-117">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="ea118-118">Mappe patch</span><span class="sxs-lookup"><span data-stu-id="ea118-118">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="ea118-119">Mappe chiave</span><span class="sxs-lookup"><span data-stu-id="ea118-119">Key Maps</span></span>](key-maps.md)

<span data-ttu-id="ea118-120">Nella figura seguente sono illustrati i ruoli di canale, patch e mappe chiave in una mappa di installazione MIDI.</span><span class="sxs-lookup"><span data-stu-id="ea118-120">The following illustration shows the roles of channel, patch, and key maps in a MIDI setup map.</span></span>

![ruoli del canale, della patch e delle mappe delle chiavi in un'immagine della mappa di installazione MIDI](images/mmap-a02.gif)

 

 




