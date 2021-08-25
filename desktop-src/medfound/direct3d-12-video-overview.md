---
description: Questo articolo contiene indicazioni generali per l'uso delle API video Direct3D 12.
ms.assetid: ''
title: Panoramica del video Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 561ceba8a3110d6aa7e9a336430c0a14ddb45bc5707c650588a08c391cd65863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828321"
---
# <a name="direct3d-12-video-overview"></a>Panoramica del video Direct3D 12

Questo articolo contiene indicazioni generali per l'uso delle API video Direct3D 12.

## <a name="about-direct3d-12-video"></a>Informazioni su Direct3D 12 Video

L'interfaccia video Direct3D 12 offre un nuovo modo per le app di implementare la decodifica e il processo video. L'interfaccia Direct3D 12 è diversa dall'interfaccia Direct3D 11 precedente perché è stata progettata per essere coerente con i principi e lo stile di Direct3D 12, che include quanto segue:

- Offrire agli sviluppatori un maggiore controllo
 - Allocazione di memoria accessibile dall'hardware
 - Thread CPU usati per generare & comandi di invio
   - Generazione e invio indipendenti
   - Senza blocco
 - Pianificazione del lavoro hardware
- Illustra le funzionalità esistenti, tra cui la maggior parte delle funzionalità video Direct3D 11, ma allo stesso tempo tiene presente la semplicità e la facilità d'uso
- Potenza e prestazioni delle principali applicazioni Direct3D 12 uguali o superiori a Direct3D 11
- Coerenza con altre API Direct3D 12
- Interoperabilità con le API grafiche esistenti


## <a name="video-decoding"></a>Decodifica video

Le sezioni seguenti descrivono alcune delle attività necessarie per l'implementazione della decodifica video Direct3D 12.

### <a name="query-for-decoding-capabilities"></a>Eseguire query per le funzionalità di decodifica

Chiamare [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) per verificare i dettagli di supporto per le operazioni di decodifica video Direct3D 12. Passare un valore [dall'enumerazione D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) per specificare la funzionalità per cui si richiedono informazioni di supporto.

### <a name="create-the-video-decoder"></a>Creare il decodificatore video

Chiamare [ID3D12VideoDevice::CreateVideoDecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) per creare un'istanza [dell'interfaccia ID3D12VideoDecoder.](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) Il decodificatore contiene lo stato per una sessione di decodifica, inclusi i dati correlati al riferimento, ad esempio vettori di movimento.  In caso di modifica della risoluzione o di una modifica [di MaxDecodePictureBufferCount,](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) l'oggetto decodificatore viene ricreato. La larghezza e l'altezza della decodifica specificano la risoluzione del flusso nativo prima di qualsiasi scala.  Il numero massimo di DPB (Decode Picture Buffer) specifica il numero DPB più grande che può essere usato senza ricreare il decodificatore video.

Il decodificatore può essere usato per registrare i comandi da più elenchi di comandi, ma può essere associato a un solo elenco di comandi alla volta.  L'applicazione è responsabile della sincronizzazione dell'accesso al decodificatore.

### <a name="create-the-video-decoder-heap"></a>Creare l'heap del decodificatore video 

Chiamare [ID3D12VideoDevice::CreateVideoDecoderHeap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) per creare un'istanza [dell'interfaccia ID3D12VideoDecoderHeap.](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) Questo oggetto contiene le risorse e lo stato dei driver dipendenti dalla risoluzione.

### <a name="decoding-a-frame"></a>Decodifica di un frame

Tutti i parametri di input e output per le operazioni di elaborazione video sono organizzati in una struttura di parametri di input, [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)e in una struttura di parametri di output, [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments).
L'applicazione gestisce i frame di riferimento e, di conseguenza, deve impostare i fotogrammi di riferimento per ogni operazione di decodifica.
Quando l'elenco di comandi viene registrato correttamente, chiamare [ID3D12CommandQueue::ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) nella coda di comandi video per inviare la decodifica dei fotogrammi alla GPU.


