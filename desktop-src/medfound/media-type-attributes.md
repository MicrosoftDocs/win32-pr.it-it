---
description: Attributi del tipo di supporto
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: Attributi del tipo di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd3bc77197a3a897cd5280338451c33f1ea2637
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351561"
---
# <a name="media-type-attributes"></a>Attributi del tipo di supporto

Gli attributi seguenti si applicano ai tipi di supporto. Alcuni di questi attributi sono destinati solo alla conversione di formati di tipi di supporto legacy in Media Foundation tipi di supporto.

## <a name="general-format-attributes"></a>Attributi di formato generale

Questi attributi possono essere applicati a tutti i tipi di supporto.



| Attributo                                                                            | Descrizione                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_ \_ tutti gli esempi MF mt \_ \_ Independent**](mf-mt-all-samples-independent-attribute.md) | Specifica se ogni esempio è indipendente dagli altri esempi nel flusso.       |
| [**\_tipo di formato MF mt \_ am \_ \_**](mf-mt-am-format-type-attribute.md)                   | GUID formato.                                                                           |
| [**\_compressione MF mt \_**](mf-mt-compressed-attribute.md)                             | Specifica se i dati multimediali sono compressi                                         |
| [**\_esempi di \_ \_ dimensioni fisse MF mt \_**](mf-mt-fixed-size-samples-attribute.md)           | Specifica se gli esempi hanno dimensioni fisse.                                       |
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                            | GUID di tipo principale.                                                                       |
| [**\_ \_ dimensioni campione MF \_ mt**](mf-mt-sample-size-attribute.md)                          | Dimensioni di ogni campione, in byte.                                                         |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                   | GUID del sottotipo.                                                                          |
| [**\_ \_ dati utente MF \_ mt**](mf-mt-user-data-attribute.md)                              | Contiene i dati utente per un tipo di supporto convertito da una struttura di formato legacy. |
| [**\_tipo di \_ incapsulamento MF mt \_**](mf-mt-wrapped-type-attribute.md)                        | Contiene un tipo di supporto di cui è stato eseguito il wrapper in un altro tipo di supporto.                     |



 

## <a name="audio-format-attributes"></a>Attributi di formato audio

Questi attributi possono essere applicati ai tipi di supporto il cui tipo principale è uguale a MFMediaType \_ audio.



