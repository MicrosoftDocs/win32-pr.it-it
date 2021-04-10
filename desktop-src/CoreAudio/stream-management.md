---
description: Gestione dei flussi
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Gestione dei flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127050"
---
# <a name="stream-management"></a><span data-ttu-id="dc7a1-103">Gestione dei flussi</span><span class="sxs-lookup"><span data-stu-id="dc7a1-103">Stream Management</span></span>

<span data-ttu-id="dc7a1-104">Dopo l'enumerazione dei [dispositivi dell'endpoint audio](audio-endpoint-devices.md) nel sistema e l'identificazione di un dispositivo di rendering o acquisizione appropriato, l'attività successiva per un'applicazione client audio consiste nell'aprire una connessione con il dispositivo endpoint e gestire il flusso di dati audio su tale connessione.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-104">After enumerating the [audio endpoint devices](audio-endpoint-devices.md) in the system and identifying a suitable rendering or capture device, the next task for an audio client application is to open a connection with the endpoint device and to manage the flow of audio data over that connection.</span></span> <span data-ttu-id="dc7a1-105">[WASAPI](wasapi.md) consente ai client di creare e gestire flussi audio.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-105">[WASAPI](wasapi.md) enables clients to create and manage audio streams.</span></span>

<span data-ttu-id="dc7a1-106">WASAPI implementa diverse interfacce per fornire servizi di gestione del flusso ai client audio.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-106">WASAPI implements several interfaces to provide stream-management services to audio clients.</span></span> <span data-ttu-id="dc7a1-107">L'interfaccia primaria è [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span><span class="sxs-lookup"><span data-stu-id="dc7a1-107">The primary interface is [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span></span> <span data-ttu-id="dc7a1-108">Un client ottiene l'interfaccia **IAudioClient** per un dispositivo endpoint audio chiamando il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (con il parametro *IID* impostato su **REFIID** IID \_ IAudioClient) nell'oggetto endpoint.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-108">A client obtains the **IAudioClient** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioClient) on the endpoint object.</span></span>

<span data-ttu-id="dc7a1-109">Il client chiama i metodi nell'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc7a1-109">The client calls the methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to do the following:</span></span>

-   <span data-ttu-id="dc7a1-110">Individuare i formati audio supportati dal dispositivo endpoint.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-110">Discover which audio formats the endpoint device supports.</span></span>
-   <span data-ttu-id="dc7a1-111">Ottenere le dimensioni del buffer dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-111">Get the endpoint buffer size.</span></span>
-   <span data-ttu-id="dc7a1-112">Ottenere il formato del flusso e la latenza.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-112">Get the stream format and latency.</span></span>
-   <span data-ttu-id="dc7a1-113">Avviare, arrestare e reimpostare il flusso che attraversa il dispositivo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-113">Start, stop, and reset the stream that flows through the endpoint device.</span></span>
-   <span data-ttu-id="dc7a1-114">Accedere ai servizi audio aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-114">Access additional audio services.</span></span>

<span data-ttu-id="dc7a1-115">Per creare un flusso, un client chiama il metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="dc7a1-115">To create a stream, a client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="dc7a1-116">Tramite questo metodo, il client specifica il formato dei dati per il flusso, le dimensioni del buffer dell'endpoint e se il flusso funziona in modalità condivisa o esclusiva.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-116">Through this method, the client specifies the data format for the stream, the size of the endpoint buffer, and whether the stream operates in shared or exclusive mode.</span></span>

<span data-ttu-id="dc7a1-117">I metodi rimanenti nell'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) rientrano in due gruppi:</span><span class="sxs-lookup"><span data-stu-id="dc7a1-117">The remaining methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface fall into two groups:</span></span>

-   <span data-ttu-id="dc7a1-118">Metodi che possono essere chiamati solo dopo l'apertura del flusso da parte di [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="dc7a1-118">Methods that can be called only after the stream has been opened by [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="dc7a1-119">Metodi che possono essere chiamati in qualsiasi momento prima o dopo la chiamata di [**inizializzazione**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="dc7a1-119">Methods that can be called at any time before or after the [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call.</span></span>

<span data-ttu-id="dc7a1-120">I metodi seguenti possono essere chiamati solo dopo la chiamata a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span><span class="sxs-lookup"><span data-stu-id="dc7a1-120">The following methods can be called only after the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span></span>