### <a name="enabling-decoder-output-conversions"></a>Abilitazione delle conversioni di output del decodificatore
Se il decodificatore supporta la conversione, abilitare le conversioni desiderate compilando correttamente D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS [struttura.](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) Il formato e le risoluzioni dell'output desiderato rispetto all'output nativo del decodificatore vengono comunicati tramite la differenza nello spazio colore e nelle risoluzioni specificate nei parametri di conversione.

##  <a name="querying-decoding-status"></a>Esecuzione di query sullo stato di decodifica 
Usare i metodi [ID3D12VideoDecodeCommandList::BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) e [ID3D12VideoDecodeCommandList::EndQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) per eseguire una query sullo stato dell'operazione di decodifica.

La [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) struttura viene usata per descrivere le statistiche di decodifica video. Per ottenere un'istanza di questa struttura chiamare [ID3D12VideoDecodeCommandList::EndQuery](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery), passando il valore del tipo di query heap [D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Si noti che questa query non usa [ID3D12VideoDecodeCommandList::BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery).

## <a name="video-processing"></a>Elaborazione video

Le API video Direct3D 12 hanno un approccio semplificato all'elaborazione video, eliminando le funzionalità di Direct3D 11 che non sono state ampiamente usate e rimuovendo i controlli delle funzionalità per le funzionalità obbligatorie nei dispositivi. Il processo di enumerazione per l'elaborazione video è stato eliminato. Chiamare invece [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) che consente a un'app di identificare le funzionalità del processore video. Il video desiderato, l'interlacciamento, i formati stereo e le frequenze vengono forniti come input per **CheckFeatureSupport**.

### <a name="removed-capabilities"></a>Funzionalità rimosse

Le funzionalità seguenti di Direct3D 11 non sono supportate nell'elaborazione video Direct3D 12:
- Tariffe personalizzate.  Durante la registrazione dei comandi [ID3D12VideoProcessCommandList::P rocessFrames](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) è invece presente una frequenza di input e output.
- Sono ora disponibili solo due modalità di dinterlazione: [BOB](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) e [CUSTOM.](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) Sono state eliminate altre modalità. CUSTOM è una modalità di dinterlacing di alta qualità fornita dal fornitore dell'hardware.
- Tutti i formati stereo [facoltativi](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) D3D11_VIDEO_PROCESSOR_STEREO_CAPS non sono più supportati. [Nono, horizontal,](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) [](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) [vertical](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)e [separate](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) sono invece obbligatori per tutti i dispositivi hardware se è supportato stereo.
- Non esiste alcun equivalente [per](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) D3D11_VIDEO_PROCESSOR_FORMAT_CAPS o [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps). I formati di input e output sono invece argomenti per la creazione del processore video e, a quel tempo, devono essere noti se il processore video può o non può eseguire l'operazione con il formato specificato. Il [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) viene usato per indicare se sono disponibili funzionalità di elaborazione automatica.
- Non esiste alcun equivalente per [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Non esiste alcun equivalente [per](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps)D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION .
- Quando si esegue la conversione da stereo a mono, si presuppone che la visualizzazione della baseline sia 0.
- L'elaborazione video Direct3D 12 non supporta la conversione di mono in stereo e non è disponibile alcun supporto per l'offset mono. 


### <a name="creating-a-video-processor"></a>Creazione di un processore video

Chiamare [ID3D12VideoDevice::CreateVideoProcessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) per creare un'istanza di [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor). Il processore video mantiene lo stato per una sessione di elaborazione video, tra cui la memoria intermedia richiesta, i dati di elaborazione memorizzati nella cache o altri spazi di lavoro temporanei. Gli argomenti di creazione del processore video specificano le operazioni da eseguire o sono disponibili in [ID3D12VideoProcessCommandList1::P rocessFrames1](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) time.  Le allocazioni dei driver per eseguire l'operazione di elaborazione video (ad esempio, intermedi) vengono allocate al momento della creazione del processore video.  Usare [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) per determinare in anticipo le dimensioni di allocazione del processore video.

Il processore video può essere usato solo per registrare i comandi da più elenchi di comandi, ma può essere associato a un solo elenco di comandi alla volta.  L'applicazione è responsabile della sincronizzazione dell'accesso al processore video.  L'applicazione deve anche registrare i comandi di elaborazione video sul procoessore video nell'ordine in cui vengono eseguiti nella GPU.

Tutti gli argomenti di input e output per le operazioni di elaborazione video sono organizzati in una struttura di argomenti di input, [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)e in una struttura di argomenti di output, [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments). L'applicazione deve chiamare [ID3D12VideoProcessCommandList::P rocessFrames](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) per registrare l'operazione di elaborazione video che vuole eseguire. 

Quando viene registrato l'elenco di comandi, chiamare [ID3D12CommandQueue::ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) nella coda di comandi video per inviare l'elaborazione dei fotogrammi alla GPU.


## <a name="tiers"></a>Livelli

Il video Direct3D 12 definisce i livelli che raggruppano le funzionalità dei dispositivi hardware, in modo che l'app possa avere meno percorsi di codice per soddisfare la varietà di hardware. I livelli vengono specificati con [l'enumerazione D3D12_VIDEO_DECODE_TIER.](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier)

