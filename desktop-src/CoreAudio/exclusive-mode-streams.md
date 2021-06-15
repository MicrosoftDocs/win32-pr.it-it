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
# <a name="exclusive-mode-streams"></a>Exclusive-Mode flussi

Come spiegato in precedenza, se un'applicazione apre un flusso in modalità esclusiva, l'applicazione usa esclusivamente il dispositivo endpoint audio che riproduce o registra il flusso. Al contrario, diverse applicazioni possono condividere un dispositivo endpoint audio aprendo flussi in modalità condivisa nel dispositivo.

L'accesso in modalità esclusiva a un dispositivo audio può bloccare i suoni di sistema cruciali, impedire l'interoperabilità con altre applicazioni e altrimenti peggiorare l'esperienza utente. Per attenuare questi problemi, un'applicazione con un flusso in modalità esclusiva in genere cinge il controllo del dispositivo audio quando l'applicazione non è il processo in primo piano o non è attivamente in streaming.

La latenza di flusso è il ritardo intrinseco nel percorso dati che connette il buffer dell'endpoint di un'applicazione a un dispositivo endpoint audio. Per un flusso di rendering, la latenza è il ritardo massimo dal momento in cui un'applicazione scrive un campione in un buffer dell'endpoint al momento in cui il campione viene udito attraverso i parlanti. Per un flusso di acquisizione, la latenza è il ritardo massimo tra il momento in cui un suono entra nel microfono e il momento in cui un'applicazione può leggere l'esempio per tale suono dal buffer dell'endpoint.

Le applicazioni che usano flussi in modalità esclusiva spesso lo fanno perché richiedono latenze basse nei percorsi dei dati tra i dispositivi endpoint audio e i thread dell'applicazione che accedono ai buffer dell'endpoint. In genere, questi thread vengono eseguiti con priorità relativamente elevata e pianificano se stessi per l'esecuzione a intervalli periodici vicini o uguali all'intervallo periodico che separa i passaggi di elaborazione successivi da parte dell'hardware audio. Durante ogni passaggio, l'hardware audio elabora i nuovi dati nei buffer dell'endpoint.

Per ottenere le latenze di flusso più piccole, un'applicazione potrebbe richiedere hardware audio speciale e un sistema di computer che viene caricato leggermente. Se l'hardware audio supera i limiti di temporizzazione o carica il sistema con attività con priorità alta in competizione, potrebbe verificarsi un problema in un flusso audio a bassa latenza. Ad esempio, per un flusso di rendering, può verificarsi un problema se l'applicazione non riesce a scrivere in un buffer dell'endpoint prima che l'hardware audio letta il buffer o se l'hardware non riesce a leggere il buffer prima dell'ora pianificata per la riproduzione del buffer. In genere, un'applicazione che deve essere eseguita su un'ampia gamma di hardware audio e in un'ampia gamma di sistemi deve soddisfare i requisiti di temporizzazione sufficienti per evitare problemi in tutti gli ambienti di destinazione.

Windows Vista offre diverse funzionalità per supportare le applicazioni che richiedono flussi audio a bassa latenza. Come descritto in Componenti [audio](user-mode-audio-components.md)in modalità utente, le applicazioni che eseguono operazioni di importanza critica possono chiamare le funzioni del servizio Utilità di pianificazione classi multimediali (MMCSS) per aumentare la priorità dei thread senza negare le risorse della CPU alle applicazioni con priorità più bassa. Inoltre, il metodo [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) supporta un flag AUDCLNT STREAMFLAGS EVENTCALLBACK che consente al thread di manutenzione del buffer di un'applicazione di pianificare l'esecuzione quando un nuovo buffer diventa disponibile dal \_ \_ dispositivo audio. Usando queste funzionalità, un thread dell'applicazione può ridurre l'incertezza sul momento in cui verrà eseguito, riducendo così il rischio di problemi in un flusso audio a bassa latenza.

È probabile che i driver per le schede audio meno recenti usino l'interfaccia DDI (Device Driver Interface) WaveCyclic o WavePci, mentre i driver per le schede audio più recenti sono più probabili supportino l'interfaccia DDI WaveRT. Per le applicazioni in modalità esclusiva, i driver WaveRT possono offrire prestazioni migliori rispetto ai driver WaveCyclic o WavePci, ma i driver WaveRT richiedono funzionalità hardware aggiuntive. Queste funzionalità includono la possibilità di condividere i buffer hardware direttamente con le applicazioni. Con la condivisione diretta, non è necessario alcun intervento del sistema per trasferire i dati tra un'applicazione in modalità esclusiva e l'hardware audio. Al contrario, i driver WaveCyclic e WavePci sono adatti per le schede audio meno recenti e meno idonee. Queste schede si basano sul software di sistema per il trasporto di blocchi di dati (collegati a pacchetti di richieste di I/O di sistema o IRP) tra i buffer dell'applicazione e i buffer hardware. Inoltre, i dispositivi audio USB si basano sul software di sistema per il trasporto dei dati tra i buffer dell'applicazione e i buffer hardware. Per migliorare le prestazioni delle applicazioni in modalità esclusiva che si connettono a dispositivi audio che si basano sul sistema per il trasporto dei dati, WASAPI aumenta automaticamente la priorità dei thread di sistema che trasferiscono i dati tra le applicazioni e l'hardware. WASAPI usa MMCSS per aumentare la priorità dei thread. In Windows Vista, se un thread di sistema gestisce il trasporto dei dati per un flusso di riproduzione audio in modalità esclusiva con un formato PCM e un periodo del dispositivo inferiore a 10 millisecondi, WASAPI assegna il nome dell'attività MMCSS "Pro Audio" al thread. Se il periodo del dispositivo del flusso è maggiore o uguale a 10 millisecondi, WASAPI assegna il nome dell'attività MMCSS "Audio" al thread. Per altre informazioni sui DDI WaveCyclic, WavePci e WaveRT, vedere la documentazione di Windows DDK. Per informazioni sulla selezione di un periodo di dispositivo appropriato, vedere [**IAudioClient::GetDevicePeriod.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)

