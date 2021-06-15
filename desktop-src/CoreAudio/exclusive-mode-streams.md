---
description: Exclusive-Mode flussi
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677efa83d099bd32ddb0674414e25a9af219bd1a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068587"
---
# <a name="exclusive-mode-streams"></a><span data-ttu-id="f7083-103">Exclusive-Mode flussi</span><span class="sxs-lookup"><span data-stu-id="f7083-103">Exclusive-Mode Streams</span></span>

<span data-ttu-id="f7083-104">Come spiegato in precedenza, se un'applicazione apre un flusso in modalità esclusiva, l'applicazione usa esclusivamente il dispositivo endpoint audio che riproduce o registra il flusso.</span><span class="sxs-lookup"><span data-stu-id="f7083-104">As explained previously, if an application opens a stream in exclusive mode, the application has exclusive use of the audio endpoint device that plays or records the stream.</span></span> <span data-ttu-id="f7083-105">Al contrario, diverse applicazioni possono condividere un dispositivo endpoint audio aprendo flussi in modalità condivisa nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7083-105">In contrast, several applications can share an audio endpoint device by opening shared-mode streams on the device.</span></span>

<span data-ttu-id="f7083-106">L'accesso in modalità esclusiva a un dispositivo audio può bloccare i suoni di sistema cruciali, impedire l'interoperabilità con altre applicazioni e altrimenti peggiorare l'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="f7083-106">Exclusive-mode access to an audio device can block crucial system sounds, prevent interoperability with other applications, and otherwise degrade the user experience.</span></span> <span data-ttu-id="f7083-107">Per attenuare questi problemi, un'applicazione con un flusso in modalità esclusiva in genere cinge il controllo del dispositivo audio quando l'applicazione non è il processo in primo piano o non è attivamente in streaming.</span><span class="sxs-lookup"><span data-stu-id="f7083-107">To mitigate these problems, an application with an exclusive-mode stream typically relinquishes control of the audio device when the application is not the foreground process or is not actively streaming.</span></span>

<span data-ttu-id="f7083-108">La latenza di flusso è il ritardo intrinseco nel percorso dati che connette il buffer dell'endpoint di un'applicazione a un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="f7083-108">Stream latency is the delay that is inherent in the data path that connects an application's endpoint buffer with an audio endpoint device.</span></span> <span data-ttu-id="f7083-109">Per un flusso di rendering, la latenza è il ritardo massimo dal momento in cui un'applicazione scrive un campione in un buffer dell'endpoint al momento in cui il campione viene udito attraverso i parlanti.</span><span class="sxs-lookup"><span data-stu-id="f7083-109">For a rendering stream, the latency is the maximum delay from the time that an application writes a sample to an endpoint buffer to the time that the sample is heard through the speakers.</span></span> <span data-ttu-id="f7083-110">Per un flusso di acquisizione, la latenza è il ritardo massimo tra il momento in cui un suono entra nel microfono e il momento in cui un'applicazione può leggere l'esempio per tale suono dal buffer dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f7083-110">For a capture stream, the latency is the maximum delay from the time that a sound enters the microphone to the time that an application can read the sample for that sound from the endpoint buffer.</span></span>

<span data-ttu-id="f7083-111">Le applicazioni che usano flussi in modalità esclusiva spesso lo fanno perché richiedono latenze basse nei percorsi dei dati tra i dispositivi endpoint audio e i thread dell'applicazione che accedono ai buffer dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f7083-111">Applications that use exclusive-mode streams often do so because they require low latencies in the data paths between the audio endpoint devices and the application threads that access the endpoint buffers.</span></span> <span data-ttu-id="f7083-112">In genere, questi thread vengono eseguiti con priorità relativamente elevata e pianificano se stessi per l'esecuzione a intervalli periodici vicini o uguali all'intervallo periodico che separa i passaggi di elaborazione successivi da parte dell'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="f7083-112">Typically, these threads run at relatively high priority and schedule themselves to run at periodic intervals that are close to or the same as the periodic interval that separates successive processing passes by the audio hardware.</span></span> <span data-ttu-id="f7083-113">Durante ogni passaggio, l'hardware audio elabora i nuovi dati nei buffer dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f7083-113">During each pass, the audio hardware processes the new data in the endpoint buffers.</span></span>

