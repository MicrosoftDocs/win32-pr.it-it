---
description: La modulazione del codice a impulsi differenziale (ADPCM) è un formato di compressione con perdita di spazio, implementato per XAudio2 per fornire funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Panoramica di ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314430"
---
# <a name="adpcm-overview"></a><span data-ttu-id="6e125-103">Panoramica di ADPCM</span><span class="sxs-lookup"><span data-stu-id="6e125-103">ADPCM Overview</span></span>

<span data-ttu-id="6e125-104">La modulazione del codice a impulsi differenziale (ADPCM) è un formato di compressione con perdita di spazio, implementato per XAudio2 per fornire funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione.</span><span class="sxs-lookup"><span data-stu-id="6e125-104">Adaptive Differential Pulse Code Modulation (ADPCM) is a lossy compression format that is implemented for XAudio2 to provide additional features for specifying the size of the compression sample block.</span></span> <span data-ttu-id="6e125-105">Con un formato di compressione con perdita di dati, alcuni dati vengono modificati e persi durante la compressione.</span><span class="sxs-lookup"><span data-stu-id="6e125-105">With a lossy compression format some data is altered and lost during compression.</span></span> <span data-ttu-id="6e125-106">ADPCM può ottenere rapporti di compressione fino a 4:1.</span><span class="sxs-lookup"><span data-stu-id="6e125-106">ADPCM can achieve compression ratios of up to 4:1.</span></span>

