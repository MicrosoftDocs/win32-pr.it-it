---
description: In questo argomento viene descritto come utilizzare l'origine sequenza per riprodurre una sequenza di file.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Come creare una playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527690"
---
# <a name="how-to-create-a-playlist"></a><span data-ttu-id="b61cf-103">Come creare una playlist</span><span class="sxs-lookup"><span data-stu-id="b61cf-103">How to Create a Playlist</span></span>

<span data-ttu-id="b61cf-104">In questo argomento viene descritto come utilizzare l'origine sequenza per riprodurre una sequenza di file.</span><span class="sxs-lookup"><span data-stu-id="b61cf-104">This topic describes how to use the Sequence Source to play a sequence of files.</span></span>

## <a name="overview"></a><span data-ttu-id="b61cf-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="b61cf-105">Overview</span></span>

<span data-ttu-id="b61cf-106">Per riprodurre file multimediali in una sequenza, l'applicazione deve aggiungere topologie in una sequenza per creare una playlist e accodare tali topologie nella sessione multimediale per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b61cf-106">To play media files in a sequence, the application must add topologies in a sequence to create a playlist, and queue these topologies on the Media Session for playback.</span></span>

<span data-ttu-id="b61cf-107">L'origine di Sequencer garantisce una riproduzione uniforme inizializzando e caricando la topologia successiva prima che la sessione multimediale inizi a riprodurre la topologia corrente.</span><span class="sxs-lookup"><span data-stu-id="b61cf-107">The sequencer source ensures seamless playback by initializing and loading the next topology before the Media Session starts playing the current topology.</span></span> <span data-ttu-id="b61cf-108">Ciò consente all'applicazione di avviare rapidamente la topologia successiva ogni volta che è necessario.</span><span class="sxs-lookup"><span data-stu-id="b61cf-108">This enables the application to start the next topology quickly whenever it is required.</span></span>

<span data-ttu-id="b61cf-109">La sessione multimediale è responsabile dell'inserimento dei dati nei sink e della riproduzione delle topologie nell'origine della sequenza.</span><span class="sxs-lookup"><span data-stu-id="b61cf-109">The Media Session is responsible for feeding data to the sinks and playing the topologies in the sequence source.</span></span> <span data-ttu-id="b61cf-110">Inoltre, la sessione multimediale gestisce l'ora di presentazione per i segmenti.</span><span class="sxs-lookup"><span data-stu-id="b61cf-110">In addition, the Media Session manages the presentation time for the segments.</span></span>

<span data-ttu-id="b61cf-111">Per ulteriori informazioni sul modo in cui l'origine di Sequencer gestisce le topologie, vedere [informazioni sull'origine di Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="b61cf-111">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="b61cf-112">Questa procedura dettagliata include i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b61cf-112">This walk-through contains the following steps:</span></span>