<span data-ttu-id="f7083-114">Per ottenere le latenze di flusso più piccole, un'applicazione potrebbe richiedere hardware audio speciale e un sistema di computer che viene caricato leggermente.</span><span class="sxs-lookup"><span data-stu-id="f7083-114">To achieve the smallest stream latencies, an application might require both special audio hardware, and a computer system that is lightly loaded.</span></span> <span data-ttu-id="f7083-115">Se l'hardware audio supera i limiti di temporizzazione o carica il sistema con attività con priorità alta in competizione, potrebbe verificarsi un problema in un flusso audio a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="f7083-115">Driving the audio hardware beyond its timing limits or loading the system with competing high-priority tasks might cause a glitch in a low-latency audio stream.</span></span> <span data-ttu-id="f7083-116">Ad esempio, per un flusso di rendering, può verificarsi un problema se l'applicazione non riesce a scrivere in un buffer dell'endpoint prima che l'hardware audio letta il buffer o se l'hardware non riesce a leggere il buffer prima dell'ora pianificata per la riproduzione del buffer.</span><span class="sxs-lookup"><span data-stu-id="f7083-116">For example, for a rendering stream, a glitch can occur if the application fails to write to an endpoint buffer before the audio hardware reads the buffer, or if the hardware fails to read the buffer before the time that the buffer is scheduled to play.</span></span> <span data-ttu-id="f7083-117">In genere, un'applicazione che deve essere eseguita su un'ampia gamma di hardware audio e in un'ampia gamma di sistemi deve soddisfare i requisiti di temporizzazione sufficienti per evitare problemi in tutti gli ambienti di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f7083-117">Typically, an application that is intended to run on a wide variety of audio hardware and in a broad range of systems should relax its timing requirements enough to avoid glitches in all target environments.</span></span>

<span data-ttu-id="f7083-118">Windows Vista offre diverse funzionalità per supportare le applicazioni che richiedono flussi audio a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="f7083-118">Windows Vista has several features to support applications that require low-latency audio streams.</span></span> <span data-ttu-id="f7083-119">Come descritto in Componenti [audio](user-mode-audio-components.md)in modalità utente, le applicazioni che eseguono operazioni di importanza critica possono chiamare le funzioni del servizio Utilità di pianificazione classi multimediali (MMCSS) per aumentare la priorità dei thread senza negare le risorse della CPU alle applicazioni con priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="f7083-119">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), applications that perform time-critical operations can call the Multimedia Class Scheduler Service (MMCSS) functions to increase thread priority without denying CPU resources to lower-priority applications.</span></span> <span data-ttu-id="f7083-120">Inoltre, il metodo [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) supporta un flag AUDCLNT STREAMFLAGS EVENTCALLBACK che consente al thread di manutenzione del buffer di un'applicazione di pianificare l'esecuzione quando un nuovo buffer diventa disponibile dal \_ \_ dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="f7083-120">In addition, the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method supports an AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK flag that enables an application's buffer-servicing thread to schedule its execution to occur when a new buffer becomes available from the audio device.</span></span> <span data-ttu-id="f7083-121">Usando queste funzionalità, un thread dell'applicazione può ridurre l'incertezza sul momento in cui verrà eseguito, riducendo così il rischio di problemi in un flusso audio a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="f7083-121">By using these features, an application thread can reduce uncertainty about when it will execute, thereby decreasing the risk of glitches in a low-latency audio stream.</span></span>

