---
description: Il sink di file MPEG-4 crea file MP4.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: MPEG-4 File Sink
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e0175a5c21cc9f7c0186f70b37a5f94f5bf12151e606a2a441b4c75919d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102111"
---
# <a name="mpeg-4-file-sink"></a>MPEG-4 File Sink

Il sink di file MPEG-4 crea file MP4. Per altre informazioni sul formato di file MP4, vedere i documenti standard seguenti:

-   ISO/IEC 14496-12: Information technology -- Codifica di *oggetti audio-visivi - Parte 12: Formato* file multimediale di base ISO
-   ISO/IEC 14496-14: Information technology -- Codifica di *oggetti audio-visivi - Parte 14: formato di file MP4*

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.

 

Il sink di file MPEG-4 non incapsula la funzionalità di codifica.

Per creare il sink di file MPEG-4, chiamare la [**funzione MFCreateMPEG4MediaSink.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) Il sink di file MPEG-4 espone le interfacce seguenti tramite **QueryInterface**:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Casella di descrizione di esempio

MP4 è un formato di contenitore estendibile. La specifica MP4 non definisce una struttura fissa per la descrizione dei tipi di supporti in un contenitore MP4. Definisce invece una gerarchia di oggetti che consente di definire strutture personalizzate per ogni formato. La descrizione del formato viene archiviata nella casella della descrizione di esempio ('stsd') per ogni flusso. La casella della descrizione di esempio contiene un elenco di voci di esempio. Per ogni voce di esempio, un codice a 4 byte, simile a fourcc, definisce la struttura del formato.

Il sink di file MPEG-4 può generare la casella di descrizione di esempio per i formati seguenti:

-   Video H.264/AVC
-   Audio AAC
-   Audio MP3

Per altri formati, la casella di descrizione di esempio deve essere specificata nel tipo di supporto per ogni flusso. Per specificare la casella di descrizione di esempio, impostare gli attributi seguenti nel tipo di supporto:



| Attributo                                                                     | Descrizione                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DESCRIZIONE \_ DELL'ESEMPIO \_ MPEG4 MF MT \_ \_](mf-mt-mpeg4-sample-description.md)      | Contiene la casella di descrizione di esempio come BLOB binario.                                                                                                         |
| [MF \_ MT \_ MPEG4 \_ CURRENT \_ SAMPLE \_ ENTRY](mf-mt-mpeg4-current-sample-entry.md) | Specifica quale delle voci di esempio nella casella di descrizione dell'esempio è attualmente attiva. Facoltativo.<br/> Attualmente, il valore deve essere zero.<br/> |



 

