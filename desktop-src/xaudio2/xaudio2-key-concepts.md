---
description: Questa panoramica introduce alcuni concetti chiave per l'uso di XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Concetti chiave di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317841"
---
# <a name="xaudio2-key-concepts"></a><span data-ttu-id="46555-103">Concetti chiave di XAudio2</span><span class="sxs-lookup"><span data-stu-id="46555-103">XAudio2 Key Concepts</span></span>

<span data-ttu-id="46555-104">Questa panoramica introduce alcuni concetti chiave per l'uso di XAudio2.</span><span class="sxs-lookup"><span data-stu-id="46555-104">This overview introduces some key concepts for using XAudio2.</span></span>

-   [<span data-ttu-id="46555-105">Motore XAudio2</span><span class="sxs-lookup"><span data-stu-id="46555-105">XAudio2 Engine</span></span>](#xaudio2-engine)
-   [<span data-ttu-id="46555-106">Voci</span><span class="sxs-lookup"><span data-stu-id="46555-106">Voices</span></span>](#voices)
-   [<span data-ttu-id="46555-107">Grafico audio</span><span class="sxs-lookup"><span data-stu-id="46555-107">Audio Graph</span></span>](#audio-graph)
-   [<span data-ttu-id="46555-108">Callback</span><span class="sxs-lookup"><span data-stu-id="46555-108">Callbacks</span></span>](#callbacks)
-   [<span data-ttu-id="46555-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46555-109">Related Topics</span></span>](#related-topics)

## <a name="xaudio2-engine"></a><span data-ttu-id="46555-110">Motore XAudio2</span><span class="sxs-lookup"><span data-stu-id="46555-110">XAudio2 Engine</span></span>

<span data-ttu-id="46555-111">L’interfaccia [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) è l’elemento principale del motore XAudio2</span><span class="sxs-lookup"><span data-stu-id="46555-111">The [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface is the core of the XAudio2 engine.</span></span> <span data-ttu-id="46555-112">La creazione di un'istanza dell'interfaccia **IXAudio2** consente al client di enumerare i dispositivi audio disponibili, di configurare le proprietà globali dell'API, di creare voci e di monitorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="46555-112">Creating an instance of the **IXAudio2** interface allows the client to enumerate the available audio devices, to configure global API properties, to create voices, and to monitor performance.</span></span> <span data-ttu-id="46555-113">La funzione helper [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) esegue le attività di creazione di istanze e di inizializzazione per XAudio2.</span><span class="sxs-lookup"><span data-stu-id="46555-113">The [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper function performs instantiation and initialization tasks for XAudio2.</span></span>

<span data-ttu-id="46555-114">È possibile creare istanze di XAudio2 più volte all'interno di un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="46555-114">You can create instances of XAudio2 multiple times within a single process.</span></span> <span data-ttu-id="46555-115">Ogni oggetto XAudio2 opera in modo indipendente e dispone di un proprio thread di elaborazione audio.</span><span class="sxs-lookup"><span data-stu-id="46555-115">Each XAudio2 object operates independently, and has its own audio processing thread.</span></span> <span data-ttu-id="46555-116">Vengono condivise solo le impostazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="46555-116">Only the debug settings are shared.</span></span> <span data-ttu-id="46555-117">Questo è importante in Windows in cui è possibile caricare diversi componenti in un unico processo.</span><span class="sxs-lookup"><span data-stu-id="46555-117">This is important on Windows where several different components may be loaded in a single process.</span></span> <span data-ttu-id="46555-118">Internet Explorer, ad esempio, potrebbe utilizzare più componenti XAudio2 contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="46555-118">For example, Internet Explorer might use multiple XAudio2 components simultaneously.</span></span> <span data-ttu-id="46555-119">Sebbene sia possibile creare più oggetti motore XAudio2 all'interno di una singola applicazione client, non è necessario passare informazioni tra i rispettivi grafici.</span><span class="sxs-lookup"><span data-stu-id="46555-119">Although it is possible to create multiple XAudio2 engine objects within a single client application, you should not pass information between their respective graphs.</span></span>

<span data-ttu-id="46555-120">Per un esempio di inizializzazione del motore XAudio2, vedere [procedura: inizializzare XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="46555-120">For an example of initializing the XAudio2 engine, see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>

## <a name="voices"></a><span data-ttu-id="46555-121">Voci</span><span class="sxs-lookup"><span data-stu-id="46555-121">Voices</span></span>

<span data-ttu-id="46555-122">Le voci sono gli oggetti utilizzati da XAudio2 per elaborare, modificare e riprodurre dati audio.</span><span class="sxs-lookup"><span data-stu-id="46555-122">Voices are the objects XAudio2 use to process, to manipulate, and to play audio data.</span></span> <span data-ttu-id="46555-123">In XAudio2 sono disponibili tre tipi di voci.</span><span class="sxs-lookup"><span data-stu-id="46555-123">There are three types of voices in XAudio2.</span></span>

-   [<span data-ttu-id="46555-124">**Voci di origine**</span><span class="sxs-lookup"><span data-stu-id="46555-124">**Source Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    <span data-ttu-id="46555-125">Le voci di origine rappresentano un flusso di dati audio.</span><span class="sxs-lookup"><span data-stu-id="46555-125">Source voices represent a stream of audio data.</span></span> <span data-ttu-id="46555-126">Le voci di origine inviano i dati ad altri tipi di voci.</span><span class="sxs-lookup"><span data-stu-id="46555-126">Source voices send their data to other types of voices.</span></span>

-   [<span data-ttu-id="46555-127">**Voci di submix**</span><span class="sxs-lookup"><span data-stu-id="46555-127">**Submix Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    <span data-ttu-id="46555-128">Le voci submix eseguono una manipolazione dei dati audio ricevuti.</span><span class="sxs-lookup"><span data-stu-id="46555-128">Submix voices perform some manipulation of audio data they receive.</span></span> <span data-ttu-id="46555-129">Un esempio di manipolazione dei dati audio potrebbe essere la conversione della frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="46555-129">One example of audio data manipulation might be sample rate conversion.</span></span> <span data-ttu-id="46555-130">Dopo che una voce submix elabora i dati, passa i dati a un'altra voce submix o a una voce Master.</span><span class="sxs-lookup"><span data-stu-id="46555-130">After a submix voice processes data, it passes that data to another submix voice or to a master voice.</span></span>

-   [<span data-ttu-id="46555-131">**Voci di mastering**</span><span class="sxs-lookup"><span data-stu-id="46555-131">**Mastering Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    <span data-ttu-id="46555-132">Le voci di mastering ricevono i dati dalle voci di origine e submix e inviano i dati all'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="46555-132">Mastering voices receive data from source voices and submix voices, and sends that data to the audio hardware.</span></span>

<span data-ttu-id="46555-133">Per una panoramica delle voci di XAudio2, vedere [XAudio2 Voices](voices.md) .</span><span class="sxs-lookup"><span data-stu-id="46555-133">See [XAudio2 Voices](voices.md) for an overview of XAudio2 voices.</span></span>

## <a name="audio-graph"></a><span data-ttu-id="46555-134">Grafico audio</span><span class="sxs-lookup"><span data-stu-id="46555-134">Audio Graph</span></span>

<span data-ttu-id="46555-135">Un grafico audio è una raccolta di voci XAudio2.</span><span class="sxs-lookup"><span data-stu-id="46555-135">An audio graph is a collection of XAudio2 voices.</span></span> <span data-ttu-id="46555-136">L'audio inizia da un lato di un grafico audio nelle voci di origine, passa facoltativamente da una o più voci submix e termina con una voce di master.</span><span class="sxs-lookup"><span data-stu-id="46555-136">Audio starts at one side of an audio graph in source voices, optionally passes through one or more submix voices, and ends at a mastering voice.</span></span> <span data-ttu-id="46555-137">Un grafico audio conterrà una voce di origine per ogni suono attualmente in riproduzione, zero o più voci submix e una voce Master.</span><span class="sxs-lookup"><span data-stu-id="46555-137">An audio graph will contain a source voice for each sound currently playing, zero or more submix voices, and one mastering voice.</span></span> <span data-ttu-id="46555-138">Il grafico audio più semplice e il minimo necessario per creare un rumore in XAudio2 sono una singola voce di origine che consente di ottenere direttamente una voce di master.</span><span class="sxs-lookup"><span data-stu-id="46555-138">The simplest audio graph, and the minimum needed to make a noise in XAudio2, is a single source voice outputting directly to a mastering voice.</span></span> <span data-ttu-id="46555-139">Vedere [procedura: riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md) per un esempio della procedura minima necessaria per riprodurre un suono con XAudio2.</span><span class="sxs-lookup"><span data-stu-id="46555-139">See [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md) for an example of the minimum steps need to play a sound with XAudio2.</span></span>

<span data-ttu-id="46555-140">Per una panoramica dei grafici audio di XAudio2, vedere [XAudio2 audio Graph](audio-graphs.md) .</span><span class="sxs-lookup"><span data-stu-id="46555-140">See [XAudio2 Audio Graph](audio-graphs.md) for an overview of XAudio2 audio graphs.</span></span>

## <a name="callbacks"></a><span data-ttu-id="46555-141">Callback</span><span class="sxs-lookup"><span data-stu-id="46555-141">Callbacks</span></span>

<span data-ttu-id="46555-142">I callback sono il meccanismo usato da XAudio2 per segnalare al codice client che si è verificato un evento in una voce o nell'oggetto motore.</span><span class="sxs-lookup"><span data-stu-id="46555-142">Callbacks are the mechanism XAudio2 uses to signal client code that some event has occurred in a voice or in the engine object.</span></span> <span data-ttu-id="46555-143">Poiché la riproduzione audio è asincrona nel motore XAudio2, i callback forniscono l'unico modo per determinare quando un suono termina la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="46555-143">Because audio playback is asynchronous in the XAudio2 engine, callbacks provide the only way to determine when a sound is finished playing.</span></span>

<span data-ttu-id="46555-144">Per una panoramica dei callback di XAudio2, vedere [callback di XAudio2](callbacks.md) .</span><span class="sxs-lookup"><span data-stu-id="46555-144">See [XAudio2 Callbacks](callbacks.md) for an overview of XAudio2 callbacks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46555-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46555-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46555-146">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="46555-146">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="46555-147">Versioni di XAudio2</span><span class="sxs-lookup"><span data-stu-id="46555-147">XAudio2 Versions</span></span>](xaudio2-versions.md)
</dt> <dt>

[<span data-ttu-id="46555-148">Procedura: Inizializzare XAudio2</span><span class="sxs-lookup"><span data-stu-id="46555-148">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="46555-149">Procedura: riprodurre un suono con XAudio2</span><span class="sxs-lookup"><span data-stu-id="46555-149">How to: Play a sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



