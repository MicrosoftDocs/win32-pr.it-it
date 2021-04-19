---
description: 'Sono disponibili tre tipi di oggetti voce XAudio2: Source, submix e mastering Voices.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Voci di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317838"
---
# <a name="xaudio2-voices"></a><span data-ttu-id="00bee-103">Voci di XAudio2</span><span class="sxs-lookup"><span data-stu-id="00bee-103">XAudio2 Voices</span></span>

<span data-ttu-id="00bee-104">Sono disponibili tre tipi di oggetti voce XAudio2: *source*, *submix* e *Mastering* Voices.</span><span class="sxs-lookup"><span data-stu-id="00bee-104">There are three types of XAudio2 voice objects: *source*, *submix*, and *mastering* voices.</span></span> <span data-ttu-id="00bee-105">Le voci di origine operano sui dati forniti dal client.</span><span class="sxs-lookup"><span data-stu-id="00bee-105">Source voices operate on audio data provided by the client.</span></span> <span data-ttu-id="00bee-106">Le voci di origine e di missaggio secondario inviano l'output a una o più voci di missaggio secondario o mastering.</span><span class="sxs-lookup"><span data-stu-id="00bee-106">Source and submix voices send their output to one or more submix or mastering voices.</span></span> <span data-ttu-id="00bee-107">Le voci di missaggio secondario e mastering missano l'audio proveniente da tutte le voci che le alimentano e operano sul risultato.</span><span class="sxs-lookup"><span data-stu-id="00bee-107">Submix and mastering voices mix the audio from all voices feeding them, and operate on the result.</span></span> <span data-ttu-id="00bee-108">Le voci mastering scrivono dati audio in un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="00bee-108">Mastering voices write audio data to an audio device.</span></span>

## <a name="actions-performed-by-all-voices"></a><span data-ttu-id="00bee-109">Azioni eseguite da tutte le voci</span><span class="sxs-lookup"><span data-stu-id="00bee-109">Actions Performed by All Voices</span></span>

<span data-ttu-id="00bee-110">Tutte le voci eseguono le azioni seguenti in ordine sull'audio che viaggia comunque.</span><span class="sxs-lookup"><span data-stu-id="00bee-110">All voices perform the following actions in order on the audio that travels though them.</span></span>

