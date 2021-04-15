---
title: Elenco degli attributi
description: Elenco degli attributi
ms.assetid: 81fc356e-ee7a-4630-841f-6c1543e022d3
keywords:
- Windows Media Format SDK, attributi
- ASF (Advanced Systems Format), attributi
- ASF (formato avanzato dei sistemi), attributi
- attributi, elenco di
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793c0a860f6f9e40257bb6aec610dc7680b34538
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516798"
---
# <a name="attribute-list"></a>Elenco degli attributi

Gli attributi predefiniti inclusi in questo SDK sono visualizzati in ordine alfabetico nella tabella seguente. Ogni attributo ha un nome, un identificatore globale e un tipo di dati come definito dal membro appropriato dell'enumerazione [**WMT \_ attr \_ DataType**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) . Alcuni attributi non utilizzano un tipo di dati semplice o vengono formattati in base a una struttura. Le voci di questi attributi elencano un nome di struttura nella colonna del tipo di dati con il tipo di dati utilizzato per impostare il valore tra parentesi.

> [!Note]  
> Vedere [elenco](drm-attribute-list.md) di attributi DRM per una tabella di tutti gli attributi correlati a DRM.

 

Quando si programma con questi attributi, è consigliabile usare l'identificatore globale anziché il nome come valore letterale stringa. Con l'identificatore globale, eventuali errori tipografici genereranno un errore in fase di compilazione.



