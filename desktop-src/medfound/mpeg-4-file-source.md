---
description: L'origine file MPEG-4 analizza i file MP4 e 3GPP.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: Origine file MPEG-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90df56d58df19a53c37436bd631a1cc68dd8114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226526"
---
# <a name="mpeg-4-file-source"></a>Origine file MPEG-4

L'origine file MPEG-4 analizza i file MP4 e 3GPP. Per ulteriori informazioni sul formato di file MP4, vedere i documenti standard seguenti:

-   ISO/IEC 14496-12: *Information Technology--codifica di oggetti visivi audio--parte 12: formato del file multimediale di base ISO*
-   ISO/IEC 14496-14: *Information Technology--codifica di oggetti visivi audio--parte 14: formato file MP4*

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.

 

L'origine file MPEG-4 non decodifica i dati audio/video nel file.

In questo argomento sono incluse le sezioni seguenti:

## <a name="file-extensions-and-mime-types"></a>Estensioni di file e tipi MIME

L'origine file MPEG-4 è l'origine multimediale predefinita per le estensioni di file seguenti.



| Estensione file | Descrizione           |
|----------------|-----------------------|
| .3G2           | 3GPP2                 |
| .3GP           | 3GPP                  |
| .3gp2          | 3GPP2                 |
| .3GPP          | 3GPP                  |
| .m4a           | Audio MPEG-4          |
| .m4v           | Video MPEG-4          |
| .mov           | Film di Apple QuickTime |
| .mp4           | Audio o video MPEG-4 |
| . mp4v          | Video MPEG-4          |



 

È anche l'origine multimediale predefinita per i tipi MIME seguenti.



| tipo MIME   | Descrizione  |
|-------------|--------------|
| audio/3GPP  | audio 3GPP   |
| audio/3GPP2 | audio 3GPP2  |
| audio/MP4   | Audio MPEG-4 |
| video/3GPP  | video di 3GPP   |
| video/3GPP2 | video di 3GPP2  |
| video/MP4   | Video MPEG-4 |



 

## <a name="media-types"></a>Tipi di supporto

MP4 è un formato di contenitore estensibile. La specifica MP4 non definisce una struttura fissa per la descrizione dei tipi di supporto in un contenitore MP4. Definisce invece una gerarchia di oggetti che consente di definire strutture personalizzate per ogni formato. La descrizione del formato viene archiviata nella casella Descrizione esempio (' STSD ') per quel flusso. Nella casella Descrizione esempio è incluso un elenco di voci di esempio. Per ogni voce di esempio, un codice a 4 byte, simile a un FOURCC, definisce la struttura del formato.

Questa estensibilità significa che l'origine file MPEG-4 non è in grado di riconoscere ogni possibile Descrizione del formato. Per la creazione di tipi di supporto per i flussi è invece necessario un approccio a due livelli. Come minimo, ogni tipo di supporto contiene gli attributi seguenti.



