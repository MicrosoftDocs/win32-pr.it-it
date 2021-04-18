---
description: Questa esercitazione illustra come riprodurre file multimediali usando l'oggetto della sessione multimediale.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Come riprodurre file multimediali con Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104561899"
---
# <a name="how-to-play-media-files-with-media-foundation"></a><span data-ttu-id="2063f-103">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2063f-103">How to Play Media Files with Media Foundation</span></span>

<span data-ttu-id="2063f-104">Questa esercitazione illustra come riprodurre file multimediali usando l'oggetto della [sessione multimediale](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="2063f-104">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2063f-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="2063f-105">Prerequisites</span></span>

<span data-ttu-id="2063f-106">Prima di leggere questo argomento, è necessario avere familiarità con i concetti Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="2063f-106">Before reading this topic, you should be familiar with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="2063f-107">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="2063f-107">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="2063f-108">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="2063f-108">Source Resolver</span></span>](source-resolver.md)
-   [<span data-ttu-id="2063f-109">Topologie</span><span class="sxs-lookup"><span data-stu-id="2063f-109">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="2063f-110">Generatori di eventi multimediali</span><span class="sxs-lookup"><span data-stu-id="2063f-110">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="2063f-111">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="2063f-111">Presentation Descriptors</span></span>](presentation-descriptors.md)

