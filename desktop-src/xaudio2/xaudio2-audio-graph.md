---
description: Il set di tutte le voci, con gli effetti contenuti e le relative interconnessioni, viene definito grafico di elaborazione audio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: Grafico audio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234060"
---
# <a name="xaudio2-audio-graph"></a><span data-ttu-id="a8c4a-103">Grafico audio XAudio2</span><span class="sxs-lookup"><span data-stu-id="a8c4a-103">XAudio2 Audio Graph</span></span>

<span data-ttu-id="a8c4a-104">Il set di tutte le voci, con gli effetti contenuti e le relative interconnessioni, viene definito grafico di elaborazione audio.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-104">The set of all voices, with their contained effects and their interconnections, is referred to as the audio processing graph.</span></span> <span data-ttu-id="a8c4a-105">Il grafico accetta un set di flussi audio dal client come input, li elabora e recapita il risultato finale a un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-105">The graph takes a set of audio streams from the client as input, processes them, and delivers the final result to an audio device.</span></span> <span data-ttu-id="a8c4a-106">Tutte le elaborazioni audio avvengono in un thread separato con una periodicità definita dal quantum del grafo (attualmente 10 millisecondi in Microsoft Windows e 5 1/3 millisecondi su Xbox 360).</span><span class="sxs-lookup"><span data-stu-id="a8c4a-106">All audio processing takes place in a separate thread with a periodicity defined by the graph's quantum (currently 10 milliseconds on Microsoft Windows, and 5 1/3 milliseconds on Xbox 360).</span></span> <span data-ttu-id="a8c4a-107">Ogni quantum di millisecondi, il thread viene riattivato e disperde i millisecondi quantici dei dati audio attraverso l'intero grafico.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-107">Every quantum milliseconds, the thread wakes up and disperses quantum milliseconds of audio data through the entire graph.</span></span> <span data-ttu-id="a8c4a-108">Per un esempio di creazione di un grafico audio di base, vedere How to: [Build a Basic audio processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="a8c4a-108">For an example of building a basic audio graph, see How to: [Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span>

<span data-ttu-id="a8c4a-109">Un semplice grafico audio:</span><span class="sxs-lookup"><span data-stu-id="a8c4a-109">A simple audio graph:</span></span>

![un semplice grafico audio](images/xaudio2-audio-graph.png)

