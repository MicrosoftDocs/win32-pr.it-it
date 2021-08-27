---
description: Questo articolo contiene indicazioni per la generazione di istogrammi durante la decodifica di video usando le API video Direct3D 11 o 12.
ms.assetid: ''
title: Istogrammi di decodifica video Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 94371fd68c981a98c4ba629822f928e148c230565b5103dfaa2350543bbe9a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061631"
---
# <a name="direct3d-video-decode-histograms"></a>Istogrammi di decodifica video Direct3D

Questo articolo contiene indicazioni per la generazione di istogrammi durante la decodifica di video usando le API video Direct3D 11 o 12.

## <a name="checking-the-video-device-for-histogram-capabilities"></a>Controllo delle funzionalità dell'istogramma nel dispositivo video

Prima di tentare di generare istogrammi, è necessario verificare se il dispositivo video corrente supporta la funzionalità dell'istogramma di decodifica video.

### <a name="direct3d-12"></a>Direct3D 12

Chiamare [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) per verificare i dettagli di supporto per le operazioni di decodifica video Direct3D 12. Passare il **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** dall'enumerazione [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) per specificare che si richiede il supporto per gli istogrammi di decodifica video.

### <a name="direct3d-11"></a>Direct3D 11

Chiamare [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) e passare il valore **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** del [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) per determinare se gli istogrammi sono supportati per il dispositivo corrente.

## <a name="enabling-histogram-during-decode"></a>Abilitazione dell'istogramma durante la decodifica

La raccolta di dati dell'istogramma viene abilitata dal chiamante che fornisce i buffer in cui vengono archiviati i dati dell'istogramma.  Un buffer di output dell'istogramma Null per un determinato componente indica che la raccolta di istogrammi è disabilitata.

### <a name="direct3d-12"></a>Direct3D 12

Per fornire buffer di output per ricevere i dati dell'istogramma usando Direct3D 12, è necessario creare l'elenco di comandi di decodifica usando il metodo [ID3D12VideoDecodeCommandList1::D ecodeFrame1.](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) Questo metodo accetta una [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) come argomento. **D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** un campo di tipo [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), che consente di specificare [id3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) in cui vengono restituiti i dati dell'istogramma.

### <a name="direct3d-11"></a>Direct3D 11

L'interfaccia [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) fornisce il metodo [DecoderBeginFrame1,](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) che consente di fornire una o più interfacce [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) in cui verranno restituiti i dati dell'istogramma. La [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) specificare i componenti per cui si desidera generare i dati dell'istogramma.


## <a name="buffer-format"></a>Formato del buffer

L'output dell'istogramma di decodifica viene scritto in un buffer come contatore integer per componente.  Il formato del buffer è un valore a 32 bit per ogni contenitore.  Un dispositivo può usare una profondità in bit del contatore intero inferiore a 32 bit, ma deve essere di 16, 24 o 32 bit.  In tal caso, il valore del contatore viene archiviato nei bit inferiori e i bit inutilizzati superiori sono pari a zero.  Quando il conteggio di un bin supera il valore massimo, il dispositivo imposta invece il valore massimo. I dispositivi segnalano il numero di contenitori supportati, che deve essere un valore di potenza pari a 2.  Il numero minimo di bin necessari per i dispositivi che supportano questa funzionalità è 64. 

È necessario specificare un buffer con un offset allineato a 256 byte e una dimensione che sia il numero supportato di bin moltiplicati per la dimensione del bin (4 byte) per ogni componente richiesto.  Il posizionamento del contenitore è determinato da:

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


Quando un formato definisce i bit utili di un componente come minori del numero di bit di archiviazione (ad esempio, P010 usa i primi 10 bit di 16 bit di archiviazione dei componenti), vengono considerati solo i bit utili (P010 viene considerato come un valore a 10 bit). 

Il dispositivo video segnala i componenti supportati.  Se il chiamante non vuole un istogramma per un determinato componente, specifica nullptr.  Se il driver non supporta un istogramma per un determinato componente, il buffer dell'istogramma di tale componente deve essere nullptr.

Quando sono supportati più componenti, l'applicazione può richiedere qualsiasi combinazione di componenti per decodifica frame.  Ad esempio, se l'hardware segnala il supporto per i componenti Y, U e V, l'applicazione può richiedere l'istogramma Y solo per il frame 1, l'istogramma U solo per il frame 2 e l'istogramma V solo per il fotogramma 3.  Possono anche richiedere qualsiasi combinazione di due componenti o di tutti e tre i componenti.

Le applicazioni forniscono un offset e un handle di buffer separati per ogni componente richiesto.  Questo puntatore può puntare alla stessa risorsa di un altro componente o a una risorsa separata.  L'offset consente di posizionare più componenti nello stesso buffer, ma l'area di output specificata dall'offset e dalle dimensioni dell'istogramma non deve sovrapporsi a un altro output del componente istogramma.  L'istogramma può anche essere scritto nello stesso buffer di altri contenuti non correlati, ad esempio quando viene usato in una strategia di sottoallocazione delle risorse.


Il runtime D3D verifica che i chiamanti abilitino solo l'istogramma per i componenti supportati, che l'offset del buffer sia allineato e che le dimensioni del buffer siano sufficienti per il numero indicato di contenitori.


## <a name="protected-content"></a>Contenuto protetto

I buffer dell'istogramma devono avere la stessa protezione della superficie della superficie di output della decodifica. Se la superficie di output della decodifica non è una risorsa protetta, il buffer dell'istogramma non deve essere una risorsa protetta. Se la superficie di output della decodifica è una risorsa protetta, l'istogramma deve essere una risorsa protetta.








## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>API video 
[Direct3D 12](direct3d-12-video-apis.md) 
 [Media Foundation di programmazione](media-foundation-programming-guide.md)
</dt> </dl>

 

 