| Attributo                                                                                            | Descrizione                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [\_ \_ \_ \_ \_ indicazione livello profilo audio MF mt \_ AAC](mf-mt-aac-audio-profile-level-indication.md)       | Specifica il profilo audio e il livello di un flusso AAC (Advanced Audio Coding).             |
| [\_tipo di payload MF mt \_ AAC \_ \_](mf-mt-aac-payload-type.md)                                             | Specifica il tipo di payload per un flusso AAC (Advanced Audio Coding).                       |
| [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | Numero medio di byte al secondo.                                                         |
| [**\_ \_ bit audio MF \_ mt \_ per \_ campione**](mf-mt-audio-bits-per-sample-attribute.md)                    | Numero di bit per esempio audio.                                                            |
| [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)                     | Allineamento del blocco in byte.                                                                  |
| [**\_ \_ \_ maschera canale audio MF \_ mt**](mf-mt-audio-channel-mask-attribute.md)                           | Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.                            |
| [**\_ \_ campioni float audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-float-samples-per-second-attribute.md) | Numero di campioni audio al secondo (valore a virgola mobile).                                  |
| [**\_ \_ \_ matrice FOLDDOWN audio MF \_ mt**](mf-mt-audio-folddown-matrix-attribute.md)                     | Specifica il modo in cui un decodificatore audio deve trasformare l'audio multicanale nell'output stereo.        |
| [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)                           | Numero dei canali audio.                                                                   |
| [**MF \_ mt \_ audio \_ preferisce \_ WAVEFORMATEX**](mf-mt-audio-prefer-waveformatex-attribute.md)             | Specifica la struttura di formato legacy preferita da usare per la conversione di un tipo di supporto audio. |
| [**\_ \_ campioni audio MF \_ mt \_ per \_ blocco**](mf-mt-audio-samples-per-block-attribute.md)                | Numero di campioni audio contenuti in un blocco compresso di dati audio.                    |
| [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md)              | Numero di campioni audio al secondo (valore intero).                                         |
| [**\_ \_ bit validi per l'audio MF mt \_ \_ \_ per \_ campione**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | Numero di bit validi di dati audio in ogni esempio audio.                                    |
| [**MF \_ mt \_ audio \_ WMADRC \_ AVGREF**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | Livello di volume medio di riferimento di un file di Windows Media Audio.                               |
| [**MF \_ mt \_ audio \_ WMADRC \_ AVGTARGET**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | Livello di volume medio di destinazione di un file di Windows Media Audio.                                  |
| [**MF \_ mt \_ audio \_ WMADRC \_ PEAKREF**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | Riferimento a livello di picco del volume di un file di Windows Media Audio.                                  |
| [**MF \_ mt \_ audio \_ WMADRC \_ PEAKTARGET**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | Livello di picco del volume di destinazione di un file di Windows Media Audio.                                     |
| [\_tag di \_ \_ formato Wave \_ originale \_ MF mt](mf-mt-original-wave-format-tag.md)                            | Contiene il tag di formato WAVE originale per un flusso audio.                                  |



 

## <a name="video-format-attributes"></a>Attributi del formato video

Questi attributi possono essere applicati ai tipi di supporto il cui tipo principale è uguale a MFMediaType \_ video.



| Attributo                                                                              | Descrizione                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_frequenza di \_ \_ errori bit \_ medio \_ MF mt**](mf-mt-avg-bit-error-rate-attribute.md)            | Frequenza degli errori dei dati.                                                                                                                        |
| [**\_velocità in \_ bit media MF mt \_**](mf-mt-avg-bitrate-attribute.md)                            | Frequenza approssimativa dei dati del flusso video.                                                                                              |
| [**\_ \_ \_ principali video personalizzati MF \_ mt**](mf-mt-custom-video-primaries-attribute.md)     | Primari colori personalizzati.                                                                                                                 |
| [**\_ \_ stride predefinito MF \_ mt**](mf-mt-default-stride-attribute.md)                      | Stride di superficie predefinito.                                                                                                                 |
| [**\_ \_ flag DRM MF \_ mt**](mf-mt-drm-flags-attribute.md)                                | Specifica se il video richiede l'applicazione della protezione della copia.                                                                         |
| [**\_ \_ frequenza fotogrammi MF mt \_**](mf-mt-frame-rate-attribute.md)                              | Frequenza di fotogrammi.                                                                                                                             |
| [\_intervallo di \_ frequenza frame MF mt \_ \_ \_ Max](mf-mt-frame-rate-range-max.md)                      | Frequenza massima dei fotogrammi supportata da un dispositivo di acquisizione video.                                                                             |
| [\_intervallo di \_ \_ frequenza frame \_ MF \_ mt](mf-mt-frame-rate-range-min.md)                      | Frequenza minima dei fotogrammi supportata da un dispositivo di acquisizione video.                                                                             |
| [**\_dimensioni del \_ frame MF mt \_**](mf-mt-frame-size-attribute.md)                              | Larghezza e altezza del fotogramma video.                                                                                                    |
| [**\_ \_ apertura geometrica MF mt \_**](mf-mt-geometric-aperture-attribute.md)              | Apertura geometrica.                                                                                                                     |
| [**\_modalità di \_ intreccio MF mt \_**](mf-mt-interlace-mode-attribute.md)                      | Descrive il modo in cui i frame vengono interlacciati.                                                                                                |
| [**\_ \_ \_ spaziatura massima del fotogramma chiave MF mt \_**](mf-mt-max-keyframe-spacing-attribute.md)         | Numero massimo di fotogrammi da un fotogramma chiave a quello successivo.                                                                                |
| [**\_ \_ \_ apertura minima schermo \_ MF mt**](mf-mt-minimum-display-aperture-attribute.md) | Apertura minima della visualizzazione.                                                                                                               |
| [**\_intestazione della sequenza MF mt \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)         | Intestazione della sequenza MPEG-1 o MPEG-2.                                                                                                       |
| [**\_ \_ \_ codice ora di inizio \_ MF mt MPEG \_**](mf-mt-mpeg-start-time-code-attribute.md)        | Codice ora di inizio del GOP (Group-of-Pictures).                                                                                                |
| [**\_ \_ Flag MPEG2 MF \_ mt**](mf-mt-mpeg2-flags-attribute.md)                            | Flag varie per il video MPEG-2.                                                                                                   |
| [**\_ \_ Livello MPEG2 MF \_ mt**](mf-mt-mpeg2-level-attribute.md)                            | Livello MPEG-2 o H. 264.                                                                                                                  |
| [**\_ \_ Profilo MPEG2 MF \_ mt**](mf-mt-mpeg2-profile-attribute.md)                        | Profilo MPEG-2 o H. 264.                                                                                                                |
| [\_ \_ 4cc originale MF \_ mt](mf-mt-original-4cc.md)                                        | Contiene il codec originale FOURCC per un flusso video.                                                                                  |
| [**\_flag di \_ \_ controllo pad MF mt \_**](mf-mt-pad-control-flags-attribute.md)               | Proporzioni del rettangolo di output.                                                                                                   |
| [**\_ \_ tavolozza MF mt**](mf-mt-palette-attribute.md)                                     | Voci della tavolozza.                                                                                                                        |
| [**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**](mf-mt-pan-scan-aperture-attribute.md)               | Definisce l'area di video da 4 × 3 da visualizzare in modalità Pan/Scan.                                                              |
| [**\_ \_ Analisi panoramica MF \_ mt \_ abilitata**](mf-mt-pan-scan-enabled-attribute.md)                 | Specifica se la modalità Pan/Scan è abilitata.                                                                                             |
| [**proporzioni MF \_ mt \_ pixel \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)             | Proporzioni pixel.                                                                                                                     |
| [**HINT per il contenuto di origine MF \_ mt \_ \_ \_**](mf-mt-source-content-hint-attribute.md)           | Proporzioni previste.                                                                                                                  |
| [**\_funzione di \_ trasferimento MF mt \_**](mf-mt-transfer-function-attribute.md)                | Funzione di conversione da RGB a SOTTOCAMPIONATURA '.                                                                                                 |
| [\_ \_ Video 3D MF \_ mt](mf-mt-video-3d.md)                                                | Specifica se un flusso video contiene contenuto 3D.                                                                                   |
| [**posizione \_ di \_ Chroma del video MF mt \_ \_**](mf-mt-video-chroma-siting-attribute.md)           | Descrive il modo in cui Chroma è stato campionato per il video di Cb'Cr.                                                                                    |
| [**\_ \_ illuminazione video MF \_ mt**](mf-mt-video-lighting-attribute.md)                      | Condizioni di illuminazione ottimali per la visualizzazione.                                                                                                |
| [**\_ \_ \_ intervallo nominale video MF \_ mt**](mf-mt-video-nominal-range-attribute.md)           | Intervallo nominale delle informazioni sul colore                                                                                                  |
| [**\_ \_ principali video MF \_ mt**](mf-mt-video-primaries-attribute.md)                    | Colori primari.                                                                                                                        |
| [\_ \_ rotazione video MF \_ mt](mf-mt-video-rotation.md)                                    | Specifica la rotazione di un frame video in senso antiorario.                                                             |
| [**\_ \_ matrice YUV MF \_ mt**](mf-mt-yuv-matrix-attribute.md)                              | Matrice di conversione dallo spazio colore Cb'Cr "allo spazio colore SOTTOCAMPIONATURA".                                                              |
| [il \_ chiamante MF XVP \_ \_ alloca \_ output](mf-xvp-caller-allocates-output.md)               | Specifica se il chiamante allocherà le trame utilizzate per l'output da parte del [**processore video MFT**](video-processor-mft.md). |
| [MF \_ XVP \_ Disabilita \_ FRC](mf-xvp-disable-frc.md)                                        | Disabilita la conversione della frequenza dei frame nella [**MFT del processore video**](video-processor-mft.md).                                               |



 

## <a name="other-format-attributes"></a>Altri attributi di formato

Gli attributi seguenti si applicano a video DV con interfoliazione.



| Attributo                                                                      | Descrizione                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MF \_ mt \_ DV \_ AAUX \_ CTRL \_ pack \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | Controllo del codice sorgente (AAUX) audio ausiliario per il primo blocco audio. |
| [**MF \_ mt \_ DV \_ AAUX \_ CTRL \_ pack \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | Pacchetto di controllo del codice sorgente AAUX per il secondo blocco audio.                  |
| [**MF \_ mt \_ DV \_ AAUX \_ src \_ pack \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | AAUX Source Pack per il primo blocco audio.                           |
| [**MF \_ mt \_ DV \_ AAUX \_ src \_ pack \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | AAUX Source Pack per il secondo blocco audio.                          |
| [**il \_ pacchetto MF mt \_ DV \_ Vaux \_ CTRL \_**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | Pacchetto di controllo del codice sorgente ausiliario video.                           |
| [**\_pacco src di MF mt \_ DV \_ Vaux \_ \_**](mf-mt-dv-vaux-src-pack-attribute.md)        | Pacchetto di origine VAUX.                                                     |



 

Gli attributi seguenti si applicano ai file ASF (Advanced Streaming Format).



| Attributo                                                      | Descrizione                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [\_ \_ formato arbitrario MF \_ mt](mf-mt-arbitrary-format.md)        | Dati di formato aggiuntivi per un flusso binario in un file ASF.       |
| [\_ \_ intestazione arbitraria MF \_ mt](mf-mt-arbitrary-header.md)        | Dati specifici del tipo per un flusso binario in un file ASF.           |
| [\_tolleranza alla \_ perdita di immagini MF mt \_ \_](mf-mt-image-loss-tolerant.md) | Specifica se un flusso di immagini ASF è un tipo JPEG degradabile. |



 

I seguenti attributi si applicano ai file MPEG-4.



| Attributo                                                                     | Descrizione                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [\_Voce di \_ \_ esempio corrente \_ MF mt MPEG4 \_](mf-mt-mpeg4-current-sample-entry.md) | Indice della voce corrente nella casella Descrizione campione. |
| [\_Descrizione dell'esempio MF mt \_ MPEG4 \_ \_](mf-mt-mpeg4-sample-description.md)      | Casella Descrizione dell'esempio.                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 



