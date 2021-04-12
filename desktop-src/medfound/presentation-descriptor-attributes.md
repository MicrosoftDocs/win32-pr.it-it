---
description: Attributi del descrittore della presentazione
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Attributi del descrittore della presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bba97a0e0428bf2ceb91b04c79f69b557876a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527853"
---
# <a name="presentation-descriptor-attributes"></a>Attributi del descrittore della presentazione

## <a name="common-presentation-descriptor-attributes"></a>Attributi comuni del descrittore di presentazione

Gli attributi seguenti possono essere applicati a qualsiasi descrittore di presentazione.



| Attributo                                                                          | Descrizione                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contesto dell' \_ app MF PD \_**](mf-pd-app-context-attribute.md)                        | Contiene un puntatore al descrittore di presentazione dal percorso multimediale protetto (PMP).                                                          |
| [**\_velocità in \_ \_ bit di codifica audio MF PD \_**](mf-pd-audio-encoding-bitrate-attribute.md) | Specifica la velocità in bit per la codifica audio per la presentazione, in bit al secondo.                                                                 |
| [\_ \_ ISVARIABLEBITRATE audio MF \_ PD](mf-pd-audio-isvariablebitrate.md)              | Specifica se i flussi audio nella presentazione presentano una velocità in bit variabile.                                                               |
| [**\_durata MF PD \_**](mf-pd-duration-attribute.md)                               | Specifica la durata di una presentazione, in unità di 100 nanosecondi.                                                                              |
| [**\_ \_ \_ ora Ultima modifica \_ MF PD**](mf-pd-last-modified-time-attribute.md)         | Specifica la data dell'Ultima modifica di una presentazione.                                                                                                |
| [**\_ \_ tipo MIME PD \_ MF**](mf-pd-mime-type-attribute.md)                            | Specifica il tipo MIME del contenuto.                                                                                                         |
| [\_ \_ \_ tempo limite riproduzione MF \_ PD](mf-pd-playback-boundary-time.md)               | Ora in cui deve iniziare la presentazione, relativa all'inizio dell'origine del supporto.                                                       |
| [\_ \_ ID elemento di riproduzione MF PD \_ \_](mf-pd-playback-element-id.md)                     | Identificatore dell'elemento della playlist nella presentazione.                                                                                     |
| [**\_ \_ contesto PMPHOST MF \_ PD**](mf-pd-pmphost-context-attribute.md)                | Contiene un puntatore all'oggetto proxy per il descrittore di presentazione dell'applicazione.                                                           |
| [\_ \_ lingua preferita MF \_ PD](mf-pd-preferred-language.md)                        | Contiene la lingua RFC 1766 preferita dell'origine multimediale.                                                                                   |
| [**\_ \_ stile Sami di MF PD \_**](mf-pd-sami-stylelist-attribute.md)                  | Contiene il nome descrittivo degli stili SAMI (Synchronized Media Interchange) supportati. Questo attributo si applica solo ai file SAMI. |
| [**\_ \_ dimensioni totali del \_ file MF PD \_**](mf-pd-total-file-size-attribute.md)               | Specifica le dimensioni totali, in byte, del file di origine.                                                                                          |
| [**\_velocità in \_ \_ bit di codifica video MF PD \_**](mf-pd-video-encoding-bitrate-attribute.md) | Specifica la velocità in bit per la codifica video per la presentazione, in bit al secondo.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Attributi del descrittore di presentazione per ASF

Gli attributi seguenti si applicano ai descrittori di presentazione per i file di formato Advanced Systems (ASF).



