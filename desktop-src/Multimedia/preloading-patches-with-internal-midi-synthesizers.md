---
title: Precaricamento di patch con sintetizzatori MIDI interni
description: Precaricamento di patch con sintetizzatori MIDI interni
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- riproduzione di file MIDI, sintetizzatori interni
- Sintetizzatori MIDI interni
- MIDI (Musical Instrument Digital Interface), precaricamento di patch
- MIDI (Musical Instrument Digital Interface), precaricamento di patch
- riproduzione di file MIDI, precaricamento di patch
- precaricamento delle patch MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956407"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a><span data-ttu-id="b2063-111">Precaricamento di patch con sintetizzatori MIDI interni</span><span class="sxs-lookup"><span data-stu-id="b2063-111">Preloading Patches with Internal MIDI Synthesizers</span></span>

<span data-ttu-id="b2063-112">Alcuni dispositivi del sintetizzatore MIDI interno non possono caricare contemporaneamente tutte le patch.</span><span class="sxs-lookup"><span data-stu-id="b2063-112">Some internal MIDI synthesizer devices cannot keep all of their patches loaded simultaneously.</span></span> <span data-ttu-id="b2063-113">Questi dispositivi devono precaricare i dati della patch.</span><span class="sxs-lookup"><span data-stu-id="b2063-113">These devices must preload their patch data.</span></span>

<span data-ttu-id="b2063-114">Windows fornisce le funzioni seguenti per richiedere il precaricamento di un sintetizzatore e la memorizzazione nella cache delle patch specificate.</span><span class="sxs-lookup"><span data-stu-id="b2063-114">Windows provides the following functions to request that a synthesizer preload and cache specified patches.</span></span>



| <span data-ttu-id="b2063-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b2063-115">Value</span></span>                                                      | <span data-ttu-id="b2063-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b2063-116">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2063-117">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="b2063-117">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | <span data-ttu-id="b2063-118">Richiede che un dispositivo del sintetizzatore MIDI interno precaricare e memorizzare nella cache le patch melodiche specificate.</span><span class="sxs-lookup"><span data-stu-id="b2063-118">Requests that an internal MIDI synthesizer device preload and cache specified melodic patches.</span></span>              |
| [<span data-ttu-id="b2063-119">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="b2063-119">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | <span data-ttu-id="b2063-120">Richiede che un dispositivo del sintetizzatore MIDI interno precaricare e memorizzare nella cache le patch di percussione basate su chiavi specificate.</span><span class="sxs-lookup"><span data-stu-id="b2063-120">Requests that an internal MIDI synthesizer device preload and cache specified key-based percussion patches.</span></span> |



 

<span data-ttu-id="b2063-121">Per informazioni su come determinare se un dispositivo specifico supporta il precaricamento delle patch, vedere [esecuzione di query sui dispositivi di output MIDI](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b2063-121">For information on how to determine if a particular device supports preloading patches, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

 

 