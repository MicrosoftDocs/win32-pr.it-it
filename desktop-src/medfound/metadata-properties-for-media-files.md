---
description: Questo argomento elenca le proprietà dei metadati più comuni per i file multimediali.
ms.assetid: 35187720-413a-45a0-8558-918f7c3161e1
title: Proprietà dei metadati dei file multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab541a480b03d7ef6bfb9a1a2036226b767774
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320483"
---
# <a name="metadata-properties-for-media-files"></a>Proprietà dei metadati dei file multimediali

Questo argomento elenca le proprietà dei metadati più comuni per i file multimediali.

-   [Proprietà dei supporti comuni](#common-media-properties)
-   [Proprietà di condivisione supporti](#media-sharing-properties)
-   [Mapping di Windows Media Format SDK](#windows-media-format-sdk-mappings)
-   [Argomenti correlati](#related-topics)

## <a name="common-media-properties"></a>Proprietà dei supporti comuni

Il sistema di proprietà della shell definisce un set di proprietà dei metadati comuni per tutti i tipi di oggetti della shell. Un subset di questi elementi è applicabile ai file multimediali. Nella tabella seguente sono elencate le proprietà della shell più comuni per i supporti. I file multimediali potrebbero supportare proprietà aggiuntive non elencate qui. Inoltre, non tutti i formati di file supportano ogni proprietà elencata. Per un elenco completo delle proprietà della shell, vedere [Proprietà](/previous-versions//ff521730(v=vs.85))della shell.



| PROPERTYKEY                                                              | Nome della shell                                                                                    | Descrizione                                                                                                                                                                                               | Tipo di dati    |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [\_ \_ \_ ID profilo DLNA contenuto \_ MFPKEY](mfpkey-content-dlna-profile-id.md) | nessuno                                                                                          | Identificatore del profilo DLNA (Digital Living Network Alliance).                                                                                                                                                | \_LPWSTR VT   |
| **PKEY \_ audio \_ ChannelCount**                                            | [System. audio. ChannelCount](../properties/props-system-audio-channelcount.md)                       | Numero dei canali audio.                                                                                                                                                                                 | \_UI4 VT      |
| **PKEY \_ audio \_ EncodingBitrate**                                         | [System. audio. EncodingBitrate](../properties/props-system-audio-encodingbitrate.md)                 | Velocità in bit audio media, in bit al secondo.                                                                                                                                                               | \_UI4 VT      |
| **\_Formato audio \_ pkey**                                                  | [System. audio. Format](../properties/props-system-audio-format.md)                                   | Sottotipo audio ([**MF \_ mt \_ sottotipo**](mf-mt-subtype-attribute.md)) espresso come stringa.                                                                                                                 | \_LPWSTR VT   |
| **PKEY \_ audio \_ IsVariableBitRate**                                       | [System. audio. IsVariableBitRate](../properties/props-system-audio-isvariablebitrate.md)             | Indica se il flusso audio utilizza la codifica a velocità in bit variabile.                                                                                                                                       | \_bool VT     |
| **PKEY \_ audio \_ PeakValue**                                               | [System. audio. PeakValue](../properties/props-system-audio-peakvalue.md)                             | Livello di picco del volume del contenuto audio.                                                                                                                                                                       | \_UI4 VT      |
| **\_ \_ Campionamento audio pkey**                                              | [System. audio. SampleRate](../properties/props-system-audio-samplerate.md)                           | Frequenza di campionamento audio in campioni al secondo. Equivalente all'attributo [**MF \_ mt \_ audio \_ Samples \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md) nel tipo di supporto.                           | \_UI4 VT      |
| **PKEY \_ audio \_ SampleSize**                                              | [System. audio. SampleSize](../properties/props-system-audio-samplesize.md)                           | Numero di bit per esempio audio. Equivale a [**MF \_ mt \_ audio \_ bits \_ per \_**](mf-mt-audio-bits-per-sample-attribute.md) attributo di esempio nel tipo di supporto.                                         | \_UI4 VT      |
| **PKEY \_ audio \_ streamNumber**                                            | [System. audio. StreamNumber](../properties/props-system-audio-streamnumber.md)                       | Identificatore del flusso audio.                                                                                                                                                                           | \_UI4 VT      |
| **Autore di PKEY \_**                                                         | [System.Author](../properties/props-system-author.md)                                               | Autore.                                                                                                                                                                                                   | \_LPWSTR VT   |
| **\_Commento pkey**                                                        | [System. Comment](../properties/props-system-comment.md)                                             | Commento allegato a un file, in genere aggiunto da un utente.                                                                                                                                                  | \_LPWSTR VT   |
| **\_Copyright pkey**                                                      | [System. Copyright](../properties/props-system-copyright.md)                                         | Informazioni sul copyright.                                                                                                                                                                                    | \_LPWSTR VT   |
| **PKEY \_ DRM \_ protetto**                                               | [System. DRM. protected](../properties/props-system-drm-isprotected.md)                             | Indica se il contenuto è protetto tramite Digital Rights Management (DRM).                                                                                                                         | \_bool VT     |
| **\_Parole chiave pkey**                                                       | [System.Keywords](../properties/props-system-keywords.md)                                           | Parole.                                                                                                                                                                                                 | \_LPWSTR VT   |
| **\_Lingua pkey**                                                       | [System. Language](../properties/props-system-language.md)                                           | Lingua.                                                                                                                                                                                                 | \_LPWSTR VT   |
| **\_AUTHORURL pkey media \_**                                               | [System. Media. AuthorUrl](../properties/props-system-media-authorurl.md)                             | URL del sito Web dell'autore.                                                                                                                                                                              | \_LPWSTR VT   |
| **\_AVERAGELEVEL pkey media \_**                                            | [System. Media. AverageLevel](../properties/props-system-media-averagelevel.md)                       | Livello medio del volume del contenuto audio.                                                                                                                                                                    | \_UI4 VT      |
| **\_CLASSPRIMARYID pkey media \_**                                          | [System. Media. ClassPrimaryID](../properties/props-system-media-classprimaryid.md)                   | Rappresentazione di stringa di un GUID che identifica la classe principale di supporti. Per i valori validi, vedere la documentazione relativa all'attributo [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md) .       | \_LPWSTR VT   |
| **\_CLASSSECONDARYID pkey media \_**                                        | [System. Media. ClassSecondaryID](../properties/props-system-media-classsecondaryid.md)               | Rappresentazione di stringa di un GUID che identifica la classe secondaria di supporti. Per i valori validi, vedere la documentazione relativa all'attributo [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md) . | \_LPWSTR VT   |
| **\_COLLECTIONGROUPID pkey media \_**                                       | [System. Media. CollectionGroupID](../properties/props-system-media-collectiongroupid.md)             | Rappresentazione di stringa di un GUID che identifica il gruppo di raccolta.                                                                                                                                 | \_LPWSTR VT   |
| **\_COLLECTIONID pkey media \_**                                            | [System. Media. CollectionID](../properties/props-system-media-collectionid.md)                       | Rappresentazione di stringa di un GUID che identifica la raccolta.                                                                                                                                       | \_LPWSTR VT   |
| **\_CONTENTDISTRIBUTOR pkey media \_**                                      | [System. Media. ContentDistributor](../properties/props-system-media-contentdistributor.md)           | Server di distribuzione del contenuto.                                                                                                                                                                               | \_LPWSTR VT   |
| **\_CONTENTID pkey media \_**                                               | [System. Media. ContentID](../properties/props-system-media-contentid.md)                             | Rappresentazione di stringa di un GUID che identifica la raccolta.                                                                                                                                       | \_LPWSTR VT   |
| **\_DATEENCODED pkey media \_**                                             | [System. Media. DateEncoded](../properties/props-system-media-dateencoded.md)                         | Ora di codifica del contenuto.                                                                                                                                                                        | FILETIME VT \_ |
| **\_DATERELEASED pkey media \_**                                            | [System. Media. DateReleased](../properties/props-system-media-datereleased.md)                       | Data di rilascio originale.                                                                                                                                                                                    | \_LPWSTR VT   |
| **\_Durata supporto \_ pkey**                                                | [System. Media. Duration](../properties/props-system-media-duration.md)                               | Durata, in unità di 100 nanosecondi. Equivale all'attributo [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) nel descrittore della presentazione.                                                       | \_UI8 VT      |
| **\_DVDID pkey media \_**                                                   | [System. Media. DVDID](../properties/props-system-media-dvdid.md)                                     | Identificatore del disco video digitale (DVDID).                                                                                                                                                                    | \_LPWSTR VT   |
| **\_ENCODEDBY pkey media \_**                                               | [System. Media. EncodedBy](../properties/props-system-media-encodedby.md)                             | Nome della persona o del gruppo che ha codificato il contenuto.                                                                                                                                                     | \_LPWSTR VT   |
| **\_ENCODINGSETTINGS pkey media \_**                                        | [System. Media. EncodingSettings](../properties/props-system-media-encodingsettings.md)               | Descrizione delle impostazioni utilizzate per codificare il contenuto.                                                                                                                                                   | \_LPWSTR VT   |
| **\_MCDI pkey media \_**                                                    | [System. Media. MCDI](../properties/props-system-media-mcdi.md)                                       | Identificatore del CD musicale. Questo valore viene usato per identificare un CD.                                                                                                                                                 | \_LPWSTR VT   |
| **\_METADATACONTENTPROVIDER pkey media \_**                                 | [System. Media. MetadataContentProvider](../properties/props-system-media-metadatacontentprovider.md) | Nome del provider di contenuto dei metadati. (Ad esempio, i metadati possono essere forniti da un servizio commerciale).                                                                                                 | \_LPWSTR VT   |
| **\_ \_ Producer multimediale pkey**                                                | [System. Media. Producer](../properties/props-system-media-producer.md)                               | Nome del producer del contenuto.                                                                                                                                                                      | \_LPWSTR VT   |
| **\_PROMOTIONURL pkey media \_**                                            | [System. Media. PromotionUrl](../properties/props-system-media-promotionurl.md)                       | URL di un sito Web che offre una promozione correlata al contenuto.                                                                                                                                             | \_LPWSTR VT   |
| **\_PROVIDERRATING pkey media \_**                                          | [System. Media. ProviderRating](../properties/props-system-media-providerrating.md)                   | Classificazione del contenuto assegnato dal provider di contenuti dei metadati.                                                                                                                                       | \_LPWSTR VT   |
| **\_PROVIDERSTYLE pkey media \_**                                           | [System. Media. ProviderStyle](../properties/props-system-media-providerstyle.md)                     | Stile o genere del contenuto assegnato dal provider di contenuti dei metadati.                                                                                                                               | \_LPWSTR VT   |
| **PKEY \_ media \_ Publisher**                                               | [System. Media. Publisher](../properties/props-system-media-publisher.md)                             | Server di pubblicazione.                                                                                                                                                                                                | \_LPWSTR VT   |
| **\_Sottotitolo supporti PKEY \_**                                                | [System. Media. sottotitolo](../properties/props-system-media-subtitle.md)                               | Sottotitolo.                                                                                                                                                                                                 | \_LPWSTR VT   |
| **\_UNIQUEFILEIDENTIFIER pkey media \_**                                    | [System. Media. UniqueFileIdentifier](../properties/props-system-media-uniquefileidentifier.md)       | Stringa generica che può essere per identificare il file.                                                                                                                                                        | \_LPWSTR VT   |
| **\_Writer multimediale \_ pkey**                                                  | [System. Media. Writer](../properties/props-system-media-writer.md)                                   | Writer.                                                                                                                                                                                                   | \_LPWSTR VT   |
| **PKEY \_ \_ anno multimediale**                                                    | [System. Media. Year](../properties/props-system-media-year.md)                                       | Anno in cui è stato pubblicato il contenuto.                                                                                                                                                                           | \_UI4 VT      |
| **PKEY \_ Music \_ AlbumArtist**                                             | [System. Music. AlbumArtist](../properties/props-system-music-albumartist.md)                         | Artista principale per l'album. Questo attributo può essere usato per distinguere l'artista principale per un album di un artista che collabora a una determinata traccia.                                            | \_LPWSTR VT   |
| **PKEY \_ Music \_ AlbumTitle**                                              | [System. Music. AlbumTitle](../properties/props-system-music-albumtitle.md)                           | Titolo dell'album.                                                                                                                                                                                              | \_LPWSTR VT   |
| **PKEY \_ Music \_ Artist**                                                  | [System. Music. Artist](../properties/props-system-music-artist.md)                                   | Artista.                                                                                                                                                                                                   | \_LPWSTR VT   |
| **PKEY \_ Music \_ BeatsPerMinute**                                          | [System. Music. BeatsPerMinute](../properties/props-system-music-beatsperminute.md)                   | Battimenti al minuto.                                                                                                                                                                                         | \_LPWSTR VT   |
| **\_Compositore musica \_ pkey**                                                | [System. Music. Composer](../properties/props-system-music-composer.md)                               | Compositore.                                                                                                                                                                                                 | \_LPWSTR VT   |
| **PKEY \_ Music \_ Conductor**                                               | [System. Music. Conductor](../properties/props-system-music-conductor.md)                             | Conduttore.                                                                                                                                                                                                | \_LPWSTR VT   |
| **PKEY \_ Music \_ ContentGroupDescription**                                 | [System. Music. ContentGroupDescription](../properties/props-system-music-contentgroupdescription.md) | Descrizione del gruppo di contenuto (ad esempio, set boxed o serie).                                                                                                                                      | \_LPWSTR VT   |
| **PKEY \_ Music \_ genre**                                                   | [System. Music. Genre](../properties/props-system-music-genre.md)                                     | Genere.                                                                                                                                                                                                    | \_LPWSTR VT   |
| **PKEY \_ Music \_ InitialKey**                                              | [System.Music.InitialKey](../properties/props-system-music-initialkey.md)                           | Chiave iniziale del brano musicale.                                                                                                                                                                             | \_LPWSTR VT   |
| **PKEY \_ Music \_ DECOMPILATION**                                           | [System. Music. di compilazione](../properties/props-system-music-iscompilation.md)                     | Indica se il file musicale fa parte di una compilazione.                                                                                                                                                | \_bool VT     |
| **PKEY \_ Music \_ lyrics**                                                  | [System. Music. lyrics](../properties/props-system-music-lyrics.md)                                   | Testi.                                                                                                                                                                                                   | \_LPWSTR VT   |
| **PKEY \_ Music \_ Mood**                                                    | [System. Music. Mood](../properties/props-system-music-mood.md)                                       | Umore.                                                                                                                                                                                                     | \_LPWSTR VT   |
| **PKEY \_ Music \_ PartOfSet**                                               | [System. Music. PartOfSet](../properties/props-system-music-partofset.md)                             | Il numero di parte e il numero totale di parti nel set a cui appartiene il file, separate da una barra.                                                                                                 | \_LPWSTR VT   |
| **\_Periodo di musica pkey \_**                                                  | [System. Music. period](../properties/props-system-music-period.md)                                   | Periodo.                                                                                                                                                                                                   | \_LPWSTR VT   |
| **PKEY \_ Music \_ numero**                                             | [System. Music. numero](../properties/props-system-music-tracknumber.md)                         | Numero di traccia.                                                                                                                                                                                             | \_UI4 VT      |
| **\_PARENTALRATING pkey**                                                 | [System. ParentalRating](../properties/props-system-parentalrating.md)                               | Classificazione parentale.                                                                                                                                                                                          | \_LPWSTR VT   |
| **\_PARENTALRATINGREASON pkey**                                           | [System. ParentalRatingReason](../properties/props-system-parentalratingreason.md)                   | Motivi della classificazione parentale assegnata.                                                                                                                                                                 | \_LPWSTR VT   |
| **\_Classificazione pkey**                                                         | [System. rating](../properties/props-system-rating.md)                                               | Classificazione utente.                                                                                                                                                                                              | \_UI4 VT      |
| **\_THUMBNAILSTREAM pkey**                                                | [System. ThumbnailStream](../properties/props-system-thumbnailstream.md)                             | Immagine di anteprima.                                                                                                                                                                                          | \_flusso VT   |
| **\_Titolo pkey**                                                          | [System.Title](../properties/props-system-title.md)                                                 | Titolo.                                                                                                                                                                                                    | \_LPWSTR VT   |
| **\_Compressione video \_ pkey**                                             | [System. video. Compression](../properties/props-system-video-compression.md)                         | Sottotipo video ([**MF \_ mt \_ sottotipo**](mf-mt-subtype-attribute.md)) espresso come stringa.                                                                                                                 | \_LPWSTR VT   |
| **PKEY \_ video \_ Director**                                                | [System. video. Director](../properties/props-system-video-director.md)                               | Direttore.                                                                                                                                                                                                 | \_LPWSTR VT   |
| **\_Video pkey \_ EncodingBitrate**                                         | [System. video. EncodingBitrate](../properties/props-system-video-encodingbitrate.md)                 | Velocità in bit video media, in bit al secondo.                                                                                                                                                               | \_UI4 VT      |
| **\_Video pkey \_ fourcc**                                                  | [System. video. FourCC](../properties/props-system-video-fourcc.md)                                   | **Fourcc** del formato di codifica video. Si applica solo se il sottotipo video può essere espresso come valore **fourcc** .                                                                                    | \_UI4 VT      |
| **\_Video pkey \_ FrameHeight**                                             | [System. video. FrameHeight](../properties/props-system-video-frameheight.md)                         | Altezza del fotogramma video.                                                                                                                                                                                       | \_UI4 VT      |
| **\_Framerate video \_ pkey**                                               | [System. video. FrameRate](../properties/props-system-video-framerate.md)                             | Frequenza dei fotogrammi video, espressa come frame al secondo × 1000.                                                                                                                                                  | \_UI4 VT      |
| **\_Video pkey \_ FrameWidth**                                              | [System. video. FrameWidth](../properties/props-system-video-framewidth.md)                           | Larghezza del fotogramma video.                                                                                                                                                                                        | \_UI4 VT      |
| **\_Video pkey \_ HorizontalAspectRatio**                                   | [System. video. HorizontalAspectRatio](../properties/props-system-video-horizontalaspectratio.md)     | Componente orizzontale della proporzioni di pixel. (Equivalente al numeratore dell'attributo di proporzioni [**MF \_ mt \_ pixel \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md) nel tipo di supporto).          | \_UI4 VT      |
| **\_Video pkey \_ stereo**                                                | [System. video. stereo](/previous-versions//mt744507(v=vs.85))                                     | Indica se il flusso video contiene contenuto video stereo.                                                                                                                                         | \_bool VT     |
| **\_Video pkey \_ streamNumber**                                            | [System. video. StreamNumber](../properties/props-system-video-streamnumber.md)                       | Identificatore del flusso video.                                                                                                                                                                           | \_UI4 VT      |
| **\_Video pkey \_ TotalBitrate**                                            | [System. video. TotalBitrate](../properties/props-system-video-totalbitrate.md)                       | Velocità totale dei dati per tutti i flussi video e audio, in bit al secondo. (Si applica solo ai file con almeno un flusso video).                                                                              | \_UI4 VT      |
| **\_Video pkey \_ VerticalAspectRatio**                                     | [System. video. VerticalAspectRatio](../properties/props-system-video-verticalaspectratio.md)         | Componente verticale delle proporzioni in pixel. (Equivalente al denominatore dell'attributo [**di \_ \_ \_ \_ proporzioni MF mt pixel**](mf-mt-pixel-aspect-ratio-attribute.md) nel tipo di supporto).          | \_UI4 VT      |



 

## <a name="media-sharing-properties"></a>Proprietà di condivisione supporti

Per rendere un file multimediale compatibile con la funzionalità di condivisione multimediale, il gestore delle proprietà deve esporre le seguenti proprietà dei metadati. Queste proprietà consentono al servizio di condivisione multimediale di offrire le opzioni appropriate per la transcodifica del contenuto in formati o velocità in bit differenti.

-   [\_ \_ \_ ID profilo DLNA contenuto \_ MFPKEY](mfpkey-content-dlna-profile-id.md)
-   **PKEY \_ audio \_ ChannelCount**
-   **PKEY \_ audio \_ EncodingBitrate**
-   **\_Formato audio \_ pkey**
-   **Pkey \_ \_Campionamento audio** (facoltativo)
-   **Pkey \_ Audio \_ SampleSize** (facoltativo)
-   **Pkey \_ DRM \_ protetto** (obbligatorio per il contenuto DRM)
-   **\_Durata supporto \_ pkey**
-   **\_Compressione video \_ pkey**
-   **\_Video pkey \_ EncodingBitrate**
-   **\_Video pkey \_ fourcc**
-   **\_Video pkey \_ FrameHeight**
-   **Pkey \_ \_Framerate video** (facoltativo)
-   **\_Video pkey \_ FrameWidth**
-   **\_Video pkey \_ TotalBitrate**

La **proprietà \_ pkey \_ DRM** protetta è obbligatoria se il contenuto è protetto tramite DRM. In caso contrario, questa proprietà è facoltativa.

Le proprietà **pkey \_ audio \_ samplere**, **pkey \_ audio \_ SampleSize** e **pkey \_ \_ framerate video** sono facoltative. Il servizio di condivisione multimediale li esporrà se disponibile.

Le proprietà nel **\_ gruppo audio \_ \* *_ pkey si applicano solo ai file con un flusso audio e le proprietà nel gruppo _* pkey \_ video \_ \*** si applicano solo ai file con un flusso video.

## <a name="windows-media-format-sdk-mappings"></a>Mapping di Windows Media Format SDK

L'origine dei supporti ASF esegue il mapping delle chiavi di proprietà seguenti agli attributi dell'intestazione ASF. In alcuni casi, i tipi di dati sono diversi tra la proprietà della shell e l'attributo Format SDK.



| PROPERTYKEY                              | Format SDK (attributo)                                                  |
|------------------------------------------|-----------------------------------------------------------------------|
| **PKEY \_ audio \_ IsVariableBitRate**       | [**IsVBR**](../wmformat/isvbr.md)                                           |
| **PKEY \_ audio \_ PeakValue**               | [**PeakValue**](../wmformat/peakvalue.md)                                   |
| **Autore di PKEY \_**                         | [**Autore**](../wmformat/author.md)                                         |
| **\_Commento pkey**                        | [**Descrizione**](../wmformat/description.md)                               |
| **\_Copyright pkey**                      | [**Copyright**](../wmformat/copyright.md)                                   |
| **PKEY \_ DRM \_ protetto**               | [**\_Protetto**](../wmformat/is-protected.md)                            |
| **\_Parole chiave pkey**                       | [**WM/categoria**](../wmformat/wm-category.md)                               |
| **\_Lingua pkey**                       | [**WM/lingua**](../wmformat/wm-language.md)                               |
| **\_AUTHORURL pkey media \_**               | [**WM/AuthorURL**](../wmformat/wm-authorurl.md)                             |
| **\_AVERAGELEVEL pkey media \_**            | [**AverageLevel**](../wmformat/averagelevel.md)                             |
| **\_CLASSPRIMARYID pkey media \_**          | [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md)              |
| **\_CLASSSECONDARYID pkey media \_**        | [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md)          |
| **\_COLLECTIONGROUPID pkey media \_**       | [**WM/WMCollectionGroupID**](../wmformat/wm-wmcollectiongroupid.md)         |
| **\_COLLECTIONID pkey media \_**            | [**WM/WMCollectionID**](../wmformat/wm-wmcollectionid.md)                   |
| **\_CONTENTDISTRIBUTOR pkey media \_**      | [**WM/ContentDistributor**](../wmformat/wm-contentdistributor.md)           |
| **\_CONTENTID pkey media \_**               | [**WM/WMContentID**](../wmformat/wm-wmcontentid.md)                         |
| **\_DATEENCODED pkey media \_**             | [**WM/EncodingTime**](../wmformat/wm-encodingtime.md)                       |
| **\_DATERELEASED pkey media \_**            | [**WM/OriginalReleaseTime**](../wmformat/wm-originalreleasetime.md)         |
| **\_DVDID pkey media \_**                   | [**WM/DVDID**](../wmformat/wm-dvdid.md)                                     |
| **\_ENCODEDBY pkey media \_**               | [**WM/EncodedBy**](../wmformat/wm-encodedby.md)                             |
| **\_ENCODINGSETTINGS pkey media \_**        | [**WM/EncodingSettings**](../wmformat/wm-encodingsettings.md)               |
| **\_MCDI pkey media \_**                    | [**WM/MCDI**](../wmformat/wm-mcdi.md)                                       |
| **\_METADATACONTENTPROVIDER pkey media \_** | [**WM/provider**](../wmformat/wm-provider.md)                               |
| **\_ \_ Producer multimediale pkey**                | [**WM/Producer**](../wmformat/wm-producer.md)                               |
| **\_PROMOTIONURL pkey media \_**            | [**WM/PromotionURL**](../wmformat/wm-promotionurl.md)                       |
| **\_PROVIDERRATING pkey media \_**          | [**WM/ProviderRating**](../wmformat/wm-providerrating.md)                   |
| **\_PROVIDERSTYLE pkey media \_**           | [**WM/ProviderStyle**](../wmformat/wm-providerstyle.md)                     |
| **PKEY \_ media \_ Publisher**               | [**WM/Publisher**](../wmformat/wm-publisher.md)                             |
| **\_Sottotitolo supporti PKEY \_**                | [**WM/SubTitleDescription**](../wmformat/wm-subtitledescription.md)         |
| **\_UNIQUEFILEIDENTIFIER pkey media \_**    | [**WM/UniqueFileIdentifier**](../wmformat/wm-uniquefileidentifier.md)       |
| **\_Writer multimediale \_ pkey**                  | [**WM/writer**](../wmformat/wm-writer.md)                                   |
| **PKEY \_ \_ anno multimediale**                    | [**WM/anno**](../wmformat/wm-year.md)                                       |
| **PKEY \_ Music \_ AlbumArtist**             | [**WM/AlbumArtist**](../wmformat/wm-albumartist.md)                         |
| **PKEY \_ Music \_ AlbumTitle**              | [**WM/AlbumTitle**](../wmformat/wm-albumtitle.md)                           |
| **PKEY \_ Music \_ Artist**                  | [**Autore**](../wmformat/author.md)                                         |
| **PKEY \_ Music \_ BeatsPerMinute**          | [**WM/BeatsPerMinute**](../wmformat/wm-beatsperminute.md)                   |
| **\_Compositore musica \_ pkey**                | [**WM/Composer**](../wmformat/wm-composer.md)                               |
| **PKEY \_ Music \_ Conductor**               | [**WM/conduttore**](../wmformat/wm-conductor.md)                             |
| **PKEY \_ Music \_ ContentGroupDescription** | [**WM/ContentGroupDescription**](../wmformat/wm-contentgroupdescription.md) |
| **PKEY \_ Music \_ genre**                   | [**WM/genre**](../wmformat/wm-genre.md)                                     |
| **PKEY \_ Music \_ InitialKey**              | [**WM/InitialKey**](../wmformat/wm-initialkey.md)                           |
| **PKEY \_ Music \_ DECOMPILATION**           | **WM/compilazione**                                                  |
| **PKEY \_ Music \_ lyrics**                  | [**WM/lyrics**](../wmformat/wm-lyrics.md)                                   |
| **PKEY \_ Music \_ Mood**                    | [**WM/umore**](../wmformat/wm-mood.md)                                       |
| **PKEY \_ Music \_ PartOfSet**               | [**WM/PartOfSet**](../wmformat/wm-partofset.md)                             |
| **\_Periodo di musica pkey \_**                  | [**WM/periodo**](../wmformat/wm-period.md)                                   |
| **PKEY \_ Music \_ numero**             | [**WM/numero**](../wmformat/wm-tracknumber.md)                         |
| **\_PARENTALRATING pkey**                 | [**WM/ParentalRating**](../wmformat/wm-parentalrating.md)                   |
| **\_PARENTALRATINGREASON pkey**           | [**WM/ParentalRatingReason**](../wmformat/wm-parentalratingreason.md)       |
| **\_Classificazione pkey**                         | [**WM/SharedUserRating**](../wmformat/wm-shareduserrating.md)               |
| **\_THUMBNAILSTREAM pkey**                | [**WM/immagine**](../wmformat/wmpicture.md)                       |
| **\_Titolo pkey**                          | [**Titolo**](../wmformat/title.md)                                           |
| **PKEY \_ video \_ Director**                | [**WM/Director**](../wmformat/wm-director.md)                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metadati del supporto](media-metadata.md)
</dt> <dt>

[Provider di metadati della shell](shell-metadata-providers.md)
</dt> </dl>

 

 
