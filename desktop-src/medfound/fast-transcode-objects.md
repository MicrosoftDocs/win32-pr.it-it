---
description: Questo argomento descrive come usare l'API transcodifica per codificare un file multimediale.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Uso dell'API Transcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e32ea24ebd4803319713be5fe7789cf41c3a99733338bdfe5ad69baf7396bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742479"
---
# <a name="using-the-transcode-api"></a>Uso dell'API Transcode

Questo argomento descrive come usare l'API transcodifica per codificare un file multimediale.

-   [Overview](#overview)
-   [Creazione di un'origine multimediale](#creating-a-media-source)
-   [Creazione di un profilo transcodifica](#creating-a-transcode-profile)
    -   [Attributi audio](#audio-attributes)
    -   [Attributi video](#video-attributes)
    -   [Attributi del contenitore](#container-attributes)
-   [Creazione di una topologia transcodifica](#creating-a-transcode-topology)
-   [Esecuzione della sessione di codifica](#running-the-encoding-session)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Prima di usare l'API transcodifica, l'applicazione deve avere le informazioni seguenti:

-   Percorso o URL di un file multimediale esistente che verrà codificato nuovamente.
-   Nome del file di output.
-   Tipo di contenitore per il file di output, ad esempio MP4 o ASF (Advanced Streaming Format).
-   Formato di codifica. Queste informazioni includono i tipi di supporti che descrivono i flussi audio e video codificati.

Per usare l'API transcodifica, un'applicazione esegue la procedura seguente.

1.  Creare un'origine multimediale per leggere il file di origine.
2.  Creare un profilo transcodifica. Aggiungere attributi che descrivono il flusso audio, il flusso video e il contenitore di file.
3.  Usare il profilo di transcodifica per creare una topologia di codifica. Per altre informazioni sulle topologie, vedere [Informazioni sulle topologie.](about-topologies.md)
4.  Impostare la topologia nella sessione [multimediale](media-session.md).
5.  Avviare la sessione multimediale e attendere [l'evento MESessionEnded.](mesessionended.md)

La parte restante di questo argomento descrive questi passaggi in modo più dettagliato.

## <a name="creating-a-media-source"></a>Creazione di un'origine multimediale

Un'origine multimediale è un oggetto che legge e analizza il file di origine. Per creare un'origine multimediale, usare il [sistema di risoluzione dell'origine](source-resolver.md). È possibile trovare codice di esempio nell'argomento [Using the Source Resolver](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Creazione di un profilo transcodifica

Un *profilo transcodifica* descrive il formato e le impostazioni usate per codificare il file di output. Il profilo di transcodifica contiene tre set di attributi:

-   Attributi audio: descrivere il formato audio di destinazione e le impostazioni del codificatore audio.
-   Attributi video: descrivere il formato video di destinazione e le impostazioni del codificatore video.
-   Attributi del contenitore: definire il tipo di contenitore di file, nonché alcune impostazioni di codifica globali.

Per creare un profilo di transcodifica, chiamare la [**funzione MFCreateTranscodeProfile.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) Questa funzione restituisce un puntatore [**all'interfaccia IMFTranscodeProfile.**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) L'oggetto profilo iniziale è vuoto. non contiene attributi. Il passaggio successivo consiste nell'aggiungere gli attributi che definiscono il profilo.

### <a name="audio-attributes"></a>Attributi audio

Per aggiungere attributi per il flusso audio, chiamare [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes). Questi attributi specificano la modalità di codifica del flusso audio. Se il file di output non conterrà un flusso audio, omettere questi attributi.

Gli attributi audio rientrano in due categorie:

-   Attributi che specificano il formato del flusso codificato
-   Attributi che specificano altri parametri di codifica.

Gli attributi di formato sono semplicemente attributi di tipo media, come descritto nella sezione [Tipi di supporti audio](audio-media-types.md). Il set esatto di attributi di formato dipende dal codificatore. Vedere [Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md). Ecco un elenco di attributi di formato audio tipici:



| Attributo Format                                                                         | Descrizione                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md)                                           | Sottotipo. Vedere [GUID sottotipo audio](audio-subtype-guids.md). |
| [MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS](mf-mt-audio-num-channels-attribute.md)                   | Numero di canali audio.                                    |
| [ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO](mf-mt-audio-samples-per-second-attribute.md)      | Numero di campioni audio al secondo.                          |
| [MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT](mf-mt-audio-block-alignment-attribute.md)             | Allineamento del blocco.                                             |
| [MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | Numero medio di byte al secondo (velocità in bit codificata).   |



 

Vengono definiti i parametri di codifica seguenti.



| Parametro di codifica                                                             | Descrizione                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [CODIFICATORE DI \_ \_ INSERIMENTO DONOT TRANSCODE \_ MF \_](mf-transcode-donot-insert-encoder.md) | Impedisce all'API di transcodifica di inserire un codificatore per il flusso audio. |
| [CODIFICA \_ \_ TRANSCODIFICA MFPROFILO](mf-transcode-encodingprofile.md)             | Specifica il modello di conformità del dispositivo. Si applica solo ai file ASF.    |
| [QUALITÀ \_ TRANSCODIFICA \_ MFVSSPEED](mf-transcode-qualityvsspeed.md)               | Specifica il compromesso tra qualità e velocità della codifica.                |



 

È necessario impostare gli attributi di formato. I parametri di codifica sono facoltativi.

Un modo per trovare un formato compatibile con il codificatore è chiamare la [**funzione MFTranscodeGetAudioOutputAvailableTypes.**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) Il codificatore desiderato viene specificato dal sottotipo. La funzione restituisce una raccolta di tipi di supporti per il codificatore. È possibile selezionare un tipo dall'elenco e copiare gli attributi nel profilo. Per codice di esempio che usa questo approccio, [vedere Esercitazione: Codifica di un file WMA.](tutorial--converting-an-mp3-file-to-a-wma-file.md)

### <a name="video-attributes"></a>Attributi video

Per aggiungere attributi per il flusso video, chiamare [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes). Questi attributi specificano la modalità di codifica del flusso video. Se il file di output non conterrà un flusso video, omettere questi attributi.

Come per gli attributi audio, gli attributi video rientrano in due categorie:

-   Attributi che specificano il formato del flusso codificato
-   Attributi che specificano altri parametri di codifica.

Gli attributi di formato sono attributi di tipo media, come descritto nella sezione [Tipi di supporti video](video-media-types.md). Ecco un elenco di attributi di formato video tipici:



| Attributo Format                                                       | Descrizione                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md)                         | Sottotipo. Vedere [GUID sottotipo video](video-subtype-guids.md). |
| [FREQUENZA \_ \_ FOTOGRAMMI MT MF \_](mf-mt-frame-rate-attribute.md)                  | Frequenza dei fotogrammi.                                                  |
| [DIMENSIONI \_ DEL FRAME MT \_ \_ MF](mf-mt-frame-size-attribute.md)                  | Dimensioni del frame.                                                  |
| [**VELOCITÀ IN BIT MEDIA MF \_ MT \_ \_**](mf-mt-avg-bitrate-attribute.md)            | Velocità in bit media.                                            |
| [PROPORZIONI \_ IN PIXEL MF MT \_ \_ \_](mf-mt-pixel-aspect-ratio-attribute.md) | Proporzioni in pixel.                                          |



 

Vengono definiti i parametri di codifica seguenti.



| Parametro di codifica                                                             | Descrizione                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [CODIFICATORE \_ \_ DONOT INSERT TRANSCODE MF \_ \_](mf-transcode-donot-insert-encoder.md) | Impedisce all'API di transcodifica di inserire un codificatore per il flusso video. |
| [CODIFICA \_ \_ TRANSCODIFICA MFPROFILO](mf-transcode-encodingprofile.md)             | Specifica il modello di conformità del dispositivo. Si applica solo ai file ASF.    |
| [QUALITÀ \_ TRANSCODIFICA \_ MFVSSPEED](mf-transcode-qualityvsspeed.md)               | Specifica il compromesso tra qualità e velocità della codifica.                |



 

È necessario impostare gli attributi di formato. I parametri di codifica sono facoltativi.

### <a name="container-attributes"></a>Attributi del contenitore

Gli attributi del contenitore definiscono le caratteristiche a livello di file del file di output. Per impostare gli attributi del contenitore, [**chiamare IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Vengono definiti gli attributi seguenti.



| Attributo                                                                          | Descrizione                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MODIFICARE IL PROFILO \_ DI TRANSCODIFICA MF \_ \_](mf-transcode-adjust-profile.md)                  | Definisce le impostazioni del flusso da usare per la topologia di transcodifica. È possibile impostare i flag per l'uso delle impostazioni di origine di input o per l'uso di attributi di flusso personalizzati. |
| [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md)                     | Specifica il formato del file di output, ad esempio MP4 o ASF. In base a questo valore, il sink multimediale appropriato viene aggiunto alla topologia.            |
| [TRANSCODIFICA MF \_ \_ SKIP METADATA \_ \_ TRANSFER](mf-transcode-skip-metadata-transfer.md) | Specifica se i metadati dell'origine vengono copiati nel file di output.                                                                               |
| [MODALITÀ TOPOLOGIA \_ TRANSCODIFICA MF \_](mf-transcode-topologymode.md)                       | Specifica se durante la transcoding è possibile usare codec basati su hardware.                                                                                |
| [Attributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)          | Sblocca un codec con restrizioni sul campo d'uso. Per altre informazioni, vedere [Field of Use Restrictions](field-of-use-restrictions.md).              |



 

[L'attributo \_ MF TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md) è obbligatorio. Gli altri attributi del contenitore sono facoltativi.

## <a name="creating-a-transcode-topology"></a>Creazione di una topologia di transcodifica

La topologia di transcodifica è una topologia parziale che contiene l'origine multimediale, i codec appropriati e il sink multimediale. Per creare la topologia di transcodifica, chiamare la [**funzione MFCreateTranscodeTopology.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) Questa funzione accetta i parametri seguenti come input:

-   Puntatore [**all'interfaccia IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.
-   Nome del file di output.
-   Puntatore [**all'interfaccia IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) del profilo di transcodifica.

La funzione restituisce un puntatore [**all'interfaccia IMFTopology.**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="running-the-encoding-session"></a>Esecuzione della sessione di codifica

Dopo aver creato la topologia, è possibile codificare il file. A questo punto è possibile rimuovere il profilo.

1.  Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare la sessione multimediale.
2.  Chiamare [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.
3.  Chiamare [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per avviare la sessione di codifica.
4.  Attendere [l'evento MESessionEnded.](mesessionended.md)
5.  Chiamare [**IMFMediaSession::Close per**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) chiudere la sessione multimediale.
6.  Attendere [l'evento MESessionClosed.](mesessionclosed.md)
7.  Chiamare [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
8.  Chiamare [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

La maggior parte del tempo impiegato per la codifica avviene tra i passaggi 3 e 4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API transcodifica](transcode-api.md)
</dt> <dt>

[Informazioni sulla sessione multimediale](about-the-media-session.md)
</dt> </dl>

 

 



