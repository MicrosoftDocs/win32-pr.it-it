---
description: Il sink di file MPEG-4 crea file MP4.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: Sink di file MPEG-4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c27517463bca7dfa88fdbc09d77f7a6512c896d
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320070"
---
# <a name="mpeg-4-file-sink"></a>Sink di file MPEG-4

Il sink di file MPEG-4 crea file MP4. Per ulteriori informazioni sul formato di file MP4, vedere i documenti standard seguenti:

-   ISO/IEC 14496-12: *Information Technology--codifica di oggetti visivi audio--parte 12: formato del file multimediale di base ISO*
-   ISO/IEC 14496-14: *Information Technology--codifica di oggetti visivi audio--parte 14: formato file MP4*

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.

 

Il sink di file MPEG-4 non incapsula la funzionalità di codifica.

Per creare il sink di file MPEG-4, chiamare la funzione [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) . Il sink di file MPEG-4 espone le interfacce seguenti tramite **QueryInterface**:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Casella Descrizione esempio

MP4 è un formato di contenitore estensibile. La specifica MP4 non definisce una struttura fissa per la descrizione dei tipi di supporto in un contenitore MP4. Definisce invece una gerarchia di oggetti che consente di definire strutture personalizzate per ogni formato. La descrizione del formato viene archiviata nella casella Descrizione esempio (' STSD ') per ogni flusso. Nella casella Descrizione esempio è incluso un elenco di voci di esempio. Per ogni voce di esempio, un codice a 4 byte, simile a un FOURCC, definisce la struttura del formato.

Il sink di file MPEG-4 può generare la casella Descrizione esempio per i formati seguenti:

-   Video H. 264/AVC
-   Audio AAC
-   Audio MP3

Per gli altri formati, è necessario specificare la casella Descrizione esempio nel tipo di supporto per ogni flusso. Per specificare la casella Descrizione esempio, impostare i seguenti attributi sul tipo di supporto:



| Attributo                                                                     | Descrizione                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Descrizione dell'esempio MF mt \_ MPEG4 \_ \_](mf-mt-mpeg4-sample-description.md)      | Contiene la casella Descrizione esempio come BLOB binario.                                                                                                         |
| [\_Voce di \_ \_ esempio corrente \_ MF mt MPEG4 \_](mf-mt-mpeg4-current-sample-entry.md) | Specifica quale delle voci di esempio nella casella Descrizione esempio è attualmente attiva. Facoltativo.<br/> Attualmente, il valore deve essere zero.<br/> |



 

In alcuni casi, non è possibile generare una casella Descrizione di esempio finché tutti i dati non sono stati codificati. Ad esempio, le informazioni come la velocità in bit media potrebbero non essere note in anticipo. In tal caso, è possibile aggiornare il tipo di supporto usando l'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nel sink di file MPEG-4. Questa operazione deve essere eseguita prima della finalizzazione del sink multimediale.

Il tipo di supporto viene in genere creato da un codificatore upstream. Il codificatore può generare un nuovo tipo di supporto durante lo streaming, tramite una modifica di formato dinamico. Per altre informazioni, vedere [Dynamic Format Changes](basic-mft-processing-model.md).

## <a name="h264avc-video"></a>Video H. 264/AVC

Il sink di file MPEG-4 supporta la versione del flusso AVC che dispone di un flusso video elementare, con il set di parametri di sequenza (SPS) e il set di parametri immagine (PPS) NALUs contenuti nella casella Descrizione esempio, come definito in ISO/IEC 14496 parte 15 sezione 5,1. Il sink di file non supporta il metodo alternativo di archiviazione di SPS/PPS NALUs come flusso elementare del set di parametri separato.

Il sink di file MPEG-4 può generare la casella Descrizione dell'esempio, ma deve essere fornita con la NALUs SPS e PPS. Specificare queste informazioni nel tipo di supporto impostando l'attributo di [**\_ intestazione della sequenza MF mt \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) . Il valore dell'attributo è l'intestazione della sequenza H. 264. L'intestazione della sequenza deve essere costituita dalle NALUs SPS e PPS delimitate da codici iniziali a 3 o a 4 byte.

Facoltativamente, quando si configura il sink di file, è possibile omettere l'attributo di [**\_ intestazione di sequenza MF mt \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) dal tipo di supporto iniziale. In tal caso, è necessario aggiornare il tipo di supporto in un secondo momento per includere l'intestazione della sequenza.