1.  [<span data-ttu-id="b61cf-113">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="b61cf-113">Prerequisites</span></span>](#prerequisites)
2.  [<span data-ttu-id="b61cf-114">Inizializzazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b61cf-114">Initializing Media Foundation</span></span>](#initializing-media-foundation)
3.  [<span data-ttu-id="b61cf-115">Creazione di oggetti Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b61cf-115">Creating Media Foundation Objects</span></span>](#creating-media-foundation-objects)
4.  [<span data-ttu-id="b61cf-116">Creazione dell'origine supporto</span><span class="sxs-lookup"><span data-stu-id="b61cf-116">Creating the Media Source</span></span>](#creating-the-media-source)
5.  [<span data-ttu-id="b61cf-117">Creazione di topologie parziali</span><span class="sxs-lookup"><span data-stu-id="b61cf-117">Creating Partial Topologies</span></span>](#creating-partial-topologies)
6.  [<span data-ttu-id="b61cf-118">Aggiunta di topologie all'origine del sequencer</span><span class="sxs-lookup"><span data-stu-id="b61cf-118">Adding Topologies to the Sequencer Source</span></span>](#adding-topologies-to-the-sequencer-source)
7.  [<span data-ttu-id="b61cf-119">Impostazione della prima topologia nella sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="b61cf-119">Setting the First Topology on the Media Session</span></span>](#setting-the-first-topology-on-the-media-session)
8.  [<span data-ttu-id="b61cf-120">Accodamento della topologia successiva nella sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="b61cf-120">Queuing the Next Topology on the Media Session</span></span>](#queuing-the-next-topology-on-the-media-session)
9.  [<span data-ttu-id="b61cf-121">Rilascio dell'origine del sequencer</span><span class="sxs-lookup"><span data-stu-id="b61cf-121">Releasing the Sequencer Source</span></span>](#releasing-the-sequencer-source)

<span data-ttu-id="b61cf-122">Gli esempi di codice illustrati in questo argomento sono estratti dall'argomento [codice di esempio dell'origine sequencer](sequencer-source-example-code.md), che contiene il codice di esempio completo.</span><span class="sxs-lookup"><span data-stu-id="b61cf-122">The code examples shown this topic are excerpts from the topic [Sequencer Source Example Code](sequencer-source-example-code.md), which contains the complete example code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b61cf-123">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="b61cf-123">Prerequisites</span></span>

<span data-ttu-id="b61cf-124">Prima di iniziare questa procedura dettagliata, acquisire familiarità con i concetti Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="b61cf-124">Before starting this walk-through, familiarize yourself with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="b61cf-125">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="b61cf-125">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="b61cf-126">Topologie</span><span class="sxs-lookup"><span data-stu-id="b61cf-126">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="b61cf-127">Generatori di eventi multimediali</span><span class="sxs-lookup"><span data-stu-id="b61cf-127">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="b61cf-128">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="b61cf-128">Presentation Descriptors</span></span>](presentation-descriptors.md)

<span data-ttu-id="b61cf-129">Vedere anche [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md), perché il codice di esempio shwon qui si espande sul codice in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="b61cf-129">Also read [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), because the example code shwon here expands on the code in that topic.</span></span>

## <a name="initializing-media-foundation"></a><span data-ttu-id="b61cf-130">Inizializzazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b61cf-130">Initializing Media Foundation</span></span>

<span data-ttu-id="b61cf-131">Prima di poter usare qualsiasi interfaccia o metodo di Media Foundation, inizializzare Media Foundation chiamando la funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-131">Before you can use any Media Foundation interfaces or methods, initialize Media Foundation by calling the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="b61cf-132">Per ulteriori informazioni, vedere [inizializzazione di Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="b61cf-132">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a><span data-ttu-id="b61cf-133">Creazione di oggetti Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b61cf-133">Creating Media Foundation Objects</span></span>

<span data-ttu-id="b61cf-134">Successivamente, creare gli oggetti Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="b61cf-134">Next, create the following Media Foundation objects:</span></span>

-   <span data-ttu-id="b61cf-135">Sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-135">Media session.</span></span> <span data-ttu-id="b61cf-136">Questo oggetto espone l'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , che fornisce i metodi per riprodurre, sospendere e arrestare la topologia corrente.</span><span class="sxs-lookup"><span data-stu-id="b61cf-136">This object exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface, which provides methods to play, pause, and stop the current topology.</span></span>
-   <span data-ttu-id="b61cf-137">Origine Sequencer.</span><span class="sxs-lookup"><span data-stu-id="b61cf-137">Sequencer source.</span></span> <span data-ttu-id="b61cf-138">Questo oggetto espone l'interfaccia [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , che fornisce metodi per l'aggiunta, l'aggiornamento e l'eliminazione di topologie in una sequenza.</span><span class="sxs-lookup"><span data-stu-id="b61cf-138">This object exposes the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface, which provides methods to add, update, and delete topologies in a sequence.</span></span>

1.  <span data-ttu-id="b61cf-139">Chiamare la funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-139">Call the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function to create the Media Session.</span></span>
2.  <span data-ttu-id="b61cf-140">Chiamare [**IMFMediaEventQueue:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) per richiedere il primo evento dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-140">Call [**IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) to request the first event from the Media Session.</span></span>
3.  <span data-ttu-id="b61cf-141">Chiamare la funzione [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) per creare l'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="b61cf-141">Call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function to create the sequencer source.</span></span>

<span data-ttu-id="b61cf-142">Il codice seguente crea la sessione multimediale e richiede il primo evento:</span><span class="sxs-lookup"><span data-stu-id="b61cf-142">The following code creates the Media Session and requests the first event:</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a><span data-ttu-id="b61cf-143">Creazione dell'origine supporto</span><span class="sxs-lookup"><span data-stu-id="b61cf-143">Creating the Media Source</span></span>

<span data-ttu-id="b61cf-144">Successivamente, creare un'origine multimediale per il primo segmento della playlist.</span><span class="sxs-lookup"><span data-stu-id="b61cf-144">Next, create a media source for the first playlist segment.</span></span> <span data-ttu-id="b61cf-145">Usare il [resolver di origine](source-resolver.md) per creare un'origine multimediale da un URL.</span><span class="sxs-lookup"><span data-stu-id="b61cf-145">Use the [Source Resolver](source-resolver.md) to create a media source from a URL.</span></span> <span data-ttu-id="b61cf-146">A tale scopo, chiamare la funzione [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) per creare un resolver di origine e quindi chiamare il metodo [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) per creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-146">To do this, call the [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) function to create a source resolver and then call the [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method to create the media source.</span></span>

<span data-ttu-id="b61cf-147">Per informazioni sulle origini multimediali, vedere [origini multimediali](media-sources.md).</span><span class="sxs-lookup"><span data-stu-id="b61cf-147">For information about media sources, see [Media Sources](media-sources.md).</span></span>

## <a name="creating-partial-topologies"></a><span data-ttu-id="b61cf-148">Creazione di topologie parziali</span><span class="sxs-lookup"><span data-stu-id="b61cf-148">Creating Partial Topologies</span></span>

<span data-ttu-id="b61cf-149">Ogni segmento nell'origine del sequencer ha una propria topologia parziale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-149">Each segment in the sequencer source has its own partial topology.</span></span> <span data-ttu-id="b61cf-150">Successivamente, creare topologie parziali per le origini multimediali.</span><span class="sxs-lookup"><span data-stu-id="b61cf-150">Next, create partial topologies for media sources.</span></span> <span data-ttu-id="b61cf-151">Per una topologia parziale, i nodi di origine della topologia sono connessi direttamente ai nodi di output, senza specificare alcuna trasformazione intermedia.</span><span class="sxs-lookup"><span data-stu-id="b61cf-151">For a partial topology, the topology source nodes are connected directly to the output nodes, without specifying any intermediate transforms.</span></span> <span data-ttu-id="b61cf-152">La sessione multimediale usa l'oggetto caricatore della topologia per risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="b61cf-152">The Media Session uses the topology loader object to resolve the topology.</span></span> <span data-ttu-id="b61cf-153">Dopo la risoluzione di una topologia, vengono aggiunti i decodificatori e altri nodi di trasformazione richiesti.</span><span class="sxs-lookup"><span data-stu-id="b61cf-153">After a topology is resolved, the required decoders and other transform nodes are added.</span></span> <span data-ttu-id="b61cf-154">L'origine del sequencer può inoltre contenere topologie complete.</span><span class="sxs-lookup"><span data-stu-id="b61cf-154">The sequencer source can also contain full topologies.</span></span>

<span data-ttu-id="b61cf-155">Per creare l'oggetto topologia, usare la funzione [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) e quindi usare l'interfaccia [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) per creare nodi di flusso.</span><span class="sxs-lookup"><span data-stu-id="b61cf-155">To create the topology object, use the [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) function and then use the [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface to create stream nodes.</span></span>

<span data-ttu-id="b61cf-156">Per istruzioni dettagliate sull'utilizzo di questi elementi di programmazione per la creazione di topologie, vedere [creazione di topologie di riproduzione](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="b61cf-156">For complete instructions on using these programming elements to create topologies, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="b61cf-157">Un'applicazione può riprodurre una parte selezionata dell'origine nativa configurando il nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="b61cf-157">An application can play a selected portion of the native source by configuring the source node.</span></span> <span data-ttu-id="b61cf-158">A tale scopo, impostare l'attributo [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) e l'attributo [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) nei nodi della topologia del **\_ \_ \_ nodo della topologia MF SOURCESTREAM** .</span><span class="sxs-lookup"><span data-stu-id="b61cf-158">To do this, set the [**MF\_TOPONODE\_MEDIASTART**](mf-toponode-mediastart-attribute.md) attribute and the [**MF\_TOPONODE\_MEDIASTOP**](mf-toponode-mediastop-attribute.md) attribute on **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** topology nodes.</span></span> <span data-ttu-id="b61cf-159">Specificare l'ora di inizio del supporto e l'ora di fine del supporto relativa all'inizio dell'origine nativa come tipi **UInt64** .</span><span class="sxs-lookup"><span data-stu-id="b61cf-159">Specify the media start time and the media stop time relative to the start of the native source as **UINT64** types.</span></span>

## <a name="adding-topologies-to-the-sequencer-source"></a><span data-ttu-id="b61cf-160">Aggiunta di topologie all'origine del sequencer</span><span class="sxs-lookup"><span data-stu-id="b61cf-160">Adding Topologies to the Sequencer Source</span></span>

<span data-ttu-id="b61cf-161">Successivamente, aggiungere all'origine sequencer le topologie parziali create.</span><span class="sxs-lookup"><span data-stu-id="b61cf-161">Next, add to the sequencer source the partial topologies that you created.</span></span> <span data-ttu-id="b61cf-162">A ogni elemento Sequence, denominato *segmento*, viene assegnato un identificatore **MFSequencerElementId** .</span><span class="sxs-lookup"><span data-stu-id="b61cf-162">Each sequence element, called a *segment*, is assigned an **MFSequencerElementId** identifier.</span></span> <span data-ttu-id="b61cf-163">Per ulteriori informazioni sul modo in cui l'origine di Sequencer gestisce le topologie, vedere [informazioni sull'origine di Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="b61cf-163">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="b61cf-164">Dopo che tutte le topologie sono state aggiunte all'origine sequencer, l'applicazione deve contrassegnare l'ultimo segmento nella sequenza per terminare la riproduzione nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="b61cf-164">After all of the topologies are added to the sequencer source, the application must flag the last segment in the sequence to end playback in the pipeline.</span></span> <span data-ttu-id="b61cf-165">Senza questo flag, l'origine del sequencer prevede l'aggiunta di più topologie.</span><span class="sxs-lookup"><span data-stu-id="b61cf-165">Without this flag, the sequencer source expects more topologies to be added.</span></span>

1.  <span data-ttu-id="b61cf-166">Chiamare il metodo [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) per aggiungere una topologia specifica all'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="b61cf-166">Call the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method to add a specific topology to the sequencer source.</span></span>

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    <span data-ttu-id="b61cf-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) aggiunge la topologia specificata alla sequenza.</span><span class="sxs-lookup"><span data-stu-id="b61cf-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adds the specified topology to the sequence.</span></span> <span data-ttu-id="b61cf-168">Questo metodo restituisce l'identificatore del segmento nel parametro *pdwId* .</span><span class="sxs-lookup"><span data-stu-id="b61cf-168">This method returns the segment identifier in the *pdwId* parameter.</span></span>

    <span data-ttu-id="b61cf-169">Se la topologia è l'ultima nell'origine del sequencer, passare SequencerTopologyFlags \_ Last nel parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="b61cf-169">If the topology is the last one in the sequencer source, pass SequencerTopologyFlags\_Last in the *dwFlags* parameter.</span></span> <span data-ttu-id="b61cf-170">Questo valore è definito nell'enumerazione [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-170">This value is defined in the [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) enumeration.</span></span>

2.  <span data-ttu-id="b61cf-171">Chiamare [**IMFSequencerSource:: UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) per aggiornare i flag per la topologia associata all'identificatore di segmento nell'elenco di input.</span><span class="sxs-lookup"><span data-stu-id="b61cf-171">Call [**IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) to update the flags for the topology associated with the segment identifier in the input list.</span></span> <span data-ttu-id="b61cf-172">In questo caso, la chiamata indica che il segmento specificato è l'ultimo segmento del sequencer.</span><span class="sxs-lookup"><span data-stu-id="b61cf-172">In this case, the call indicates that the specified segment is the last segment in the sequencer.</span></span> <span data-ttu-id="b61cf-173">Questa chiamata è facoltativa se l'ultima topologia è specificata nella chiamata [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-173">(This call is optional if the last topology is specified in the [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) call.)</span></span>

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

<span data-ttu-id="b61cf-174">L'applicazione può sostituire la topologia di un segmento con un'altra topologia chiamando [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) e passando la nuova topologia in *pTopology*.</span><span class="sxs-lookup"><span data-stu-id="b61cf-174">The application can replace a segment's topology with another topology by calling the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) and passing the new topology in *pTopology*.</span></span> <span data-ttu-id="b61cf-175">Se sono presenti nuove origini native nella nuova topologia, le origini vengono aggiunte alla cache di origine.</span><span class="sxs-lookup"><span data-stu-id="b61cf-175">If there are new native sources in the new topology, the sources are added to the source cache.</span></span> <span data-ttu-id="b61cf-176">Viene aggiornato anche l'elenco di preroll.</span><span class="sxs-lookup"><span data-stu-id="b61cf-176">The preroll list is also refreshed.</span></span>

## <a name="setting-the-first-topology-on-the-media-session"></a><span data-ttu-id="b61cf-177">Impostazione della prima topologia nella sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="b61cf-177">Setting the First Topology on the Media Session</span></span>

<span data-ttu-id="b61cf-178">Accodare quindi la prima topologia nell'origine della sequenza nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-178">Next, queue the first topology in the sequence source on the Media Session.</span></span> <span data-ttu-id="b61cf-179">Per ottenere la prima topologia dall'origine del sequencer, l'applicazione deve chiamare il metodo [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-179">To get the first topology from the sequencer source, the application must call the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="b61cf-180">Questo metodo restituisce la topologia parziale, che viene risolta dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-180">This method returns the partial topology, which is resolved by the Media Session.</span></span>

<span data-ttu-id="b61cf-181">Per informazioni sulle topologie parziali, vedere [informazioni sulle topologie](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="b61cf-181">For information about partial topologies, see [About Topologies](about-topologies.md).</span></span>

1.  <span data-ttu-id="b61cf-182">Recuperare l'origine multimediale nativa per la prima topologia dell'origine della sequenza.</span><span class="sxs-lookup"><span data-stu-id="b61cf-182">Retrieve the native media source for the first topology of the sequence source.</span></span>
2.  <span data-ttu-id="b61cf-183">Creare un descrittore di presentazione per l'origine multimediale chiamando il metodo [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-183">Create a presentation descriptor for the media source by calling the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>
3.  <span data-ttu-id="b61cf-184">Recuperare la topologia associata per la presentazione chiamando il metodo [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-184">Retrieve the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
4.  <span data-ttu-id="b61cf-185">Impostare la prima topologia nella sessione multimediale chiamando [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="b61cf-185">Set the first topology on the Media Session by Calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

    <span data-ttu-id="b61cf-186">Chiamare la [**topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con il parametro *DwSetTopologyFlags* impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="b61cf-186">Call [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the *dwSetTopologyFlags* parameter set to **NULL**.</span></span> <span data-ttu-id="b61cf-187">Indica alla sessione multimediale di avviare la topologia specificata quando la topologia corrente è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b61cf-187">This instructs the Media Session to start the specified topology when the current topology has been completed.</span></span> <span data-ttu-id="b61cf-188">Poiché in questo caso, la topologia specificata è la prima topologia e non è presente alcuna presentazione corrente, la sessione multimediale avvia immediatamente la nuova presentazione.</span><span class="sxs-lookup"><span data-stu-id="b61cf-188">Because in this case, the specified topology is the first topology and there is no current presentation, the Media Session starts the new presentation immediately.</span></span>

    <span data-ttu-id="b61cf-189">Il valore **null** indica anche che la sessione multimediale deve risolvere la topologia perché la topologia restituita dal provider di topologia è sempre una topologia parziale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-189">The **NULL** value also indicates that Media Session must resolve the topology because the topology returned by the topology provider is always a partial topology.</span></span>


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



## <a name="queuing-the-next-topology-on-the-media-session"></a><span data-ttu-id="b61cf-190">Accodamento della topologia successiva nella sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="b61cf-190">Queuing the Next Topology on the Media Session</span></span>

<span data-ttu-id="b61cf-191">Successivamente, l'applicazione deve gestire l'evento [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-191">Next, the application needs to handle the [MENewPresentation](menewpresentation.md) event.</span></span>

<span data-ttu-id="b61cf-192">L'origine di sequencer genera [MENewPresentation](menewpresentation.md) quando la sessione multimediale inizia a riprodurre un segmento con un altro segmento che lo segue.</span><span class="sxs-lookup"><span data-stu-id="b61cf-192">Sequencer source raises [MENewPresentation](menewpresentation.md) when the Media Session starts playing a segment that has another segment following it.</span></span> <span data-ttu-id="b61cf-193">Questo evento informa l'applicazione della successiva topologia nell'origine della sequenza fornendo il descrittore di presentazione per il segmento successivo nell'elenco di preroll.</span><span class="sxs-lookup"><span data-stu-id="b61cf-193">This event informs the application about the next topology in the sequence source by providing the presentation descriptor for the next segment in the preroll list.</span></span> <span data-ttu-id="b61cf-194">L'applicazione deve recuperare la topologia associata, usando il provider di topologia e accodarla nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-194">The application must retrieve the associated topology, by using the topology provider, and queue it on the Media Session.</span></span> <span data-ttu-id="b61cf-195">L'origine di Sequencer esegue quindi la preregistrazione di questa topologia, che garantisce una transizione senza problemi tra le presentazioni.</span><span class="sxs-lookup"><span data-stu-id="b61cf-195">The sequencer source then prerolls this topology, which ensures a seamless transition between presentations.</span></span>

<span data-ttu-id="b61cf-196">Quando l'applicazione esegue la ricerca in più segmenti, l'applicazione riceve diversi eventi [MENewPresentation](menewpresentation.md) poiché l'origine del sequencer aggiorna l'elenco di preroll e imposta la topologia corretta.</span><span class="sxs-lookup"><span data-stu-id="b61cf-196">When the application seeks across segments, the application receives several [MENewPresentation](menewpresentation.md) events as the sequencer source refreshes the preroll list and sets up the correct topology.</span></span> <span data-ttu-id="b61cf-197">L'applicazione deve gestire ogni evento e accodare la topologia restituita nei dati dell'evento, nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="b61cf-197">The application must handle each event and queue the topology returned in the event data, on the Media Session.</span></span> <span data-ttu-id="b61cf-198">Per informazioni sull'omissione dei segmenti, vedere [uso dell'origine di Sequencer](using-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="b61cf-198">For information about skipping segments, see [Using the Sequencer Source](using-the-sequencer-source.md).</span></span>

<span data-ttu-id="b61cf-199">Per informazioni su come ottenere le notifiche di origine di Sequencer, vedere [eventi di origine di Sequencer](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="b61cf-199">For information about getting sequencer source notifications, see [Sequencer Source Events](sequencer-source-events.md).</span></span>

1.  <span data-ttu-id="b61cf-200">Nel gestore dell'evento [MENewPresentation](menewpresentation.md) recuperare il descrittore di presentazione per il segmento successivo dai dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b61cf-200">In the [MENewPresentation](menewpresentation.md) event handler, retrieve the presentation descriptor for the next segment from the event data.</span></span>
2.  <span data-ttu-id="b61cf-201">Ottenere la topologia associata per la presentazione chiamando il metodo [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-201">Get the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
3.  <span data-ttu-id="b61cf-202">Impostare la topologia nella sessione multimediale chiamando il metodo [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) SetValue.</span><span class="sxs-lookup"><span data-stu-id="b61cf-202">Set the topology on the Media Session by calling the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>

    <span data-ttu-id="b61cf-203">La sessione multimediale avvia la nuova presentazione quando la presentazione corrente è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b61cf-203">The Media Session starts the new presentation when the current presentation has been completed.</span></span>


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a><span data-ttu-id="b61cf-204">Rilascio dell'origine del sequencer</span><span class="sxs-lookup"><span data-stu-id="b61cf-204">Releasing the Sequencer Source</span></span>

<span data-ttu-id="b61cf-205">Arrestare infine l'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="b61cf-205">Finally, shut down the sequencer source.</span></span> <span data-ttu-id="b61cf-206">A tale scopo, chiamare il metodo [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="b61cf-206">To do so, call the [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) method on the sequencer source.</span></span> <span data-ttu-id="b61cf-207">Questa chiamata arresta tutte le origini multimediali native sottostanti nell'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="b61cf-207">This call shuts down all of the underlying native media sources in the sequencer source.</span></span>

<span data-ttu-id="b61cf-208">Dopo il rilascio dell'origine del sequencer, l'applicazione deve chiudere e arrestare la sessione multimediale chiamando [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) e [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="b61cf-208">After releasing the sequencer source, the application should close and shut down the Media Session by calling [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) and [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in that order.</span></span>

<span data-ttu-id="b61cf-209">Per evitare perdite di memoria, l'applicazione deve rilasciare i puntatori alle interfacce Media Foundation quando non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="b61cf-209">To avoid memory leaks, the application must release pointers to Media Foundation interfaces when they are no longer needed.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b61cf-210">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="b61cf-210">Next Steps</span></span>

<span data-ttu-id="b61cf-211">Questa procedura dettagliata illustra come creare una playlist di base usando l'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="b61cf-211">This walk-through illustrated how to create a basic playlist by using the sequencer source.</span></span> <span data-ttu-id="b61cf-212">Dopo aver creato la playlist, potrebbe essere necessario aggiungere funzionalità avanzate, ad esempio l'omissione del segmento, la modifica dello stato di riproduzione e la ricerca all'interno di un segmento.</span><span class="sxs-lookup"><span data-stu-id="b61cf-212">After creating the playlist, you might want to add advanced features such as segment skipping, changing the playback state, and seeking within a segment.</span></span> <span data-ttu-id="b61cf-213">L'elenco seguente contiene i collegamenti agli argomenti correlati:</span><span class="sxs-lookup"><span data-stu-id="b61cf-213">The following list provides links to the related topics:</span></span>

-   <span data-ttu-id="b61cf-214">[Come controllare gli Stati di presentazione](how-to-control-presentation-states.md): l'origine di Sequencer si basa sulla sessione multimediale per fornire il controllo del trasporto, ad esempio riproduzione, pausa e arresto.</span><span class="sxs-lookup"><span data-stu-id="b61cf-214">[How to Control Presentation States](how-to-control-presentation-states.md): The sequencer source relies on the Media Session to provide transport control such as, Play, Pause, and Stop.</span></span>
-   <span data-ttu-id="b61cf-215">[Come eseguire lo scrubbing,](how-to-perform-scrubbing.md) descrive i passaggi necessari per cercare una posizione specifica in un flusso.</span><span class="sxs-lookup"><span data-stu-id="b61cf-215">[How to Perform Scrubbing](how-to-perform-scrubbing.md) describes the steps required to seek to a specific position in a stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b61cf-216">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b61cf-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b61cf-217">Origine sequencer</span><span class="sxs-lookup"><span data-stu-id="b61cf-217">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