<span data-ttu-id="6e125-107">L'implementazione di ADPCM per XAudio2 fornisce funzionalità aggiuntive per specificare le dimensioni del blocco di esempio di compressione.</span><span class="sxs-lookup"><span data-stu-id="6e125-107">The implementation of ADPCM for XAudio2 provides additional features to specify the size of the compression sample block.</span></span> <span data-ttu-id="6e125-108">ADPCM consente alla finestra di progettazione audio di scegliere un'impostazione che rappresenta un compromesso appropriato tra dimensioni, qualità e risoluzione (per l'inserimento di punti di ciclo).</span><span class="sxs-lookup"><span data-stu-id="6e125-108">ADPCM enables the audio designer to choose a setting that is an appropriate compromise among size, quality, and resolution (for placing loop points).</span></span>

<span data-ttu-id="6e125-109">XAudio2 usa una versione modificata del codec Microsoft ADPCM che supporta la formattazione dei dati estesa necessaria per fornire dimensioni del blocco di esempio personalizzate.</span><span class="sxs-lookup"><span data-stu-id="6e125-109">XAudio2 uses a modified version of the Microsoft ADPCM codec that supports the extended data formatting required to provide custom sample block sizes.</span></span> <span data-ttu-id="6e125-110">Per questo motivo, non è possibile riprodurre i dati audio XAudio2 da motori audio che non supportano questa versione del codec ADPCM.</span><span class="sxs-lookup"><span data-stu-id="6e125-110">For this reason, XAudio2 audio data cannot be played by audio engines that do not support this version of the ADPCM codec.</span></span>

> [!Note]  
> <span data-ttu-id="6e125-111">Attualmente, la compressione ADPCM è disponibile solo per Windows, incluse le distribuzioni XNA Game Studio Express per Windows.</span><span class="sxs-lookup"><span data-stu-id="6e125-111">Currently, ADPCM compression is only available for Windows, including XNA Game Studio Express for Windows deployments.</span></span>

 

## <a name="adpcm-encoding"></a><span data-ttu-id="6e125-112">Codifica ADPCM</span><span class="sxs-lookup"><span data-stu-id="6e125-112">ADPCM Encoding</span></span>

<span data-ttu-id="6e125-113">I dati audio sono codificati in ADPCM usando lo strumento da riga di comando AdpcmEncode.</span><span class="sxs-lookup"><span data-stu-id="6e125-113">Audio data is encoded to ADPCM using the AdpcmEncode command-line tool.</span></span>

-   <span data-ttu-id="6e125-114">AdpcmEncode</span><span class="sxs-lookup"><span data-stu-id="6e125-114">AdpcmEncode</span></span>

    <span data-ttu-id="6e125-115">Per codificare i file audio come ADPCM per l'uso con XAudio2, usare lo strumento da riga di comando **AdpcmEncode** .</span><span class="sxs-lookup"><span data-stu-id="6e125-115">In order to encode audio files as ADPCM for use with XAudio2, use the **AdpcmEncode** command-line tool.</span></span>

## <a name="adpcm-decoding"></a><span data-ttu-id="6e125-116">Decodifica ADPCM</span><span class="sxs-lookup"><span data-stu-id="6e125-116">ADPCM Decoding</span></span>

<span data-ttu-id="6e125-117">La decodifica software di ADPCM è supportata in XAudio2.</span><span class="sxs-lookup"><span data-stu-id="6e125-117">Software decoding of ADPCM is supported in XAudio2.</span></span>

-   <span data-ttu-id="6e125-118">XAudio2</span><span class="sxs-lookup"><span data-stu-id="6e125-118">XAudio2</span></span>

    <span data-ttu-id="6e125-119">Per usare i dati con codifica ADPCM in XAudio2, è necessario inizializzare una struttura **ADPCMWAVEFORMAT** con valori specifici di ADPCM e passarla come argomento a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) quando si crea una voce di origine.</span><span class="sxs-lookup"><span data-stu-id="6e125-119">In order to use ADPCM encoded data in XAudio2, you need to initialize a **ADPCMWAVEFORMAT** structure with ADPCM specific values, and pass it as an argument to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) when you create a source voice.</span></span> <span data-ttu-id="6e125-120">Per un esempio di caricamento e riproduzione di un suono in XAudio2, vedere [procedura: riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="6e125-120">For an example of loading and playing a sound in XAudio2, see [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md).</span></span>

## <a name="samplesperblock"></a><span data-ttu-id="6e125-121">SamplesPerBlock</span><span class="sxs-lookup"><span data-stu-id="6e125-121">SamplesPerBlock</span></span>

<span data-ttu-id="6e125-122">La compressione ADPCM funziona separando la forma d'onda in blocchi e stimando la variazione degli esempi di forma d'onda all'interno di ogni blocco.</span><span class="sxs-lookup"><span data-stu-id="6e125-122">ADPCM compression works by separating the waveform into blocks, and predicting the variation of the waveform samples within each block.</span></span> <span data-ttu-id="6e125-123">Le dimensioni dei blocchi sono misurate in esempi.</span><span class="sxs-lookup"><span data-stu-id="6e125-123">The size of the blocks is measured in samples.</span></span> <span data-ttu-id="6e125-124">La dimensione minima del blocco è di 32 campioni e la più alta è 512 campioni.</span><span class="sxs-lookup"><span data-stu-id="6e125-124">The smallest block size is 32 samples, and the highest is 512 samples.</span></span>

<span data-ttu-id="6e125-125">I blocchi di dimensioni maggiori consentono una compressione migliore, che comporta dimensioni di file più ridotte, ma a scapito della qualità e della risoluzione del suono per l'allineamento dei punti del ciclo.</span><span class="sxs-lookup"><span data-stu-id="6e125-125">Larger blocks allow better compression, which results in smaller file sizes, but at the expense of sound quality and resolution for aligning loop points.</span></span>

<span data-ttu-id="6e125-126">In generale, la modifica del valore di SamplesPerBlock determina i compromessi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e125-126">In general, modifying the SamplesPerBlock value results in these tradeoffs:</span></span>



| <span data-ttu-id="6e125-127">Se SamplesPerBlock...</span><span class="sxs-lookup"><span data-stu-id="6e125-127">If SamplesPerBlock...</span></span>      | <span data-ttu-id="6e125-128">Compressione file</span><span class="sxs-lookup"><span data-stu-id="6e125-128">File Compression</span></span> | <span data-ttu-id="6e125-129">Qualità audio</span><span class="sxs-lookup"><span data-stu-id="6e125-129">Sound Quality</span></span> | <span data-ttu-id="6e125-130">Risoluzione del punto di ciclo</span><span class="sxs-lookup"><span data-stu-id="6e125-130">Loop Point Resolution</span></span> |
|----------------------------|------------------|---------------|-----------------------|
| <span data-ttu-id="6e125-131">Aumenta (fino al massimo 512)</span><span class="sxs-lookup"><span data-stu-id="6e125-131">Increases (up to max 512)</span></span>  | <span data-ttu-id="6e125-132">Aumenta</span><span class="sxs-lookup"><span data-stu-id="6e125-132">Increases</span></span>        | <span data-ttu-id="6e125-133">Riduce</span><span class="sxs-lookup"><span data-stu-id="6e125-133">Decreases</span></span>     | <span data-ttu-id="6e125-134">Riduce</span><span class="sxs-lookup"><span data-stu-id="6e125-134">Decreases</span></span>             |
| <span data-ttu-id="6e125-135">Diminuisce (fino a min 32)</span><span class="sxs-lookup"><span data-stu-id="6e125-135">Decreases (down to min 32)</span></span> | <span data-ttu-id="6e125-136">Riduce</span><span class="sxs-lookup"><span data-stu-id="6e125-136">Decreases</span></span>        | <span data-ttu-id="6e125-137">Aumenta</span><span class="sxs-lookup"><span data-stu-id="6e125-137">Increases</span></span>     | <span data-ttu-id="6e125-138">Aumenta</span><span class="sxs-lookup"><span data-stu-id="6e125-138">Increases</span></span>             |



 

## <a name="restrictions"></a><span data-ttu-id="6e125-139">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="6e125-139">Restrictions</span></span>

<span data-ttu-id="6e125-140">Poiché ADPCM utilizza blocchi di esempio che sono allineati uno dopo l'altro, un'onda compressa con ADPCM potrebbe avere un blocco parziale non completato alla fine.</span><span class="sxs-lookup"><span data-stu-id="6e125-140">Because ADPCM uses sample blocks that are aligned one after the other, a wave compressed with ADPCM may have an unfinished, partial block at its end.</span></span> <span data-ttu-id="6e125-141">Il decodificatore ADPCM genera silenzio per la parte restante del blocco parziale, che impedisce l'iterazione del ciclo in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="6e125-141">The ADPCM decoder generates silence for the remainder of this partial block, which keeps the wave from looping seamlessly.</span></span>

<span data-ttu-id="6e125-142">Il valore del parametro *SamplesPerBlock* influiscono sulla risoluzione con cui è possibile allineare i dati Wave e i punti di ciclo.</span><span class="sxs-lookup"><span data-stu-id="6e125-142">The value of the *SamplesPerBlock* parameter affects the resolution with which you can align wave data and loop points.</span></span>

<span data-ttu-id="6e125-143">Se si tenta di applicare la compressione a un'onda non allineata, verrà visualizzato un errore o un avviso a seconda che l'onda venga usata in qualsiasi evento di riproduzione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="6e125-143">If you try to apply compression to a non-aligned wave, you will get an error or a warning depending on whether the wave is used in any looping play events.</span></span> <span data-ttu-id="6e125-144">Non è possibile comprimere un'onda utilizzata negli eventi di riproduzione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="6e125-144">You cannot compress a wave used in any looping play events.</span></span> <span data-ttu-id="6e125-145">Rimuoverlo dagli eventi di riproduzione del ciclo, quindi applicare nuovamente la compressione.</span><span class="sxs-lookup"><span data-stu-id="6e125-145">Remove it from the looping play events, and re-apply compression.</span></span>

<span data-ttu-id="6e125-146">Se si usa l'onda esclusivamente in modalità non di ciclo, la restrizione dell'allineamento del blocco di esempio non si applica.</span><span class="sxs-lookup"><span data-stu-id="6e125-146">If you use the wave exclusively in non-looping mode, the sample block alignment restriction does not apply.</span></span>

## <a name="adpcm-file-structure"></a><span data-ttu-id="6e125-147">Struttura di file ADPCM</span><span class="sxs-lookup"><span data-stu-id="6e125-147">ADPCM File Structure</span></span>

<span data-ttu-id="6e125-148">Un file ADPCM è un file RIFF standard con i tipi di blocchi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e125-148">An ADPCM file is a standard RIFF file with the following chunk types.</span></span>



| <span data-ttu-id="6e125-149">Blocco FCC</span><span class="sxs-lookup"><span data-stu-id="6e125-149">Chunk FCC</span></span>     | <span data-ttu-id="6e125-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e125-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e125-151">RIFF</span><span class="sxs-lookup"><span data-stu-id="6e125-151">RIFF</span></span>          | <span data-ttu-id="6e125-152">Blocco RIFF standard contenente un tipo di file con il valore WAVE nei primi quattro byte della sezione relativa ai dati e gli altri blocchi del file nel resto della sezione relativa ai dati.</span><span class="sxs-lookup"><span data-stu-id="6e125-152">Standard RIFF chunk containing a file type with the value WAVE in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6e125-153">FMT</span><span class="sxs-lookup"><span data-stu-id="6e125-153">fmt</span></span>           | <span data-ttu-id="6e125-154">Contiene l'intestazione del formato per il file ADPCM.</span><span class="sxs-lookup"><span data-stu-id="6e125-154">Contains the format header for the ADPCM file.</span></span> <span data-ttu-id="6e125-155">I dati in questo blocco corrispondono a una struttura **ADPCMWAVEFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="6e125-155">The data in this chunk corresponds to a **ADPCMWAVEFORMAT** structure.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6e125-156">data</span><span class="sxs-lookup"><span data-stu-id="6e125-156">data</span></span>          | <span data-ttu-id="6e125-157">Contiene i dati audio ADPCM codificati.</span><span class="sxs-lookup"><span data-stu-id="6e125-157">Contains the encoded ADPCM audio data.</span></span> <span data-ttu-id="6e125-158">Quando si usa ADPCM in XAudio2, è necessario leggere il contenuto del blocco di dati in un buffer e passarlo a una voce di origine come membro **pAudioData** di una struttura di [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="6e125-158">When you use ADPCM in XAudio2, you need to read the contents of the data chunk into a buffer, and pass it to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="6e125-159">Non è necessario scambiare byte con il contenuto del blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="6e125-159">You don't need to byte swap the contents of the data chunk.</span></span>                                                                                                                            |
| <span data-ttu-id="6e125-160">SMPL e wsmp</span><span class="sxs-lookup"><span data-stu-id="6e125-160">smpl and wsmp</span></span> | <span data-ttu-id="6e125-161">Tipi di blocchi facoltativi contenenti le informazioni di ciclo per il file ADPCM.</span><span class="sxs-lookup"><span data-stu-id="6e125-161">Optional chunk types containing the looping information for the ADPCM file.</span></span> <span data-ttu-id="6e125-162">Quando si usa ADPCM in XAudio2, i valori contenuti nei blocchi SMPL o wsmp vengono usati per popolare i membri **LoopBeginLoopLength** e **LoopCount** della struttura del [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="6e125-162">When you use ADPCM in XAudio2, the values contained in the smpl or wsmp chunks are used to populate the **LoopBeginLoopLength** and **LoopCount** members of the [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="6e125-163">In Xbox 360 è necessario scambiare i dati caricati da un blocco SMPL per tenere conto della differenza di caratteristica tra Windows e Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="6e125-163">On the Xbox 360, you need to byte swap the data loaded from a smpl chunk to account for the endianness difference between Windows and Xbox 360.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6e125-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e125-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e125-165">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="6e125-165">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
