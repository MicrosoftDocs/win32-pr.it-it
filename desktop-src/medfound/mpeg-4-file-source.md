---
description: L'origine file MPEG-4 analizza i file MP4 e 3GPP.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: Origine file MPEG-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece07ec0f2a2d94b477335e885f11c0d36769bffd11002ba464cec1d9c6ffb21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848051"
---
# <a name="mpeg-4-file-source"></a>Origine file MPEG-4

L'origine file MPEG-4 analizza i file MP4 e 3GPP. Per altre informazioni sul formato di file MP4, vedere i documenti standard seguenti:

-   ISO/IEC 14496-12: Information technology -- Codifica di *oggetti audio-visivi - Parte 12: Formato* file multimediale di base ISO
-   ISO/IEC 14496-14: Information technology -- Codifica di *oggetti audio-visivi -- Parte 14: formato di file MP4*

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.

 

L'origine file MPEG-4 non decodifica i dati audio/video nel file.

In questo argomento sono incluse le sezioni seguenti:

## <a name="file-extensions-and-mime-types"></a>Estensioni di file e tipi MIME

L'origine file MPEG-4 è l'origine multimediale predefinita per le estensioni di file seguenti.



| Estensione file | Descrizione           |
|----------------|-----------------------|
| .3g2           | 3GPP2                 |
| .3gp           | 3GPP                  |
| .3gp2          | 3GPP2                 |
| .3gpp          | 3GPP                  |
| .m4a           | Audio MPEG-4          |
| .m4v           | Video MPEG-4          |
| .mov           | Apple QuickTime Movie |
| .mp4           | Audio o video MPEG-4 |
| Mp4v          | Video MPEG-4          |



 

È anche l'origine multimediale predefinita per i tipi MIME seguenti.



| tipo MIME   | Descrizione  |
|-------------|--------------|
| audio/3gpp  | Audio 3GPP   |
| audio/3gpp2 | Audio 3GPP2  |
| audio/mp4   | Audio MPEG-4 |
| video/3gpp  | Video 3GPP   |
| video/3gpp2 | Video 3GPP2  |
| video/mp4   | Video MPEG-4 |



 

## <a name="media-types"></a>Tipi di supporti

MP4 è un formato di contenitore estendibile. La specifica MP4 non definisce una struttura fissa per la descrizione dei tipi di supporti in un contenitore MP4. Definisce invece una gerarchia di oggetti che consente di definire strutture personalizzate per ogni formato. La descrizione del formato viene archiviata nella casella della descrizione di esempio ('stsd') per il flusso. La casella della descrizione di esempio contiene un elenco di voci di esempio. Per ogni voce di esempio, un codice a 4 byte, simile a FOURCC, definisce la struttura del formato.

Questa estendibilità significa che l'origine file MPEG-4 non è in grado di riconoscere ogni possibile descrizione del formato. Al contrario, è necessario un approccio a due livelli quando si creano tipi di supporti per i flussi. Come minimo, ogni tipo di supporto contiene gli attributi seguenti.



