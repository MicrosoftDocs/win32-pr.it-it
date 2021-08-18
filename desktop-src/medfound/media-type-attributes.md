---
description: Attributi del tipo di supporto
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: Attributi del tipo di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52e906baa7bbac14d33dbc263e3a1edfa43b65851d96d0573032784c0149425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827461"
---
# <a name="media-type-attributes"></a>Attributi del tipo di supporto

Gli attributi seguenti si applicano ai tipi di supporti. Alcuni di questi attributi sono destinati solo alla conversione di formati di tipi di supporti legacy Media Foundation tipi di supporti.

## <a name="general-format-attributes"></a>Attributi di formato generali

Questi attributi possono essere applicati a tutti i tipi di supporti.



| Attributo                                                                            | Descrizione                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) | Specifica se ogni campione è indipendente dagli altri esempi nel flusso.       |
| [**TIPO DI \_ FORMATO MF MT \_ \_ \_ AM**](mf-mt-am-format-type-attribute.md)                   | GUID di formato.                                                                           |
| [**MF \_ MT \_ COMPRESSO**](mf-mt-compressed-attribute.md)                             | Specifica se i dati multimediali sono compressi                                         |
| [**ESEMPI DI \_ DIMENSIONI \_ \_ FISSE MF MT \_**](mf-mt-fixed-size-samples-attribute.md)           | Specifica se gli esempi hanno dimensioni fisse.                                       |
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                            | GUID di tipo principale.                                                                       |
| [**DIMENSIONI DEL \_ CAMPIONE MF \_ \_ MT**](mf-mt-sample-size-attribute.md)                          | Dimensioni di ogni campione, in byte.                                                         |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)                                   | GUID del sottotipo.                                                                          |
| [**MF \_ MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md)                              | Contiene i dati utente per un tipo di supporto convertito da una struttura di formato legacy. |
| [**TIPO MF \_ MT DI CUI È STATO ESEGUITO IL \_ \_ WRAPPING**](mf-mt-wrapped-type-attribute.md)                        | Contiene un tipo di supporto di cui è stato eseguito il wrapping in un altro tipo di supporto.                     |



 

## <a name="audio-format-attributes"></a>Attributi del formato audio

Questi attributi possono essere applicati ai tipi di supporti il cui tipo principale è uguale a MFMediaType \_ Audio.



