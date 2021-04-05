---
title: Arresto, sospensione e riavvio della riproduzione
description: Arresto, sospensione e riavvio della riproduzione
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- audio della forma d'onda, arresto della riproduzione
- waveform-interfaccia audio, arresto della riproduzione
- riproduzione di file audio Waveform, arresto della riproduzione
- audio della forma d'onda, sospensione della riproduzione
- waveform-interfaccia audio, sospensione della riproduzione
- riproduzione di file audio Waveform, sospensione della riproduzione
- audio della forma d'onda, riavvio della riproduzione
- waveform-interfaccia audio, riavvio della riproduzione
- riproduzione di file audio Waveform, riavvio della riproduzione
- waveOutPause (funzione)
- waveOutReset (funzione)
- waveOutRestart (funzione)
- arresto della forma d'onda-riproduzione audio
- sospensione delle forme d'onda-riproduzione audio
- riavvio della forma d'onda-riproduzione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117602"
---
# <a name="stopping-pausing-and-restarting-playback"></a><span data-ttu-id="bc8d7-118">Arresto, sospensione e riavvio della riproduzione</span><span class="sxs-lookup"><span data-stu-id="bc8d7-118">Stopping, Pausing, and Restarting Playback</span></span>

<span data-ttu-id="bc8d7-119">È possibile arrestare o sospendere la riproduzione durante la riproduzione dell'audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-119">You can stop or pause playback while waveform audio is playing.</span></span> <span data-ttu-id="bc8d7-120">Una volta sospesa la riproduzione, è possibile riavviarla.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-120">After playback has been paused, you can restart it.</span></span> <span data-ttu-id="bc8d7-121">Windows fornisce le funzioni seguenti per controllare la riproduzione dell'audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-121">Windows provides the following functions for controlling waveform-audio playback.</span></span>



| <span data-ttu-id="bc8d7-122">Funzione</span><span class="sxs-lookup"><span data-stu-id="bc8d7-122">Function</span></span>                                 | <span data-ttu-id="bc8d7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc8d7-123">Description</span></span>                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc8d7-124">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="bc8d7-124">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | <span data-ttu-id="bc8d7-125">Sospende la riproduzione in un dispositivo di output waveform-audio.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-125">Pauses playback on a waveform-audio output device.</span></span>                                          |
| [<span data-ttu-id="bc8d7-126">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="bc8d7-126">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | <span data-ttu-id="bc8d7-127">Interrompe la riproduzione in un dispositivo di output waveform-audio e contrassegna tutti i blocchi di dati in sospeso come completato.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-127">Stops playback on a waveform-audio output device and marks all pending data blocks as done.</span></span> |
| [<span data-ttu-id="bc8d7-128">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="bc8d7-128">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | <span data-ttu-id="bc8d7-129">Riprende la riproduzione in un dispositivo di output della forma d'onda-audio in pausa.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-129">Resumes playback on a paused waveform-audio output device.</span></span>                                  |



 

<span data-ttu-id="bc8d7-130">La sospensione di un dispositivo audio Waveform con [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) potrebbe non essere immediata; è possibile che il driver completi la riproduzione del blocco corrente prima di sospendere la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-130">Pausing a waveform-audio device by using [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) might not be instantaneous; the driver may finish playing the current block before pausing playback.</span></span>

<span data-ttu-id="bc8d7-131">In genere, non appena viene inviato il primo blocco di dati waveform-audio tramite la funzione [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , il dispositivo Waveform-Audio inizia la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-131">Generally, as soon as the first waveform-audio data block is sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function, the waveform-audio device begins playing.</span></span> <span data-ttu-id="bc8d7-132">Se non si desidera che il suono inizi immediatamente a riprodurre, chiamare **waveOutPause** prima di chiamare **waveOutWrite**.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-132">If you do not want the sound to start playing immediately, call **waveOutPause** before calling **waveOutWrite**.</span></span> <span data-ttu-id="bc8d7-133">Quindi, quando si desidera iniziare a riprodurre i dati audio della forma d'onda, chiamare [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span><span class="sxs-lookup"><span data-stu-id="bc8d7-133">Then, when you want to begin playing waveform-audio data, call [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span></span>

<span data-ttu-id="bc8d7-134">Non è possibile usare **waveOutRestart** per riavviare un dispositivo che è stato arrestato con [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); è necessario usare **waveOutWrite** per inviare il primo blocco di dati per riprendere la riproduzione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc8d7-134">You cannot use **waveOutRestart** to restart a device that has been stopped with [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); you must use **waveOutWrite** to send the first data block to resume playback on the device.</span></span>

 

 