| Attributo                                                                     | Descrizione                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                     | Uguale a **MFMediaType \_ Audio** o **MFMediaType \_ Video.**     |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)                            | Specifica il sottotipo di flusso.                                  |
| [DESCRIZIONE \_ DELL'ESEMPIO \_ MPEG4 MF MT \_ \_](mf-mt-mpeg4-sample-description.md)      | Contiene la casella di descrizione di esempio completa come BLOB binario. |
| [MF \_ MT \_ MPEG4 \_ CURRENT \_ SAMPLE \_ ENTRY](mf-mt-mpeg4-current-sample-entry.md) | Specifica la voce corrente nella casella della descrizione dell'esempio.     |



 

L'origine file MPEG-4 riconosce alcuni tipi di voci di esempio. Per queste voci, può analizzare la struttura del formato e creare un tipo di supporto completo, con attributi aggiuntivi che descrivono i dettagli del formato. Vedere [Attributi del tipo di supporto](media-type-attributes.md).

L'origine file MPEG-4 può analizzare le voci di esempio seguenti.



| Codice di voce di esempio | Tipo principale | Subtype                                                               | Descrizione                                         | Note                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 'alaw'            | Audio      | **WAVE \_ FORMAT \_ ALAW**                                                | Codifica A-law                                        |                                                                                                                                                                                                  |
| 'jpeg'            | Video      | **MFVideoFormat \_ MJPG**                                               | Flusso photo-JPEG                                   | Il formato del contenitore QuickTime supporta anche flussi JPEG in movimento con voci 'mjpa' o 'mjpb', ma l'origine file MPEG-4 non fornisce un tipo di supporto completo per questi tipi.               |
| 'avc1'            | Video      | **MFVideoFormat \_ H264**                                               | Video H.264                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Audio      | **MFAudioFormat \_ AAC**<br/> **MFAudioFormat \_ MP3**<br/>   | AAC o MP3                                          | La voce 'mp4a' può descrivere altri formati audio MPEG, ma l'origine file MPEG-4 non analizza la struttura del formato.                                                                          |
| 'mp4v'            | Video      | **MFVideoFormat \_ M4S2**<br/> **MFVideoFormat \_ MP4V**<br/> | MPEG-4 parte 2                                       | **MFVideoFormat \_ M4S2 viene** usato per mpeg-4 parte 2 profilo semplice.<br/> **MFVideoFormat \_ MP4V viene** usato per tutti gli altri profili MPEG-4 parte 2, tra cui Advanced Simple Profile.<br/> |
| 'raw '            | Audio      | **MFAudioFormat \_ PCM**                                                | Audio PCM a 8 bit                                     |                                                                                                                                                                                                  |
| 'sowt'            | Audio      | **MFAudioFormat \_ PCM**                                                | Audio PCM little-endian a 16 bit                      |                                                                                                                                                                                                  |
| 'twos'            | Audio      | **MFAudioFormat \_ PCM**                                                | Audio PCM big-endian a 16 bit                         | L'origine file MPEG-4 converte i dati audio in formato little-endian.                                                                                                                          |
| 'ulaw'            | Audio      | **WAVE \_ FORMAT \_ MULAW**                                               | μ codice legale                                        |                                                                                                                                                                                                  |
| 'vc-1'            | Video      | **MFVideoFormat \_ WVC1**                                               | Video di VC-1                                          |                                                                                                                                                                                                  |
| 'NONE'            | Audio      | **MFAudioFormat \_ PCM**                                                | Audio PCM big-endian a 8 bit o a 16 bit                | L'origine file MPEG-4 converte i dati audio in formato little-endian.                                                                                                                          |
| 0x00000000        | Audio      | **MFAudioFormat \_ PCM**                                                | Audio PCM big-endian a 8 bit o a 16 bit                | L'origine file MPEG-4 converte i dati audio in formato little-endian.                                                                                                                          |
| 0x6d730002        | Audio      | **FORMATO \_ WAVE \_ ADPCM**                                               | Adaptive Differential Pulse Code Modulation (ADPCM) |                                                                                                                                                                                                  |
| 0x6d730011        | Audio      | **FORMATO \_ WAVE \_ IMA \_ ADPCM**                                          | Adpcm                                               |                                                                                                                                                                                                  |



 

Per tutti gli altri codici non visualizzati nella tabella precedente, l'origine file MPEG-4 imposta il sottotipo come segue:

1.  *subtype* = MFMPEG4Format \_ Base
2.  *sottotipo*. Data1 = codice di immissione di esempio

Per i codici non visualizzati nella tabella, un decodificatore deve usare l'attributo [MF \_ MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION](mf-mt-mpeg4-sample-description.md) per analizzare la casella di descrizione dell'esempio.

Per un elenco di codici di immissione di esempio e collegamenti alle specifiche pertinenti, vedere il sito Web dell'autorità di registrazione ["MP4".](https://mp4ra.org)

## <a name="limitations"></a>Limitazioni

L'origine file MPEG-4 non supporta le funzionalità seguenti dei file MP4:

-   Tracce esterne.
-   Frammenti di film (caselle "moof" o "mfra"). 'moof' è supportato in Windows 8.
-   Presentazioni in streaming. L'origine file MPEG-4 ignora automaticamente le tracce dei suggerimenti.
-   Ricerca da parte di SMPTE time code.
-   Atomi compressi ('cmov').

Sono supportati solo flussi audio e video. Tutte le tracce che contengono altri tipi di flusso vengono automaticamente ignorate. I dati multimediali devono essere inseriti all'interno di atomi 'mdat'.

Se è installato platform update supplement for Windows Vista, l'origine file MPEG-4 è disponibile in Windows Vista, ma è accessibile in Windows Vista solo tramite il lettore di origine [.](source-reader.md)

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 aggiornamenti all'origine e al sink MPEG-4

-   Supporto di lettura e scrittura per la rotazione Windows 8'origine e sink MPEG-4. Questa operazione non è supportata nell'origine e nel sink Windows MPEG-4 7.

    L'origine MPEG-4 legge l'angolo di rotazione per una traccia video attiva come somma dell'angolo di rotazione da 'mvhd' e da 'tkhd'.

    Il sink Microsoft MPEG-4 scrive l'angolo di rotazione in 'tkhd', ma scrive una matrice di 0 gradi (identità) in 'mvhd'. Si noti che il sink Microsoft MPEG-4 supporta solo una singola traccia video.

    IPropertyStore legge l'angolo di rotazione solo per la prima traccia video come somma dell'angolo di rotazione da 'mvhd' e da 'tkhd'.

    IPropertyStore scrive l'angolo di rotazione solo per la prima traccia video in 'tkhd' dopo che l'angolo di rotazione è stato regolato in base all'angolo di rotazione in 'mvhd', se esistente.

-   I frammenti di film ('moof') sono supportati Windows 8'origine e sink MPEG-4, mentre 'mfra' non lo è.
-   H.263 è supportato nell'Windows 8 MPEG-4.

    L'origine MPEG-4 ora esegue il mapping di due fourcc di 'h263' e 's263' in formato di file MPEG-4 al tipo di supporto **di MFVideoFormat \_ H263.**

-   È stato aggiunto altro supporto fourcc per MJPEG Windows 8'origine MPEG-4.

    L'origine MPEG-4 esegue il mapping di 'dmb1' al tipo di supporto **\_ MJPG MFVideoFormat.**

-   Aggiunta del supporto dei metadati Furigana Windows 8'origine MPEG-4.

    L'origine MPEG-4 legge i metadati Furigana da 'soal', 'soar', 'soaa', 'sonm' e 'soco'. IPropertyStore legge i metadati Furignana tramite il set di PKEY corrispondenti.

    La tabella seguente illustra il mapping tra il nome canonico della shell, la chiave di proprietà e l'ID casella/tag nel formato di file MPEG-4.

    

    | Campo                                | Chiave di proprietà                         | ID tag/casella |
    |--------------------------------------|--------------------------------------|------------|
    | Sistema. Musica. AlbumTitleSortOverride  | PKEY \_ Musica \_ AlbumTitleSortOverride  | soal       |
    | Sistema. Musica. ArtistSortOverride      | PKEY \_ Musica \_ ArtistSortOverride      | librarsi       |
    | Sistema. Musica. AlbumArtistSortOverride | PKEY \_ Musica \_ AlbumArtistSortOverride | soaa       |
    | System.TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | Sistema. Musica. ComposerSortOverride    | PKEY \_ Musica \_ ComposerSortOverride    | Soco       |

    

     

-   Aggiunta del supporto per atomi Stereo 3D Windows 8'origine MPEG-4.

-   Aggiunta del supporto AC3 e DD+ Windows 8'origine e sink MPEG-4.
-   I file di dimensioni superiori a 4 gigabyte (GB) sono supportati Windows 8 sink MPEG-4 per MP4 non frammentale.
-   Lo scrubbing è stato ottimizzato Windows 8'origine MPEG-4.

    Per ridurre la latenza, le informazioni per i due fotogrammi chiave più vicini per una particolare posizione di ricerca vengono esposte tramite [**IMFSeekInfo::GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Poiché il fotogramma chiave non ha fotogrammi dipendenti, lo presenta dopo la decodifica di un solo fotogramma. Usare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere questa interfaccia tramite l'origine multimediale, la pipeline o l'applicazione.

    Impostare la frequenza su zero nell'origine MPEG-4. Quando la pipeline è in modalità di scrubbing, la frequenza è zero.

-   SPS e PPS possono essere archiviati in dati di esempio nel sink MPEG-4.

    [MF \_ L'attributo PASSTHROUGH MPEG4SINK \_ SPSPPS \_ ](mf-mpeg4sink-spspps-passthrough.md) nel sink MPEG-4 è definito per consentire il salvataggio di sps e PPS con esempi di input (dati video H.264). Le clip mp4 prodotte possono essere riprodotte Windows 7 sorgente MPEG-4 e altre.

-   SPS e PPS possono essere estratti dagli esempi di input nel sink MPEG-4.

    Quando SPS e PPS non sono impostati tramite [MF \_ MT \_ MPEG \_ SEQUENCE \_ HEADER](mf-mt-mpeg-sequence-header-attribute.md) sul tipo di supporto di input del sink MPEG-4, il sink MPEG-4 tenterà di estrarre SPS e PPS dagli esempi di input. Il sink MPEG-4 ignora tutti gli esempi di input finché non trova i primi SPS e PPS, perché tutti gli esempi di input senza SPS e PPS non sono decodificabile.

-   Le informazioni 3D nel record di configurazione di AVC sono supportate per MP4 non frammentale.
-   La lunghezza NALU è esposta per gli esempi compressi H.264 per ottimizzare la decodifica DXVA VLD H.264.

    L'origine MPEG-4 imposta [MF \_ NALU \_ LENGTH \_ SET](mf-nalu-length-set.md) sul tipo di supporto di output **MFVideoFormat \_ H264** o **MFVideoFormat \_ h264**. Imposta il BLOB di [MF \_ NALU \_ LENGTH \_ INFORMATION](mf-nalu-length-information.md) in ogni campione di output, con lunghezza NALU a quattro byte per diverse NALU in un campione compresso.

-   Aggiunta del supporto per l'audio MPEG2 ADTS nell'origine MP4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini multimediali e sink](media-sources-and-sinks.md)
</dt> <dt>

[Supporto MPEG-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