<span data-ttu-id="a8c4a-111">Il client può controllare dinamicamente lo stato del grafo mentre è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-111">The client can control the graph's state dynamically while it is running.</span></span> <span data-ttu-id="a8c4a-112">Le azioni di controllo possono includere l'aggiunta e la rimozione di input e output, la modifica degli effetti interni e delle interconnessioni, l'impostazione dei parametri sugli effetti, l'abilitazione e la disabilitazione di parti del grafico e così via.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-112">Control actions might include adding and removing inputs and outputs, changing the internal effects and interconnections, setting parameters on the effects, enabling and disabling parts of the graph, and so on.</span></span> <span data-ttu-id="a8c4a-113">Per un esempio di modifica dinamica di un grafico audio, vedere [procedura: aggiungere o rimuovere voci da un grafico audio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-113">For an example of dynamically changing an audio graph, see [How to: Dynamically Add or Remove Voices From an Audio Graph](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span></span>

## <a name="processing-the-graph"></a><span data-ttu-id="a8c4a-114">Elaborazione del grafo</span><span class="sxs-lookup"><span data-stu-id="a8c4a-114">Processing the Graph</span></span>

<span data-ttu-id="a8c4a-115">Qualsiasi chiamata al metodo che influisce su un oggetto nel grafico viene considerata una modifica dello stato del grafico.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-115">Any method call that affects any object in the graph is considered to be effecting a graph state change.</span></span> <span data-ttu-id="a8c4a-116">Le modifiche dello stato del grafo includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a8c4a-116">Graph state changes include the following:</span></span>

-   <span data-ttu-id="a8c4a-117">Creazione ed eliminazione di voci</span><span class="sxs-lookup"><span data-stu-id="a8c4a-117">Creating and destroying voices</span></span>
-   <span data-ttu-id="a8c4a-118">Avvio o arresto di voci</span><span class="sxs-lookup"><span data-stu-id="a8c4a-118">Starting or stopping voices</span></span>
-   <span data-ttu-id="a8c4a-119">Modifica delle destinazioni di una voce</span><span class="sxs-lookup"><span data-stu-id="a8c4a-119">Changing the destinations of a voice</span></span>
-   <span data-ttu-id="a8c4a-120">Modifica delle catene degli effetti</span><span class="sxs-lookup"><span data-stu-id="a8c4a-120">Modifying effect chains</span></span>
-   <span data-ttu-id="a8c4a-121">Abilitazione o disabilitazione degli effetti</span><span class="sxs-lookup"><span data-stu-id="a8c4a-121">Enabling or disabling effects</span></span>
-   <span data-ttu-id="a8c4a-122">Impostazione di parametri per gli effetti o per SRCs, filtri, volumi e mixer predefiniti</span><span class="sxs-lookup"><span data-stu-id="a8c4a-122">Setting parameters on the effects or on the built-in SRCs, filters, volumes, and mixers</span></span>

<span data-ttu-id="a8c4a-123">Qualsiasi set di modifiche dello stato del grafico può essere combinato ed eseguito come transazione atomica.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-123">Any set of graph state changes can be combined and performed as an atomic transaction.</span></span> <span data-ttu-id="a8c4a-124">Queste operazioni atomiche sono note come set di operazioni.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-124">These atomic operations are known as operation sets.</span></span> <span data-ttu-id="a8c4a-125">Sono illustrati nella panoramica dei [set di operazioni XAudio2](xaudio2-operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c4a-125">They are discussed in the [XAudio2 Operation Sets](xaudio2-operation-sets.md) overview.</span></span>

## <a name="internal-data-representation"></a><span data-ttu-id="a8c4a-126">Rappresentazione dati interna</span><span class="sxs-lookup"><span data-stu-id="a8c4a-126">Internal Data Representation</span></span>

<span data-ttu-id="a8c4a-127">I dati audio all'interno del grafo XAudio2 vengono sempre archiviati ed elaborati in formato PCM a virgola mobile a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-127">Audio data within the XAudio2 graph is always stored and processed in 32-bit floating-point PCM form.</span></span> <span data-ttu-id="a8c4a-128">Tuttavia, il numero di canali e la frequenza di campionamento possono variare all'interno del grafico.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-128">However, the channel count and sample rate can vary within the graph.</span></span> <span data-ttu-id="a8c4a-129">Il formato in cui una determinata voce elabora audio è determinato dal tipo di voce e dai parametri usati per creare la voce.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-129">The format in which a given voice processes audio is determined by the voice type and parameters used to create the voice.</span></span>



| <span data-ttu-id="a8c4a-130">Tipo voce</span><span class="sxs-lookup"><span data-stu-id="a8c4a-130">Voice Type</span></span>                                                                                                      | <span data-ttu-id="a8c4a-131">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8c4a-131">Parameters</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8c4a-132">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="a8c4a-132">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | <span data-ttu-id="a8c4a-133">Il numero di canali e la frequenza di campionamento delle voci a cui la voce di origine invia audio.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-133">The channel count and sample rate of the voices to which the source voice sends audio.</span></span>         |
| <span data-ttu-id="a8c4a-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span><span class="sxs-lookup"><span data-stu-id="a8c4a-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) and [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span></span> | <span data-ttu-id="a8c4a-135">Argomenti *InputChannels* e *InputSampleRate* usati per creare la voce di submix/master.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-135">The *InputChannels* and *InputSampleRate* arguments used to create the submix/mastering voice.</span></span> |



 

## <a name="format-conversion"></a><span data-ttu-id="a8c4a-136">Conversione del formato</span><span class="sxs-lookup"><span data-stu-id="a8c4a-136">Format Conversion</span></span>

<span data-ttu-id="a8c4a-137">XAudio2 gestisce la frequenza di campionamento o le conversioni di canale richieste quando l'audio passa da una voce all'altra, con le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8c4a-137">XAudio2 handles any sample rate or channel conversions that are required as audio travels from one voice to another, with the following limitations:</span></span>

-   <span data-ttu-id="a8c4a-138">Tutte le voci di destinazione per una voce specifica devono essere in esecuzione alla stessa frequenza di campionamento</span><span class="sxs-lookup"><span data-stu-id="a8c4a-138">All destination voices for a particular voice must be running at the same sample rate</span></span>
-   <span data-ttu-id="a8c4a-139">Gli effetti di una catena di effetti possono modificare il numero di canali audio, ma non la frequenza di campionamento</span><span class="sxs-lookup"><span data-stu-id="a8c4a-139">Effects in an effect chain can change the audio's channel count, but not its sample rate</span></span>
-   <span data-ttu-id="a8c4a-140">Il numero di canali di output di una catena di effetti deve corrispondere a quello delle voci a cui viene inviato</span><span class="sxs-lookup"><span data-stu-id="a8c4a-140">An effect chain's output channel count must match that of the voices to which it sends</span></span>
-   <span data-ttu-id="a8c4a-141">Non è possibile apportare modifiche a grafici dinamici che interrompono le regole precedenti</span><span class="sxs-lookup"><span data-stu-id="a8c4a-141">No dynamic graph change can be made which would break the rules above</span></span>

<span data-ttu-id="a8c4a-142">Sul lato input, le voci di origine possono leggere i dati in qualsiasi formato PCM valido o in uno dei formati compressi supportati da XAudio2.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-142">On the input side, source voices can read data in any valid PCM format, or in any of the compressed formats supported by XAudio2.</span></span> <span data-ttu-id="a8c4a-143">Se i dati di input vengono compressi, vengono decodificati in PCM a virgola mobile prima di eseguire altre operazioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-143">If the input data is compressed, it is decoded to floating-point PCM before any further processing is done.</span></span>

<span data-ttu-id="a8c4a-144">Sul lato output, le voci di mastering possono produrre solo dati PCM.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-144">On the output side, mastering voices can only produce PCM data.</span></span> <span data-ttu-id="a8c4a-145">Questi dati soddisferanno sempre le stesse restrizioni descritte in precedenza per i dati PCM di input.</span><span class="sxs-lookup"><span data-stu-id="a8c4a-145">This data will always satisfy the same restrictions described above for input PCM data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8c4a-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8c4a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8c4a-147">Grafici audio</span><span class="sxs-lookup"><span data-stu-id="a8c4a-147">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="a8c4a-148">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="a8c4a-148">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a8c4a-149">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="a8c4a-149">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="a8c4a-150">Procedura: Aggiungere o rimuovere dinamicamente voci da un grafico audio</span><span class="sxs-lookup"><span data-stu-id="a8c4a-150">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[<span data-ttu-id="a8c4a-151">Procedura: Usare voci di missaggio secondario</span><span class="sxs-lookup"><span data-stu-id="a8c4a-151">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="a8c4a-152">Procedura: Creare una catena di effetti</span><span class="sxs-lookup"><span data-stu-id="a8c4a-152">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