<span data-ttu-id="f7083-122">È probabile che i driver per le schede audio meno recenti usino l'interfaccia DDI (Device Driver Interface) WaveCyclic o WavePci, mentre i driver per le schede audio più recenti sono più probabili supportino l'interfaccia DDI WaveRT.</span><span class="sxs-lookup"><span data-stu-id="f7083-122">The drivers for older audio adapters are likely to use the WaveCyclic or WavePci device driver interface (DDI), whereas the drivers for newer audio adapters are more likely to support the WaveRT DDI.</span></span> <span data-ttu-id="f7083-123">Per le applicazioni in modalità esclusiva, i driver WaveRT possono offrire prestazioni migliori rispetto ai driver WaveCyclic o WavePci, ma i driver WaveRT richiedono funzionalità hardware aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="f7083-123">For exclusive-mode applications, WaveRT drivers can provide better performance than WaveCyclic or WavePci drivers, but WaveRT drivers require additional hardware capabilities.</span></span> <span data-ttu-id="f7083-124">Queste funzionalità includono la possibilità di condividere i buffer hardware direttamente con le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f7083-124">These capabilities include the ability to share hardware buffers directly with applications.</span></span> <span data-ttu-id="f7083-125">Con la condivisione diretta, non è necessario alcun intervento del sistema per trasferire i dati tra un'applicazione in modalità esclusiva e l'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="f7083-125">With direct sharing, no system intervention is required to transfer data between an exclusive-mode application and the audio hardware.</span></span> <span data-ttu-id="f7083-126">Al contrario, i driver WaveCyclic e WavePci sono adatti per le schede audio meno recenti e meno idonee.</span><span class="sxs-lookup"><span data-stu-id="f7083-126">In contrast, WaveCyclic and WavePci drivers are suitable for older, less capable audio adapters.</span></span> <span data-ttu-id="f7083-127">Queste schede si basano sul software di sistema per il trasporto di blocchi di dati (collegati a pacchetti di richieste di I/O di sistema o IRP) tra i buffer dell'applicazione e i buffer hardware.</span><span class="sxs-lookup"><span data-stu-id="f7083-127">These adapters rely on system software to transport blocks of data (attached to system I/O request packets, or IRPs) between application buffers and hardware buffers.</span></span> <span data-ttu-id="f7083-128">Inoltre, i dispositivi audio USB si basano sul software di sistema per il trasporto dei dati tra i buffer dell'applicazione e i buffer hardware.</span><span class="sxs-lookup"><span data-stu-id="f7083-128">In addition, USB audio devices rely on system software to transport data between application buffers and hardware buffers.</span></span> <span data-ttu-id="f7083-129">Per migliorare le prestazioni delle applicazioni in modalità esclusiva che si connettono a dispositivi audio che si basano sul sistema per il trasporto dei dati, WASAPI aumenta automaticamente la priorità dei thread di sistema che trasferiscono i dati tra le applicazioni e l'hardware.</span><span class="sxs-lookup"><span data-stu-id="f7083-129">To improve the performance of exclusive-mode applications that connect to audio devices that rely on the system for data transport, WASAPI automatically increases the priority of the system threads that transfer data between the applications and the hardware.</span></span> <span data-ttu-id="f7083-130">WASAPI usa MMCSS per aumentare la priorità dei thread.</span><span class="sxs-lookup"><span data-stu-id="f7083-130">WASAPI uses MMCSS to increase the thread priority.</span></span> <span data-ttu-id="f7083-131">In Windows Vista, se un thread di sistema gestisce il trasporto dei dati per un flusso di riproduzione audio in modalità esclusiva con un formato PCM e un periodo del dispositivo inferiore a 10 millisecondi, WASAPI assegna il nome dell'attività MMCSS "Pro Audio" al thread.</span><span class="sxs-lookup"><span data-stu-id="f7083-131">In Windows Vista, if a system thread manages data transport for an exclusive-mode audio playback stream with a PCM format and a device period of less than 10 milliseconds, WASAPI assigns the MMCSS task name "Pro Audio" to the thread.</span></span> <span data-ttu-id="f7083-132">Se il periodo del dispositivo del flusso è maggiore o uguale a 10 millisecondi, WASAPI assegna il nome dell'attività MMCSS "Audio" al thread.</span><span class="sxs-lookup"><span data-stu-id="f7083-132">If the device period of the stream is greater than or equal to 10 milliseconds, WASAPI assigns the MMCSS task name "Audio" to the thread.</span></span> <span data-ttu-id="f7083-133">Per altre informazioni sui DDI WaveCyclic, WavePci e WaveRT, vedere la documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="f7083-133">For more information about the WaveCyclic, WavePci, and WaveRT DDIs, see the Windows DDK documentation.</span></span> <span data-ttu-id="f7083-134">Per informazioni sulla selezione di un periodo di dispositivo appropriato, vedere [**IAudioClient::GetDevicePeriod.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)</span><span class="sxs-lookup"><span data-stu-id="f7083-134">For information about selecting an appropriate device period, see [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span></span>

