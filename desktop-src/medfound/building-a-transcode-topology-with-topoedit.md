---
description: Questo argomento descrive come creare una topologia di transcodifica in TopoEdit.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Creazione di una topologia transcodifica con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5386af09b04f155295b807523cdb1c5519c946b45228df51d767e9d2a3aabe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959461"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Creazione di una topologia transcodifica con TopoEdit

Questo argomento descrive come creare una topologia di transcodifica in TopoEdit.

> [!Note]  
> Questa funzionalità richiede Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>Per creare una topologia di transcoding

1.  Scegliere **Esegui** rendering **transcodifica dal** menu File .

2.  Nella finestra **di dialogo Seleziona origine** multimediale selezionare il file di origine per la transcoding.
3.  Fare clic su **Apri**.
4.  Nella finestra di dialogo Scegli profilo **transcodifica** selezionare uno dei profili di codifica dall'elenco a discesa.
    > [!Note]  
    > I profili vengono caricati dal file TranscodeProfiles.xml.

     

5.  Nella finestra **di dialogo Scegli file di** destinazione selezionare il nome del file di output.
6.  TopoEdit crea la topologia di transcodifica e visualizza i nodi della topologia nella finestra principale dell'applicazione.
7.  Fare clic **sul pulsante** Riproduci sulla barra degli strumenti per eseguire la sessione multimediale. Attendere il completamento della codifica.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopoEdit carica i profili di codifica dal file TranscodeProfiles.xml. Questo file si trova nella directory Bin di Windows SDK.

Il file inizia con un **elemento TedTranscodeProfiles.** Ogni profilo inizia con un **elemento TedTranscodeProfile.** Ogni profilo è costituito da un set di valori nel formato `<VALUE_NAME Value="VALUE"/>` . Vengono definiti i valori seguenti:



| Valore                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | Byte medi al secondo per il flusso audio. Equivale [**all'attributo \_ MF MT AUDIO \_ \_ AVG BYTES AL \_ \_ \_ SECONDO.**](mf-mt-audio-avg-bytes-per-second-attribute.md)<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | Numero di bit per campione per il flusso audio. Equivale [**all'attributo \_ MF MT AUDIO \_ \_ BITS PER \_ \_ SAMPLE.**](mf-mt-audio-bits-per-sample-attribute.md)<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | Allineamento del blocco per il flusso audio. Equivale [**all'attributo \_ MF MT AUDIO BLOCK \_ \_ \_ ALIGNMENT.**](mf-mt-audio-block-alignment-attribute.md)<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | Valore specifico del codec che definisce il profilo audio. Equivale [all'attributo MF \_ TRANSCODE \_ ENCODINGPROFILE.](mf-transcode-encodingprofile.md) <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**AudioFormat**<br/>                                                                                     | Sottotipo audio codificato. Equivale [**all'attributo \_ MF MT \_ SUBTYPE.**](mf-mt-subtype-attribute.md)<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | Numero di canali nel flusso audio. Equivale [**all'attributo \_ MF MT AUDIO NUM \_ \_ \_ CHANNELS.**](mf-mt-audio-num-channels-attribute.md)<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | Frequenza di campionamento del flusso audio, in campioni al secondo. Equivale [**all'attributo \_ MF MT AUDIO SAMPLES \_ AL \_ \_ \_ SECONDO.**](mf-mt-audio-samples-per-second-attribute.md)<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**ContainerType**<br/>                                                                             | Tipo di contenitore di file. Equivale [all'attributo MF \_ TRANSCODE \_ CONTAINERTYPE.](mf-transcode-containertype.md) <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**Profilename**<br/>                                                                                     | Nome visualizzato del profilo.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Specificare 1 se i metadati non devono essere trasferiti nel file di output oppure 0 se i metadati devono essere trasferiti. Equivale [all'attributo MF \_ TRANSCODE \_ SKIP METADATA \_ \_ TRANSFER.](mf-transcode-skip-metadata-transfer.md)<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**VideoBitrate**<br/>                                                                                 | Velocità in bit media del video. Equivale [**all'attributo \_ MF MT \_ AVG \_ BITRATE.**](mf-mt-avg-bitrate-attribute.md) <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | Valore specifico del codec che definisce la qualità di codifica. Equivale [all'attributo MF \_ TRANSCODE \_ QUALITYVSSPEED.](mf-transcode-qualityvsspeed.md) <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | Valore specifico del codec che definisce il profilo video. Equivale [all'attributo MF \_ TRANSCODE \_ ENCODINGPROFILE.](mf-transcode-encodingprofile.md) <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**VideoFormat**<br/>                                                                                     | Sottotipo video codificato. Equivale [**all'attributo \_ MF MT \_ SUBTYPE.**](mf-mt-subtype-attribute.md)<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | Altezza del video di output. Equivale [**all'attributo \_ MF MT FRAME \_ \_ SIZE.**](mf-mt-frame-size-attribute.md)<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | Denominatore della frequenza dei fotogrammi del video di output. Equivale [**all'attributo \_ MF MT FRAME \_ \_ RATE.**](mf-mt-frame-rate-attribute.md)<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | Numeratore della frequenza fotogrammi del video di output. Equivale [**all'attributo \_ MF MT FRAME \_ \_ RATE.**](mf-mt-frame-rate-attribute.md)<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | Larghezza del video di output. Equivale [**all'attributo \_ MF MT FRAME \_ \_ SIZE.**](mf-mt-frame-size-attribute.md)<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | Denominatore delle proporzioni pixel (PAR) del video di output. Equivale [**all'attributo \_ MF MT PIXEL ASPECT \_ \_ \_ RATIO.**](mf-mt-pixel-aspect-ratio-attribute.md) <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | Numeratore del par del video di output. Equivale [**all'attributo \_ MF MT PIXEL ASPECT \_ \_ \_ RATIO.**](mf-mt-pixel-aspect-ratio-attribute.md) <br/>                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TopoModifica](topoedit.md)
</dt> </dl>

 

 