Il sink di file MPEG-4 presenta i requisiti seguenti per i Bitstream AVC:

-   Il Bitstream deve essere conforme alla specifica del formato H. 264 Annex B. In particolare, NALUs deve essere delimitato da codici iniziali a 3 o a 4 byte.
-   Gli esempi di supporti devono contenere tutti i NALUs di sezione e dati che corrispondono a una singola ora di presentazione.
-   Quando si scrivono fotogrammi B in un file MP4, è necessario impostare sia il timestamp di presentazione che il timestamp di decodifica. Se il flusso ha un frame B e il timestamp di decodifica non è impostato, il writer MP4 visualizzerà il tempo del fotogramma indietro e ridurrà il frame. 

## <a name="aac-audio"></a>Audio ACC

Per l'audio AAC, il sink di file MPEG-4 può generare la casella Descrizione esempio per i sottotipi seguenti:

-   **MFAudioFormat \_ AAC**
-   **MEDIASUBTYPE \_ RAW \_ AAC1**

Per ulteriori informazioni su questi substypes, vedere [AAC media types](aac-media-types.md).

Per il sottotipo **\_ AAC MFAudioFormat** , il tipo di supporto contiene facoltativamente l'attributo [**\_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) . Se presente, questo attributo indica la parte della struttura [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) visualizzata dopo la struttura **WAVEFORMATEX** (ovvero dopo il membro **wfx** ). Questa operazione è seguita dai dati di AudioSpecificConfig (), definiti da ISO/IEC 14496-3. Se l' **attributo \_ \_ \_ dei dati utente MF mt** non è presente, si presuppone che il flusso sia un profilo con complessità AAC (LC) e che il sink di file MPEG-4 generi una casella di descrizione di esempio appropriata.

Per il sottotipo **MEDIASUBTYPE \_ RAW \_ AAC1** , il sink multimediale deve contenere l' [**attributo \_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) e l'attributo deve contenere i dati AudioSpecificConfig ().

Il sink di file MPEG-4 crea la variante MPEG-4 della casella della descrizione dell'esempio AAC, usando una voce di esempio ' mp4a ' con objectTypeIndication = 0x40. Non usa i tipi di oggetto MPEG-2.

## <a name="mp3-audio"></a>Audio MP3

Per l'audio MP3, il sink di file MPEG-4 può generare la casella Descrizione esempio da un tipo di supporto audio standard. Vedere [tipi di supporti audio](audio-media-types.md).

Il sink di file MPEG-4 crea la variante MPEG-4 della casella Descrizione di esempio MP3, usando una voce di esempio "mp4a" con objectTypeIndication = 0x6B per l'audio MPEG-1.

## <a name="limitations"></a>Limitazioni