-   [<span data-ttu-id="dc7a1-121">**IAudioClient:: GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-121">**IAudioClient::GetBufferSize**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [<span data-ttu-id="dc7a1-122">**IAudioClient::GetCurrentPadding**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-122">**IAudioClient::GetCurrentPadding**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [<span data-ttu-id="dc7a1-123">**IAudioClient:: GetService**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-123">**IAudioClient::GetService**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [<span data-ttu-id="dc7a1-124">**IAudioClient::GetStreamLatency**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-124">**IAudioClient::GetStreamLatency**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [<span data-ttu-id="dc7a1-125">**IAudioClient:: Reset**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-125">**IAudioClient::Reset**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [<span data-ttu-id="dc7a1-126">**IAudioClient:: Start**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-126">**IAudioClient::Start**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [<span data-ttu-id="dc7a1-127">**IAudioClient:: Stop**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-127">**IAudioClient::Stop**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

<span data-ttu-id="dc7a1-128">I metodi seguenti possono essere chiamati prima o dopo la chiamata a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) :</span><span class="sxs-lookup"><span data-stu-id="dc7a1-128">The following methods can be called before or after the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call:</span></span>

-   [<span data-ttu-id="dc7a1-129">**IAudioClient::GetDevicePeriod**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-129">**IAudioClient::GetDevicePeriod**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [<span data-ttu-id="dc7a1-130">**IAudioClient::GetMixFormat**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-130">**IAudioClient::GetMixFormat**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [<span data-ttu-id="dc7a1-131">**IAudioClient::IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-131">**IAudioClient::IsFormatSupported**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

<span data-ttu-id="dc7a1-132">Per accedere ai servizi client audio aggiuntivi, il client chiama il metodo [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="dc7a1-132">To access the additional audio client services, the client calls the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="dc7a1-133">Tramite questo metodo, il client può ottenere riferimenti alle interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc7a1-133">Through this method, the client can obtain references to the following interfaces:</span></span>

-   [<span data-ttu-id="dc7a1-134">**IAudioRenderClient**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-134">**IAudioRenderClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    <span data-ttu-id="dc7a1-135">Scrive i dati di rendering in un buffer dell'endpoint di rendering audio.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-135">Writes rendering data to an audio-rendering endpoint buffer.</span></span>

-   [<span data-ttu-id="dc7a1-136">**IAudioCaptureClient**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-136">**IAudioCaptureClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    <span data-ttu-id="dc7a1-137">Legge i dati acquisiti da un buffer dell'endpoint di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-137">Reads captured data from an audio-capture endpoint buffer.</span></span>

-   [<span data-ttu-id="dc7a1-138">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-138">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    <span data-ttu-id="dc7a1-139">Comunica con gestione sessioni audio per configurare e gestire la sessione audio associata al flusso.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-139">Communicates with the audio session manager to configure and manage the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="dc7a1-140">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-140">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    <span data-ttu-id="dc7a1-141">Controlla il livello del volume della sessione audio associata al flusso.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-141">Controls the volume level of the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="dc7a1-142">**IChannelAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-142">**IChannelAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    <span data-ttu-id="dc7a1-143">Controlla i livelli di volume dei singoli canali della sessione audio associata al flusso.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-143">Controls the volume levels of the individual channels in the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="dc7a1-144">**IAudioClock**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-144">**IAudioClock**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    <span data-ttu-id="dc7a1-145">Monitora la velocità dei dati del flusso e la posizione del flusso.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-145">Monitors the stream data rate and stream position.</span></span>

<span data-ttu-id="dc7a1-146">Inoltre, i client WASAPI che richiedono la notifica di eventi correlati alla sessione devono implementare l'interfaccia seguente:</span><span class="sxs-lookup"><span data-stu-id="dc7a1-146">In addition, WASAPI clients that require notification of session-related events should implement the following interface:</span></span>

-   [<span data-ttu-id="dc7a1-147">**IAudioSessionEvents**</span><span class="sxs-lookup"><span data-stu-id="dc7a1-147">**IAudioSessionEvents**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    <span data-ttu-id="dc7a1-148">Per ricevere le notifiche degli eventi, il client passa un puntatore alla relativa interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) al metodo [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) come parametro di chiamata.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-148">To receive event notifications, the client passes a pointer to its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method as a call parameter.</span></span>

<span data-ttu-id="dc7a1-149">Infine, un client può usare un'API di livello superiore per creare un flusso audio, ma anche richiedere l'accesso ai controlli di sessione e ai controlli volume per la sessione che contiene il flusso.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-149">Finally, a client might use a higher-level API to create an audio stream, but also require access to the session controls and volume controls for the session that contains the stream.</span></span> <span data-ttu-id="dc7a1-150">Un'API di livello superiore in genere non fornisce questo accesso.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-150">A higher-level API typically does not provide this access.</span></span> <span data-ttu-id="dc7a1-151">Il client può ottenere i controlli per una sessione specifica tramite l'interfaccia [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) .</span><span class="sxs-lookup"><span data-stu-id="dc7a1-151">The client can obtain the controls for a particular session through the [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface.</span></span> <span data-ttu-id="dc7a1-152">Questa interfaccia consente al client di ottenere le interfacce [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) e [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) per una sessione senza richiedere al client di usare l'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) per creare un flusso e assegnare il flusso alla sessione.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-152">This interface enables the client to obtain the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) and [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interfaces for a session without requiring the client to use the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to create a stream and to assign the stream to the session.</span></span> <span data-ttu-id="dc7a1-153">Un client ottiene l'interfaccia **IAudioSessionManager** per un dispositivo endpoint audio chiamando il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (con il parametro *IID* impostato su **REFIID** IID \_ IAudioSessionManager) nell'oggetto endpoint.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-153">A client obtains the **IAudioSessionManager** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioSessionManager) on the endpoint object.</span></span>

<span data-ttu-id="dc7a1-154">Le interfacce [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)e [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) sono definite nel file di intestazione Audiopolicy. h.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-154">The [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents), and [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interfaces are defined in header file Audiopolicy.h.</span></span> <span data-ttu-id="dc7a1-155">Tutte le altre interfacce WASAPI sono definite nel file di intestazione Audioclient. h.</span><span class="sxs-lookup"><span data-stu-id="dc7a1-155">All other WASAPI interfaces are defined in header file Audioclient.h.</span></span>

<span data-ttu-id="dc7a1-156">Le sezioni seguenti descrivono come usare WASAPI per gestire i flussi audio:</span><span class="sxs-lookup"><span data-stu-id="dc7a1-156">The following sections describe how to use WASAPI to manage audio streams:</span></span>

-   [<span data-ttu-id="dc7a1-157">Informazioni su WASAPI</span><span class="sxs-lookup"><span data-stu-id="dc7a1-157">About WASAPI</span></span>](wasapi.md)
-   [<span data-ttu-id="dc7a1-158">Rendering di un flusso</span><span class="sxs-lookup"><span data-stu-id="dc7a1-158">Rendering a Stream</span></span>](rendering-a-stream.md)
-   [<span data-ttu-id="dc7a1-159">Acquisizione di un flusso</span><span class="sxs-lookup"><span data-stu-id="dc7a1-159">Capturing a Stream</span></span>](capturing-a-stream.md)
-   [<span data-ttu-id="dc7a1-160">Registrazione loopback</span><span class="sxs-lookup"><span data-stu-id="dc7a1-160">Loopback Recording</span></span>](loopback-recording.md)
-   [<span data-ttu-id="dc7a1-161">Flussi in modalità esclusiva</span><span class="sxs-lookup"><span data-stu-id="dc7a1-161">Exclusive-Mode Streams</span></span>](exclusive-mode-streams.md)
-   [<span data-ttu-id="dc7a1-162">Ripristino da un errore di Invalid-Device</span><span class="sxs-lookup"><span data-stu-id="dc7a1-162">Recovering from an Invalid-Device Error</span></span>](recovering-from-an-invalid-device-error.md)
-   [<span data-ttu-id="dc7a1-163">Uso di un dispositivo di comunicazione</span><span class="sxs-lookup"><span data-stu-id="dc7a1-163">Using a Communication Device</span></span>](using-the-communication-device.md)
-   [<span data-ttu-id="dc7a1-164">Routing del flusso</span><span class="sxs-lookup"><span data-stu-id="dc7a1-164">Stream Routing</span></span>](stream-routing.md)

## <a name="related-topics"></a><span data-ttu-id="dc7a1-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc7a1-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc7a1-166">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="dc7a1-166">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



