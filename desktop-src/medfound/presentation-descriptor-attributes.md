---
description: Attributi del descrittore di presentazione
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Attributi del descrittore di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb9947a926fc6ea5e21f81219e6bd8d85a8d74bea9b9432ac497c539450b638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238967"
---
# <a name="presentation-descriptor-attributes"></a>Attributi del descrittore di presentazione

## <a name="common-presentation-descriptor-attributes"></a>Attributi comuni del descrittore di presentazione

Gli attributi seguenti possono essere applicati a qualsiasi descrittore di presentazione.



| Attributo                                                                          | Descrizione                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CONTESTO \_ DELL'APP MF PD \_ \_**](mf-pd-app-context-attribute.md)                        | Contiene un puntatore al descrittore di presentazione dal percorso del supporto protetto (PMP).                                                          |
| [**VELOCITÀ IN BIT DELLA CODIFICA \_ AUDIO PD MF \_ \_ \_**](mf-pd-audio-encoding-bitrate-attribute.md) | Specifica la velocità in bit di codifica audio per la presentazione, in bit al secondo.                                                                 |
| [MF \_ PD \_ AUDIO \_ ISVARIABLEBITRATE](mf-pd-audio-isvariablebitrate.md)              | Specifica se i flussi audio nella presentazione hanno una velocità in bit variabile.                                                               |
| [**MF \_ PD \_ DURATION**](mf-pd-duration-attribute.md)                               | Specifica la durata di una presentazione, in unità di 100 nanosecondi.                                                                              |
| [**ORA ULTIMA MODIFICA DEL FILE MF \_ PD \_ \_ \_**](mf-pd-last-modified-time-attribute.md)         | Specifica l'ultima modifica di una presentazione.                                                                                                |
| [**MF \_ PD \_ MIME \_ TYPE**](mf-pd-mime-type-attribute.md)                            | Specifica il tipo MIME del contenuto.                                                                                                         |
| [TEMPO LIMITE \_ RIPRODUZIONE MF PD \_ \_ \_](mf-pd-playback-boundary-time.md)               | Ora in cui deve iniziare la presentazione, rispetto all'inizio dell'origine multimediale.                                                       |
| [ID \_ DELL'ELEMENTO DI RIPRODUZIONE DEL PD MF \_ \_ \_](mf-pd-playback-element-id.md)                     | Identificatore dell'elemento playlist nella presentazione.                                                                                     |
| [**CONTESTO MF \_ PD \_ \_ PMPHOST**](mf-pd-pmphost-context-attribute.md)                | Contiene un puntatore all'oggetto proxy per il descrittore di presentazione dell'applicazione.                                                           |
| [MF \_ PD \_ PREFERRED \_ LANGUAGE](mf-pd-preferred-language.md)                        | Contiene la lingua RFC 1766 preferita dell'origine multimediale.                                                                                   |
| [**MF \_ PD \_ SAMI \_ STYLELIST**](mf-pd-sami-stylelist-attribute.md)                  | Contiene il nome descrittivo degli stili SAMI (Synchronized Accessible Media Interchange) supportati. Questo attributo si applica solo ai file SAMI. |
| [**MF \_ PD \_ TOTAL \_ FILE \_ SIZE**](mf-pd-total-file-size-attribute.md)               | Specifica le dimensioni totali del file di origine, in byte.                                                                                          |
| [**VELOCITÀ IN BIT \_ DELLA CODIFICA VIDEO MF PD \_ \_ \_**](mf-pd-video-encoding-bitrate-attribute.md) | Specifica la velocità in bit di codifica video per la presentazione, in bit al secondo.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Attributi del descrittore di presentazione per ASF

Gli attributi seguenti si applicano ai descrittori di presentazione per i file ASF (Advanced Systems Format).



| Attributo                                                                                                             | Descrizione                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md)                                                       | Contiene informazioni sui codec usati per codificare il contenuto in un file ASF.                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Specifica l'identificatore di chiave per un file ASF crittografato.                                              |
| [**URL DI LICENZA \_ DI MF PD \_ \_ ASF CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Specifica l'URL di acquisizione della licenza per un file ASF crittografato.                                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ SECRET \_ DATA**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Contiene dati segreti per un file ASF crittografato.                                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ TYPE**](mf-pd-asf-contentencryption-type-attribute.md)                            | Specifica il tipo di meccanismo di protezione usato in un file ASF.                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTIONEX \_ ENCRYPTION \_ DATA**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Contiene i dati di crittografia per un file ASF.                                                            |
| [**MF \_ PD \_ ASF \_ DATA \_ LENGTH**](mf-pd-asf-data-length-attribute.md)                                                  | Specifica le dimensioni, in byte, della sezione di dati di un file ASF.                                    |
| [**MF \_ PD \_ ASF \_ DATA \_ START \_ OFFSET**](mf-pd-asf-data-start-offset-attribute.md)                                     | Specifica l'offset, in byte, dall'inizio di un file ASF all'inizio del primo pacchetto di dati. |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ CREATION \_ TIME**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Specifica la data e l'ora di creazione iniziale di un file ASF.                                  |
| [**\_MF PD \_ ASF \_ \_ FILEPROPRIETÀ \_ ID FILE**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Specifica l'identificatore di file di un file ASF.                                                        |
| [**FILE \_ ASF MF \_ \_ FILEPROPERTIES \_ FLAGS**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Contiene flag vari da un'intestazione ASF.                                                     |
| [**FILE \_ ASF PD \_ \_ MFPROPRIETÀ \_ VELOCITÀ \_ IN BIT MASSIMA**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Specifica la velocità in bit massima istantanea, in bit al secondo, per un file ASF.                   |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Specifica le dimensioni massime del pacchetto, in byte, per un file ASF                                         |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Specifica le dimensioni minime del pacchetto, in byte, per un file ASF.                                        |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PACKETS**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Specifica il numero di pacchetti nella sezione data di un file ASF.                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PLAY \_ DURATION**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Specifica il tempo necessario per riprodurre un file ASF, in unità di 100 nanosecondi.                              |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PREROLL**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Specifica il tempo di memorizzazione nel buffer dei dati prima di iniziare a riprodurre un file ASF, espresso in millisecondi.    |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Specifica il tempo necessario per inviare un file ASF, in unità di 100 nanosecondi.                              |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ AUDIO**](mf-pd-asf-info-has-audio-attribute.md)                                           | Specifica se un file ASF contiene almeno un flusso audio.                                    |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ NON \_ AUDIO \_ VIDEO**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Specifica se un file ASF contiene flussi non audio e non video.                             |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ VIDEO**](mf-pd-asf-info-has-video-attribute.md)                                           | Specifica se un file ASF contiene almeno un flusso video.                                    |
| [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)                                                         | Specifica l'elenco delle lingue usate in un file ASF.                                                 |
| [MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER](mf-pd-asf-langlist-legacyorder.md)                                              | Contiene un elenco di lingue RFC 1766 usate nella presentazione corrente.                              |
| [**MF \_ PD \_ ASF \_ MARKER**](mf-pd-asf-marker-attribute.md)                                                             | Specifica i marcatori in un file ASF.                                                                |
| [**MF \_ PD \_ ASF \_ METADATA \_ IS \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Specifica se un file ASF usa la codifica VBR (Variable Bit Rate).                                 |
| [**COPPIE DI BUCKET DI PERDITA DEI \_ \_ METADATI ASF DEL PD \_ \_ \_ \_ MF**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Descrive i requisiti di memorizzazione nel buffer per un file ASF VBR.                                             |
| [**MF \_ PD \_ ASF \_ METADATA \_ V8 \_ BUFFERAVERAGE**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Specifica le dimensioni medie del buffer necessarie per un file ASF VBR.                                         |
| [**MF \_ PD \_ ASF \_ METADATA \_ V8 \_ VBRPEAK**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Specifica la velocità in bit momentanea più elevata in un file ASF VBR.                                          |
| [**MF \_ PD \_ ASF \_ SCRIPT**](mf-pd-asf-script-attribute.md)                                                             | Specifica i comandi script in un file ASF.                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