| Attributo                                                                                                             | Descrizione                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**codec di MF \_ PD \_ ASF \_**](mf-pd-asf-codeclist-attribute.md)                                                       | Contiene informazioni sui codec utilizzati per codificare il contenuto in un file ASF.                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Specifica l'identificatore di chiave per un file ASF crittografato.                                              |
| [**\_URL della licenza MF PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Specifica l'URL di acquisizione della licenza per un file ASF crittografato.                                     |
| [**\_ \_ \_ dati segreti del CONTENTENCRYPTION \_ MF PD ASF \_**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Contiene dati segreti per un file ASF crittografato.                                                      |
| [**\_tipo di CONTENTENCRYPTION MF PD \_ ASF \_ \_**](mf-pd-asf-contentencryption-type-attribute.md)                            | Specifica il tipo di meccanismo di protezione utilizzato in un file ASF.                                      |
| [**\_dati di crittografia MF PD \_ ASF \_ CONTENTENCRYPTIONEX \_ \_**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Contiene i dati di crittografia per un file ASF.                                                            |
| [**\_ \_ \_ lunghezza dei dati MF PD ASF \_**](mf-pd-asf-data-length-attribute.md)                                                  | Specifica la dimensione, in byte, della sezione di dati di un file ASF.                                    |
| [**\_ \_ \_ \_ offset avvio dati ASF MF PD \_**](mf-pd-asf-data-start-offset-attribute.md)                                     | Specifica l'offset, in byte, dall'inizio di un file ASF all'inizio del primo pacchetto di dati. |
| [**ora di creazione delle proprietà di MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Specifica la data e l'ora di creazione iniziale di un file ASF.                                  |
| [**\_ \_ \_ ID file delle proprietà dell'ASF MF \_ PD \_**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Specifica l'identificatore di file di un file ASF.                                                        |
| [**flag per le proprietà di MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Contiene i flag vari da un'intestazione ASF.                                                     |
| [**\_velocità in \_ \_ \_ bit max PD ASF FileProperties \_**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Specifica la velocità in bit massima istantanea, in bit al secondo, per un file ASF.                   |
| [**\_dimensioni del \_ \_ \_ pacchetto max PD ASF FileProperties \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Specifica la dimensione massima del pacchetto, in byte, per un file ASF                                         |
| [**\_ \_ \_ \_ dimensioni minime del \_ pacchetto \_ per le proprietà ASF del valore MF PD ASF**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Specifica le dimensioni minime del pacchetto, in byte, per un file ASF.                                        |
| [**\_ \_ \_ pacchetti FileProperties ASF MF \_ PD**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Specifica il numero di pacchetti nella sezione dati di un file ASF.                                  |
| [**\_ \_ \_ durata riproduzione FileProperties ASF \_ di MF PD \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Specifica il tempo necessario per riprodurre un file ASF, in unità di 100 nanosecondi.                              |
| [**preroll delle proprietà di MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Specifica la quantità di tempo per il buffering dei dati prima di iniziare a riprodurre un file ASF, in millisecondi.    |
| [**\_durata dell' \_ \_ invio delle Proprietà FileProperties ASF \_ \_ di MF PD**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Specifica il tempo necessario per l'invio di un file ASF, in unità di 100 nanosecondi.                              |
| [**informazioni su MF \_ PD \_ ASF \_ \_ con \_ audio**](mf-pd-asf-info-has-audio-attribute.md)                                           | Specifica se un file ASF contiene almeno un flusso audio.                                    |
| [**il \_ video sulle informazioni di MF PD \_ ASF \_ \_ è \_ non \_ audio \_**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Specifica se un file ASF contiene flussi non audio e non video.                             |
| [**informazioni su MF \_ PD \_ ASF \_ \_ con \_ video**](mf-pd-asf-info-has-video-attribute.md)                                           | Specifica se un file ASF contiene almeno un flusso video.                                    |
| [**lingua di MF \_ PD \_ ASF \_**](mf-pd-asf-langlist-attribute.md)                                                         | Specifica l'elenco di lingue utilizzate in un file ASF.                                                 |
| [LEGACYORDER di MF \_ PD \_ ASF \_ \_](mf-pd-asf-langlist-legacyorder.md)                                              | Contiene un elenco di lingue RFC 1766 utilizzate nella presentazione corrente.                              |
| [**\_ \_ marcatore ASF MF PD \_**](mf-pd-asf-marker-attribute.md)                                                             | Specifica i marcatori in un file ASF.                                                                |
| [**i \_ metadati di MF PD \_ ASF \_ \_ sono \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Specifica se un file ASF utilizza la codifica con velocità in bit variabile (VBR).                                 |
| [**coppie di bucket per i metadati di MF \_ PD \_ ASF \_ \_ \_ \_**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Descrive i requisiti di buffering per un file ASF VBR.                                             |
| [**Metadati di MF \_ PD \_ ASF \_ \_ V8 \_ BUFFERAVERAGE**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Specifica la dimensione media del buffer necessaria per un file ASF VBR.                                         |
| [**Metadati di MF \_ PD \_ ASF \_ \_ V8 \_ VBRPEAK**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Specifica la velocità in bit più elevata del momento in un file ASF VBR.                                          |
| [**\_script MF PD \_ ASF \_**](mf-pd-asf-script-attribute.md)                                                             | Specifica i comandi script in un file ASF.                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