Come descritto in Session [Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) fornisce le interfacce [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) per controllare i livelli di volume dei flussi audio in modalità condivisa. Tuttavia, i controlli in queste interfacce non hanno alcun effetto sui flussi in modalità esclusiva. Al contrario, le applicazioni che gestiscono flussi in modalità esclusiva usano in genere [**l'interfaccia IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) nell'API [EndpointVolume](endpointvolume-api.md) per controllare i livelli di volume di tali flussi. Per informazioni su questa interfaccia, vedere [Endpoint Volume Controls](endpoint-volume-controls.md).

Per ogni dispositivo di riproduzione e dispositivo di acquisizione nel sistema, l'utente può controllare se il dispositivo può essere usato in modalità esclusiva. Se l'utente disabilita l'uso in modalità esclusiva del dispositivo, il dispositivo può essere usato per riprodurre o registrare solo flussi in modalità condivisa.

Se l'utente consente l'uso in modalità esclusiva del dispositivo, l'utente può anche controllare se una richiesta da parte di un'applicazione di usare il dispositivo in modalità esclusiva presciderà l'uso del dispositivo da parte di applicazioni che potrebbero attualmente riprodurre o registrare flussi in modalità condivisa attraverso il dispositivo. Se la preemption è abilitata, una richiesta da parte di un'applicazione di assumere il controllo esclusivo del dispositivo ha esito positivo se il dispositivo non è attualmente in uso o se il dispositivo è in uso in modalità condivisa, ma la richiesta ha esito negativo se un'altra applicazione ha già il controllo esclusivo del dispositivo. Se la preemption è disabilitata, una richiesta da parte di un'applicazione di assumere il controllo esclusivo del dispositivo ha esito positivo se il dispositivo non è attualmente in uso, ma la richiesta ha esito negativo se il dispositivo è già in uso in modalità condivisa o in modalità esclusiva.

In Windows Vista le impostazioni predefinite per un dispositivo endpoint audio sono le seguenti:

-   Il dispositivo può essere usato per riprodurre o registrare flussi in modalità esclusiva.
-   Una richiesta di usare un dispositivo per riprodurre o registrare un flusso in modalità esclusiva ha la presunzione di qualsiasi flusso in modalità condivisa attualmente riprodotto o registrato tramite il dispositivo.

**Per modificare le impostazioni della modalità esclusiva di un dispositivo di riproduzione o registrazione**

1.  Fare clic con il pulsante destro del mouse sull'icona dell'altoparlante nell'area di notifica, che si trova sul lato destro della barra delle applicazioni, e selezionare **Dispositivi** di riproduzione o Dispositivi **di registrazione.** In alternativa, eseguire il pannello di controllo multimediale di Windows, Mmsys.cpl, da una finestra del prompt dei comandi. Per altre informazioni, vedere Note in [Costanti DEVICE \_ STATE \_ XXX.](device-state-xxx-constants.md)
2.  Quando viene **visualizzata la** finestra Audio, selezionare **Playback (Riproduzione)** **o Recording (Registrazione).** Selezionare quindi una voce nell'elenco dei nomi di dispositivo e fare clic su **Proprietà**.
3.  Quando viene **visualizzata la** finestra Proprietà , fare clic **su Avanzate**.
4.  Per consentire alle applicazioni di usare il dispositivo in modalità esclusiva, selezionare la casella Consenti alle applicazioni di assumere il controllo **esclusivo del dispositivo.** Per disabilitare l'uso in modalità esclusiva del dispositivo, deselezionare la casella di controllo.
5.  Se è abilitato l'uso in modalità esclusiva del dispositivo, è possibile specificare se una richiesta di controllo esclusivo del dispositivo avrà esito positivo se il dispositivo è attualmente in riproduzione o sta registrando flussi in modalità condivisa. Per assegnare la priorità alle applicazioni in modalità esclusiva rispetto alle applicazioni in modalità condivisa, selezionare la casella Assegnare la priorità **alle applicazioni in modalità esclusiva**. Per negare la priorità delle applicazioni in modalità esclusiva rispetto alle applicazioni in modalità condivisa, deselezionare la casella di controllo.

L'esempio di codice seguente illustra come riprodurre un flusso audio a bassa latenza in un dispositivo di rendering audio configurato per l'uso in modalità esclusiva:


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



Nell'esempio di codice precedente la funzione PlayExclusiveStream viene eseguita nel thread dell'applicazione che gestisce i buffer dell'endpoint durante la riproduzione di un flusso di rendering. La funzione accetta un singolo parametro, pMySource, che è un puntatore a un oggetto che appartiene a una classe definita dal client, MyAudioSource. Questa classe ha due funzioni membro, LoadData e SetFormat, chiamate nell'esempio di codice. MyAudioSource è descritto in [Rendering di un flusso.](rendering-a-stream.md)

La funzione PlayExclusiveStream chiama una funzione helper, GetStreamFormat, che negozia con il dispositivo di rendering predefinito per determinare se il dispositivo supporta un formato di flusso in modalità esclusiva adatto all'uso da parte dell'applicazione. Il codice per la funzione GetStreamFormat non viene visualizzato nell'esempio di codice. ciò è dovuto al fatto che i dettagli dell'implementazione dipendono interamente dai requisiti dell'applicazione. Tuttavia, l'operazione della funzione GetStreamFormat può essere descritta semplicemente: chiama il metodo [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) una o più volte per determinare se il dispositivo supporta un formato appropriato. I requisiti dell'applicazione determinano quali formati GetStreamFormat presenta al metodo **IsFormatSupported** e l'ordine in cui vengono presentati. Per altre informazioni su **IsFormatSupported,** vedere [Formati di dispositivo.](device-formats.md)

Dopo la chiamata a GetStreamFormat, la funzione PlayExclusiveStream chiama il metodo [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) per ottenere il periodo minimo di dispositivo supportato dall'hardware audio. La funzione chiama quindi il metodo [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) per richiedere una durata del buffer uguale al periodo minimo. Se la chiamata ha esito positivo, il metodo **Initialize** alloca due buffer dell'endpoint, ognuno dei quali ha una durata uguale al periodo minimo. Successivamente, quando inizia l'esecuzione del flusso audio, l'applicazione e l'hardware audio condivideranno i due buffer in modalità "ping-pong", ovvero mentre l'applicazione scrive in un buffer, l'hardware legge dall'altro buffer.

Prima di avviare il flusso, la funzione PlayExclusiveStream esegue le operazioni seguenti:

-   Crea e registra l'handle dell'evento tramite il quale riceverà notifiche quando i buffer saranno pronti per il riempimento.
-   Riempie il primo buffer con i dati provenienti dall'origine audio per ridurre il ritardo da quando inizia l'esecuzione del flusso a quando viene udito il suono iniziale.
-   Chiama la **funzione AvSetMmThreadCharacteristics** per richiedere che MMCSS aumenti la priorità del thread in cui viene eseguito PlayExclusiveStream. All'arresto dell'esecuzione del flusso, la chiamata alla funzione **AvRevertMmThreadCharacteristics** ripristina la priorità del thread originale.

Per altre informazioni su **AvSetMmThreadCharacteristics** e **AvRevertMmThreadCharacteristics,** vedere la documentazione Windows SDK.

Durante l'esecuzione del flusso, ogni iterazione del ciclo **while** nell'esempio di codice precedente riempie un buffer endpoint. Tra le iterazioni, la chiamata di funzione **WaitForSingleObject** attende che l'handle di evento sia segnalato. Quando l'handle viene segnalato, il corpo del ciclo esegue le operazioni seguenti:

1.  Chiama il [**metodo IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) per ottenere il buffer successivo.
2.  Riempie il buffer.
3.  Chiama il [**metodo IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) per rilasciare il buffer.

Per altre informazioni su **WaitForSingleObject,** vedere la documentazione Windows SDK.

Se la scheda audio è controllata da un driver WaveRT, la segnalazione dell'handle di evento è associata alle notifiche di trasferimento DMA dall'hardware audio. Per un dispositivo audio USB o per un dispositivo audio controllato da un driver WaveCyclic o WavePci, la segnalazione dell'handle di evento è associata ai completamenti degli ISP che trasferiscono i dati dal buffer dell'applicazione al buffer hardware.

L'esempio di codice precedente esegue il push dell'hardware audio e del sistema informatico ai limiti di prestazioni. In primo luogo, per ridurre la latenza del flusso, l'applicazione pianifica il thread di manutenzione del buffer in modo da usare il periodo minimo del dispositivo supportato dall'hardware audio. In secondo momento, per garantire che il thread sia eseguito in modo affidabile all'interno di ogni periodo di dispositivo, la chiamata di funzione **AvSetMmThreadCharacteristics** imposta il parametro TaskName su "Pro Audio", ovvero, in Windows Vista, il nome dell'attività predefinito con la priorità più alta. Valutare se i requisiti di temporizzazione dell'applicazione potrebbero essere meno precisi senza compromettere l'utilità. Ad esempio, l'applicazione potrebbe pianificare il thread di manutenzione del buffer per l'uso di un periodo più lungo del minimo. Un periodo più lungo potrebbe consentire in modo sicuro l'uso di una priorità di thread inferiore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 



