---
description: Questo articolo contiene indicazioni generali per l'uso delle API video Direct3D 12.
ms.assetid: ''
title: Panoramica di Direct3D 12 video
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: b21587f2784b34131da9c050655b6f3fbe43582d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524562"
---
# <a name="direct3d-12-video-overview"></a>Panoramica di Direct3D 12 video

Questo articolo contiene indicazioni generali per l'uso delle API video Direct3D 12.

## <a name="about-direct3d-12-video"></a>Informazioni sul video di Direct3D 12

L'interfaccia video Direct3D 12 fornisce un nuovo modo per le app per implementare la decodifica video e il processo. L'interfaccia Direct3D 12 è diversa dall'interfaccia Direct3D 11 precedente perché è stata progettata per essere coerente con i principi e lo stile di Direct3D 12, che include quanto segue:

- Fornire agli sviluppatori maggiore controllo
 - Allocazione della memoria accessibile dall'hardware
 - Thread CPU usati per generare comandi di invio &
   - Generazione e invio indipendenti
   - Senza blocco
 - Pianificazione del lavoro hardware
- Viene illustrata la funzionalità esistente, inclusa la maggior parte delle funzionalità video Direct3D 11, ma allo stesso tempo mantiene la semplicità e la facilità d'uso
- Potenza e prestazioni delle applicazioni Direct3D 12 principali uguali o migliori di Direct3D 11
- Coerenza con altre API Direct3D 12
- Interoperabilità con le API grafiche esistenti


## <a name="video-decoding"></a>Decodifica video

Le sezioni seguenti descrivono alcune delle attività necessarie per implementare la decodifica video di Direct3D 12.

### <a name="query-for-decoding-capabilities"></a>Query per la decodifica delle funzionalità

Chiamare [ID3D12VideoDevice:: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) per verificare i dettagli del supporto per le operazioni di decodifica video di Direct3D 12. Passare un valore dall'enumerazione [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) per specificare la funzionalità per cui si richiedono le informazioni di supporto.

### <a name="create-the-video-decoder"></a>Creare il decodificatore video

Chiamare [ID3D12VideoDevice:: CreateVideoDecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) per creare un'istanza dell'interfaccia [ID3D12VideoDecoder](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) . Il decodificatore include lo stato di una sessione di decodifica, inclusi i dati correlati al riferimento, ad esempio i vettori di movimento.  In caso di modifica della risoluzione o di una modifica [MaxDecodePictureBufferCount](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) , l'oggetto decoder viene ricreato. La larghezza e l'altezza della decodifica specificano la risoluzione del flusso nativa prima di qualsiasi scala.  Il numero massimo di DPB (Decode Picture buffer) specifica il numero di DPB più grande che può essere utilizzato senza ricreare il decodificatore video.

Il decodificatore può essere usato per registrare i comandi da più elenchi di comandi, ma può essere associato solo a un elenco di comandi alla volta.  L'applicazione è responsabile della sincronizzazione dell'accesso al decodificatore.

### <a name="create-the-video-decoder-heap"></a>Creare l'heap del decodificatore video 

Chiamare [ID3D12VideoDevice:: CreateVideoDecoderHeap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) per creare un'istanza dell'interfaccia [ID3D12VideoDecoderHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) . Questo oggetto contiene le risorse e lo stato dei driver dipendenti dalla risoluzione.

### <a name="decoding-a-frame"></a>Decodifica di un frame

Tutti i parametri di input e di output per le operazioni di elaborazione video sono organizzati in una struttura di parametri di input, [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)e una struttura di parametri di output, [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments).
L'applicazione gestisce i frame di riferimento e, di conseguenza, deve impostare i frame di riferimento per ogni operazione di decodifica.
Quando l'elenco dei comandi viene registrato correttamente, chiamare [ID3D12CommandQueue:: oggetti executecommandlist](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) nella coda dei comandi video per inviare la decodifica del frame alla GPU.


### <a name="enabling-decoder-output-conversions"></a>Abilitazione delle conversioni di output del decodificatore
Se il decodificatore supporta la conversione, abilitare le conversioni desiderate compilando correttamente la struttura [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) . Il formato e le risoluzioni dell'output desiderato rispetto all'output nativo del decodificatore vengono comunicati tramite la differenza nello spazio dei colori e nelle risoluzioni specificate nei parametri di conversione.

##  <a name="querying-decoding-status"></a>Esecuzione di query sullo stato di decodifica 
Usare i metodi [ID3D12VideoDecodeCommandList:: BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) e [ID3D12VideoDecodeCommandList:: EndQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) per eseguire una query sullo stato dell'operazione di decodifica.

