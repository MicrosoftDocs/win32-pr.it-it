---
description: In questo argomento viene descritto come creare una topologia di transcodifica in TopoEdit.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Compilazione di una topologia transcode con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ef750b4dd54ef05ab7733cc861d7a09dd5d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524649"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Compilazione di una topologia transcode con TopoEdit

In questo argomento viene descritto come creare una topologia di transcodifica in TopoEdit.

> [!Note]  
> Questa funzionalità richiede Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>Per creare una topologia di transcodifica

1.  Scegliere **rendering transcode** dal menu **file** .

2.  Nella finestra di dialogo **Seleziona origine supporto** selezionare il file di origine per la transcodifica.
3.  Fare clic su **Apri**.
4.  Nella finestra di dialogo **Scegli profilo di transcodifica** selezionare uno dei profili di codifica dall'elenco a discesa.
    > [!Note]  
    > I profili vengono caricati dal file TranscodeProfiles.xml.

     

5.  Nella finestra di dialogo **Scegli file di destinazione** selezionare il nome del file di output.
6.  TopoEdit crea la topologia transcode e Visualizza i nodi della topologia nella finestra principale dell'applicazione.
7.  Fare clic sul pulsante **Riproduci** sulla barra degli strumenti per eseguire la sessione multimediale. Attendere il completamento della codifica.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopoEdit carica i profili di codifica dal file TranscodeProfiles.xml. Questo file si trova nella directory bin del Windows SDK.

Il file inizia con un elemento **TedTranscodeProfiles** . Ogni profilo inizia con un elemento **TedTranscodeProfile** . Ogni profilo è costituito da un set di valori nel formato `<VALUE_NAME Value="VALUE"/>` . Vengono definiti i valori seguenti:



| Valore                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | Byte medi al secondo per il flusso audio. Equivalente all'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) .<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | Numero di bit per campione per il flusso audio. Equivale a [**MF \_ mt \_ audio \_ bits \_ per \_**](mf-mt-audio-bits-per-sample-attribute.md) attributo di esempio.<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | Allineamento del blocco per il flusso audio. Equivale a [**MF \_ mt \_ audio \_ Block \_ Alignment**](mf-mt-audio-block-alignment-attribute.md) Attribute.<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | Valore specifico del codec che definisce il profilo audio. Equivalente all'attributo [MF \_ transcode \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**AudioFormat**<br/>                                                                                     | Sottotipo audio codificato. Equivalente all'attributo [**del \_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | Il numero di canali nel flusso audio. Equivalente all'attributo [**MF \_ mt \_ audio \_ num \_ Channels**](mf-mt-audio-num-channels-attribute.md) .<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | Frequenza di campionamento del flusso audio, in campioni al secondo. Equivalente all'attributo [**MF \_ mt \_ audio \_ Samples \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md) .<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**ContainerType**<br/>                                                                             | Tipo di contenitore di file. Equivalente all'attributo [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) . <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**ProfileName**<br/>                                                                                     | Nome visualizzato del profilo.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Specificare 1 se i metadati non devono essere trasferiti al file di output oppure 0 se i metadati devono essere trasferiti. Equivalente all'attributo [MF \_ transcode \_ Skip \_ Metadata \_ Transfer](mf-transcode-skip-metadata-transfer.md) .<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**VideoBitrate**<br/>                                                                                 | Velocità in bit media dei video. Equivalente all'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) . <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | Valore specifico del codec che definisce la qualità di codifica. Equivalente all'attributo [MF \_ transcode \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md) . <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | Valore specifico del codec che definisce il profilo video. Equivalente all'attributo [MF \_ transcode \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**VideoFormat**<br/>                                                                                     | Sottotipo video codificato. Equivalente all'attributo [**del \_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | Altezza del video di output. Equivale a [**MF \_ mt \_ frame \_ size**](mf-mt-frame-size-attribute.md) Attribute.<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | Denominatore della frequenza dei fotogrammi del video di output. Equivale a [**MF \_ mt \_ frame \_ rate**](mf-mt-frame-rate-attribute.md) Attribute.<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | Il numeratore della frequenza dei fotogrammi del video di output. Equivale a [**MF \_ mt \_ frame \_ rate**](mf-mt-frame-rate-attribute.md) Attribute.<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | Larghezza del video di output. Equivale a [**MF \_ mt \_ frame \_ size**](mf-mt-frame-size-attribute.md) Attribute.<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | Il denominatore delle proporzioni in pixel (PAR) del video di output. Equivale all'attributo di proporzioni del [**\_ \_ pixel \_ \_ MF mt**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | Il numeratore della PAR del video di output. Equivale all'attributo di proporzioni del [**\_ \_ pixel \_ \_ MF mt**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