1.  <span data-ttu-id="00bee-111">Regolazione complessiva del volume, che interessano tutti i canali audio.</span><span class="sxs-lookup"><span data-stu-id="00bee-111">Overall volume adjustment, affecting all audio channels.</span></span> <span data-ttu-id="00bee-112">Vedere [**IXAudio2Voice:: sevolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span><span class="sxs-lookup"><span data-stu-id="00bee-112">See [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span></span>
2.  <span data-ttu-id="00bee-113">Una catena facoltativa specificata dal client di uno o più effetti DSP, ad esempio il riverbero incorporato o un effetto utente definito dall'interfaccia [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) .</span><span class="sxs-lookup"><span data-stu-id="00bee-113">An optional client-specified chain of one or more DSP effects, such as the built-in reverb or a user effect defined by the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface.</span></span> <span data-ttu-id="00bee-114">Vedere [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span><span class="sxs-lookup"><span data-stu-id="00bee-114">See [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span></span>
3.  <span data-ttu-id="00bee-115">Regolazione del volume di output per canale.</span><span class="sxs-lookup"><span data-stu-id="00bee-115">Per-channel output volume adjustment.</span></span> <span data-ttu-id="00bee-116">Vedere [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span><span class="sxs-lookup"><span data-stu-id="00bee-116">See [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span></span>
4.  <span data-ttu-id="00bee-117">Separare la combinazione di matrici in ogni voce di destinazione o nel dispositivo di output audio per le voci di mastering.</span><span class="sxs-lookup"><span data-stu-id="00bee-117">Separate matrix mix to each of the destination voices or to the audio output device for mastering voices.</span></span> <span data-ttu-id="00bee-118">Questa combinazione modifica il numero di canali nell'audio, se necessario.</span><span class="sxs-lookup"><span data-stu-id="00bee-118">This mix changes the number of channels in the audio, if necessary.</span></span>

## <a name="source-voices"></a><span data-ttu-id="00bee-119">Voci di origine</span><span class="sxs-lookup"><span data-stu-id="00bee-119">Source Voices</span></span>

<span data-ttu-id="00bee-120">Usare le voci di origine per inviare i dati audio alla pipeline di elaborazione XAudio2.</span><span class="sxs-lookup"><span data-stu-id="00bee-120">Use source voices to submit audio data into the XAudio2 processing pipeline.</span></span> <span data-ttu-id="00bee-121">Sono i punti di ingresso nel [grafico audio XAudio2](xaudio2-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="00bee-121">They are the entry points into the [XAudio2 Audio Graph](xaudio2-audio-graph.md).</span></span> <span data-ttu-id="00bee-122">È necessario inviare i dati vocali a una voce di Mastering da ascoltare, direttamente o tramite le voci submix intermedie.</span><span class="sxs-lookup"><span data-stu-id="00bee-122">You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices.</span></span>

<span data-ttu-id="00bee-123">Oltre alle azioni eseguite da tutte le voci, le voci di origine eseguono le azioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="00bee-123">In addition to the actions performed by all voices, source voices perform the following actions.</span></span>

-   <span data-ttu-id="00bee-124">Se necessario, viene eseguito prima un decodificatore per convertire i dati di origine codificati in Pulse Code Modulation (PCM).</span><span class="sxs-lookup"><span data-stu-id="00bee-124">If necessary, a decoder runs first to convert encoded source data to Pulse Code Modulation (PCM).</span></span>
-   <span data-ttu-id="00bee-125">Una conversione della frequenza di campionamento a frequenza variabile (SRC) converte i dati audio di origine della voce nella frequenza di campionamento prevista dalle voci di destinazione, se necessario, e supporta anche le modifiche di Dynamic pitch.</span><span class="sxs-lookup"><span data-stu-id="00bee-125">A variable-rate sample rate conversion (SRC) converts the voice's source audio data to the sample rate expected by its destination voices, if necessary, and also supports dynamic pitch changes.</span></span>
-   <span data-ttu-id="00bee-126">Un filtro facoltativo di variabile di stato può essere utilizzato per colorare il suono in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="00bee-126">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="00bee-127">Vedere [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="00bee-127">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="00bee-128">È possibile applicare un filtro facoltativo agli output della voce.</span><span class="sxs-lookup"><span data-stu-id="00bee-128">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="00bee-129">Vedere [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="00bee-129">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="submix-voices"></a><span data-ttu-id="00bee-130">Voci di submix</span><span class="sxs-lookup"><span data-stu-id="00bee-130">Submix Voices</span></span>

<span data-ttu-id="00bee-131">Una voce submix viene utilizzata principalmente per i miglioramenti delle prestazioni e l'elaborazione degli effetti.</span><span class="sxs-lookup"><span data-stu-id="00bee-131">A submix voice is used primarily for performance improvements and effects processing.</span></span> <span data-ttu-id="00bee-132">Non è possibile inviare i buffer di dati direttamente alle voci submix.</span><span class="sxs-lookup"><span data-stu-id="00bee-132">You cannot submit data buffers directly to submix voices.</span></span> <span data-ttu-id="00bee-133">Non sarà udibile a meno che non lo invii a una voce Master.</span><span class="sxs-lookup"><span data-stu-id="00bee-133">It will not be audible unless you submit it to a mastering voice.</span></span> <span data-ttu-id="00bee-134">È possibile usare un submix Voice per assicurarsi che un particolare set di dati vocali venga convertito nello stesso formato e che una particolare catena di effetti venga elaborata sul risultato collettivo.</span><span class="sxs-lookup"><span data-stu-id="00bee-134">You can use a submix voice to ensure that a particular set of voice data is converted to the same format and to have a particular effect chain processed on the collective result.</span></span>

<span data-ttu-id="00bee-135">Oltre alle azioni eseguite da tutte le voci, le voci submix eseguono le azioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="00bee-135">In addition to the actions performed by all voices, submix voices perform the following actions.</span></span>

-   <span data-ttu-id="00bee-136">Un SRC a frequenza fissa viene eseguito sull'output della voce, se necessario, per convertire l'audio nella frequenza di campionamento prevista dalle voci di destinazione.</span><span class="sxs-lookup"><span data-stu-id="00bee-136">A fixed-rate SRC runs on the voice's output, if necessary, to convert the audio to the sample rate expected by its destination voices.</span></span>
-   <span data-ttu-id="00bee-137">Un filtro facoltativo di variabile di stato può essere utilizzato per colorare il suono in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="00bee-137">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="00bee-138">Vedere [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="00bee-138">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="00bee-139">È possibile applicare un filtro facoltativo agli output della voce.</span><span class="sxs-lookup"><span data-stu-id="00bee-139">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="00bee-140">Vedere [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="00bee-140">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="mastering-voices"></a><span data-ttu-id="00bee-141">Voci di mastering</span><span class="sxs-lookup"><span data-stu-id="00bee-141">Mastering Voices</span></span>

<span data-ttu-id="00bee-142">Usare una voce Master per rappresentare il dispositivo di output audio.</span><span class="sxs-lookup"><span data-stu-id="00bee-142">Use a mastering voice to represent the audio output device.</span></span> <span data-ttu-id="00bee-143">Non è possibile inviare i buffer di dati direttamente a voci di mastering, ma i dati inviati ad altri tipi di voci devono essere indirizzati a una voce di Mastering da sentire.</span><span class="sxs-lookup"><span data-stu-id="00bee-143">You cannot submit data buffers directly to mastering voices, but data submitted to other types of voices must go to a mastering voice to be heard.</span></span>

<span data-ttu-id="00bee-144">Oltre alle azioni eseguite da tutte le voci, le voci di mastering eseguono le azioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="00bee-144">In addition to the actions performed by all voices, mastering voices perform the following actions.</span></span>

-   <span data-ttu-id="00bee-145">Se si crea la voce Master con un valore *InputSampleRate* esplicito che non è supportato dal dispositivo audio, viene usata una src a frequenza fissa per eseguire la conversione alla frequenza di campionamento più vicina supportata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00bee-145">If you create the mastering voice with an explicit *InputSampleRate* value that is not supported by the audio device, a fixed-rate SRC is used to convert to the closest sample rate supported by the device.</span></span>
-   <span data-ttu-id="00bee-146">Ritagliare l'audio di output finale, se richiesto dal dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="00bee-146">Clip the final output audio, if it is required by the output device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00bee-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00bee-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00bee-148">Voci</span><span class="sxs-lookup"><span data-stu-id="00bee-148">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="00bee-149">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="00bee-149">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="00bee-150">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="00bee-150">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[<span data-ttu-id="00bee-151">**IXAudio2SubmixVoice**</span><span class="sxs-lookup"><span data-stu-id="00bee-151">**IXAudio2SubmixVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[<span data-ttu-id="00bee-152">**IXAudio2MasteringVoice**</span><span class="sxs-lookup"><span data-stu-id="00bee-152">**IXAudio2MasteringVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
