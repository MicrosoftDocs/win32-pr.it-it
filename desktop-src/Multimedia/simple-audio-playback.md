---
title: Riproduzione audio semplice
description: Riproduzione audio semplice
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- audio multimediale, forma d'onda
- audio, forma d'onda
- audio Waveform, riproduzione semplice
- MessageBeep (funzione)
- sndPlaySound (funzione)
- Funzione PlaySound, riproduzione semplice
- audio multimediale, funzione PlaySound
- audio, funzione PlaySound
- audio Waveform, funzione PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956417"
---
# <a name="simple-audio-playback"></a><span data-ttu-id="a7d87-112">Riproduzione audio semplice</span><span class="sxs-lookup"><span data-stu-id="a7d87-112">Simple Audio Playback</span></span>

<span data-ttu-id="a7d87-113">È possibile usare le funzioni seguenti per riprodurre l'audio della forma d'onda nell'applicazione in una singola chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="a7d87-113">You can use the following functions to play waveform audio in your application in a single function call.</span></span>



| <span data-ttu-id="a7d87-114">Funzione</span><span class="sxs-lookup"><span data-stu-id="a7d87-114">Function</span></span>                                                      | <span data-ttu-id="a7d87-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7d87-115">Description</span></span>                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7d87-116">MessageBeep</span><span class="sxs-lookup"><span data-stu-id="a7d87-116">MessageBeep</span></span>](/windows/win32/api/winuser/nf-winuser-messagebeep) | <span data-ttu-id="a7d87-117">Riproduce il suono che corrisponde a un livello di avviso di sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="a7d87-117">Plays the sound that corresponds to a specified system-alert level.</span></span>                                                 |
| <span data-ttu-id="a7d87-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7d87-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>                          | <span data-ttu-id="a7d87-119">Riproduce il suono che corrisponde al suono di sistema immesso nel registro di sistema o al contenuto del file specificato.</span><span class="sxs-lookup"><span data-stu-id="a7d87-119">Plays the sound that corresponds to the system sound entered in the registry or the contents of the specified file.</span></span> |
| <span data-ttu-id="a7d87-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7d87-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>                                | <span data-ttu-id="a7d87-121">Fornisce tutte le funzionalità di [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e può accedere direttamente alle risorse.</span><span class="sxs-lookup"><span data-stu-id="a7d87-121">Provides all the functionality of [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and can directly access resources.</span></span>           |



 

<span data-ttu-id="a7d87-122">La funzione **MessageBeep** è una parte standard dell'API Win32. Poiché le sue funzionalità sono molto limitate e sono documentate altrove, non vengono discusse qui.</span><span class="sxs-lookup"><span data-stu-id="a7d87-122">The **MessageBeep** function is a standard part of the Win32 API; because its capabilities are very limited and it is documented elsewhere, it is not discussed here.</span></span>

<span data-ttu-id="a7d87-123">Le funzioni elencate supportano le seguenti origini dell'audio della forma d'onda:</span><span class="sxs-lookup"><span data-stu-id="a7d87-123">The functions listed support the following sources of waveform audio:</span></span>

-   <span data-ttu-id="a7d87-124">Waveform-file audio associati ai livelli di avviso di sistema</span><span class="sxs-lookup"><span data-stu-id="a7d87-124">Waveform-audio files associated with system-alert levels</span></span>
-   <span data-ttu-id="a7d87-125">Waveform-file audio specificati da voci nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a7d87-125">Waveform-audio files specified by entries in the registry</span></span>
-   <span data-ttu-id="a7d87-126">Risorse WAVE in memoria</span><span class="sxs-lookup"><span data-stu-id="a7d87-126">In-memory WAVE resources</span></span>
-   <span data-ttu-id="a7d87-127">Waveform-file audio specificati per nome</span><span class="sxs-lookup"><span data-stu-id="a7d87-127">Waveform-audio files specified by name</span></span>

<span data-ttu-id="a7d87-128">Le funzioni [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e [**PlaySound**](/previous-versions//dd743680(v=vs.85)) caricano in memoria un intero file audio e di forma d'onda e, in effetti, limitano le dimensioni del file che è possibile riprodurre.</span><span class="sxs-lookup"><span data-stu-id="a7d87-128">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and [**PlaySound**](/previous-versions//dd743680(v=vs.85)) functions load an entire waveform-audio file into memory and, in effect, limit the size of the file they can play.</span></span> <span data-ttu-id="a7d87-129">Usare **sndPlaySound** e **PlaySound** per riprodurre file audio con forma d'onda di dimensioni ridotte, fino a circa 100.000.</span><span class="sxs-lookup"><span data-stu-id="a7d87-129">Use **sndPlaySound** and **PlaySound** to play waveform-audio files that are small — up to about 100K.</span></span> <span data-ttu-id="a7d87-130">Queste due funzioni richiedono anche che i dati audio siano in un formato riproducibile da uno dei driver audio della forma d'onda, incluso il mapper wave.</span><span class="sxs-lookup"><span data-stu-id="a7d87-130">These two functions also require the sound data to be in a format that is playable by one of the installed waveform-audio drivers, including the wave mapper.</span></span>

<span data-ttu-id="a7d87-131">Per i file audio di dimensioni maggiori, usare i servizi MCI (Media Control Interface).</span><span class="sxs-lookup"><span data-stu-id="a7d87-131">For larger sound files, use the Media Control Interface (MCI) services.</span></span> <span data-ttu-id="a7d87-132">Per ulteriori informazioni, vedere [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="a7d87-132">For more information, see [MCI](mci.md).</span></span>

 

 