| Attributo                                                                                            | Descrizione                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [MF \_ MT \_ AAC \_ AUDIO \_ PROFILE \_ LEVEL \_ INDICATION](mf-mt-aac-audio-profile-level-indication.md)       | Specifica il profilo audio e il livello di un flusso AAC (Advanced Audio Coding).             |
| [TIPO DI \_ PAYLOAD MF MT \_ AAC \_ \_](mf-mt-aac-payload-type.md)                                             | Specifica il tipo di payload per un flusso AAC (Advanced Audio Coding).                       |
| [**MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | Numero medio di byte al secondo.                                                         |
| [**MF \_ MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)                    | Numero di bit per campione audio.                                                            |
| [**MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)                     | Allineamento del blocco, in byte.                                                                  |
| [**MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK**](mf-mt-audio-channel-mask-attribute.md)                           | Specifica l'assegnazione dei canali audio alle posizioni del parlante.                            |
| [**MF \_ MT AUDIO FLOAT SAMPLES AL \_ \_ \_ \_ \_ SECONDO**](mf-mt-audio-float-samples-per-second-attribute.md) | Numero di campioni audio al secondo (valore a virgola mobile).                                  |
| [**MF \_ MT \_ AUDIO \_ FOLDDOWN \_ MATRIX**](mf-mt-audio-folddown-matrix-attribute.md)                     | Specifica in che modo un decodificatore audio deve trasformare l'audio multicanale in output stereo.        |
| [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)                           | Numero dei canali audio.                                                                   |
| [**MF \_ MT \_ AUDIO \_ PREFER \_ WAVEFORMATEX**](mf-mt-audio-prefer-waveformatex-attribute.md)             | Specifica la struttura di formato legacy preferita da usare durante la conversione di un tipo di supporto audio. |
| [**ESEMPI \_ DI AUDIO MT MF \_ \_ PER \_ \_ BLOCCO**](mf-mt-audio-samples-per-block-attribute.md)                | Numero di campioni audio contenuti in un blocco compresso di dati audio.                    |
| [**ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO**](mf-mt-audio-samples-per-second-attribute.md)              | Numero di campioni audio al secondo (valore intero).                                         |
| [**MF \_ MT \_ AUDIO \_ VALID \_ BITS \_ PER \_ SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | Numero di bit validi di dati audio in ogni campione audio.                                    |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ AVGREF**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | Fare riferimento al livello medio di volume di Windows file audio multimediale.                               |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ AVGTARGET**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | Livello medio di volume di destinazione di un Windows file audio multimediale.                                  |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ PEAKREF**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | Fare riferimento al livello di picco del volume di Windows file audio multimediale.                                  |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ PEAKTARGET**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | Livello di volume di picco di destinazione di Windows file audio multimediale.                                     |
| [MF \_ MT \_ ORIGINAL \_ WAVE \_ FORMAT \_ TAG](mf-mt-original-wave-format-tag.md)                            | Contiene il tag di formato WAVE originale per un flusso audio.                                  |



 

## <a name="video-format-attributes"></a>Attributi del formato video

Questi attributi possono essere applicati ai tipi di supporti il cui tipo principale è uguale a MFMediaType \_ Video.



| Attributo                                                                              | Descrizione                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ AVG \_ BIT \_ ERROR \_ RATE**](mf-mt-avg-bit-error-rate-attribute.md)            | Frequenza degli errori dei dati.                                                                                                                        |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                            | Velocità approssimativa dei dati del flusso video.                                                                                              |
| [**PRIMARIE \_ \_ VIDEO PERSONALIZZATE MF MT \_ \_**](mf-mt-custom-video-primaries-attribute.md)     | Primarie di colore personalizzate.                                                                                                                 |
| [**MF \_ MT \_ DEFAULT \_ STRIDE**](mf-mt-default-stride-attribute.md)                      | Stride della superficie predefinito.                                                                                                                 |
| [**MF \_ MT \_ DRM \_ FLAGS**](mf-mt-drm-flags-attribute.md)                                | Specifica se il video richiede l'applicazione della protezione della copia.                                                                         |
| [**FREQUENZA \_ \_ FOTOGRAMMI MT MF \_**](mf-mt-frame-rate-attribute.md)                              | Frequenza fotogrammi.                                                                                                                             |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MAX](mf-mt-frame-rate-range-max.md)                      | Frequenza fotogrammi massima supportata da un dispositivo di acquisizione video.                                                                             |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md)                      | Frequenza fotogrammi minima supportata da un dispositivo di acquisizione video.                                                                             |
| [**DIMENSIONI \_ DEL FRAME MT \_ \_ MF**](mf-mt-frame-size-attribute.md)                              | Larghezza e altezza del fotogramma video.                                                                                                    |
| [**APERTURA \_ GEOMETRICA MF MT \_ \_**](mf-mt-geometric-aperture-attribute.md)              | Apertura geometrica.                                                                                                                     |
| [**MODALITÀ \_ INTERLACE MF MT \_ \_**](mf-mt-interlace-mode-attribute.md)                      | Descrive come interlacciare i fotogrammi.                                                                                                |
| [**MF \_ MT \_ MAX \_ KEYFRAME \_ SPACING**](mf-mt-max-keyframe-spacing-attribute.md)         | Numero massimo di fotogrammi da un fotogramma chiave al successivo.                                                                                |
| [**APERTURA MINIMA \_ \_ DELLO \_ \_ SCHERMO MF MT**](mf-mt-minimum-display-aperture-attribute.md) | Apertura minima dello schermo.                                                                                                               |
| [**INTESTAZIONE DELLA \_ SEQUENZA \_ MPEG MF MT \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)         | Intestazione di sequenza MPEG-1 o MPEG-2.                                                                                                       |
| [**CODICE ORA \_ DI \_ INIZIO MPEG MF MT \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md)        | Il gruppo di immagini (GOP) viene avviato time code.                                                                                                |
| [**FLAG \_ \_ MPEG2 MF MT \_**](mf-mt-mpeg2-flags-attribute.md)                            | Flag vari per video MPEG-2.                                                                                                   |
| [**MF \_ MT \_ MPEG2 \_ LEVEL**](mf-mt-mpeg2-level-attribute.md)                            | Livello MPEG-2 o H.264.                                                                                                                  |
| [**PROFILO \_ \_ MPEG2 MF MT \_**](mf-mt-mpeg2-profile-attribute.md)                        | Profilo MPEG-2 o H.264.                                                                                                                |
| [MF \_ MT \_ ORIGINAL \_ 4CC](mf-mt-original-4cc.md)                                        | Contiene il codec originale FOURCC per un flusso video.                                                                                  |
| [**FLAG DI \_ CONTROLLO MF MT \_ PAD \_ \_**](mf-mt-pad-control-flags-attribute.md)               | Proporzioni del rettangolo di output.                                                                                                   |
| [**MF \_ MT \_ PALETTE**](mf-mt-palette-attribute.md)                                     | Voci della tavolozza.                                                                                                                        |
| [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)               | Definisce l'area × 4 o 3 video che deve essere visualizzata in modalità panoramica/digitalizzazione.                                                              |
| [**MF \_ MT PAN SCAN \_ \_ \_ ABILITATO**](mf-mt-pan-scan-enabled-attribute.md)                 | Specifica se la modalità panoramica/analisi è abilitata.                                                                                             |
| [**PROPORZIONI \_ IN PIXEL MF MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)             | Proporzioni pixel.                                                                                                                     |
| [**HINT PER IL \_ CONTENUTO \_ DI ORIGINE MF MT \_ \_**](mf-mt-source-content-hint-attribute.md)           | Proporzioni progettate.                                                                                                                  |
| [**FUNZIONE MF \_ MT \_ TRANSFER \_**](mf-mt-transfer-function-attribute.md)                | Funzione di conversione da RGB a R'G'B'.                                                                                                 |
| [MF \_ MT \_ VIDEO \_ 3D](mf-mt-video-3d.md)                                                | Specifica se un flusso video contiene contenuto 3D.                                                                                   |
| [**MF \_ MT \_ VIDEO \_ CHROMA \_ SITING**](mf-mt-video-chroma-siting-attribute.md)           | Descrive come è stata campionata la chroma per il video Y'Cb'Cr'.                                                                                    |
| [**ILLUMINAZIONE VIDEO \_ MF MT \_ \_**](mf-mt-video-lighting-attribute.md)                      | Condizioni di illuminazione ottimali per la visualizzazione.                                                                                                |
| [**MF \_ MT \_ VIDEO \_ NOMINAL \_ RANGE**](mf-mt-video-nominal-range-attribute.md)           | Intervallo nominale delle informazioni sui colori                                                                                                  |
| [**PRIMARIE \_ VIDEO MF MT \_ \_**](mf-mt-video-primaries-attribute.md)                    | Primarie di colore.                                                                                                                        |
| [ROTAZIONE VIDEO \_ MF MT \_ \_](mf-mt-video-rotation.md)                                    | Specifica la rotazione di un fotogramma video in senso antiorario.                                                             |
| [**MF \_ MT \_ YUV \_ MATRIX**](mf-mt-yuv-matrix-attribute.md)                              | Matrice di conversione dallo spazio colori Y'Cb'Cr' allo spazio colori R'G'B'.                                                              |
| [IL CHIAMANTE XVP MF \_ \_ \_ ALLOCA \_ L'OUTPUT](mf-xvp-caller-allocates-output.md)               | Specifica se il chiamante alloca le trame usate per l'output dal [**processore video MFT.**](video-processor-mft.md) |
| [MF \_ XVP \_ DISABLE \_ FRC](mf-xvp-disable-frc.md)                                        | Disabilita la conversione della frequenza dei fotogrammi nel [**processore video MFT.**](video-processor-mft.md)                                               |



 

## <a name="other-format-attributes"></a>Altri attributi di formato

Gli attributi seguenti si applicano al video DV interleaved.



| Attributo                                                                      | Descrizione                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MF \_ MT \_ DV \_ AAUX \_ CTRL PACK \_ \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | Pacchetto di controllo del codice sorgente ausiliario audio (AAUX) per il primo blocco audio. |
| [**MF \_ MT \_ DV \_ AAUX \_ CTRL PACK \_ \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | Pacchetto di controllo del codice sorgente AAUX per il secondo blocco audio.                  |
| [**MF \_ MT \_ DV \_ AAUX \_ SRC PACK \_ \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | Pacchetto di origine AAUX per il primo blocco audio.                           |
| [**MF \_ MT \_ DV \_ AAUX \_ SRC PACK \_ \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | Pacchetto di origine AAUX per il secondo blocco audio.                          |
| [**MF \_ MT \_ DV \_ VAUX \_ CTRL \_ PACK**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | Pacchetto di controllo del codice sorgente video ausiliario (VAUX).                           |
| [**MF \_ MT \_ DV \_ VAUX \_ SRC \_ PACK**](mf-mt-dv-vaux-src-pack-attribute.md)        | Pacchetto di origine VAUX.                                                     |



 

I seguenti attributi si applicano ai file ASF (Advanced Streaming Format).



| Attributo                                                      | Descrizione                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [FORMATO ARBITRARIO \_ MF MT \_ \_](mf-mt-arbitrary-format.md)        | Dati di formato aggiuntivi per un flusso binario in un file ASF.       |
| [INTESTAZIONE \_ ARBITRARIA MF \_ \_ MT](mf-mt-arbitrary-header.md)        | Dati specifici del tipo per un flusso binario in un file ASF.           |
| [MF \_ MT \_ IMAGE \_ LOSS \_ TOLERANT](mf-mt-image-loss-tolerant.md) | Specifica se un flusso di immagini ASF è un tipo JPEG degradabile. |



 

I seguenti attributi si applicano ai file MPEG-4.



| Attributo                                                                     | Descrizione                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MF \_ MT \_ MPEG4 \_ CURRENT \_ SAMPLE \_ ENTRY](mf-mt-mpeg4-current-sample-entry.md) | Indice della voce corrente nella casella della descrizione di esempio. |
| [DESCRIZIONE \_ DELL'ESEMPIO \_ MPEG4 MF MT \_ \_](mf-mt-mpeg4-sample-description.md)      | Casella di descrizione dell'esempio.                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[Tipi di file multimediali video](video-media-types.md)
</dt> </dl>

 

 



