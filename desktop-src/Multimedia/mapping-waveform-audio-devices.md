---
title: Mapping di dispositivi Waveform-Audio
description: Mapping di dispositivi Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- audio multimediale, mapping della forma d'onda-dispositivi audio
- audio, mapping della forma d'onda-dispositivi audio
- Gestione compressione audio (ACM), mapping di forme d'onda-dispositivi audio
- ACM (Gestione compressione audio), mapping di forme d'onda-dispositivi audio
- mapping della forma d'onda-dispositivi audio
- audio multimediale, Mapper
- audio, Mapper
- Gestione compressione audio (ACM), Mapper
- ACM (Gestione compressione audio), Mapper
- mapper
- audio Waveform, mapping dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855862"
---
# <a name="mapping-waveform-audio-devices"></a><span data-ttu-id="4f1d9-114">Mapping di dispositivi Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="4f1d9-114">Mapping Waveform-Audio Devices</span></span>

<span data-ttu-id="4f1d9-115">Windows fornisce un set di funzioni standard per i dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-115">Windows provides a set of standard functions for audio devices.</span></span> <span data-ttu-id="4f1d9-116">Queste funzioni rilasciano chiamate ai driver di dispositivo che gestiscono i dispositivi hardware.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-116">These functions issue calls to device drivers that manage hardware devices.</span></span> <span data-ttu-id="4f1d9-117">Il sistema usa un modulo denominato "Mapper" per gestire i dispositivi installati.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-117">The system uses a module called a "mapper" to manage installed devices.</span></span> <span data-ttu-id="4f1d9-118">Il Mapper utilizza hook speciali nell'interfaccia del driver per intercettare le chiamate e fungere da intermediario tra il sistema e i driver installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-118">The mapper uses special hooks in the driver interface to intercept calls and to act as an intermediary between the system and the drivers installed in the system.</span></span> <span data-ttu-id="4f1d9-119">Il Mapper è responsabile della corrispondenza delle richieste di un'applicazione per l'accesso a un dispositivo con i dispositivi disponibili e per la ricerca di un dispositivo che soddisfi i requisiti audio dell'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-119">The mapper is responsible for matching an application's requests for access to a device with the available devices and for finding a device that meets the current application's audio requirements.</span></span> <span data-ttu-id="4f1d9-120">Il sistema fornisce Mapper per i tipi di driver standard: Waveform-Audio, MIDI (Musical Instrument Digital Interface) e dispositivi ausiliari.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-120">The system provides mappers for standard driver types: waveform-audio, MIDI (Musical Instrument Digital Interface), and auxiliary devices.</span></span>

<span data-ttu-id="4f1d9-121">ACM è un'estensione del sistema multimediale di base e viene installato come Mapper.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-121">The ACM is an extension of the basic multimedia system and is installed as a mapper.</span></span> <span data-ttu-id="4f1d9-122">Questo significa che ACM usa i hook del mapper dell'interfaccia del driver per i dispositivi audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-122">This means the ACM uses the driver-interface mapper hooks for waveform-audio devices.</span></span> <span data-ttu-id="4f1d9-123">L'uso di questi hook consente all'ACM di decodificare o codificare i dati dell'audio della forma d'onda prima di passarli a o da un driver di dispositivo Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-123">Using these hooks allows the ACM to decode or encode waveform-audio data before passing it to or from a waveform-audio device driver.</span></span> <span data-ttu-id="4f1d9-124">La differenza tra l'ACM e il mapper di sistema standard consiste nel fatto che l'ACM può cercare un dispositivo audio Waveform che supporta un formato specificato o trovare una combinazione di un dispositivo audio e di una forma d'onda, un compressore o un decompressore ACM che supporti un formato specificato.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-124">The difference between the ACM and the standard system mapper is that the ACM can search for a waveform-audio device that supports a specified format or find a combination of a waveform-audio device and an ACM compressor or decompressor that supports a specified format.</span></span>

<span data-ttu-id="4f1d9-125">Quando un'applicazione richiede che il sistema apra un dispositivo audio waveform per l'input o l'output, la richiesta specifica il formato e il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-125">When an application requests that the system open a waveform-audio device for input or output, the request specifies the format and device.</span></span> <span data-ttu-id="4f1d9-126">Quando il dispositivo specificato è il Mapper, è necessario che il mapper trovi un dispositivo che supporta il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-126">When the specified device is the mapper, the mapper must find a device that supports the specified format.</span></span> <span data-ttu-id="4f1d9-127">Il mapper implementato in ACM Cerca un dispositivo audio Waveform installato che supporta il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-127">The mapper implemented in the ACM searches for an installed waveform-audio device that supports the specified format.</span></span> <span data-ttu-id="4f1d9-128">Se l'ACM non riesce a trovare un dispositivo di questo tipo, Cerca un dispositivo audio e una forma d'onda, un compressore o un decompressore che insieme supporti il formato.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-128">If the ACM cannot find such a device, it searches for a waveform-audio device and a compressor or decompressor that together support the format.</span></span> <span data-ttu-id="4f1d9-129">In particolare, l'ACM Cerca un compressore o un decompressore che converte il formato specificato in un formato supportato da un dispositivo audio e una forma d'onda installata.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-129">Specifically, the ACM searches for a compressor or decompressor that converts the specified format into a format that is supported by an installed waveform-audio device.</span></span> <span data-ttu-id="4f1d9-130">Dopo che l'ACM ha individuato un dispositivo che supporta il formato convertito, può rispettare le richieste di riproduzione o registrazione del formato originariamente richiesto, anche se non è supportato direttamente da un dispositivo wave-audio installato.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-130">After the ACM finds a device that supports the converted format, it can honor requests to play or record the format originally requested, even though no installed waveform-audio device directly supports that format.</span></span>

<span data-ttu-id="4f1d9-131">Oltre alla conversione del formato, ACM offre anche servizi per supportare la compressione, la decompressione, il filtraggio, la selezione del formato e la selezione dei filtri.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-131">In addition to format conversion, the ACM also offers services to support compression, decompression, filtering, format selection, and filter selection.</span></span> <span data-ttu-id="4f1d9-132">Fornisce un'API standard che supporta chiamando i relativi driver.</span><span class="sxs-lookup"><span data-stu-id="4f1d9-132">It provides a standard API that it supports by calling its own drivers.</span></span>

 

 