In alcuni casi, non è possibile generare una casella di descrizione di esempio fino a quando tutti i dati non sono stati codificati. Ad esempio, informazioni come la velocità in bit media potrebbero non essere note in anticipo. In tal caso, è possibile aggiornare il tipo di supporto usando [**l'interfaccia IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nel sink di file MPEG-4. Questa operazione deve essere eseguita prima che il sink multimediale venga finalizzato.

In genere il tipo di supporto viene creato da un codificatore upstream. Il codificatore può generare un nuovo tipo di supporto durante lo streaming, tramite una modifica dinamica del formato. Per altre informazioni, vedere [Modifiche al formato dinamico](basic-mft-processing-model.md).

## <a name="h264avc-video"></a>H.264/AVC Video

Il sink di file MPEG-4 supporta la versione del flusso AVC con un flusso video elementare, con set di parametri di sequenza (SPS) e NALU del set di parametri immagine (PPS) contenuti nella casella di descrizione dell'esempio, come definito in ISO/IEC 14496 parte 15 sezione 5.1. Il sink di file non supporta il metodo alternativo di archiviazione delle unità NALU SPS/PPS come flusso elementare separato del set di parametri.

Il sink di file MPEG-4 può generare la casella di descrizione dell'esempio, ma deve essere fornito con le unità NALU SPS e PPS. Specificare queste informazioni nel tipo di supporto impostando l'attributo [**\_ MF MT \_ MPEG \_ SEQUENCE \_ HEADER.**](mf-mt-mpeg-sequence-header-attribute.md) Il valore dell'attributo è l'intestazione della sequenza H.264. L'intestazione della sequenza deve essere costituita dalle unità NALU SPS e PPS delimitate da codici di avvio a 3 o 4 byte.

Facoltativamente, quando si configura il sink di file, è possibile omettere l'attributo [**\_ MF MT \_ MPEG \_ SEQUENCE \_ HEADER**](mf-mt-mpeg-sequence-header-attribute.md) dal tipo di supporto iniziale. In tal caso, è necessario aggiornare il tipo di supporto in un secondo momento per includere l'intestazione della sequenza.

Il sink di file MPEG-4 presenta i requisiti seguenti per i bitstream AVC:

-   Il flusso di bit deve essere conforme alla specifica di formato H.264 Annex B. In particolare, le unità NALU devono essere delimitate da codici di avvio a 3 o 4 byte.
-   Gli esempi di supporti devono contenere tutte le sezioni e i dati NALU che corrispondono a una singola ora di presentazione.
-   Quando si scrivono fotogrammi B in un file MP4, è necessario impostare sia il timestamp di presentazione che il timestamp di decodifica. Se il flusso ha un frame B e il timestamp di decodifica non è impostato, il writer MP4 visualizza l'intervallo di tempo che va indietro e elimina il frame. 

## <a name="aac-audio"></a>Audio ACC

Per l'audio AAC, il sink di file MPEG-4 può generare la casella di descrizione di esempio per i sottotipi seguenti:

-   **MFAudioFormat \_ AAC**
-   **MEDIASUBTYPE \_ RAW \_ AAC1**

Per altre informazioni su questi sottotipi, vedere [Tipi di supporti AAC](aac-media-types.md).

Per il **sottotipo \_ AAC MFAudioFormat,** il tipo di supporto contiene facoltativamente l'attributo [**\_ MF MT \_ USER \_ DATA.**](mf-mt-user-data-attribute.md) Se presente, questo attributo rappresenta la parte della struttura [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) visualizzata dopo la struttura **WAVEFORMATEX,** ovvero dopo il **membro wfx.** Questo è seguito dai dati AudioSpecificConfig(), come definito da ISO/IEC 14496-3. Se l'attributo **\_ MF MT \_ USER \_ DATA** non è presente, si presuppone che il flusso sia un profilo AAC Low Complexity (LC) e che il sink di file MPEG-4 generi una casella di descrizione di esempio appropriata.

Per il **sottotipo MEDIASUBTYPE \_ RAW \_ AAC1,** il sink multimediale deve contenere l'attributo [**\_ MF MT USER \_ \_ DATA**](mf-mt-user-data-attribute.md) e l'attributo deve contenere i dati AudioSpecificConfig().

Il sink di file MPEG-4 crea la variante MPEG-4 della casella di descrizione dell'esempio AAC, usando una voce di esempio "mp4a" con objectTypeIndication = 0x40. Non usa tipi di oggetto MPEG-2.

## <a name="mp3-audio"></a>MP3 Audio

Per l'audio MP3, il sink di file MPEG-4 può generare la casella di descrizione di esempio da un tipo di supporto audio standard. Vedere Tipi [di supporti audio.](audio-media-types.md)

Il sink di file MPEG-4 crea la variante MPEG-4 della casella di descrizione dell'esempio MP3, usando una voce di esempio "mp4a" con objectTypeIndication = 0x6b per l'audio MPEG-1.

## <a name="limitations"></a>Limitazioni

-   Le dimensioni massime del file creato sono di 4 GB. In Windows 8 sono supportati file di dimensioni superiori a 4 GB.
-   Il sink di file MPEG-4 non supporta gli elenchi di modifiche (caselle 'edts' ed 'elst').

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 aggiornamenti all'origine e al sink MPEG-4

-   Supporto di lettura e scrittura per la rotazione Windows 8'origine e sink MPEG-4. Questa operazione non è supportata nell'Windows 7 mpeg-4 e nel sink.

    L'origine MPEG-4 legge l'angolo di rotazione per una traccia video attiva come somma dell'angolo di rotazione da 'mvhd' e da 'tkhd'.

    Il sink MICROSOFT MPEG-4 scrive l'angolo di rotazione in 'tkhd' ma scrive una matrice di 0 gradi (identità) in 'mvhd'. Si noti che il sink MICROSOFT MPEG-4 supporta solo una traccia video singola.

    IPropertyStore legge l'angolo di rotazione solo per la prima traccia video come somma dell'angolo di rotazione da 'mvhd' e da 'tkhd'.

    IPropertyStore scrive l'angolo di rotazione solo per la prima traccia video in 'tkhd' dopo che l'angolo di rotazione è stato regolato in base all'angolo di rotazione in 'mvhd', se presente.

-   I frammenti di film ('moof') sono supportati Windows 8 nell'origine e nel sink MPEG-4, ma 'mfra' non lo è.
-   H.263 è supportato nell'Windows 8 MPEG-4.

    L'origine MPEG-4 ora esegue il mapping di due quattro cc di 'h263' e 's263' nel formato di file MPEG-4 al tipo di supporto **di MFVideoFormat \_ H263.**

-   È stato aggiunto più supporto fourcc per MJPEG Windows 8'origine MPEG-4.

    L'origine MPEG-4 esegue il mapping di foucc di 'dmb1' al tipo di supporto **MFVideoFormat \_ MJPG.**

-   Supporto dei metadati Furigana aggiunto Windows 8'origine MPEG-4.

    L'origine MPEG-4 legge i metadati furigana da 'soal', 'soar', 'soaa', 'sonm' e 'soco'. IPropertyStore legge i metadati di Furignana tramite il set di PKEY corrispondenti.

    La tabella seguente illustra il mapping tra il nome canonico della shell, la chiave della proprietà e l'ID casella/tag in formato di file MPEG-4.

    

    | Campo                                | Chiave di proprietà                         | ID tag/casella |
    |--------------------------------------|--------------------------------------|------------|
    | Sistema. Musica. AlbumTitleSortOverride  | PKEY \_ Musica \_ AlbumTitleSortOverride  | soal       |
    | Sistema. Musica. ArtistSortOverride      | PKEY \_ Musica \_ ArtistSortOverride      | librarsi       |
    | Sistema. Musica. AlbumArtistSortOverride | PKEY \_ Musica \_ AlbumArtistSortOverride | soaa       |
    | System.TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | Sistema. Musica. ComposerSortOverride    | PKEY \_ Musica \_ ComposerSortOverride    | Soco       |

    

     

-   Aggiunta del supporto per atomi Stereo 3D Windows 8'origine MPEG-4.

-   Aggiunta del supporto AC3 e DD+ Windows 8'origine e sink MPEG-4.
-   I file di dimensioni superiori a 4 GB sono supportati Windows 8 sink MPEG-4 per MP4 non frammentale.
-   Lo scrubbing è stato ottimizzato Windows 8'origine MPEG-4.

    Per ridurre la latenza, le informazioni per i due fotogrammi chiave più vicini per una particolare posizione di ricerca vengono esposte tramite [**IMFSeekInfo::GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Poiché il fotogramma chiave non ha fotogrammi dipendenti, lo presenta dopo la decodifica di un solo fotogramma. Usare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere questa interfaccia tramite l'origine multimediale, la pipeline o l'applicazione.

    Impostare la frequenza su zero nell'origine MPEG-4. Quando la pipeline è in modalità di pulitura, la frequenza è zero.

-   SPS e PPS possono essere archiviati nei dati di esempio nel sink MPEG-4.

    [MF \_ L'attributo MPEG4SINK \_ SPSPPS \_ PASSTHROUGH](mf-mpeg4sink-spspps-passthrough.md) nel sink MPEG-4 è definito per consentire il salvataggio di SPS e PPS con esempi di input (dati video H.264). Le clip mp4 prodotte possono essere riprodotte Windows 7 mpeg-4 e altre.

-   SPS e PPS possono essere estratti da esempi di input nel sink MPEG-4.

    Quando SPS e PPS non sono impostati tramite [MF \_ MT \_ MPEG \_ SEQUENCE \_ HEADER](mf-mt-mpeg-sequence-header-attribute.md) nel tipo di supporto di input del sink MPEG-4, il sink MPEG-4 tenterà di estrarre SPS e PPS dagli esempi di input. Il sink MPEG-4 ignora tutti gli esempi di input fino a quando non trova i primi SPS e PPS, perché tutti gli esempi di input senza SPS e PPS non sono in grado di decodificare.

-   Le informazioni 3D nel record di configurazione AVC sono supportate per MP4 non frammentale.
-   La lunghezza NALU è esposta per gli esempi compressi H.264 per ottimizzare la decodifica DXVA H.264 VLD.

    L'origine MPEG-4 imposta [MF \_ NALU \_ LENGTH \_ SET](mf-nalu-length-set.md) sul tipo di supporto di output **di MFVideoFormat \_ H264** o **MFVideoFormat \_ h264.** Imposta il BLOB di [MF \_ NALU \_ LENGTH \_ INFORMATION](mf-nalu-length-information.md) in ogni esempio di output, con lunghezza NALU di quattro byte per NALU diverse in un campione compresso.

-   Aggiunta del supporto per l'audio MPEG2 ADTS nell'origine MP4.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Origini multimediali e sink](media-sources-and-sinks.md)
</dt> <dt>

[Sink multimediali](media-sinks.md)
</dt> <dt>

[Supporto MPEG-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
