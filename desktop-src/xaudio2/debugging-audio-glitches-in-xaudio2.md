---
description: Le anomalie possono verificarsi in XAudio2, in questo argomento vengono illustrate le modalità di segnalazione e alcuni approcci per correggerli.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Debug di glitch audio in XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883138"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a><span data-ttu-id="0d659-103">Debug di glitch audio in XAudio2</span><span class="sxs-lookup"><span data-stu-id="0d659-103">Debugging Audio Glitches in XAudio2</span></span>

<span data-ttu-id="0d659-104">Le anomalie possono verificarsi in XAudio2, in questo argomento vengono illustrate le modalità di segnalazione e alcuni approcci per correggerli.</span><span class="sxs-lookup"><span data-stu-id="0d659-104">Glitches can occur in XAudio2, this topic covers how they are reported and some approaches to fixing them.</span></span>

<span data-ttu-id="0d659-105">Questa panoramica illustra gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d659-105">This overview covers the following topics:</span></span>

-   [<span data-ttu-id="0d659-106">Cause di problemi di output audio o glitch</span><span class="sxs-lookup"><span data-stu-id="0d659-106">Causes of audio output problems or glitches</span></span>](#causes-of-audio-output-problems-or-glitches)
-   [<span data-ttu-id="0d659-107">Come XAudio2 segnala i problemi</span><span class="sxs-lookup"><span data-stu-id="0d659-107">How XAudio2 reports problems</span></span>](#how-xaudio2-reports-problems)
-   [<span data-ttu-id="0d659-108">Approcci alla risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="0d659-108">Approaches to fixing problems</span></span>](#approaches-to-fixing-problems)
-   [<span data-ttu-id="0d659-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d659-109">Related topics</span></span>](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a><span data-ttu-id="0d659-110">Cause di problemi di output audio o glitch</span><span class="sxs-lookup"><span data-stu-id="0d659-110">Causes of audio output problems or glitches</span></span>

<span data-ttu-id="0d659-111">Per diversi motivi, è possibile che si verifichino problemi nell'output di XAudio2.</span><span class="sxs-lookup"><span data-stu-id="0d659-111">Glitches can occur in XAudio2 output for several reasons.</span></span>

-   <span data-ttu-id="0d659-112">Una voce di origine XAudio2 è affamata.</span><span class="sxs-lookup"><span data-stu-id="0d659-112">An XAudio2 source voice is starved.</span></span> <span data-ttu-id="0d659-113">Il client non invia audio aggiornato in modo sufficientemente rapido.</span><span class="sxs-lookup"><span data-stu-id="0d659-113">The client is not submitting fresh audio to it fast enough.</span></span> <span data-ttu-id="0d659-114">Si ottiene il silenzio perché non sono disponibili dati da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="0d659-114">You get silence because it has no data to play.</span></span>
-   <span data-ttu-id="0d659-115">Il XAudio2 nel suo complesso è sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="0d659-115">XAudio2 as a whole is overburdened.</span></span> <span data-ttu-id="0d659-116">Sono necessari più di *x* MS per produrre *x* MS di audio.</span><span class="sxs-lookup"><span data-stu-id="0d659-116">It takes longer than *X* ms to produce *X* ms of audio.</span></span> <span data-ttu-id="0d659-117">Si ottengono forcelle perché XAudio2 non può produrre dati con la stessa velocità con cui il dispositivo audio lo richiede.</span><span class="sxs-lookup"><span data-stu-id="0d659-117">You get dropouts because XAudio2 can't produce data as fast as the audio device needs it.</span></span> <span data-ttu-id="0d659-118">È possibile che si stiano eseguendo troppe voci o effetti per volta, eseguendo troppe operazioni nei callback XAudio2 o eseguendo troppo spesso chiamate API XAudio2.</span><span class="sxs-lookup"><span data-stu-id="0d659-118">You might be running too many voices or effects at a time, doing too much work in XAudio2 callbacks, or making XAudio2 API calls too frequently.</span></span>
-   <span data-ttu-id="0d659-119">Il thread di elaborazione audio è bloccato perché l'implementazione del client di un callback XAudio2 sta eseguendo operazioni che possono bloccare il thread.</span><span class="sxs-lookup"><span data-stu-id="0d659-119">The audio processing thread is stalling because the client's implementation of some XAudio2 callback is doing things that can block the thread.</span></span> <span data-ttu-id="0d659-120">Ad esempio, potrebbe accedere al disco, sincronizzarsi con altri thread o chiamare altre funzioni che potrebbero bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="0d659-120">For example, it might be accessing the disk, synchronizing with other threads, or calling other functions that may block.</span></span> <span data-ttu-id="0d659-121">Usare un thread in background con priorità bassa che il callback può segnalare per eseguire tali attività.</span><span class="sxs-lookup"><span data-stu-id="0d659-121">Use a lower-priority background thread that the callback can signal to perform such tasks.</span></span>
-   <span data-ttu-id="0d659-122">Il sistema nel suo complesso è sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="0d659-122">The system as a whole is overloaded.</span></span> <span data-ttu-id="0d659-123">Gli altri thread in esecuzione con una priorità uguale o superiore a quella di XAudio2 eseguono troppe operazioni.</span><span class="sxs-lookup"><span data-stu-id="0d659-123">Other threads running at the same or higher priority than XAudio2 are doing too much work.</span></span> <span data-ttu-id="0d659-124">Sono in competizione con il thread audio per il tempo di CPU.</span><span class="sxs-lookup"><span data-stu-id="0d659-124">They are competing with the audio thread for CPU time.</span></span>

## <a name="how-xaudio2-reports-problems"></a><span data-ttu-id="0d659-125">Come XAudio2 segnala i problemi</span><span class="sxs-lookup"><span data-stu-id="0d659-125">How XAudio2 reports problems</span></span>

<span data-ttu-id="0d659-126">XAudio2 può comunicare le anomalie nella compilazione di debug in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="0d659-126">XAudio2 can communicate glitches in the debug build in several ways.</span></span>

-   <span data-ttu-id="0d659-127">Se una voce sta per esaurirsi, XAudio2 Visualizza un messaggio in questo formato.</span><span class="sxs-lookup"><span data-stu-id="0d659-127">If a voice is being starved, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   <span data-ttu-id="0d659-128">Se il thread audio viene eseguito per troppo tempo, XAudio2 Visualizza un messaggio in questo formato.</span><span class="sxs-lookup"><span data-stu-id="0d659-128">If the audio thread runs for too long, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    <span data-ttu-id="0d659-129">In genere, questo messaggio viene visualizzato con il messaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="0d659-129">Typically, this message occurs with the next message.</span></span>

-   <span data-ttu-id="0d659-130">Se non è possibile alimentare i nuovi dati audio in un driver audio, XAudio2 Visualizza un messaggio in questo modulo.</span><span class="sxs-lookup"><span data-stu-id="0d659-130">If the audio driver can't be fed new audio data on time, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   <span data-ttu-id="0d659-131">La chiamata di [**IXAudio2:: GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) fornisce dati sulle prestazioni di XAudio2, incluso il numero totale di glitch dall'avvio del motore XAudio2.</span><span class="sxs-lookup"><span data-stu-id="0d659-131">Calling [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) provides XAudio2 performance data, including the total number of glitches since the XAudio2 engine started.</span></span>

## <a name="approaches-to-fixing-problems"></a><span data-ttu-id="0d659-132">Approcci alla risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="0d659-132">Approaches to fixing problems</span></span>

<span data-ttu-id="0d659-133">Di seguito sono riportati i possibili modi per ridurre i problemi di audio.</span><span class="sxs-lookup"><span data-stu-id="0d659-133">Possible ways to reduce audio glitches include the following.</span></span>

-   <span data-ttu-id="0d659-134">Nel caso di inedia vocale: aumentare la quantità di dati audio accodati in avanti su una voce.</span><span class="sxs-lookup"><span data-stu-id="0d659-134">In the voice starvation case: Increase the amount of audio data that is queued ahead on a voice.</span></span> <span data-ttu-id="0d659-135">È possibile usare [**IXAudio2SourceVoice:: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) per individuare il numero di buffer accodati in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="0d659-135">You can use [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) to discover the number of buffers queued at any moment.</span></span> <span data-ttu-id="0d659-136">Se si verificano ancora errori di inedia vocale, ma non è possibile udire alcun problema, assicurarsi di impostare il [**\_ buffer di XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flag** per XAUDIO2 \_ \_ la fine del \_ flusso sul buffer finale di un suono.</span><span class="sxs-lookup"><span data-stu-id="0d659-136">If you still see voice starvation errors, but can't hear any glitch, make sure you are setting [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flags** to XAUDIO2\_END\_OF\_STREAM on the final buffer of a sound.</span></span> <span data-ttu-id="0d659-137">Ciò indica a XAudio2 di non prevedere che altri buffer siano necessariamente disponibili non appena questo viene completato.</span><span class="sxs-lookup"><span data-stu-id="0d659-137">This tells XAudio2 not to expect any more buffers necessarily to be available as soon as this one completes.</span></span>

    <span data-ttu-id="0d659-138">Negli altri casi:</span><span class="sxs-lookup"><span data-stu-id="0d659-138">In the other cases:</span></span>

    -   <span data-ttu-id="0d659-139">Ridurre il numero di voci attive ed effetti nel grafico, soprattutto gli effetti costosi come il riverbero.</span><span class="sxs-lookup"><span data-stu-id="0d659-139">Reduce the number of active voices and effects in the graph, especially expensive effects like reverb.</span></span>
    -   <span data-ttu-id="0d659-140">Disabilitare le voci e gli effetti che non si sta usando.</span><span class="sxs-lookup"><span data-stu-id="0d659-140">Disable voices and effects you're not using.</span></span>
    -   <span data-ttu-id="0d659-141">Usare i \_ flag XAUDIO2 Voice \_ NOSRC e XAUDIO2 \_ Voice \_ nopitch in [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), quando possibile.</span><span class="sxs-lookup"><span data-stu-id="0d659-141">Use the XAUDIO2\_VOICE\_NOSRC and XAUDIO2\_VOICE\_NOPITCH flags in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), whenever possible.</span></span> <span data-ttu-id="0d659-142">La conversione della frequenza di campionamento è costosa.</span><span class="sxs-lookup"><span data-stu-id="0d659-142">Sample rate conversion is costly.</span></span>
    -   <span data-ttu-id="0d659-143">Ridurre la frequenza di campionamento delle singole voci.</span><span class="sxs-lookup"><span data-stu-id="0d659-143">Reduce the sample rate of individual voices.</span></span> <span data-ttu-id="0d659-144">Ad esempio, una voce submix che ospita un effetto di riverbero può avere una frequenza di campionamento inferiore rispetto a quella di origine che invia alla voce.</span><span class="sxs-lookup"><span data-stu-id="0d659-144">For example, a submix voice hosting a reverb effect can have a lower sample rate than the source voice sending to it.</span></span> <span data-ttu-id="0d659-145">I suoni come le esplosioni e gli spari che non necessitano di fedeltà elevata possono essere registrati anche a tariffe di campionamento inferiori.</span><span class="sxs-lookup"><span data-stu-id="0d659-145">Sounds such as explosions and gunshots that don't need high fidelity can also be recorded at lower sample rates.</span></span>
    -   <span data-ttu-id="0d659-146">Assicurarsi che le implementazioni di callback eseguano il minor lavoro possibile e mai si blocchino.</span><span class="sxs-lookup"><span data-stu-id="0d659-146">Ensure that callback implementations do as little work as possible and never block.</span></span>
    -   <span data-ttu-id="0d659-147">Effettuare un minor numero di chiamate a XAudio2.</span><span class="sxs-lookup"><span data-stu-id="0d659-147">Make fewer calls to XAudio2.</span></span> <span data-ttu-id="0d659-148">In genere non è necessario aggiornare i parametri audio per ogni fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="0d659-148">Audio parameters usually don't need to be updated for every video frame.</span></span> <span data-ttu-id="0d659-149">Ogni 30 ms è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="0d659-149">Every 30 ms or so is sufficient.</span></span> <span data-ttu-id="0d659-150">È consigliabile eliminare le chiamate ridondanti, ad esempio impostando il volume più volte in rapida successione.</span><span class="sxs-lookup"><span data-stu-id="0d659-150">You should eliminate redundant calls, such as setting volume several times in quick succession.</span></span>
    -   <span data-ttu-id="0d659-151">Ridurre l'utilizzo complessivo della CPU del gioco.</span><span class="sxs-lookup"><span data-stu-id="0d659-151">Reduce the game's overall CPU usage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d659-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d659-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d659-153">Funzionalità di debug</span><span class="sxs-lookup"><span data-stu-id="0d659-153">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="0d659-154">Guida di riferimento alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="0d659-154">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