In tutti i livelli saranno disponibili gli elementi seguenti:

- Non è necessaria la ricreazione del decodificatore in caso di modifiche alla risoluzione. Solo l'heap del decodificatore deve essere ricreato in base alla modifica della risoluzione.
- Tutti i frame di riferimento verranno gestiti dall'app. Ciò consente al sistema di risparmiare memoria poiché non è necessario allocare il numero massimo di DDB al momento della creazione del decodificatore in alcuni livelli e offre alle app flessibilità negli scenari di modifica della risoluzione.

Si noti che i livelli sono superset. Un'app può decidere di eseguire il livello 1 e non usare le funzionalità di livello superiore, consentite ma che potrebbero non offrire prestazioni ottimali. Per altre informazioni sulle funzionalità associate a livelli diversi, [vedere](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier)D3D12_VIDEO_DECODE_TIER .

## <a name="reference-frames"></a>Frame di riferimento

Con il video Direct3D 12, i fotogrammi di riferimento vengono passati in modo esplicito. Ciò consente un uso chiaro di matrici di trame o matrici di trame durante la decodifica dei fotogrammi. L'app non deve passare esattamente lo stesso handle di risorsa quando lo si usa come riferimento. può, ad esempio, decidere di copiare una risorsa in un'altra e quindi passare la copia anziché quella originale. Gli indici DXVA *RefFrameList* e *CurrPic* vengono comunque usati dal driver per archiviare i dati rilevanti per ogni frame decodificato.


## <a name="directx-12-fences"></a>Recinti DirectX 12

In DirectX 12 l'app è responsabile della sincronizzazione dell'accesso ai relativi buffer. Per il caso di decodifica, sarà necessario aggiungere recinti ai buffer di input e ai buffer di output. A ogni recinto è associato un valore e vengono usati per la sincronizzazione della CPU e dei motori hardware. Per altre informazioni, vedere [Uso di barriere alle risorse per sincronizzare gli stati delle risorse in Direct3D 12.](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)

Un'implementazione tipica avrà un limite per ogni buffer di input. Nel caso dei buffer di input, è possibile che il buffer sia disponibile prima di eseguire l'intero processo di decodifica. Il sistema ignorerà questo caso e presupporrà che il buffer di input sia disponibile al termine della decodifica.
Un'implementazione avrà in genere anche un limite per ogni buffer di output. Nel caso dell'invio dell'output al compositor, ad esempio, è necessario un limite che viene segnalato al termine della presentazione del frame, a indicare che l'output è nuovamente disponibile per il decodificatore.


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>API Video 
[Direct3D 12](direct3d-12-video-apis.md) 
 [Media Foundation per programmatori](media-foundation-programming-guide.md)
</dt> </dl>

 

 