| Attributo                                                                     | Descrizione                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                     | Uguale a **MFMediaType \_ audio** o **MFMediaType \_ video**.     |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                            | Specifica il sottotipo del flusso.                                  |
| [\_Descrizione dell'esempio MF mt \_ MPEG4 \_ \_](mf-mt-mpeg4-sample-description.md)      | Contiene la casella Descrizione di esempio completa come BLOB binario. |
| [\_Voce di \_ \_ esempio corrente \_ MF mt MPEG4 \_](mf-mt-mpeg4-current-sample-entry.md) | Specifica la voce corrente nella casella Descrizione esempio.     |



 

L'origine file MPEG-4 riconosce alcuni tipi di voce di esempio. Per queste voci, può analizzare la struttura del formato e creare un tipo di supporto completo, con attributi aggiuntivi che descrivono i dettagli del formato. Vedere [attributi del tipo di supporto](media-type-attributes.md).

L'origine file MPEG-4 può analizzare le voci di esempio seguenti.



| Codice di immissione di esempio | Tipo principale | Subtype                                                               | Descrizione                                         | Note                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alegge            | Audio      | **\_formato Wave \_ alegge**                                                | Codifica A-Law                                        |                                                                                                                                                                                                  |
| JPEG            | Video      | **\_MJPG MFVideoFormat**                                               | Foto-flusso JPEG                                   | Il formato del contenitore QuickTime supporta anche i flussi JPEG di movimento con le voci ' MJPA ' o ' mjpb ', ma l'origine file MPEG-4 non fornisce un tipo di supporto completo per questi tipi.               |
| 'avc1'            | Video      | **MFVideoFormat \_ H264**                                               | Video H. 264                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Audio      | **MFAudioFormat \_ AAC**<br/> **MFAudioFormat \_ MP3**<br/>   | AAC o MP3                                          | La voce "mp4a" può descrivere altri formati audio MPEG, ma l'origine file MPEG-4 non analizza la struttura del formato.                                                                          |
| MP4V            | Video      | **\_M4S2 MFVideoFormat**<br/> **\_MP4V MFVideoFormat**<br/> | MPEG-4 parte 2                                       | **MFVideoFormat \_ M4S2** viene usato per il profilo semplice MPEG-4 Part 2.<br/> **MFVideoFormat \_ MP4V** viene usato per tutti gli altri profili MPEG-4 Part 2, incluso il profilo semplice avanzato.<br/> |
| non elaborati            | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM a 8 bit                                     |                                                                                                                                                                                                  |
| 'sowt'            | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM a 16 bit Little-Endian                      |                                                                                                                                                                                                  |
| due            | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM big-endian a 16 bit                         | L'origine file MPEG-4 converte i dati audio in formato little-endian.                                                                                                                          |
| ulaw            | Audio      | **\_formato Wave \_ MULAW**                                               | μ-codifica della legge                                        |                                                                                                                                                                                                  |
| ' VC-1'            | Video      | **\_WVC1 MFVideoFormat**                                               | Video VC-1                                          |                                                                                                                                                                                                  |
| NESSUNO            | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM big-endian a 8 bit o a 16 bit                | L'origine file MPEG-4 converte i dati audio in formato little-endian.                                                                                                                          |
| 0x00000000        | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM big-endian a 8 bit o a 16 bit                | L'origine file MPEG-4 converte i dati audio in formato little-endian.                                                                                                                          |
| 0x6d730002        | Audio      | **\_formato Wave \_ ADPCM**                                               | Modulazione del codice Pulse differenziale adattivo (ADPCM) |                                                                                                                                                                                                  |
| 0x6d730011        | Audio      | **\_formato Wave \_ IMA \_ ADPCM**                                          | ADPCM                                               |                                                                                                                                                                                                  |



 

Per qualsiasi altro codice non illustrato nella tabella precedente, l'origine file MPEG-4 imposta il sottotipo come segue:

1.  *sottotipo* = MFMPEG4Format \_ base
2.  *sottotipo*. Data1 = codice di immissione di esempio

Per i codici non visualizzati nella tabella, un decodificatore deve usare l'attributo della [ \_ Descrizione dell'esempio MF mt \_ MPEG4 \_ \_ ](mf-mt-mpeg4-sample-description.md) per analizzare la casella della descrizione dell'esempio.

Per un elenco di codici di immissione di esempio e collegamenti a specifiche rilevanti, vedere il sito Web dell' [autorità di registrazione "MP4"](https://mp4ra.org) .

## <a name="limitations"></a>Limitazioni

L'origine file MPEG-4 non supporta le funzionalità seguenti dei file MP4:

-   Tracce esterne.
-   Frammenti di film (caselle ' Moof ' o ' MFRA '). ' Moof ' è supportato in Windows 8.
-   Presentazioni trasmesse. L'origine file MPEG-4 ignora le tracce di hint in modo invisibile all'utente.
-   Ricerca in base al codice ora SMPTE.
-   Atomi compressi (' CMOV ').

Sono supportati solo flussi video e audio. Tutte le tracce che contengono altri tipi di flusso vengono ignorate automaticamente. I dati multimediali devono essere posizionati all'interno di atomi ' mdat '.

Se è installato il supplemento di aggiornamento della piattaforma per Windows Vista, l'origine file MPEG-4 è disponibile in Windows Vista, ma è accessibile solo in Windows Vista tramite il [lettore di origine](source-reader.md).

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
-   I file di dimensioni superiori a 4 gigabyte (GB) sono supportati nel sink MPEG-4 di Windows 8 per MP4 non frammentato.
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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini e sink multimediali](media-sources-and-sinks.md)
</dt> <dt>

[Supporto MPEG-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