<span data-ttu-id="f7083-135">Come descritto in Session [Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) fornisce le interfacce [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) per controllare i livelli di volume dei flussi audio in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="f7083-135">As described in [Session Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) provides the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces for controlling the volume levels of shared-mode audio streams.</span></span> <span data-ttu-id="f7083-136">Tuttavia, i controlli in queste interfacce non hanno alcun effetto sui flussi in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="f7083-136">However, the controls in these interfaces have no effect on exclusive-mode streams.</span></span> <span data-ttu-id="f7083-137">Al contrario, le applicazioni che gestiscono flussi in modalità esclusiva usano in genere [**l'interfaccia IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) nell'API [EndpointVolume](endpointvolume-api.md) per controllare i livelli di volume di tali flussi.</span><span class="sxs-lookup"><span data-stu-id="f7083-137">Instead, applications that manage exclusive-mode streams typically use the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the [EndpointVolume API](endpointvolume-api.md) to control the volume levels of those streams.</span></span> <span data-ttu-id="f7083-138">Per informazioni su questa interfaccia, vedere [Endpoint Volume Controls](endpoint-volume-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f7083-138">For information about this interface, see [Endpoint Volume Controls](endpoint-volume-controls.md).</span></span>

<span data-ttu-id="f7083-139">Per ogni dispositivo di riproduzione e dispositivo di acquisizione nel sistema, l'utente può controllare se il dispositivo può essere usato in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="f7083-139">For each playback device and capture device in the system, the user can control whether the device can be used in exclusive mode.</span></span> <span data-ttu-id="f7083-140">Se l'utente disabilita l'uso in modalità esclusiva del dispositivo, il dispositivo può essere usato per riprodurre o registrare solo flussi in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="f7083-140">If the user disables exclusive-mode use of the device, the device can be used to play or record only shared-mode streams.</span></span>

<span data-ttu-id="f7083-141">Se l'utente consente l'uso in modalità esclusiva del dispositivo, l'utente può anche controllare se una richiesta da parte di un'applicazione di usare il dispositivo in modalità esclusiva presciderà l'uso del dispositivo da parte di applicazioni che potrebbero attualmente riprodurre o registrare flussi in modalità condivisa attraverso il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7083-141">If the user enables exclusive-mode use of the device, the user can also control whether a request by an application to use the device in exclusive mode will preempt the use of the device by applications that might currently be playing or recording shared-mode streams through the device.</span></span> <span data-ttu-id="f7083-142">Se la preemption è abilitata, una richiesta da parte di un'applicazione di assumere il controllo esclusivo del dispositivo ha esito positivo se il dispositivo non è attualmente in uso o se il dispositivo è in uso in modalità condivisa, ma la richiesta ha esito negativo se un'altra applicazione ha già il controllo esclusivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7083-142">If preemption is enabled, a request by an application to take exclusive control of the device succeeds if the device is currently not in use, or if the device is being used in shared mode, but the request fails if another application already has exclusive control of the device.</span></span> <span data-ttu-id="f7083-143">Se la preemption è disabilitata, una richiesta da parte di un'applicazione di assumere il controllo esclusivo del dispositivo ha esito positivo se il dispositivo non è attualmente in uso, ma la richiesta ha esito negativo se il dispositivo è già in uso in modalità condivisa o in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="f7083-143">If preemption is disabled, a request by an application to take exclusive control of the device succeeds if the device is not currently in use, but the request fails if the device is already being used either in shared mode or in exclusive mode.</span></span>

<span data-ttu-id="f7083-144">In Windows Vista le impostazioni predefinite per un dispositivo endpoint audio sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7083-144">In Windows Vista, the default settings for an audio endpoint device are the following:</span></span>

-   <span data-ttu-id="f7083-145">Il dispositivo può essere usato per riprodurre o registrare flussi in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="f7083-145">The device can be used to play or record exclusive-mode streams.</span></span>
-   <span data-ttu-id="f7083-146">Una richiesta di usare un dispositivo per riprodurre o registrare un flusso in modalità esclusiva ha la presunzione di qualsiasi flusso in modalità condivisa attualmente riprodotto o registrato tramite il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7083-146">A request to use a device to play or record an exclusive-mode stream preempts any shared-mode stream that is currently being played or recorded through the device.</span></span>

<span data-ttu-id="f7083-147">**Per modificare le impostazioni della modalità esclusiva di un dispositivo di riproduzione o registrazione**</span><span class="sxs-lookup"><span data-stu-id="f7083-147">**To change the exclusive-mode settings of a playback or recording device**</span></span>

1.  <span data-ttu-id="f7083-148">Fare clic con il pulsante destro del mouse sull'icona dell'altoparlante nell'area di notifica, che si trova sul lato destro della barra delle applicazioni, e selezionare **Dispositivi** di riproduzione o Dispositivi **di registrazione.**</span><span class="sxs-lookup"><span data-stu-id="f7083-148">Right-click the speaker icon in the notification area, which is located on the right side of the taskbar, and select **Playback Devices** or **Recording Devices**.</span></span> <span data-ttu-id="f7083-149">In alternativa, eseguire il pannello di controllo multimediale di Windows, Mmsys.cpl, da una finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="f7083-149">(As an alternative, run the Windows multimedia control panel, Mmsys.cpl, from a Command Prompt window.</span></span> <span data-ttu-id="f7083-150">Per altre informazioni, vedere Note in [Costanti DEVICE \_ STATE \_ XXX.](device-state-xxx-constants.md)</span><span class="sxs-lookup"><span data-stu-id="f7083-150">For more information, see Remarks in [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).)</span></span>
2.  <span data-ttu-id="f7083-151">Quando viene **visualizzata la** finestra Audio, selezionare **Playback (Riproduzione)** **o Recording (Registrazione).**</span><span class="sxs-lookup"><span data-stu-id="f7083-151">After the **Sound** window appears, select **Playback** or **Recording**.</span></span> <span data-ttu-id="f7083-152">Selezionare quindi una voce nell'elenco dei nomi di dispositivo e fare clic su **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="f7083-152">Next, select an entry in the list of device names, and click **Properties**.</span></span>
3.  <span data-ttu-id="f7083-153">Quando viene **visualizzata la** finestra Proprietà , fare clic **su Avanzate**.</span><span class="sxs-lookup"><span data-stu-id="f7083-153">After the **Properties** window appears, click **Advanced**.</span></span>
4.  <span data-ttu-id="f7083-154">Per consentire alle applicazioni di usare il dispositivo in modalità esclusiva, selezionare la casella Consenti alle applicazioni di assumere il controllo **esclusivo del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f7083-154">To enable applications to use the device in exclusive mode, check the box labeled **Allow applications to take exclusive control of this device**.</span></span> <span data-ttu-id="f7083-155">Per disabilitare l'uso in modalità esclusiva del dispositivo, deselezionare la casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="f7083-155">To disable exclusive-mode use of the device, clear the check box.</span></span>
5.  <span data-ttu-id="f7083-156">Se è abilitato l'uso in modalità esclusiva del dispositivo, è possibile specificare se una richiesta di controllo esclusivo del dispositivo avrà esito positivo se il dispositivo è attualmente in riproduzione o sta registrando flussi in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="f7083-156">If exclusive-mode use of the device is enabled, you can specify whether a request for exclusive control of the device will succeed if the device is currently playing or recording shared-mode streams.</span></span> <span data-ttu-id="f7083-157">Per assegnare la priorità alle applicazioni in modalità esclusiva rispetto alle applicazioni in modalità condivisa, selezionare la casella Assegnare la priorità **alle applicazioni in modalità esclusiva**.</span><span class="sxs-lookup"><span data-stu-id="f7083-157">To give exclusive-mode applications priority over shared-mode applications, check the box labeled **Give exclusive mode applications priority**.</span></span> <span data-ttu-id="f7083-158">Per negare la priorità delle applicazioni in modalità esclusiva rispetto alle applicazioni in modalità condivisa, deselezionare la casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="f7083-158">To deny exclusive-mode applications priority over shared-mode applications, clear the check box.</span></span>

<span data-ttu-id="f7083-159">L'esempio di codice seguente illustra come riprodurre un flusso audio a bassa latenza in un dispositivo di rendering audio configurato per l'uso in modalità esclusiva:</span><span class="sxs-lookup"><span data-stu-id="f7083-159">The following code example shows how to play a low-latency audio stream on an audio-rendering device that is configured for use in exclusive mode:</span></span>


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;
    DWORD taskIndex = 0;
    
    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    if (hr == AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED) {
        // Align the buffer if needed, see IAudioClient::Initialize() documentation
        UINT32 nFrames = 0;
        hr = pAudioClient->GetBufferSize(&nFrames);
        EXIT_ON_ERROR(hr)
        hnsRequestedDuration = (REFERENCE_TIME)((double)REFTIMES_PER_SEC / pwfx->nSamplesPerSec * nFrames + 0.5);
        hr = pAudioClient->Initialize(
            AUDCLNT_SHAREMODE_EXCLUSIVE,
            AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
            hnsRequestedDuration,
            hnsRequestedDuration,
            pwfx,
            NULL);
    }
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="f7083-160">Nell'esempio di codice precedente la funzione PlayExclusiveStream viene eseguita nel thread dell'applicazione che gestisce i buffer dell'endpoint durante la riproduzione di un flusso di rendering.</span><span class="sxs-lookup"><span data-stu-id="f7083-160">In the preceding code example, the PlayExclusiveStream function runs in the application thread that services the endpoint buffers while a rendering stream is playing.</span></span> <span data-ttu-id="f7083-161">La funzione accetta un singolo parametro, pMySource, che è un puntatore a un oggetto che appartiene a una classe definita dal client, MyAudioSource.</span><span class="sxs-lookup"><span data-stu-id="f7083-161">The function takes a single parameter, pMySource, which is a pointer to an object that belongs to a client-defined class, MyAudioSource.</span></span> <span data-ttu-id="f7083-162">Questa classe ha due funzioni membro, LoadData e SetFormat, chiamate nell'esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="f7083-162">This class has two member functions, LoadData and SetFormat, that are called in the code example.</span></span> <span data-ttu-id="f7083-163">MyAudioSource è descritto in [Rendering di un flusso.](rendering-a-stream.md)</span><span class="sxs-lookup"><span data-stu-id="f7083-163">MyAudioSource is described in [Rendering a Stream](rendering-a-stream.md).</span></span>

<span data-ttu-id="f7083-164">La funzione PlayExclusiveStream chiama una funzione helper, GetStreamFormat, che negozia con il dispositivo di rendering predefinito per determinare se il dispositivo supporta un formato di flusso in modalità esclusiva adatto all'uso da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7083-164">The PlayExclusiveStream function calls a helper function, GetStreamFormat, that negotiates with the default rendering device to determine whether the device supports an exclusive-mode stream format that is suitable for use by the application.</span></span> <span data-ttu-id="f7083-165">Il codice per la funzione GetStreamFormat non viene visualizzato nell'esempio di codice. ciò è dovuto al fatto che i dettagli dell'implementazione dipendono interamente dai requisiti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7083-165">The code for the GetStreamFormat function does not appear in the code example; that is because the details of its implementation depend entirely on the requirements of the application.</span></span> <span data-ttu-id="f7083-166">Tuttavia, l'operazione della funzione GetStreamFormat può essere descritta semplicemente: chiama il metodo [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) una o più volte per determinare se il dispositivo supporta un formato appropriato.</span><span class="sxs-lookup"><span data-stu-id="f7083-166">However, the operation of the GetStreamFormat function can be described simply—it calls the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method one or more times to determine whether the device supports a suitable format.</span></span> <span data-ttu-id="f7083-167">I requisiti dell'applicazione determinano quali formati GetStreamFormat presenta al metodo **IsFormatSupported** e l'ordine in cui vengono presentati.</span><span class="sxs-lookup"><span data-stu-id="f7083-167">The requirements of the application dictate which formats GetStreamFormat presents to the **IsFormatSupported** method and the order in which it presents them.</span></span> <span data-ttu-id="f7083-168">Per altre informazioni su **IsFormatSupported,** vedere [Formati di dispositivo.](device-formats.md)</span><span class="sxs-lookup"><span data-stu-id="f7083-168">For more information about **IsFormatSupported**, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="f7083-169">Dopo la chiamata a GetStreamFormat, la funzione PlayExclusiveStream chiama il metodo [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) per ottenere il periodo minimo di dispositivo supportato dall'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="f7083-169">After the GetStreamFormat call, the PlayExclusiveStream function calls the [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) method to obtain the minimum device period supported by the audio hardware.</span></span> <span data-ttu-id="f7083-170">La funzione chiama quindi il metodo [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) per richiedere una durata del buffer uguale al periodo minimo.</span><span class="sxs-lookup"><span data-stu-id="f7083-170">Next, the function calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to request a buffer duration equal to the minimum period.</span></span> <span data-ttu-id="f7083-171">Se la chiamata ha esito positivo, il metodo **Initialize** alloca due buffer dell'endpoint, ognuno dei quali ha una durata uguale al periodo minimo.</span><span class="sxs-lookup"><span data-stu-id="f7083-171">If the call succeeds, the **Initialize** method allocates two endpoint buffers, each of which is equal in duration to the minimum period.</span></span> <span data-ttu-id="f7083-172">Successivamente, quando inizia l'esecuzione del flusso audio, l'applicazione e l'hardware audio condivideranno i due buffer in modalità "ping-pong", ovvero mentre l'applicazione scrive in un buffer, l'hardware legge dall'altro buffer.</span><span class="sxs-lookup"><span data-stu-id="f7083-172">Later, when the audio stream begins running, the application and audio hardware will share the two buffers in "ping-pong" fashion—that is, while the application writes to one buffer, the hardware reads from the other buffer.</span></span>

<span data-ttu-id="f7083-173">Prima di avviare il flusso, la funzione PlayExclusiveStream esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7083-173">Before starting the stream, the PlayExclusiveStream function does the following:</span></span>

-   <span data-ttu-id="f7083-174">Crea e registra l'handle dell'evento tramite il quale riceverà notifiche quando i buffer saranno pronti per il riempimento.</span><span class="sxs-lookup"><span data-stu-id="f7083-174">Creates and registers the event handle through which it will receive notifications when buffers become ready to fill.</span></span>
-   <span data-ttu-id="f7083-175">Riempie il primo buffer con i dati provenienti dall'origine audio per ridurre il ritardo da quando inizia l'esecuzione del flusso a quando viene udito il suono iniziale.</span><span class="sxs-lookup"><span data-stu-id="f7083-175">Fills the first buffer with data from the audio source to reduce the delay from when the stream starts running to when the initial sound is heard.</span></span>
-   <span data-ttu-id="f7083-176">Chiama la **funzione AvSetMmThreadCharacteristics** per richiedere che MMCSS aumenti la priorità del thread in cui viene eseguito PlayExclusiveStream.</span><span class="sxs-lookup"><span data-stu-id="f7083-176">Calls the **AvSetMmThreadCharacteristics** function to request that MMCSS increase the priority of the thread in which PlayExclusiveStream executes.</span></span> <span data-ttu-id="f7083-177">All'arresto dell'esecuzione del flusso, la chiamata alla funzione **AvRevertMmThreadCharacteristics** ripristina la priorità del thread originale.</span><span class="sxs-lookup"><span data-stu-id="f7083-177">(When the stream stops running, the **AvRevertMmThreadCharacteristics** function call restores the original thread priority.)</span></span>

<span data-ttu-id="f7083-178">Per altre informazioni su **AvSetMmThreadCharacteristics** e **AvRevertMmThreadCharacteristics,** vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f7083-178">For more information about **AvSetMmThreadCharacteristics** and **AvRevertMmThreadCharacteristics**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="f7083-179">Durante l'esecuzione del flusso, ogni iterazione del ciclo **while** nell'esempio di codice precedente riempie un buffer endpoint.</span><span class="sxs-lookup"><span data-stu-id="f7083-179">While the stream is running, each iteration of the **while**-loop in the preceding code example fills one endpoint buffer.</span></span> <span data-ttu-id="f7083-180">Tra le iterazioni, la chiamata di funzione **WaitForSingleObject** attende che l'handle di evento sia segnalato.</span><span class="sxs-lookup"><span data-stu-id="f7083-180">Between iterations, the **WaitForSingleObject** function call waits for the event handle to be signaled.</span></span> <span data-ttu-id="f7083-181">Quando l'handle viene segnalato, il corpo del ciclo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7083-181">When the handle is signaled, the loop body does the following:</span></span>

1.  <span data-ttu-id="f7083-182">Chiama il [**metodo IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) per ottenere il buffer successivo.</span><span class="sxs-lookup"><span data-stu-id="f7083-182">Calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method to get the next buffer.</span></span>
2.  <span data-ttu-id="f7083-183">Riempie il buffer.</span><span class="sxs-lookup"><span data-stu-id="f7083-183">Fills the buffer.</span></span>
3.  <span data-ttu-id="f7083-184">Chiama il [**metodo IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) per rilasciare il buffer.</span><span class="sxs-lookup"><span data-stu-id="f7083-184">Calls the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method to release the buffer.</span></span>

<span data-ttu-id="f7083-185">Per altre informazioni su **WaitForSingleObject,** vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f7083-185">For more information about **WaitForSingleObject**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="f7083-186">Se la scheda audio è controllata da un driver WaveRT, la segnalazione dell'handle di evento è associata alle notifiche di trasferimento DMA dall'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="f7083-186">If the audio adapter is controlled by a WaveRT driver, the signaling of the event handle is tied to the DMA-transfer notifications from the audio hardware.</span></span> <span data-ttu-id="f7083-187">Per un dispositivo audio USB o per un dispositivo audio controllato da un driver WaveCyclic o WavePci, la segnalazione dell'handle di evento è associata ai completamenti degli ISP che trasferiscono i dati dal buffer dell'applicazione al buffer hardware.</span><span class="sxs-lookup"><span data-stu-id="f7083-187">For a USB audio device, or for an audio device that is controlled by a WaveCyclic or WavePci driver, the signaling of the event handle is tied to completions of the IRPs that transfer data from the application buffer to the hardware buffer.</span></span>

<span data-ttu-id="f7083-188">L'esempio di codice precedente esegue il push dell'hardware audio e del sistema informatico ai limiti di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f7083-188">The preceding code example pushes the audio hardware and the computer system to their performance limits.</span></span> <span data-ttu-id="f7083-189">In primo luogo, per ridurre la latenza del flusso, l'applicazione pianifica il thread di manutenzione del buffer in modo da usare il periodo minimo del dispositivo supportato dall'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="f7083-189">First, to reduce the stream latency, the application schedules its buffer-servicing thread to use the minimum device period that the audio hardware will support.</span></span> <span data-ttu-id="f7083-190">In secondo momento, per garantire che il thread sia eseguito in modo affidabile all'interno di ogni periodo di dispositivo, la chiamata di funzione **AvSetMmThreadCharacteristics** imposta il parametro TaskName su "Pro Audio", ovvero, in Windows Vista, il nome dell'attività predefinito con la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="f7083-190">Second, to ensure that the thread reliably executes within each device period, the **AvSetMmThreadCharacteristics** function call sets the TaskName parameter to "Pro Audio", which is, in Windows Vista, the default task name with the highest priority.</span></span> <span data-ttu-id="f7083-191">Valutare se i requisiti di temporizzazione dell'applicazione potrebbero essere meno precisi senza compromettere l'utilità.</span><span class="sxs-lookup"><span data-stu-id="f7083-191">Consider whether the timing requirements of your application might be relaxed without compromising its usefulness.</span></span> <span data-ttu-id="f7083-192">Ad esempio, l'applicazione potrebbe pianificare il thread di manutenzione del buffer per l'uso di un periodo più lungo del minimo.</span><span class="sxs-lookup"><span data-stu-id="f7083-192">For example, the application might schedule its buffer-servicing thread to use a period that is longer than the minimum.</span></span> <span data-ttu-id="f7083-193">Un periodo più lungo potrebbe consentire in modo sicuro l'uso di una priorità di thread inferiore.</span><span class="sxs-lookup"><span data-stu-id="f7083-193">A longer period might safely allow the use of a lower thread priority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7083-194">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7083-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7083-195">Gestione dei flussi</span><span class="sxs-lookup"><span data-stu-id="f7083-195">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