> [!Note]  
> <span data-ttu-id="2063f-112">In questo argomento non viene descritto come riprodurre file protetti da Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="2063f-112">This topic does not describe how to play files that are protected by digital rights management (DRM).</span></span> <span data-ttu-id="2063f-113">Per informazioni su DRM in Microsoft Media Foundation, vedere [How to Play Protected Media Files](how-to-play-protected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="2063f-113">For information about DRM in Microsoft Media Foundation, see [How to Play Protected Media Files](how-to-play-protected-media-files.md).</span></span>

 

## <a name="overview"></a><span data-ttu-id="2063f-114">Panoramica</span><span class="sxs-lookup"><span data-stu-id="2063f-114">Overview</span></span>

<span data-ttu-id="2063f-115">Gli oggetti seguenti vengono usati per riprodurre un file multimediale con la sessione multimediale:</span><span class="sxs-lookup"><span data-stu-id="2063f-115">The following objects are used to play a media file with the Media Session:</span></span>

-   <span data-ttu-id="2063f-116">Un' *origine multimediale* è un oggetto che analizza un file multimediale o un'altra origine dei dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="2063f-116">A *media source* is an object that parses a media file or other source of media data.</span></span> <span data-ttu-id="2063f-117">L'origine multimediale crea oggetti *flusso* per ogni flusso audio o video del file.</span><span class="sxs-lookup"><span data-stu-id="2063f-117">The media source creates *stream* objects for each audio or video stream in the file.</span></span> <span data-ttu-id="2063f-118">I *decodificatori* convertono i dati multimediali codificati in audio e video non compressi.</span><span class="sxs-lookup"><span data-stu-id="2063f-118">*Decoders* convert encoded media data into uncompressed video and audio.</span></span>
-   <span data-ttu-id="2063f-119">Il *resolver di origine* crea un'origine multimediale da un URL.</span><span class="sxs-lookup"><span data-stu-id="2063f-119">The *Source Resolver* creates a media source from a URL.</span></span>
-   <span data-ttu-id="2063f-120">Il [renderer video migliorato](enhanced-video-renderer.md) (EVR) esegue il rendering dei video sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2063f-120">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) renders video to the screen.</span></span>
-   <span data-ttu-id="2063f-121">Il [renderer di streaming audio](streaming-audio-renderer.md) (SAR) esegue il rendering dell'audio in un altoparlante o in un altro dispositivo di output audio.</span><span class="sxs-lookup"><span data-stu-id="2063f-121">The [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) renders audio to a speaker or other audio output device.</span></span>
-   <span data-ttu-id="2063f-122">Una *topologia* definisce il flusso dei dati dall'origine multimediale a EVR e SAR.</span><span class="sxs-lookup"><span data-stu-id="2063f-122">A *topology* defines the flow of data from the media source to the EVR and SAR.</span></span>
-   <span data-ttu-id="2063f-123">La *sessione multimediale* controlla il flusso di dati e invia eventi di stato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2063f-123">The *Media Session* controls the data flow and sends status events to the application.</span></span> <span data-ttu-id="2063f-124">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="2063f-124">The following diagram illustrates this process.</span></span>

![diagramma che mostra la riproduzione mediante la sessione multimediale](images/session-playback.gif)

<span data-ttu-id="2063f-126">Di seguito è riportata una descrizione generale dei passaggi necessari per riprodurre un file multimediale tramite la sessione multimediale:</span><span class="sxs-lookup"><span data-stu-id="2063f-126">The following is a general outline of the steps needed to play a media file using the Media Session:</span></span>

1.  <span data-ttu-id="2063f-127">Chiamare la funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare la piattaforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2063f-127">Call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="2063f-128">Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare una nuova istanza della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="2063f-128">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="2063f-129">Usare il resolver di origine per creare un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="2063f-129">Use the source resolver to create a media source.</span></span> <span data-ttu-id="2063f-130">Per ulteriori informazioni, vedere [using the source resolver](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="2063f-130">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>
4.  <span data-ttu-id="2063f-131">Creare una topologia che connette l'origine multimediale a EVR e SAR.</span><span class="sxs-lookup"><span data-stu-id="2063f-131">Create a topology that connects the media source to the EVR and SAR.</span></span> <span data-ttu-id="2063f-132">In questo passaggio, l'applicazione crea una topologia *parziale* che non include i decodificatori.</span><span class="sxs-lookup"><span data-stu-id="2063f-132">In this step, the application creates a *partial* topology that does not include the decoders.</span></span> <span data-ttu-id="2063f-133">Per ulteriori informazioni, vedere [creazione di topologie di riproduzione](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="2063f-133">For more information, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="2063f-134">Chiamare [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="2063f-134">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
6.  <span data-ttu-id="2063f-135">Usare l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) per ottenere gli eventi dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="2063f-135">Use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface to get events from the Media Session.</span></span>
7.  <span data-ttu-id="2063f-136">Chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per avviare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2063f-136">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start playback.</span></span> <span data-ttu-id="2063f-137">Una volta avviata la riproduzione, è possibile sospenderla chiamando [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)o arrestarla chiamando [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="2063f-137">After playback starts, you can pause it by calling [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or stop it by calling [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
8.  <span data-ttu-id="2063f-138">Quando l'applicazione viene chiusa, rilasciare le risorse:</span><span class="sxs-lookup"><span data-stu-id="2063f-138">When the application exits, release resources:</span></span>

    1.  <span data-ttu-id="2063f-139">Chiamare [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="2063f-139">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span> <span data-ttu-id="2063f-140">Questo metodo è asincrono.</span><span class="sxs-lookup"><span data-stu-id="2063f-140">This method is asynchronous.</span></span> <span data-ttu-id="2063f-141">Al termine, la sessione multimediale Invia un evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="2063f-141">When it completes, the Media Session sends an [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="2063f-142">Quindi, è possibile eseguire i passaggi rimanenti.</span><span class="sxs-lookup"><span data-stu-id="2063f-142">Then it is safe to perform the remaining steps.</span></span>
    2.  <span data-ttu-id="2063f-143">Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) per arrestare l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="2063f-143">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
    3.  <span data-ttu-id="2063f-144">Chiamare [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) per arrestare la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="2063f-144">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) to shut down the Media Session.</span></span>
    4.  <span data-ttu-id="2063f-145">Chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare la piattaforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2063f-145">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>

<span data-ttu-id="2063f-146">Le sezioni seguenti mostrano un esempio di codice completo:</span><span class="sxs-lookup"><span data-stu-id="2063f-146">The following sections show a complete code example:</span></span>

-   [<span data-ttu-id="2063f-147">Passaggio 1: dichiarare la classe CPlayer</span><span class="sxs-lookup"><span data-stu-id="2063f-147">Step 1: Declare the CPlayer Class</span></span>](step-1--declare-the-cplayer-class.md)
-   [<span data-ttu-id="2063f-148">Passaggio 2: creare l'oggetto CPlayer</span><span class="sxs-lookup"><span data-stu-id="2063f-148">Step 2: Create the CPlayer Object</span></span>](step-2--create-the-cplayer-object.md)
-   [<span data-ttu-id="2063f-149">Passaggio 3: aprire un file multimediale</span><span class="sxs-lookup"><span data-stu-id="2063f-149">Step 3: Open a Media File</span></span>](step-3--open-a-media-file.md)
-   [<span data-ttu-id="2063f-150">Passaggio 4: creare la sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="2063f-150">Step 4: Create the Media Session</span></span>](step-4--create-the-media-session.md)
-   [<span data-ttu-id="2063f-151">Passaggio 5: gestire gli eventi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="2063f-151">Step 5: Handle Media Session Events</span></span>](step-5--handle-media-session-events.md)
-   [<span data-ttu-id="2063f-152">Passaggio 6: controllare la riproduzione</span><span class="sxs-lookup"><span data-stu-id="2063f-152">Step 6: Control Playback</span></span>](step-6--control-playback.md)
-   [<span data-ttu-id="2063f-153">Passaggio 7: arrestare la sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="2063f-153">Step 7: Shut Down the Media Session</span></span>](step-7--shut-down-the-media-session.md)
-   [<span data-ttu-id="2063f-154">Esempio di riproduzione della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="2063f-154">Media Session Playback Example</span></span>](media-session-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="2063f-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2063f-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2063f-156">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="2063f-156">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="2063f-157">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="2063f-157">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



