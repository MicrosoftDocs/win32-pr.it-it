---
title: Modifica della frequenza di pitch e playback
description: Modifica della frequenza di pitch e playback
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- audio Waveform, pitch
- waveform-interfaccia audio, pitch
- audio Waveform, velocità di riproduzione
- waveform-interfaccia audio, velocità di riproduzione
- audio Waveform, modifica del pitch
- waveform-interfaccia audio, modifica del passo
- audio Waveform, modifica della velocità di riproduzione
- waveform-interfaccia audio, modifica della velocità di riproduzione
- modifica della frequenza di riproduzione audio
- modifica della forma d'onda-audio pitch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473123"
---
# <a name="changing-pitch-and-playback-rate"></a><span data-ttu-id="0293e-113">Modifica della frequenza di pitch e playback</span><span class="sxs-lookup"><span data-stu-id="0293e-113">Changing Pitch and Playback Rate</span></span>

<span data-ttu-id="0293e-114">Alcuni dispositivi di output audio e della forma d'onda possono variare il pitch e la velocità di riproduzione dei dati audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="0293e-114">Some waveform-audio output devices can vary the pitch and the playback rate of waveform-audio data.</span></span> <span data-ttu-id="0293e-115">Non tutti i dispositivi Waveform-Audio supportano le variazioni della velocità di riproduzione e del pitch.</span><span class="sxs-lookup"><span data-stu-id="0293e-115">Not all waveform-audio devices support pitch and playback-rate changes.</span></span> <span data-ttu-id="0293e-116">Per informazioni su come determinare se una particolare periferica waveform-audio supporta le modifiche alla frequenza di Pitch and playback, vedere [dispositivi e tipi di dati](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="0293e-116">For information about how to determine whether a particular waveform-audio device supports pitch and playback rate changes, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="0293e-117">Di seguito sono riportate le differenze tra la variazione del pitch e della frequenza di riproduzione:</span><span class="sxs-lookup"><span data-stu-id="0293e-117">The differences between changing pitch and playback rate are as follows:</span></span>

-   <span data-ttu-id="0293e-118">La modifica della velocità di riproduzione viene eseguita dal driver di dispositivo e non richiede hardware specializzato.</span><span class="sxs-lookup"><span data-stu-id="0293e-118">Changing the playback rate is performed by the device driver and does not require specialized hardware.</span></span> <span data-ttu-id="0293e-119">La frequenza di campionamento non viene modificata, ma il driver esegue l'interpolazione ignorando o sintetizzando gli esempi.</span><span class="sxs-lookup"><span data-stu-id="0293e-119">The sample rate is not changed, but the driver interpolates by skipping or synthesizing samples.</span></span> <span data-ttu-id="0293e-120">Se, ad esempio, la velocità di riproduzione viene modificata in base a un fattore di due, il driver ignora tutti gli altri esempi.</span><span class="sxs-lookup"><span data-stu-id="0293e-120">For example, if the playback rate is changed by a factor of two, the driver skips every other sample.</span></span>
-   <span data-ttu-id="0293e-121">Per modificare il pitch è necessario hardware specializzato.</span><span class="sxs-lookup"><span data-stu-id="0293e-121">Changing the pitch requires specialized hardware.</span></span> <span data-ttu-id="0293e-122">La frequenza di riproduzione e la frequenza di campionamento non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="0293e-122">The playback rate and sample rate are not changed.</span></span>

<span data-ttu-id="0293e-123">Windows fornisce le funzioni seguenti per eseguire query e impostare frequenze di velocità di riproduzione e pitch di forma d'onda audio.</span><span class="sxs-lookup"><span data-stu-id="0293e-123">Windows provides the following functions to query and set waveform-audio pitch and playback rates.</span></span>



| <span data-ttu-id="0293e-124">Funzione</span><span class="sxs-lookup"><span data-stu-id="0293e-124">Function</span></span>                                                 | <span data-ttu-id="0293e-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0293e-125">Description</span></span>                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="0293e-126">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="0293e-126">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | <span data-ttu-id="0293e-127">Recupera il pitch per il dispositivo di output dell'audio e della forma d'onda specificato.</span><span class="sxs-lookup"><span data-stu-id="0293e-127">Retrieves the pitch for the specified waveform-audio output device.</span></span>         |
| [<span data-ttu-id="0293e-128">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="0293e-128">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | <span data-ttu-id="0293e-129">Recupera la velocità di riproduzione per il dispositivo di output dell'audio e della forma d'onda specificato.</span><span class="sxs-lookup"><span data-stu-id="0293e-129">Retrieves the playback rate for the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="0293e-130">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="0293e-130">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | <span data-ttu-id="0293e-131">Imposta il pitch per il dispositivo di output dell'audio e della forma d'onda specificato.</span><span class="sxs-lookup"><span data-stu-id="0293e-131">Sets the pitch for the specified waveform-audio output device.</span></span>              |
| [<span data-ttu-id="0293e-132">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="0293e-132">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | <span data-ttu-id="0293e-133">Imposta la velocità di riproduzione per il dispositivo di output dell'audio e della forma d'onda specificato.</span><span class="sxs-lookup"><span data-stu-id="0293e-133">Sets the playback rate for the specified waveform-audio output device.</span></span>      |



 

<span data-ttu-id="0293e-134">Le frequenze di pitch e playback vengono modificate da un fattore specificato con un numero a virgola fissa compresso in un valore parola doppia.</span><span class="sxs-lookup"><span data-stu-id="0293e-134">The pitch and playback rates are changed by a factor specified with a fixed-point number packed into a doubleword value.</span></span> <span data-ttu-id="0293e-135">I 16 bit superiori specificano la parte intera del numero; i 16 bit inferiori specificano la parte frazionaria.</span><span class="sxs-lookup"><span data-stu-id="0293e-135">The upper 16 bits specify the integer part of the number; the lower 16 bits specify the fractional part.</span></span> <span data-ttu-id="0293e-136">Ad esempio, il valore 1,5 viene rappresentato come 0x00018000L.</span><span class="sxs-lookup"><span data-stu-id="0293e-136">For example, the value 1.5 is represented as 0x00018000L.</span></span> <span data-ttu-id="0293e-137">Il valore 0,75 è rappresentato come 0x0000C000L.</span><span class="sxs-lookup"><span data-stu-id="0293e-137">The value 0.75 is represented as 0x0000C000L.</span></span> <span data-ttu-id="0293e-138">Il valore 1,0 (0x00010000) indica che il pitch o la velocità di riproduzione è invariata.</span><span class="sxs-lookup"><span data-stu-id="0293e-138">A value of 1.0 (0x00010000) means the pitch or playback rate is unchanged.</span></span>

 

 