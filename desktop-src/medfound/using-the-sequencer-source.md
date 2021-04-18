---
description: In questo argomento viene descritto come utilizzare l'origine di Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Utilizzo dell'origine sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308984"
---
# <a name="using-the-sequencer-source"></a><span data-ttu-id="1dc82-103">Utilizzo dell'origine sequencer</span><span class="sxs-lookup"><span data-stu-id="1dc82-103">Using the Sequencer Source</span></span>

<span data-ttu-id="1dc82-104">In questo argomento viene descritto come utilizzare l' [origine di Sequencer](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="1dc82-104">This topic describes how to use the [Sequencer Source](sequencer-source.md).</span></span> <span data-ttu-id="1dc82-105">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1dc82-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="1dc82-106">Overview</span><span class="sxs-lookup"><span data-stu-id="1dc82-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="1dc82-107">Aggiunta di topologie</span><span class="sxs-lookup"><span data-stu-id="1dc82-107">Adding Topologies</span></span>](#adding-topologies)
-   [<span data-ttu-id="1dc82-108">Eliminazione di topologie</span><span class="sxs-lookup"><span data-stu-id="1dc82-108">Deleting Topologies</span></span>](#deleting-topologies)
-   [<span data-ttu-id="1dc82-109">Ignorare un segmento</span><span class="sxs-lookup"><span data-stu-id="1dc82-109">Skipping to a Segment</span></span>](#skipping-to-a-segment)
-   [<span data-ttu-id="1dc82-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dc82-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="1dc82-111">Per una panoramica generale dell'origine di Sequencer, vedere [informazioni sull'origine di Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="1dc82-111">For a general overview of the sequencer source, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

## <a name="overview"></a><span data-ttu-id="1dc82-112">Panoramica</span><span class="sxs-lookup"><span data-stu-id="1dc82-112">Overview</span></span>

<span data-ttu-id="1dc82-113">L'origine di Sequencer espone le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="1dc82-113">The sequencer source exposes the following interfaces.</span></span>



| <span data-ttu-id="1dc82-114">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="1dc82-114">Interface</span></span>                                                                        | <span data-ttu-id="1dc82-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dc82-115">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dc82-116">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="1dc82-116">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | <span data-ttu-id="1dc82-117">Espone la funzionalità generica di origine dei supporti.</span><span class="sxs-lookup"><span data-stu-id="1dc82-117">Exposes generic media source functionality.</span></span>                                        |
| [<span data-ttu-id="1dc82-118">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="1dc82-118">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | <span data-ttu-id="1dc82-119">Consente all'applicazione di aggiungere o rimuovere topologie.</span><span class="sxs-lookup"><span data-stu-id="1dc82-119">Enables the application to add or remove topologies.</span></span>                               |
| [<span data-ttu-id="1dc82-120">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="1dc82-120">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | <span data-ttu-id="1dc82-121">Recupera la topologia successiva da accodare nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="1dc82-121">Retrieves the next topology to queue on the Media Session.</span></span>                         |
| [<span data-ttu-id="1dc82-122">**IMFMediaSourcePresentationProvider**</span><span class="sxs-lookup"><span data-stu-id="1dc82-122">**IMFMediaSourcePresentationProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | <span data-ttu-id="1dc82-123">Usato dalla sessione multimediale per terminare i segmenti.</span><span class="sxs-lookup"><span data-stu-id="1dc82-123">Used by the Media Session to end segments.</span></span> <span data-ttu-id="1dc82-124">Le applicazioni non utilizzano questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1dc82-124">Applications do not use this interface.</span></span> |
| [<span data-ttu-id="1dc82-125">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="1dc82-125">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | <span data-ttu-id="1dc82-126">Esegue una query sull'origine del sequencer per le [interfacce del servizio](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="1dc82-126">Queries the sequencer source for [Service Interfaces](service-interfaces.md).</span></span>     |



 

<span data-ttu-id="1dc82-127">Per riprodurre una sequenza di origini multimediali, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="1dc82-127">To play a sequence of media sources, perform the following steps:</span></span>

1.  <span data-ttu-id="1dc82-128">Per creare l'origine del sequencer, chiamare la funzione [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-128">To create the sequencer source, call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function.</span></span>
2.  <span data-ttu-id="1dc82-129">Per ogni segmento, creare una topologia di riproduzione, come descritto in [creazione di topologie di riproduzione](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="1dc82-129">For each segment, create a playback topology, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span> <span data-ttu-id="1dc82-130">Per aggiungere la topologia alla presentazione, chiamare [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="1dc82-130">To add the topology to the presentation, call [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span>
3.  <span data-ttu-id="1dc82-131">Prima di avviare la riproduzione, chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="1dc82-131">Before starting playback, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the sequencer source.</span></span> <span data-ttu-id="1dc82-132">Questo metodo restituisce un puntatore a un descrittore di presentazione per il primo segmento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-132">This method returns a pointer to a presentation descriptor for the first segment.</span></span> <span data-ttu-id="1dc82-133">Per ottenere la topologia associata a questo segmento, chiamare **QueryInterface** sull'origine del sequencer per l'interfaccia [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-133">To get the topology associated with this segment, call **QueryInterface** on the sequencer source for the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface.</span></span> <span data-ttu-id="1dc82-134">Passare il descrittore della presentazione al metodo [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-134">Pass the presentation descriptor to the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="1dc82-135">Questo metodo restituisce un puntatore alla topologia.</span><span class="sxs-lookup"><span data-stu-id="1dc82-135">This method returns a pointer to the topology.</span></span>
4.  <span data-ttu-id="1dc82-136">Passare la topologia per il primo segmento alla sessione multimediale chiamando il metodo [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) SetValue della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="1dc82-136">Pass the topology for the first segment to the Media Session, by calling the Media Session's [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>
5.  <span data-ttu-id="1dc82-137">Avviare la riproduzione chiamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="1dc82-137">Start playback by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>
6.  <span data-ttu-id="1dc82-138">Quando l'origine del sequencer è pronta per la prerolling del segmento successivo, invia un evento [MENewPresentation](menewpresentation.md) i cui dati dell'evento sono un puntatore di interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-138">When the sequencer source is ready to preroll the next segment, it sends an [MENewPresentation](menewpresentation.md) event whose event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface pointer.</span></span> <span data-ttu-id="1dc82-139">Anche in questo caso, ottenere la topologia per il segmento chiamando [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) nell'origine del sequencer e impostare la topologia nella sessione multimediale chiamando [**la topologia.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)</span><span class="sxs-lookup"><span data-stu-id="1dc82-139">Again, get the topology for the segment by calling [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the sequencer source, and set the topology on the Media Session by calling [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="1dc82-140">Non è necessario riavviare l'origine multimediale; verrà automaticamente riprodotto fino al segmento successivo.</span><span class="sxs-lookup"><span data-stu-id="1dc82-140">It is not necessary to re-start the media source; it will automatically play through to the next segment.</span></span>
7.  <span data-ttu-id="1dc82-141">Prima di chiudere l'applicazione, arrestare l'origine del sequencer chiamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="1dc82-141">Before the application quits, shut down the sequencer source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>

<span data-ttu-id="1dc82-142">Nel codice seguente viene illustrato come ottenere la topologia e impostarla nella sessione multimediale:</span><span class="sxs-lookup"><span data-stu-id="1dc82-142">The following code shows how to get the topology and set it on the Media Session:</span></span>


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



<span data-ttu-id="1dc82-143">Per un esempio di codice completo, vedere [codice di esempio dell'origine sequencer](sequencer-source-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="1dc82-143">For a complete code example, see [Sequencer Source Example Code](sequencer-source-example-code.md).</span></span>

## <a name="adding-topologies"></a><span data-ttu-id="1dc82-144">Aggiunta di topologie</span><span class="sxs-lookup"><span data-stu-id="1dc82-144">Adding Topologies</span></span>

<span data-ttu-id="1dc82-145">L'origine di Sequencer gestisce due elenchi di topologie: l' *elenco di input* e l'elenco di *preroll*.</span><span class="sxs-lookup"><span data-stu-id="1dc82-145">The sequencer source maintains two lists of topologies: the *input list* and the *preroll list*.</span></span>

<span data-ttu-id="1dc82-146">L'elenco di input è una raccolta di topologie corrispondenti ai segmenti della playlist, nell'ordine in cui sono stati aggiunti dall'applicazione chiamando [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="1dc82-146">The input list is a collection of topologies corresponding to playlist segments, in the order that they were added by the application by calling [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span> <span data-ttu-id="1dc82-147">Questo metodo assegna a ogni topologia un *identificatore di segmento* univoco del tipo **MFSequencerElementId**.</span><span class="sxs-lookup"><span data-stu-id="1dc82-147">This method assigns each topology a unique *segment identifier* of the type **MFSequencerElementId**.</span></span> <span data-ttu-id="1dc82-148">L'identificatore di segmento viene impostato come attributo per tutti i nodi della topologia di origine.</span><span class="sxs-lookup"><span data-stu-id="1dc82-148">The segment identifier is set as an attribute for all source topology nodes.</span></span> <span data-ttu-id="1dc82-149">Un'applicazione può ottenere l'identificatore di segmento da un nodo di origine usando l'attributo [ \_ ElementID della \_ sequenza \_ MF TOPONODE](mf-toponode-sequence-elementid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-149">An application can get the segment identifier from a source node by using the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute.</span></span> <span data-ttu-id="1dc82-150">L'elenco di input può includere topologie duplicate se l'applicazione ha chiamato **AppendTopology** nella stessa topologia più di una volta. Tuttavia, vengono identificati da identificatori di segmenti univoci.</span><span class="sxs-lookup"><span data-stu-id="1dc82-150">The input list can have duplicate topologies if the application called **AppendTopology** on the same topology more than once; however, they are identified by their unique segment identifiers.</span></span>

<span data-ttu-id="1dc82-151">L'elenco preroll è una raccolta di topologie di elenco di input inizializzate in preparazione per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="1dc82-151">The preroll list is a collection of input list topologies that have been initialized in preparation for playback.</span></span> <span data-ttu-id="1dc82-152">In questo modo, la sessione multimediale passa alla topologia successiva facilmente al termine della topologia attiva.</span><span class="sxs-lookup"><span data-stu-id="1dc82-152">This enables the Media Session to transition to the next topology seamlessly when the active topology ends.</span></span> <span data-ttu-id="1dc82-153">L'applicazione non è in grado di aggiungere o rimuovere direttamente le topologie dall'elenco preroll; viene generato dall'origine del sequencer quando viene selezionata una topologia dall'elenco di input per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="1dc82-153">The application cannot directly add or remove topologies from the preroll list; it is generated by the sequencer source when a topology from the input list is selected for playback.</span></span> <span data-ttu-id="1dc82-154">In questo modo, l'origine del sequencer aggiungerà la topologia successiva dall'elenco di input all'elenco preroll.</span><span class="sxs-lookup"><span data-stu-id="1dc82-154">This causes the sequencer source to add the next topology from the input list to the preroll list.</span></span> <span data-ttu-id="1dc82-155">Dopo questa operazione, l'origine sequencer genera in modo asincrono l'evento [MENewPresentation](menewpresentation.md) e passa il descrittore di presentazione per la topologia di preroll come dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-155">After doing so, the sequencer source asynchronously raises the [MENewPresentation](menewpresentation.md) event and passes the presentation descriptor for the preroll topology as event data.</span></span> <span data-ttu-id="1dc82-156">L'applicazione deve restare in ascolto di questo evento usando l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) della sessione multimediale e accodare la topologia di preroll nella sessione multimediale chiamando [**IMFMediaSession:: la topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="1dc82-156">The application must listen for this event by using the Media Session's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface and queue the preroll topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="1dc82-157">Questa operazione deve essere eseguita prima che la sessione multimediale completi la riproduzione della topologia attiva.</span><span class="sxs-lookup"><span data-stu-id="1dc82-157">This must be done before the Media Session completes playback of the active topology.</span></span> <span data-ttu-id="1dc82-158">La **topologia** informa la sessione multimediale sulla successiva topologia che deve essere riprodotta al termine della riproduzione della topologia attiva.</span><span class="sxs-lookup"><span data-stu-id="1dc82-158">**SetTopology** informs the Media Session about the next topology that it must play after playback of the active topology has ended.</span></span> <span data-ttu-id="1dc82-159">Per garantire un treansition trasparente, l'applicazione deve chiamare la **topologia** prima che la sessione multimediale venga completata con la topologia precedente.</span><span class="sxs-lookup"><span data-stu-id="1dc82-159">To ensure a seamless treansition, the application must call **SetTopology** before the Media Session completes playing the previous topology.</span></span> <span data-ttu-id="1dc82-160">In caso contrario, si verifica un divario tra i segmenti.</span><span class="sxs-lookup"><span data-stu-id="1dc82-160">Otherwise, there will be a gap between the segments.</span></span>

<span data-ttu-id="1dc82-161">L'evento [MENewPresentation](menewpresentation.md) viene generato purché esista una topologia successiva alla topologia attiva.</span><span class="sxs-lookup"><span data-stu-id="1dc82-161">The [MENewPresentation](menewpresentation.md) event is raised as long as there is a topology following the active topology.</span></span> <span data-ttu-id="1dc82-162">Di conseguenza, se l'elenco di input contiene una sola topologia o se la topologia attiva è l'ultima nell'elenco di input, questo evento non viene generato.</span><span class="sxs-lookup"><span data-stu-id="1dc82-162">Consequently, if the input list contains only one topology, or if the active topology is the last one in the input list, this event is not raised.</span></span>

<span data-ttu-id="1dc82-163">L'elenco preroll viene sincronizzato con l'elenco di input e viene aggiornato ogni volta che viene aggiunta o eliminata una topologia dall'elenco di input.</span><span class="sxs-lookup"><span data-stu-id="1dc82-163">The preroll list is synchronized with the input list and is refreshed each time a topology is added to or deleted from the input list.</span></span>

## <a name="deleting-topologies"></a><span data-ttu-id="1dc82-164">Eliminazione di topologie</span><span class="sxs-lookup"><span data-stu-id="1dc82-164">Deleting Topologies</span></span>

<span data-ttu-id="1dc82-165">Per rimuovere una topologia dall'origine del sequencer, un'applicazione deve chiamare il metodo [**IMFSequencerSource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) e specificare l'identificatore del segmento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-165">To remove a topology from the sequencer source, an application must call the [**IMFSequencerSource::DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) method and specify the segment identifier.</span></span>

<span data-ttu-id="1dc82-166">Prima di chiamare [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), l'applicazione deve assicurarsi che la sessione multimediale non usi la topologia che l'applicazione vuole eliminare.</span><span class="sxs-lookup"><span data-stu-id="1dc82-166">Before calling [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), the application must make sure that Media Session is not using the topology that the application wants to delete.</span></span> <span data-ttu-id="1dc82-167">A tale scopo, prima che l'applicazione chiami **DeleteTopology**, è necessario che si verifichino entrambe le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1dc82-167">To do this, both of the following must occur before the application calls **DeleteTopology**:</span></span>

-   <span data-ttu-id="1dc82-168">[](mesessiontopologystatus.md) \_ \_ Per la topologia per garantire che la sessione multimediale abbia completato la riproduzione, viene ricevuto l'evento MESessionTopologyStatus con MF TOPOSTATUS terminato.</span><span class="sxs-lookup"><span data-stu-id="1dc82-168">[MESessionTopologyStatus](mesessiontopologystatus.md) event with MF\_TOPOSTATUS\_ENDED is received for the topology to ensure that Media Session has completed playback.</span></span>

-   <span data-ttu-id="1dc82-169">[MESessionTopologyStatus](mesessiontopologystatus.md) con MF \_ TOPOSTATUS \_ Started \_ source viene ricevuto per la topologia successiva per assicurarsi che la sessione multimediale abbia iniziato a riprodurre la topologia successiva, viene ricevuto l'evento [MESessionEnded](mesessionended.md) per assicurarsi che la sessione multimediale venga eseguita con l'ultima topologia nell'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="1dc82-169">[MESessionTopologyStatus](mesessiontopologystatus.md) with MF\_TOPOSTATUS\_STARTED\_SOURCE is received for the next topology to ensure that the Media Session has started playing the next topology, [MESessionEnded](mesessionended.md) event is received to ensure that Media Session is done with the last topology in the sequencer source.</span></span>

<span data-ttu-id="1dc82-170">Se il segmento da eliminare è la topologia attiva, la riproduzione viene arrestata e l'origine del sequencer genera l'evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-170">If the segment being deleted is the active topology, playback is stopped and the sequencer source raises the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span> <span data-ttu-id="1dc82-171">Se la topologia attiva è anche l'ultima topologia, viene generato l'evento [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-171">If the active topology is also the last topology, the [MEEndOfPresentation](meendofpresentation.md) event is raised.</span></span>

## <a name="skipping-to-a-segment"></a><span data-ttu-id="1dc82-172">Ignorare un segmento</span><span class="sxs-lookup"><span data-stu-id="1dc82-172">Skipping to a Segment</span></span>

<span data-ttu-id="1dc82-173">Un'applicazione può passare a un segmento specifico nella sequenza avviando la [sessione multimediale](media-session.md) con un offset del segmento, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="1dc82-173">An application can skip to a particular segment in the sequence by starting the [Media Session](media-session.md) with a segment offset, as follows:</span></span>

1.  <span data-ttu-id="1dc82-174">Chiamare la funzione [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) per creare l'offset del segmento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-174">Call the [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) function to create the segment offset.</span></span> <span data-ttu-id="1dc82-175">Specificare l'identificatore del segmento nel parametro *dwID* .</span><span class="sxs-lookup"><span data-stu-id="1dc82-175">Specify the identifier of the segment in the *dwId* parameter.</span></span> <span data-ttu-id="1dc82-176">(L'identificatore è stato restituito dal metodo [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) quando la topologia è stata aggiunta per la prima volta all'origine del sequencer). Il parametro *hnsOffset* specifica un offset temporale, relativo all'inizio del segmento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-176">(The identifier was returned by the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method when you first added the topology to the sequencer source.) The *hnsOffset* parameter specifies a time offset, relative to the start of the segment.</span></span> <span data-ttu-id="1dc82-177">La riproduzione verrà avviata in questo momento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-177">Playback will start at this time.</span></span> <span data-ttu-id="1dc82-178">Per il parametro *pvarSegmentOffset* , passare l'indirizzo di un **PROPVARIANT** vuoto.</span><span class="sxs-lookup"><span data-stu-id="1dc82-178">For the *pvarSegmentOffset* parameter, pass in the address of an empty **PROPVARIANT**.</span></span> <span data-ttu-id="1dc82-179">Quando la funzione restituisce, questo **PROPVARIANT** contiene l'offset del segmento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-179">When the function returns, this **PROPVARIANT** contains the segment offset.</span></span>

2.  <span data-ttu-id="1dc82-180">Chiamare il metodo [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="1dc82-180">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method on the Media Session.</span></span> <span data-ttu-id="1dc82-181">Per il parametro *pguidTimeFormat* , usare l'offset del segmento di formato dell'ora MF valore GUID \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1dc82-181">For the *pguidTimeFormat* parameter, use the GUID value MF\_TIME\_FORMAT\_SEGMENT\_OFFSET.</span></span> <span data-ttu-id="1dc82-182">Questo valore indica la ricerca in base all'offset del segmento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-182">This value indicates seeking by segment offset.</span></span> <span data-ttu-id="1dc82-183">Per il parametro *pvarStartPosition* , passare l'indirizzo del **PROPVARIANT** creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="1dc82-183">For the *pvarStartPosition* parameter, pass the address of the **PROPVARIANT** created in the previous step.</span></span>

<span data-ttu-id="1dc82-184">Nell'esempio di codice seguente viene illustrato come passare all'inizio di un segmento specificato in una sequenza.</span><span class="sxs-lookup"><span data-stu-id="1dc82-184">The following code example shows how to skip to the start of a specified segment in a sequence.</span></span>


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="1dc82-185">Quando l'applicazione esegue la ricerca tra segmenti, l'applicazione riceve diversi eventi quando l'origine del sequencer termina il segmento corrente e prepara la riproduzione del nuovo segmento.</span><span class="sxs-lookup"><span data-stu-id="1dc82-185">When the application seeks across segments, the application receives several events as the sequencer source ends the current segment and prepares to play the new segment.</span></span> <span data-ttu-id="1dc82-186">Poiché questi eventi vengono ricevuti in modo asincrono, è difficile prevedere la sequenza esatta di eventi.</span><span class="sxs-lookup"><span data-stu-id="1dc82-186">Because these events are received asynchronously, it is difficult to predict the exact sequence of events.</span></span> <span data-ttu-id="1dc82-187">Questi eventi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1dc82-187">These events are as follows:</span></span>

-   <span data-ttu-id="1dc82-188">L'origine di Sequencer Invia un evento [MENewPresentation](menewpresentation.md) per il nuovo segmento a cui è stata ignorata la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="1dc82-188">The sequencer source sends an [MENewPresentation](menewpresentation.md) event for the new segment to which the Media Session is skipping.</span></span>

-   <span data-ttu-id="1dc82-189">Quando l'origine del sequencer termina il segmento attivo, invia l'evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-189">When the sequencer source ends the active segment, it sends the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span>
-   <span data-ttu-id="1dc82-190">L'origine del sequencer Annulla quindi la topologia di preroll.</span><span class="sxs-lookup"><span data-stu-id="1dc82-190">The sequencer source then cancels the preroll topology.</span></span> <span data-ttu-id="1dc82-191">Ciò comporta gli eventi seguenti per la topologia annullata:</span><span class="sxs-lookup"><span data-stu-id="1dc82-191">This results in the following events for the canceled topology:</span></span>

    -   <span data-ttu-id="1dc82-192">Evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag MF TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="1dc82-192">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span>
    -   <span data-ttu-id="1dc82-193">Evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il flag di origine con MF \_ TOPOSTATUS \_ avviato \_ .</span><span class="sxs-lookup"><span data-stu-id="1dc82-193">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_STARTED\_SOURCE flag.</span></span>
    -   <span data-ttu-id="1dc82-194">Evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) con l'attributo della [ \_ \_ topologia di origine eventi \_ \_ MF](mf-event-source-topology-canceled-attribute.md) per indicare che la topologia è stata annullata dall'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="1dc82-194">[MEEndOfPresentationSegment](meendofpresentationsegment.md) event with the [MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED](mf-event-source-topology-canceled-attribute.md) attribute to indicate that the topology was canceled by the sequencer source.</span></span>

-   <span data-ttu-id="1dc82-195">L'origine di Sequencer invia quindi gli eventi per il nuovo segmento, inclusi i vari eventi [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc82-195">Next, the sequencer source sends events for the new segment, including various [MESessionTopologyStatus](mesessiontopologystatus.md) events.</span></span>
-   <span data-ttu-id="1dc82-196">Se il nuovo segmento non è l'ultimo nell'elenco, l'origine del sequencer aggiorna l'elenco di preroll e genera un altro [MENewPresentation](menewpresentation.md) per la nuova topologia di preroll.</span><span class="sxs-lookup"><span data-stu-id="1dc82-196">If the new segment is not the last on the list, the sequencer source refreshes the preroll list and raises another [MENewPresentation](menewpresentation.md) for the new preroll topology.</span></span> <span data-ttu-id="1dc82-197">Per informazioni sulle topologie nell'elenco preroll, vedere [informazioni sull'origine del sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="1dc82-197">For information about topologies in the preroll list, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="1dc82-198">Per ulteriori informazioni sugli eventi inviati dall'origine sequencer, vedere l'argomento relativo [agli eventi di origine di Sequencer](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="1dc82-198">More details about the events sent by the sequencer source can be found in the topic [Sequencer Source Events](sequencer-source-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dc82-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dc82-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc82-200">Come creare una playlist</span><span class="sxs-lookup"><span data-stu-id="1dc82-200">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="1dc82-201">Origine sequencer</span><span class="sxs-lookup"><span data-stu-id="1dc82-201">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