| Nome attributo                                                                       | Identificatore globale                             | Tipo di dati                                            |
|--------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------------|
| [**ASFLeakyBucketPairs**](asfleakybucketpairs.md)                                   | g \_ wszASFLeakyBucketPairs                     | **\_binario di tipo WMT \_**                                |
| [**AspectRatioX**](aspectratiox.md)                                                 | g \_ wszWMAspectRatioX                          | **WMT \_ tipo \_ DWORD**                                 |
| [**AspectRatioY**](aspectratioy.md)                                                 | g \_ wszWMAspectRatioY                          | **WMT \_ tipo \_ DWORD**                                 |
| [**Autore**](author.md)                                                             | g \_ wszWMAuthor                                | **\_stringa di tipo WMT \_**                                |
| [**AverageLevel**](averagelevel.md)                                                 | g \_ wszAverageLevel                            | **WMT \_ tipo \_ DWORD**                                 |
| [**BannerImageData**](bannerimagedata.md)                                           | g \_ wszWMBannerImageData                       | **\_binario di tipo WMT \_**                                |
| [**BannerImageType**](bannerimagetype.md)                                           | g \_ wszWMBannerImageType                       | **WMT \_ tipo \_ DWORD**                                 |
| [**BannerImageURL**](bannerimageurl.md)                                             | g \_ wszWMBannerImageURL                        | **\_stringa di tipo WMT \_**                                |
| [**Velocità in bit**](bit-rate.md)                                                          | g \_ wszWMBitrate                               | **WMT \_ tipo \_ DWORD**                                 |
| [**Trasmissione**](broadcast.md)                                                       | g \_ wszWMBroadcast                             | **\_tipo WMT \_ bool**                                  |
| [**BufferAverage**](bufferaverage.md)                                               | g \_ wszBufferAverage                           | **WMT \_ tipo \_ DWORD**                                 |
| [**Può \_ ignorare le \_ versioni precedenti**](can-skip-backward.md)                                     | g \_ wszWMSkipBackward                          | **\_tipo WMT \_ bool**                                  |
| [**Può \_ saltare \_ Avanti**](can-skip-forward.md)                                       | g \_ wszWMSkipForward                           | **\_tipo WMT \_ bool**                                  |
| [**Copyright**](copyright.md)                                                       | g \_ wszWMCopyright                             | **\_stringa di tipo WMT \_**                                |
| [**CopyrightURL**](copyrighturl.md)                                                 | g \_ wszWMCopyrightURL                          | **\_stringa di tipo WMT \_**                                |
| [**CurrentBitrate**](currentbitrate.md)                                             | g \_ wszWMCurrentBitrate                        | **WMT \_ tipo \_ DWORD**                                 |
| [**Descrizione**](description.md)                                                   | g \_ wszWMDescription                           | **\_stringa di tipo WMT \_**                                |
| [**\_CONTENTID DRM**](drm-contentid.md)                                              | g \_ wszWMDRM \_ ContentID                        | **\_stringa di tipo WMT \_**                                |
| [**\_Contentdistributor DRMHEADER \_ DRM**](drm-drmheader-contentdistributor.md)       | g \_ wszWMDRM \_ DRMHeader \_ contentdistributor    | **\_stringa di tipo WMT \_**                                |
| [**\_ContentID DRMHEADER \_ DRM**](drm-drmheader-contentid.md)                         | g \_ wszWMDRM \_ DRMHeader \_ ContentID             | **\_stringa di tipo WMT \_**                                |
| [**\_IndividualizedVersion DRMHEADER \_ DRM**](drm-drmheader-individualizedversion.md) | g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion | **\_stringa di tipo WMT \_**                                |
| [**\_KeyId DRMHEADER \_ DRM**](drm-drmheader-keyid.md)                                 | g \_ wszWMDRM \_ DRMHeader \_ keyId                 | **\_stringa di tipo WMT \_**                                |
| [**\_LicenseAcqURL DRMHEADER \_ DRM**](drm-drmheader-licenseacqurl.md)                 | g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL         | **\_stringa di tipo WMT \_**                                |
| [**\_SubscriptionContentID DRMHEADER \_ DRM**](drm-drmheader-subscriptioncontentid.md) | g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID | **\_stringa di tipo WMT \_**                                |
| [**\_DRMHEADER DRM**](drm-drmheader.md)                                              | g \_ wszWMDRM \_ DRMHeader                        | **\_stringa di tipo WMT \_**                                |
| [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)                      | g \_ wszWMDRM \_ IndividualizedVersion            | **\_stringa di tipo WMT \_**                                |
| [**\_KEYID DRM**](drm-keyid.md)                                                      | g \_ wszWMDRM \_ keyId                            | **\_stringa di tipo WMT \_**                                |
| [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)                                  | g \_ wszWMDRM \_ LASignatureCert                  | **\_stringa di tipo WMT \_**                                |
| [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)                      | g \_ wszWMDRM \_ LASignatureLicSrvCert            | **\_stringa di tipo WMT \_**                                |
| [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)                            | g \_ wszWMDRM \_ LASignaturePrivKey               | **\_stringa di tipo WMT \_**                                |
| [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)                          | g \_ wszWMDRM \_ LASignatureRootCert              | **\_stringa di tipo WMT \_**                                |
| [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)                                      | g \_ wszWMDRM \_ LicenseAcqURL                    | **\_stringa di tipo WMT \_**                                |
| [**\_LICENSEID DRM**](drm-licenseid.md)                                              | g \_ wszWMDRM \_ LicenseID                        | **\_stringa di tipo WMT \_**                                |
| [**\_SOURCEID DRM**](drm-sourceid.md)                                                | g \_ wszWMDRM \_ SourceID                         | **WMT \_ tipo \_ DWORD**                                 |
| [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)                                  | g \_ wszWMDRM \_ V1LicenseAcqURL                  | **\_stringa di tipo WMT \_**                                |
| [**Duration**](duration.md)                                                         | g \_ wszWMDuration                              | **WMT \_ tipo \_ QWORD**                                 |
| [**FileSize**](filesize.md)                                                         | g \_ wszWMFileSize                              | **WMT \_ tipo \_ QWORD**                                 |
| [**HasArbitraryDataStream**](hasarbitrarydatastream.md)                             | g \_ wszWMHasArbitraryDataStream                | **\_tipo WMT \_ bool**                                  |
| [**HasAttachedImages**](hasattachedimages.md)                                       | g \_ wszWMHasAttachedImages                     | **\_tipo WMT \_ bool**                                  |
| [**HasAudio**](hasaudio.md)                                                         | g \_ wszWMHasAudio                              | **\_tipo WMT \_ bool**                                  |
| [**HasFileTransferStream**](hasfiletransferstream.md)                               | g \_ wszWMHasFileTransferStream                 | **\_tipo WMT \_ bool**                                  |
| [**HasImage**](hasimage.md)                                                         | g \_ wszWMHasImage                              | **\_tipo WMT \_ bool**                                  |
| [**HasScript**](hasscript.md)                                                       | g \_ wszWMHasScript                             | **\_tipo WMT \_ bool**                                  |
| [**HasVideo**](hasvideo.md)                                                         | g \_ wszWMHasVideo                              | **\_tipo WMT \_ bool**                                  |
| [**\_Protetto**](is-protected.md)                                                | g \_ wszWMProtected                             | **\_tipo WMT \_ bool**                                  |
| [**\_Attendibile**](is-trusted.md)                                                    | g \_ wszWMTrusted                               | **\_tipo WMT \_ bool**                                  |
| [**ISAN**](isan.md)                                                                 | g \_ wszISAN                                    | **\_stringa di tipo WMT \_**                                |
| [**IsVBR**](isvbr.md)                                                               | g \_ wszWMIsVBR                                 | **\_tipo WMT \_ bool**                                  |
| [**\_Indirizzo NSC**](nsc-address.md)                                                  | g \_ wszWMNSCAddress                            | **\_stringa di tipo WMT \_**                                |
| [**\_Descrizione NSC**](nsc-description.md)                                          | g \_ wszWMNSCDescription                        | **\_stringa di tipo WMT \_**                                |
| [**\_Posta elettronica NSC**](nsc-email.md)                                                      | g \_ wszWMNSCEmail                              | **\_stringa di tipo WMT \_**                                |
| [**\_Nome NSC**](nsc-name.md)                                                        | g \_ wszWMNSCName                               | **\_stringa di tipo WMT \_**                                |
| [**\_Telefono NSC**](nsc-phone.md)                                                      | g \_ wszWMNSCPhone                              | **\_stringa di tipo WMT \_**                                |
| [**NumberOfFrames**](numberofframes.md)                                             | g \_ wszWMNumberOfFrames                        | **WMT \_ tipo \_ QWORD**                                 |
| [**OptimalBitrate**](optimalbitrate.md)                                             | g \_ wszWMOptimalBitrate                        | **WMT \_ tipo \_ DWORD**                                 |
| [**PeakValue**](peakvalue.md)                                                       | g \_ wszPeakValue                               | **WMT \_ tipo \_ DWORD**                                 |
| [**Classificazione**](rating.md)                                                             | g \_ wszWMRating                                | **\_stringa di tipo WMT \_**                                |
| [**Ricercabile**](seekable.md)                                                         | g \_ wszWMSeekable                              | **\_tipo WMT \_ bool**                                  |
| [**\_Nome firma**](signature-name.md)                                            | \_nome wszWMSignature \_ g                       | **\_stringa di tipo WMT \_**                                |
| [**Stridable**](stridable.md)                                                       | g \_ wszWMStridable                             | **\_tipo WMT \_ bool**                                  |
| [**Titolo**](title.md)                                                               | g \_ wszWMTitle                                 | **\_stringa di tipo WMT \_**                                |
| [**VBRPeak**](vbrpeak.md)                                                           | g \_ wszVBRPeak                                 | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/AlbumArtist**](wm-albumartist.md)                                             | g \_ wszWMAlbumArtist                           | **\_stringa di tipo WMT \_**                                |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)                                         | g \_ wszWMAlbumCoverURL                         | **\_stringa di tipo WMT \_**                                |
| [**WM/AlbumTitle**](wm-albumtitle.md)                                               | g \_ wszWMAlbumTitle                            | **\_stringa di tipo WMT \_**                                |
| [**WM/ASFPacketCount**](wm-asfpacketcount.md)                                       | g \_ wszWMASFPacketCount                        | **WMT \_ tipo \_ QWORD**                                 |
| [**WM/ASFSecurityObjectsSize**](wm-asfsecurityobjectssize.md)                       | g \_ wszWMASFSecurityObjectsSize                | **WMT \_ tipo \_ QWORD**                                 |
| [**WM/AudioFileURL**](wm-audiofileurl.md)                                           | g \_ wszWMAudioFileURL                          | **\_stringa di tipo WMT \_**                                |
| [**WM/AudioSourceURL**](wm-audiosourceurl.md)                                       | g \_ wszWMAudioSourceURL                        | **\_stringa di tipo WMT \_**                                |
| [**WM/AuthorURL**](wm-authorurl.md)                                                 | g \_ wszWMAuthorURL                             | **\_stringa di tipo WMT \_**                                |
| [**WM/BeatsPerMinute**](wm-beatsperminute.md)                                       | g \_ wszWMBeatsPerMinute                        | **\_stringa di tipo WMT \_**                                |
| [**WM/categoria**](wm-category.md)                                                   | g \_ wszWMCategory                              | **\_stringa di tipo WMT \_**                                |
| [**WM/codec**](wm-codec.md)                                                         | g \_ wszWMCodec                                 | **\_stringa di tipo WMT \_**                                |
| [**WM/Composer**](wm-composer.md)                                                   | g \_ wszWMComposer                              | **\_stringa di tipo WMT \_**                                |
| [**WM/conduttore**](wm-conductor.md)                                                 | g \_ wszWMConductor                             | **\_stringa di tipo WMT \_**                                |
| [**WM/ContainerFormat**](wm-containerformat.md)                                     | g \_ wszWMContainerFormat                       | **WMT \_ \_formato di archiviazione** (**\_ \_ binario di tipo WMT**)     |
| [**WM/ContentDistributor**](wm-contentdistributor.md)                               | g \_ wszWMContentDistributor                    | **\_stringa di tipo WMT \_**                                |
| [**WM/ContentGroupDescription**](wm-contentgroupdescription.md)                     | g \_ wszWMContentGroupDescription               | **\_stringa di tipo WMT \_**                                |
| [**WM/Director**](wm-director.md)                                                   | g \_ wszWMDirector                              | **\_stringa di tipo WMT \_**                                |
| [**WM/DRM**](wm-drm.md)                                                             | g \_ wszWMDRM                                   | **\_stringa di tipo WMT \_**                                |
| [**WM/DVDID**](wm-dvdid.md)                                                         | g \_ wszWMDVDID                                 | **\_stringa di tipo WMT \_**                                |
| [**WM/EncodedBy**](wm-encodedby.md)                                                 | g \_ wszWMEncodedBy                             | **\_stringa di tipo WMT \_**                                |
| [**WM/EncodingSettings**](wm-encodingsettings.md)                                   | g \_ wszWMEncodingSettings                      | **\_stringa di tipo WMT \_**                                |
| [**WM/EncodingTime**](wm-encodingtime.md)                                           | g \_ wszWMEncodingTime                          | **FILETIME** (**\_ tipo WMT \_ QWORD**)                  |
| [**WM/genre**](wm-genre.md)                                                         | g \_ wszWMGenre                                 | **\_stringa di tipo WMT \_**                                |
| [**WM/GenreID**](wm-genreid.md)                                                     | g \_ wszWMGenreID                               | **\_stringa di tipo WMT \_**                                |
| [**WM/InitialKey**](wm-initialkey.md)                                               | g \_ wszWMInitialKey                            | **\_stringa di tipo WMT \_**                                |
| [**WM/ISRC**](wm-isrc.md)                                                           | g \_ wszWMISRC                                  | **\_stringa di tipo WMT \_**                                |
| [**WM/lingua**](wm-language.md)                                                   | g \_ wszWMLanguage                              | **\_stringa di tipo WMT \_**                                |
| [**WM/lyrics**](wm-lyrics.md)                                                       | g \_ wszWMLyrics                                | **\_stringa di tipo WMT \_**                                |
| [**WM/lyrics \_ sincronizzati**](wm-lyrics-synchronised.md)                            | g \_ wszWMLyrics \_ sincronizzato                  | **WM \_ \_lyrics sincronizzati** (**WMT di \_ tipo \_ binario**) |
| [**WM/MCDI**](wm-mcdi.md)                                                           | g \_ wszWMMCDI                                  | **\_binario di tipo WMT \_**                                |
| [**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)                                  | g \_ wszWMMediaClassPrimaryID                   | **\_GUID di tipo WMT \_**                                  |
| [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)                              | g \_ wszWMMediaClassSecondaryID                 | **\_GUID di tipo WMT \_**                                  |
| [**WM/MediaCredits**](wm-mediacredits.md)                                           | g \_ wszWMMediaCredits                          | **\_stringa di tipo WMT \_**                                |
| [**WM/MediaIsDelay**](wm-mediaisdelay.md)                                           | g \_ wszWMMediaIsDelay                          | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaIsFinale**](wm-mediaisfinale.md)                                         | g \_ wszWMMediaIsFinale                         | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaIsLive**](wm-mediaislive.md)                                             | g \_ wszWMMediaIsLive                           | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaIsPremiere**](wm-mediaispremiere.md)                                     | g \_ wszWMMediaIsPremiere                       | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaIsRepeat**](wm-mediaisrepeat.md)                                         | g \_ wszWMMediaIsRepeat                         | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaIsSAP**](wm-mediaissap.md)                                               | g \_ wszWMMediaIsSAP                            | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaIsStereo**](wm-mediaisstereo.md)                                         | g \_ wszWMMediaIsStereo                         | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaIsSubtitled**](wm-mediaissubtitled.md)                                   | g \_ wszWMMediaIsSubtitled                      | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaIsTape**](wm-mediaistape.md)                                             | g \_ wszWMMediaIsTape                           | **\_tipo WMT \_ bool**                                  |
| [**WM/MediaNetworkAffiliation**](wm-medianetworkaffiliation.md)                     | g \_ wszWMMediaNetworkAffiliation               | **\_stringa di tipo WMT \_**                                |
| [**WM/MediaOriginalBroadcastDateTime**](wm-mediaoriginalbroadcastdatetime.md)       | g \_ wszWMMediaOriginalBroadcastDateTime        | **\_stringa di tipo WMT \_**                                |
| [**WM/MediaOriginalChannel**](wm-mediaoriginalchannel.md)                           | g \_ wszWMMediaOriginalChannel                  | **\_stringa di tipo WMT \_**                                |
| [**WM/MediaStationCallSign**](wm-mediastationcallsign.md)                           | g \_ wszWMMediaStationCallSign                  | **\_stringa di tipo WMT \_**                                |
| [**WM/MediaStationName**](wm-mediastationname.md)                                   | g \_ wszWMMediaStationName                      | **\_stringa di tipo WMT \_**                                |
| [**WM/ModifiedBy**](wm-modifiedby.md)                                               | g \_ wszWMModifiedBy                            | **\_stringa di tipo WMT \_**                                |
| [**WM/umore**](wm-mood.md)                                                           | g \_ wszWMMood                                  | **\_stringa di tipo WMT \_**                                |
| [**WM/OriginalAlbumTitle**](wm-originalalbumtitle.md)                               | g \_ wszWMOriginalAlbumTitle                    | **\_stringa di tipo WMT \_**                                |
| [**WM/OriginalArtist**](wm-originalartist.md)                                       | g \_ wszWMOriginalArtist                        | **\_stringa di tipo WMT \_**                                |
| [**WM/OriginalFilename**](wm-originalfilename.md)                                   | g \_ wszWMOriginalFilename                      | **\_stringa di tipo WMT \_**                                |
| [**WM/OriginalLyricist**](wm-originallyricist.md)                                   | g \_ wszWMOriginalLyricist                      | **\_stringa di tipo WMT \_**                                |
| [**WM/OriginalReleaseTime**](wm-originalreleasetime.md)                             | g \_ wszWMOriginalReleaseTime                   | **\_stringa di tipo WMT \_**                                |
| [**WM/OriginalReleaseYear**](wm-originalreleaseyear.md)                             | g \_ wszWMOriginalReleaseYear                   | **\_stringa di tipo WMT \_**                                |
| [**WM/ParentalRating**](wm-parentalrating.md)                                       | g \_ wszWMParentalRating                        | **\_stringa di tipo WMT \_**                                |
| [**WM/ParentalRatingReason**](wm-parentalratingreason.md)                           | g \_ wszWMParentalRatingReason                  | **\_stringa di tipo WMT \_**                                |
| [**WM/PartOfSet**](wm-partofset.md)                                                 | g \_ wszWMPartOfSet                             | **\_stringa di tipo WMT \_**                                |
| [**WM/PeakBitrate**](wm-peakbitrate.md)                                             | g \_ wszWMPeakBitrate                           | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/periodo**](wm-period.md)                                                       | g \_ wszWMPeriod                                | **\_stringa di tipo WMT \_**                                |
| [**WM/immagine**](/windows/desktop/wmformat/wmpicture)                                      | g \_ wszWMPicture                               | **WM \_ PICTURE** (**\_ \_ Binary di tipo WMT**)              |
| [**WM/PlaylistDelay**](wm-playlistdelay.md)                                         | g \_ wszWMPlaylistDelay                         | **\_stringa di tipo WMT \_**                                |
| [**WM/Producer**](wm-producer.md)                                                   | g \_ wszWMProducer                              | **\_stringa di tipo WMT \_**                                |
| [**WM/PromotionURL**](wm-promotionurl.md)                                           | g \_ wszWMPromotionURL                          | **\_stringa di tipo WMT \_**                                |
| [**WM/ProtectionType**](wm-protectiontype.md)                                       | g \_ wszWMProtectionType                        | **\_stringa di tipo WMT \_**                                |
| [**WM/provider**](wm-provider.md)                                                   | g \_ wszWMProvider                              | **\_stringa di tipo WMT \_**                                |
| [**WM/ProviderCopyright**](wm-providercopyright.md)                                 | g \_ wszWMProviderCopyright                     | **\_stringa di tipo WMT \_**                                |
| [**WM/ProviderRating**](wm-providerrating.md)                                       | g \_ wszWMProviderRating                        | **\_stringa di tipo WMT \_**                                |
| [**WM/ProviderStyle**](wm-providerstyle.md)                                         | g \_ wszWMProviderStyle                         | **\_stringa di tipo WMT \_**                                |
| [**WM/Publisher**](wm-publisher.md)                                                 | g \_ wszWMPublisher                             | **\_stringa di tipo WMT \_**                                |
| [**WM/radiostationname**](wm-radiostationname.md)                                   | g \_ wszWMRadioStationName                      | **\_stringa di tipo WMT \_**                                |
| [**WM/RadioStationOwner**](wm-radiostationowner.md)                                 | g \_ wszWMRadioStationOwner                     | **\_stringa di tipo WMT \_**                                |
| [**WM/SharedUserRating**](wm-shareduserrating.md)                                   | g \_ wszWMSharedUserRating                      | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/StreamTypeInfo**](wm-streamtypeinfo.md)                                       | g \_ wszWMStreamTypeInfo                        | **WM \_ \_ \_ informazioni sul tipo di flusso** (**\_ \_ Binary di tipo WMT**)   |
| [**WM/SubscriptionContentID**](wm-subscriptioncontentid.md)                         | g \_ wszWMSubscriptionContentID                 | **\_stringa di tipo WMT \_**                                |
| [**WM/sottotitolo**](wm-subtitle.md)                                                   | g \_ wszWMSubTitle                              | **\_stringa di tipo WMT \_**                                |
| [**WM/SubTitleDescription**](wm-subtitledescription.md)                             | g \_ wszWMSubTitleDescription                   | **\_stringa di tipo WMT \_**                                |
| [**WM/testo**](wm-text.md)                                                           | g \_ wszWMText                                  | **WM \_ \_testo utente** (**WMT di \_ tipo \_ binario**)           |
| [**WM/ToolName**](wm-toolname.md)                                                   | g \_ wszWMToolName                              | **\_stringa di tipo WMT \_**                                |
| [**WM/ToolVersion dell'**](wm-toolversion.md)                                             | g \_ wszWMToolVersion                           | **\_stringa di tipo WMT \_**                                |
| [**WM/Track**](wm-track.md)                                                         | g \_ wszWMTrack                                 | **\_stringa di tipo WMT \_**                                |
| [**WM/numero**](wm-tracknumber.md)                                             | g \_ wszWMTrackNumber                           | **\_stringa di tipo WMT \_**                                |
| [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)                           | g \_ wszWMUniqueFileIdentifier                  | **\_stringa di tipo WMT \_**                                |
| [**WM/UserWebURL**](wm-userweburl.md)                                               | g \_ wszWMUserWebURL                            | **WM \_ \_ \_ URL Web utente** (**WMT \_ tipo \_ binario**)       |
| [**WM/VideoClosedCaptioning**](wm-videoclosedcaptioning.md)                         | g \_ wszWMVideoClosedCaptioning                 | **\_tipo WMT \_ bool**                                  |
| [**WM/VideoFrameRate**](wm-videoframerate.md)                                       | g \_ wszWMVideoFrameRate                        | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/VideoHeight**](wm-videoheight.md)                                             | g \_ wszWMVideoHeight                           | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/VideoWidth**](wm-videowidth.md)                                               | g \_ wszWMVideoWidth                            | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)                       | g \_ wszWMWMADRCAverageReference                | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)                             | g \_ wszWMWMADRCAverageTarget                   | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)                             | g \_ wszWMWMADRCPeakReference                   | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)                                   | g \_ wszWMWMADRCPeakTarget                      | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)                             | g \_ wszWMWMCollectionGroupID                   | **\_GUID di tipo WMT \_**                                  |
| [**WM/WMCollectionID**](wm-wmcollectionid.md)                                       | g \_ wszWMWMCollectionID                        | **\_GUID di tipo WMT \_**                                  |
| [**WM/WMContentID**](wm-wmcontentid.md)                                             | g \_ wszWMWMContentID                           | **\_GUID di tipo WMT \_**                                  |
| [**WM/WMShadowFileSourceDRMType**](wm-wmshadowfilesourcedrmtype.md)                 | g \_ wszWMWMShadowFileSourceDRMType             | **\_stringa di tipo WMT \_**                                |
| [**WM/WMShadowFileSourceFileType**](wm-wmshadowfilesourcefiletype.md)               | g \_ wszWMWMShadowFileSourceFileType            | **\_stringa di tipo WMT \_**                                |
| [**WM/writer**](wm-writer.md)                                                       | g \_ wszWMWriter                                | **\_stringa di tipo WMT \_**                                |
| [**WM/anno**](wm-year.md)                                                           | g \_ wszWMYear                                  | **\_stringa di tipo WMT \_**                                |



 

## <a name="remarks"></a>Commenti

Le costanti seguenti sono definite con gli attributi. Ognuno indica il numero di un tipo specifico di attributo. Non è necessario usare questi valori per qualsiasi elemento nelle applicazioni.



| Costante                 | Valore |
|--------------------------|-------|
| g \_ dwWMSpecialAttributes | 20    |
| g \_ dwWMContentAttributes | 5     |
| g \_ dwWMNSCAttributes     | 5     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 