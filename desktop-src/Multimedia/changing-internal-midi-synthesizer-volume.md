---
title: Modifica del volume del sintetizzatore MIDI interno
description: Modifica del volume del sintetizzatore MIDI interno
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- riproduzione di file MIDI, sintetizzatori interni
- Sintetizzatori MIDI interni
- MIDI (Musical Instrument Digital Interface), modifica del volume
- MIDI (Musical Instrument Digital Interface), modifica del volume
- riproduzione di file MIDI, modifica del volume
- modifica del volume MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963053"
---
# <a name="changing-internal-midi-synthesizer-volume"></a><span data-ttu-id="7dea2-111">Modifica del volume del sintetizzatore MIDI interno</span><span class="sxs-lookup"><span data-stu-id="7dea2-111">Changing Internal MIDI Synthesizer Volume</span></span>

<span data-ttu-id="7dea2-112">Windows fornisce le funzioni seguenti per recuperare e impostare il livello di volume dei dispositivi del sintetizzatore MIDI interno:</span><span class="sxs-lookup"><span data-stu-id="7dea2-112">Windows provides the following functions to retrieve and set the volume level of internal MIDI synthesizer devices:</span></span>



| <span data-ttu-id="7dea2-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7dea2-113">Value</span></span>                                        | <span data-ttu-id="7dea2-114">Significato</span><span class="sxs-lookup"><span data-stu-id="7dea2-114">Meaning</span></span>                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="7dea2-115">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="7dea2-115">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | <span data-ttu-id="7dea2-116">Recupera il livello del volume del dispositivo del sintetizzatore MIDI interno specificato.</span><span class="sxs-lookup"><span data-stu-id="7dea2-116">Retrieves the volume level of the specified internal MIDI synthesizer device.</span></span> |
| [<span data-ttu-id="7dea2-117">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="7dea2-117">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | <span data-ttu-id="7dea2-118">Imposta il livello del volume del dispositivo del sintetizzatore MIDI interno specificato.</span><span class="sxs-lookup"><span data-stu-id="7dea2-118">Sets the volume level of the specified internal MIDI synthesizer device.</span></span>      |



 

<span data-ttu-id="7dea2-119">Non tutti i dispositivi di output MIDI supportano le modifiche del volume.</span><span class="sxs-lookup"><span data-stu-id="7dea2-119">Not all MIDI output devices support volume changes.</span></span> <span data-ttu-id="7dea2-120">Alcuni dispositivi sono in grado di supportare singole modifiche dei volumi nei canali sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="7dea2-120">Some devices can support individual volume changes on both the left and right channels.</span></span> <span data-ttu-id="7dea2-121">Per informazioni su come determinare se un dispositivo specifico supporta le modifiche del volume, vedere [esecuzione di query sui dispositivi di output MIDI](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="7dea2-121">For information on how to determine if a particular device supports volume changes, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

<span data-ttu-id="7dea2-122">A meno che l'applicazione non sia progettata come applicazione di controllo del volume principale (fornisce all'utente il controllo del volume per tutti i dispositivi audio in un sistema), è necessario aprire un dispositivo audio prima di modificare il volume.</span><span class="sxs-lookup"><span data-stu-id="7dea2-122">Unless your application is designed to be a master volume-control application (provides the user with volume control for all audio devices in a system), you should open an audio device before changing its volume.</span></span> <span data-ttu-id="7dea2-123">È inoltre consigliabile controllare il livello del volume prima di modificarlo e ripristinare il livello del volume precedente il prima possibile.</span><span class="sxs-lookup"><span data-stu-id="7dea2-123">You should also check the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="7dea2-124">Il volume viene specificato come valore parola doppia.</span><span class="sxs-lookup"><span data-stu-id="7dea2-124">Volume is specified as a doubleword value.</span></span> <span data-ttu-id="7dea2-125">I 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro.</span><span class="sxs-lookup"><span data-stu-id="7dea2-125">The upper 16 bits specify the relative volume of the right channel, and the lower 16 bits specify the relative volume of the left channel.</span></span>

<span data-ttu-id="7dea2-126">Per i dispositivi che non supportano modifiche dei singoli volumi nei canali sinistro e destro, i 16 bit inferiori specificano il livello di volume e i 16 bit superiori vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="7dea2-126">For devices that do not support individual volume changes on both the left and right channels, the lower 16 bits specify the volume level and the upper 16 bits are ignored.</span></span> <span data-ttu-id="7dea2-127">I valori per il livello del volume variano da 0x0 (silenzioso) a 0xFFFF (volume massimo) e vengono interpretati come logaritmicamente.</span><span class="sxs-lookup"><span data-stu-id="7dea2-127">Values for the volume level range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="7dea2-128">L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000, come da 0x4000 a 0x5000.</span><span class="sxs-lookup"><span data-stu-id="7dea2-128">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 