-   La dimensione massima del file creato è 4 GB. In Windows 8 sono supportati i file di dimensioni maggiori di 4 GBGB.
-   Il sink di file MPEG-4 non supporta gli elenchi di modifica (caselle ' Edts ' è Elst ').

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Aggiornamenti di Windows 8 per l'origine e il sink MPEG-4

-   Supporto di lettura e scrittura della rotazione aggiunto in Windows 8 MPEG-4 source e sink. Questa operazione non è supportata in Windows 7 MPEG-4 source e sink.

    MPEG-4 source legge l'angolo di rotazione per una traccia video attiva come somma dell'angolo di rotazione tra' mvhd ' è tkhd '.

    Microsoft MPEG-4 sink scrive l'angolo di rotazione in ' tkhd ', ma scrive una matrice di 0 gradi (identità) in ' mvhd '. Si noti che il sink Microsoft MPEG-4 supporta solo una singola traccia video.

    IPropertyStore legge l'angolo di rotazione solo per la prima traccia video come somma dell'angolo di rotazione tra' mvhd ' è tkhd '.

    IPropertyStore scrive l'angolo di rotazione solo per la prima traccia video in ' tkhd ' dopo che l'angolo di rotazione viene regolato in base all'angolo di rotazione in ' mvhd ', se esistente.

-   I frammenti di film (' Moof ') sono supportati nell'origine e nel sink di Windows 8 MPEG-4, ma ' MFRA ' non lo è.
-   H. 263 è supportato nell'origine MPEG-4 di Windows 8.

    MPEG-4 source ora esegue il mapping di due FourCC ' H263' è 263' nel formato di file MPEG-4 al tipo di supporto di **MFVideoFormat \_ H263**.

-   È stato aggiunto un ulteriore supporto FourCC per MJPEG nell'origine MPEG-4 di Windows 8.

    L'origine MPEG-4 esegue il mapping di foucc di ' dmb1' al tipo di supporto di **MFVideoFormat \_ MJPG**.

-   Supporto dei metadati Furigana aggiunto nell'origine MPEG-4 di Windows 8.

    L'origine MPEG-4 legge i metadati Furigana da' Soal ',' Soar ',' soaa ',' sonm ' è Soco '. IPropertyStore legge i metadati Furignana tramite il set di PKEYs corrispondenti.

    La tabella seguente illustra il mapping tra il nome canonico della shell, la chiave della proprietà e l'ID box/Tag nel formato di file MPEG-4.

    

    | Campo                                | Chiave della proprietà                         | ID Tag/box |
    |--------------------------------------|--------------------------------------|------------|
    | System. Music. AlbumTitleSortOverride  | PKEY \_ Music \_ AlbumTitleSortOverride  | Soal       |
    | System. Music. ArtistSortOverride      | PKEY \_ Music \_ ArtistSortOverride      | aumenterà       |
    | System. Music. AlbumArtistSortOverride | PKEY \_ Music \_ AlbumArtistSortOverride | soaa       |
    | System. TitleSortOverride             | \_TITLESORTOVERRIDE pkey             | sonm       |
    | System. Music. ComposerSortOverride    | PKEY \_ Music \_ ComposerSortOverride    | Soco       |

    

     

-   Supporto Atom stereo 3D aggiunto nell'origine MPEG-4 di Windows 8.

-   Supporto per AC3 e DD + aggiunto in Windows 8 MPEG-4 source e sink.
-   I file di dimensioni superiori a 4 GB sono supportati nel sink MPEG-4 di Windows 8 per MP4 non frammentato.
-   Lo scrubbing è stato ottimizzato nell'origine MPEG-4 di Windows 8.

    Per ridurre la latenza, le informazioni per i due fotogrammi chiave più vicini per una particolare posizione di ricerca vengono esposte tramite [**IMFSeekInfo:: GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Poiché il fotogramma chiave non dispone di frame dipendenti, presenta il frame dopo la decodifica di un solo frame. Usare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere questa interfaccia tramite l'origine multimediale, la pipeline o l'applicazione.

    Impostare la frequenza su zero nell'origine MPEG-4. Quando la pipeline è in modalità di pulitura, la frequenza è zero.

-   SPS e PPS possono essere archiviati nei dati di esempio nel sink MPEG-4.

    [MF \_ L' \_ attributo \_ PassThrough MPEG4SINK SPSPPS](mf-mpeg4sink-spspps-passthrough.md) sul sink MPEG-4 è definito in modo da consentire il salvataggio di SPS e PPS insieme agli esempi di input (dati video H. 264). Le clip MP4 prodotte sono riprodotte da Windows 7 MPEG-4 source e altri.

-   SPS e PPS possono essere estratti dagli esempi di input nel sink MPEG-4.

    Quando SPS e PPS non vengono impostati tramite [l' \_ \_ intestazione della \_ sequenza \_ MPEG mt MPEG](mf-mt-mpeg-sequence-header-attribute.md) per il tipo di supporto di input del sink MPEG-4, il sink MPEG-4 tenterà di estrarre SPS e PPS dagli esempi di input. Il sink MPEG-4 ignora gli esempi di input fino a quando non trova il primo SPS e PPS, perché tutti gli esempi di input senza SPS e PPS non sono decodificabili.

-   le informazioni 3D nel record di configurazione AVC sono supportate per MP4 non frammentato.
-   La lunghezza di NALU è esposta per gli esempi compressi H. 264 per ottimizzare la decodifica DXVA H. 264 VLD.

    MPEG-4 source sets [MF \_ Nalu \_ length \_ set](mf-nalu-length-set.md) on the output media type of **MFVideoFormat \_ H264** o **MFVideoFormat \_ H264**. Imposta il BLOB delle [informazioni sulla \_ \_ lunghezza MF \_ Nalu](mf-nalu-length-information.md) in ogni esempio di output, con lunghezza NALU a quattro byte per Nalu diversi in un campione compresso.

-   Aggiunto il supporto per l'audio MPEG2 ADTS in MP4 source.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Origini e sink multimediali](media-sources-and-sinks.md)
</dt> <dt>

[Sink di supporti](media-sinks.md)
</dt> <dt>

[Supporto MPEG-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
