---
description: Questo argomento descrive come usare l'API transcode per codificare un file multimediale.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Uso dell'API transcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127887"
---
# <a name="using-the-transcode-api"></a>Uso dell'API transcode

Questo argomento descrive come usare l'API transcode per codificare un file multimediale.

-   [Overview](#overview)
-   [Creazione di un'origine multimediale](#creating-a-media-source)
-   [Creazione di un profilo di transcodifica](#creating-a-transcode-profile)
    -   [Attributi audio](#audio-attributes)
    -   [Attributi video](#video-attributes)
    -   [Attributi del contenitore](#container-attributes)
-   [Creazione di una topologia transcodifica](#creating-a-transcode-topology)
-   [Esecuzione della sessione di codifica](#running-the-encoding-session)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Prima di utilizzare l'API transcode, l'applicazione deve disporre delle seguenti informazioni:

-   Il percorso o l'URL di un file multimediale esistente che verrà codificato nuovamente.
-   Nome del file di output.
-   Tipo di contenitore per il file di output, ad esempio MP4 o Advanced Streaming Format (ASF).
-   Formato di codifica. Queste informazioni includono i tipi di supporto che descrivono i flussi audio e video codificati.

Per usare l'API transcode, un'applicazione esegue i passaggi seguenti.

1.  Creare un'origine multimediale per leggere il file di origine.
2.  Creare un profilo transcodifica. Aggiungere gli attributi che descrivono il flusso audio, il flusso video e il contenitore di file.
3.  Utilizzare il profilo transcodifica per creare una topologia di codifica. Per ulteriori informazioni sulle topologie, vedere [informazioni sulle topologie](about-topologies.md).
4.  Impostare la topologia nella [sessione multimediale](media-session.md).
5.  Avviare la sessione multimediale e attendere l'evento [MESessionEnded](mesessionended.md) .

Nella parte restante di questo argomento vengono descritti in modo più dettagliato questi passaggi.

## <a name="creating-a-media-source"></a>Creazione di un'origine multimediale

Un'origine multimediale è un oggetto che legge e analizza il file di origine. Per creare un'origine multimediale, usare il [resolver di origine](source-resolver.md). È possibile trovare il codice di esempio nell'argomento [usando il resolver di origine](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Creazione di un profilo di transcodifica

Un *profilo di transcodifica* descrive il formato e le impostazioni utilizzati per codificare il file di output. Il profilo transcode contiene tre set di attributi:

-   Attributi audio: descrivere il formato audio di destinazione e le impostazioni del codificatore audio.
-   Attributi video: descrivere il formato video di destinazione e le impostazioni del codificatore video.
-   Attributi del contenitore: definire il tipo di contenitore di file, nonché alcune impostazioni di codifica globali.

Per creare un profilo transcodifica, chiamare la funzione [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) . Questa funzione restituisce un puntatore all'interfaccia [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) . L'oggetto profilo iniziale è vuoto; non contiene attributi. Il passaggio successivo consiste nell'aggiungere gli attributi che definiscono il profilo.

### <a name="audio-attributes"></a>Attributi audio

Per aggiungere attributi per il flusso audio, chiamare [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes). Questi attributi specificano come codificare il flusso audio. Se il file di output non conterrà un flusso audio, omettere questi attributi.

Gli attributi audio rientrano in due categorie:

-   Attributi che specificano il formato del flusso codificato
-   Attributi che specificano altri parametri di codifica.

Gli attributi di formato sono semplicemente attributi di tipo media, come descritto nella sezione [tipi di supporti audio](audio-media-types.md). Il set esatto di attributi di formato dipende dal codificatore. (Vedere [formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)). Di seguito è riportato un elenco di attributi di formato audio tipici:



| Format (attributo)                                                                         | Descrizione                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [sottotipo MF \_ mt \_](mf-mt-subtype-attribute.md)                                           | Sottotipo. Vedere [GUID del sottotipo audio](audio-subtype-guids.md). |
| [numero \_ di \_ \_ canali audio MF mt \_](mf-mt-audio-num-channels-attribute.md)                   | Numero di canali audio.                                    |
| [\_ \_ campioni audio MF \_ mt \_ al \_ secondo](mf-mt-audio-samples-per-second-attribute.md)      | Numero di campioni audio al secondo.                          |
| [\_ \_ \_ allineamento blocchi audio MF \_ mt](mf-mt-audio-block-alignment-attribute.md)             | Allineamento del blocco.                                             |
| [\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) | Numero medio di byte al secondo (velocità in bit codificata).   |



 

Sono definiti i seguenti parametri di codifica.



| Parametro di codifica                                                             | Descrizione                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ \_ codificatore INserimenti MF transcode \_](mf-transcode-donot-insert-encoder.md) | Impedisce all'API transcodifica di inserire un codificatore per il flusso audio. |
| [MF \_ transcode \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | Specifica il modello di conformità del dispositivo. (Si applica solo ai file ASF).    |
| [MF \_ transcode \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | Specifica il compromesso tra la qualità e la velocità di codifica.                |



 

È necessario impostare gli attributi di formato. I parametri di codifica sono facoltativi.

Un modo per trovare un formato compatibile con il codificatore consiste nel chiamare la funzione [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . Il codificatore desiderato è specificato dal sottotipo. La funzione restituisce una raccolta di tipi di supporto per il codificatore. È possibile selezionare un tipo dall'elenco e copiare gli attributi nel profilo. Per un codice di esempio che usa questo approccio, vedere [esercitazione: codifica di un file WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).

### <a name="video-attributes"></a>Attributi video

Per aggiungere attributi per il flusso video, chiamare [**IMFTranscodeProfile:: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes). Questi attributi specificano il modo in cui il flusso video è codificato. Se il file di output non conterrà un flusso video, omettere questi attributi.

Come per gli attributi audio, gli attributi video rientrano in due categorie:

-   Attributi che specificano il formato del flusso codificato
-   Attributi che specificano altri parametri di codifica.

Gli attributi di formato sono attributi del tipo di supporto, come descritto nella sezione [tipi di supporti video](video-media-types.md). Di seguito è riportato un elenco di attributi di formato video tipici:



| Format (attributo)                                                       | Descrizione                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [sottotipo MF \_ mt \_](mf-mt-subtype-attribute.md)                         | Sottotipo. Vedere [GUID del sottotipo video](video-subtype-guids.md). |
| [\_ \_ frequenza fotogrammi MF mt \_](mf-mt-frame-rate-attribute.md)                  | Frequenza dei fotogrammi.                                                  |
| [\_dimensioni del \_ frame MF mt \_](mf-mt-frame-size-attribute.md)                  | Dimensioni del frame.                                                  |
| [**\_velocità in \_ bit media MF mt \_**](mf-mt-avg-bitrate-attribute.md)            | Velocità in bit media.                                            |
| [proporzioni MF \_ mt \_ pixel \_ \_](mf-mt-pixel-aspect-ratio-attribute.md) | Proporzioni dei pixel.                                          |



 

Sono definiti i seguenti parametri di codifica.



| Parametro di codifica                                                             | Descrizione                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ \_ codificatore INserimenti MF transcode \_](mf-transcode-donot-insert-encoder.md) | Impedisce all'API transcodifica di inserire un codificatore per il flusso video. |
| [MF \_ transcode \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | Specifica il modello di conformità del dispositivo. (Si applica solo ai file ASF).    |
| [MF \_ transcode \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | Specifica il compromesso tra la qualità e la velocità di codifica.                |



 

È necessario impostare gli attributi di formato. I parametri di codifica sono facoltativi.

### <a name="container-attributes"></a>Attributi del contenitore

Gli attributi del contenitore definiscono le caratteristiche a livello di file del file di output. Per impostare gli attributi del contenitore, chiamare [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Vengono definiti gli attributi seguenti.



| Attributo                                                                          | Descrizione                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ transcode \_ Adjust \_ profile](mf-transcode-adjust-profile.md)                  | Definisce le impostazioni del flusso da utilizzare per la topologia transcodifica. È possibile impostare i flag per utilizzare le impostazioni di origine di input o utilizzare attributi di flusso personalizzati. |
| [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md)                     | Specifica il formato del file di output, ad esempio MP4 o ASF. In base a questo valore, il sink multimediale appropriato viene aggiunto alla topologia.            |
| [MF \_ transcode \_ Ignora \_ \_ trasferimento metadati](mf-transcode-skip-metadata-transfer.md) | Specifica se i metadati dell'origine vengono copiati nel file di output.                                                                               |
| [MF \_ transcode \_ TOPOLOGYMODE](mf-transcode-topologymode.md)                       | Specifica se i codec basati su hardware possono essere utilizzati durante la transcodifica.                                                                                |
| [\_Attributo di \_ sblocco \_ FIELDOFUSE MFT](mft-fieldofuse-unlock-attribute.md)          | Sblocca un codec con restrizioni di campo di utilizzo. Per ulteriori informazioni, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md).              |



 

L'attributo [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) è obbligatorio. Gli altri attributi del contenitore sono facoltativi.

## <a name="creating-a-transcode-topology"></a>Creazione di una topologia transcodifica

La topologia transcodifica è una topologia parziale che contiene l'origine multimediale, i codec appropriati e il sink multimediale. Per creare la topologia transcode, chiamare la funzione [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) . Questa funzione accetta come input i parametri seguenti:

-   Puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.
-   Nome del file di output.
-   Puntatore all'interfaccia [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) del profilo transcodifica.

La funzione restituisce un puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .

## <a name="running-the-encoding-session"></a>Esecuzione della sessione di codifica

Dopo aver creato la topologia, si è pronti per codificare il file. A questo punto è possibile rimuovere il profilo.

1.  Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare la sessione multimediale.
2.  Chiamare [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.
3.  Chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per avviare la sessione di codifica.
4.  Attendere l'evento [MESessionEnded](mesessionended.md) .
5.  Chiamare [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la sessione multimediale.
6.  Attendere l'evento [MESessionClosed](mesessionclosed.md) .
7.  Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
8.  Chiamare [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

La maggior parte del tempo impiegato per la codifica viene eseguita tra i passaggi 3 e 4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API transcodifica](transcode-api.md)
</dt> <dt>

[Informazioni sulla sessione multimediale](about-the-media-session.md)
</dt> </dl>

 

 