La struttura [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) viene utilizzata per descrivere le statistiche di decodifica dei video. Per ottenere un'istanza di questa struttura, chiamare [ID3D12VideoDecodeCommandList:: EndQuery](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery), passando il valore del tipo di query dell'heap di [D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Si noti che questa query non usa [ID3D12VideoDecodeCommandList:: BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery).

## <a name="video-processing"></a>Elaborazione video

Le API di Direct3D 12 video adottano un approccio semplificato all'elaborazione video, eliminando funzionalità di Direct3D 11 che non sono state ampiamente utilizzate e rimuovendo i controlli delle funzionalità che sono obbligatori tra i dispositivi. Il processo di enumerazione per l'elaborazione video viene eliminato. In alternativa, chiamare [ID3D12VideoDevice:: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) che consente a un'app di identificare le funzionalità del processore video. I formati video, interlacci, stereo e i prezzi desiderati vengono forniti come input per **CheckFeatureSupport**.

### <a name="removed-capabilities"></a>Funzionalità rimosse

Le funzionalità seguenti di Direct3D 11 non sono supportate nell'elaborazione video Direct3D 12:
- Tariffe personalizzate.  È invece prevista una frequenza di input e di output durante la registrazione del comando [ID3D12VideoProcessCommandList::P rocessframes](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) .
- Sono ora disponibili solo due modalità di deinterlacciamento: [Bob](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) e [Custom](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags). Sono state eliminate altre modalità. CUSTOM è una modalità di deinterlacciamento di alta qualità fornita dal fornitore dell'hardware.
- Tutti i formati stereo facoltativi in [D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) non sono più supportati. In alternativa, [nono](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [orizzontale](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [verticale](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)e [separato](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) sono obbligatori per tutti i dispositivi hardware se lo stereo è supportato.
- Non esiste alcun equivalente per [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) o [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps). I formati di input e di output sono invece argomenti per la creazione del processore video e, in quel momento, dovrebbero essere noti se il processore video può o non può eseguire l'operazione con il formato specificato. Il [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) viene utilizzato per indicare se le funzionalità di elaborazione automatica sono disponibili.
- Non esiste alcun equivalente per [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Non esiste alcun equivalente per [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Quando si esegue la conversione da stereo a mono, si presuppone che la visualizzazione Baseline sia 0.
- L'elaborazione video Direct3D 12 non supporta la conversione da mono a stereo e non è disponibile alcun supporto per l'offset mono. 


### <a name="creating-a-video-processor"></a>Creazione di un processore video

Chiamare [ID3D12VideoDevice:: CreateVideoProcessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) per creare un'istanza di [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor). Il processore video include lo stato di una sessione di elaborazione video, tra cui memoria intermedia richiesta, dati di elaborazione memorizzati nella cache o altro spazio di lavoro temporaneo. Gli argomenti di creazione del processore video specificano le operazioni eseguite o disponibili in [ID3D12VideoProcessCommandList1::P rocessframes1](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) tempo.  Le allocazioni di driver per eseguire l'operazione di elaborazione video (ad esempio intermedi) vengono allocate in fase di creazione del processore video.  Utilizzare [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) per determinare in anticipo le dimensioni di allocazione del processore video.

Il processore video può essere usato solo per registrare i comandi da più elenchi di comandi, ma può essere associato solo a un elenco di comandi alla volta.  L'applicazione è responsabile della sincronizzazione dell'accesso al processore video.  L'applicazione deve anche registrare i comandi di elaborazione video nel video procoessor nell'ordine in cui vengono eseguiti sulla GPU.

Tutti gli argomenti di input e di output per le operazioni di elaborazione video sono organizzati in una struttura di argomenti di input, in [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)e in una struttura di argomenti di output, [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments). L'applicazione deve chiamare [ID3D12VideoProcessCommandList::P rocessframes](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) per registrare l'operazione di elaborazione video che vuole eseguire. 

Quando viene registrato l'elenco di comandi, chiamare [ID3D12CommandQueue:: oggetti executecommandlist](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) nella coda dei comandi video per inviare l'elaborazione del frame alla GPU.


## <a name="tiers"></a>Livelli

Il video Direct3D 12 definisce i livelli che raggruppano le funzionalità dei dispositivi hardware, in modo che l'app possa avere un minor numero di percorsi di codice per soddisfare l'ampia gamma di hardware. I livelli vengono specificati con l'enumerazione [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) .

In tutti i livelli, saranno disponibili gli elementi seguenti:

- Non è necessaria la ricreazione del decodificatore per le modifiche della risoluzione. Per la modifica della risoluzione è necessario ricreare solo l'heap del decodificatore.
- Tutti i frame di riferimento verranno gestiti dall'app. Ciò consente al sistema di risparmiare memoria, in quanto non è necessario allocare il numero massimo di DPBs al momento della creazione del decodificatore in alcuni livelli e offre la flessibilità delle app negli scenari di modifica della risoluzione.

Si noti che i livelli sono i superset. Un'app può decidere di eseguire il livello 1 e non usare le funzionalità di livello superiore, che è consentita, ma potrebbe non offrire prestazioni ottimali. Per ulteriori informazioni sulle funzionalità associate a diversi livelli di livello, vedere [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier).

## <a name="reference-frames"></a>Frame di riferimento

Con il video Direct3D 12, i frame di riferimento vengono passati in modo esplicito. Questo consente di utilizzare in modo chiaro una matrice di trame o matrici di trama durante la decodifica dei frame. Non è necessario che l'app passi esattamente lo stesso handle di risorsa quando viene usato come riferimento; potrebbe, ad esempio, decidere di copiare una risorsa in un'altra e quindi passare la copia invece di quella originale. Gli indici DXVA *RefFrameList* e *CurrPic* vengono comunque usati dal driver per archiviare i dati rilevanti per ogni frame decodificato.


## <a name="directx-12-fences"></a>Recinzioni DirectX 12

In DirectX 12, l'app è responsabile della sincronizzazione dell'accesso ai propri buffer. Per il caso di decodifica, sarà necessario aggiungere i limiti ai buffer di input e ai buffer di output. A ogni limite è associato un valore e vengono usati per la sincronizzazione dei motori della CPU e dell'hardware. Per altre informazioni, vedere [uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12).

Un'implementazione tipica avrà una recinzione per ogni buffer di input. Nel caso dei buffer di input, è possibile che il buffer sia disponibile prima di eseguire l'intero processo di decodifica. Il sistema ignorerà questo caso e presuppone che il buffer di input sia disponibile al termine della decodifica.
Un'implementazione di in genere include anche una recinzione per ogni buffer di output. Nel caso di invio dell'output al compositor, ad esempio, è necessario un limite che viene segnalato al termine della presentazione del frame, a indicare che l'output è nuovamente disponibile per il decodificatore.


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>API video Direct3D 
[12](direct3d-12-video-apis.md) 
 [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
