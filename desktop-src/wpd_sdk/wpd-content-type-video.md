---
description: VIDEO SUL TIPO DI CONTENUTO WPD \_ \_ \_
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aacf30a9e646a6089058104bd39577fad832e31
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424122"
---
# <a name="wpd_content_type_video"></a>VIDEO SUL TIPO DI CONTENUTO WPD \_ \_ \_

Un oggetto che descrive il tipo come WPD \_ CONTENT TYPE VIDEO rappresenta un file \_ \_ video.

Questo tipo di oggetto supporta le proprietà seguenti.



|  Nome della proprietà                             | Obbligatorio o facoltativo              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                               |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                                                                                    |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                                                                    |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                               |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                                                                    |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                                                                    |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                            |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                                        |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto dispone di almeno una risorsa.                                                                            |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                                    |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo.                                                        |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                                                      |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                                                                    |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                                                                    |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                                       |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                                                                    |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                                                                 |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                         | facoltativo.                                                                                                                    |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                                                | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.                                                                   |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                                                                    |
| [GENERAZIONE \_ DELL'ANTEPRIMA \_ \_ DELL'OGGETTO \_ WPD DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                                                                    |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                                                                    |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                | facoltativo.                                                                                                                    |
| [VELOCITÀ IN \_ BIT TOTALE DEI FILE MULTIMEDIALI WPD \_ \_](media-properties.md)                                            | Consigliato.                                                                                                                 |
| [TIPO DI VELOCITÀ IN \_ \_ BIT MULTIMEDIALE WPD \_](media-properties.md)                                              | facoltativo.                                                                                                                    |
| [COPYRIGHT DEI SUPPORTI WPD \_ \_](media-properties.md)                                                     | facoltativo.                                                                                                                    |
| [ID CONTENUTO SOTTOSCRIZIONE MULTIMEDIALE WPD \_ \_ \_ \_](media-properties.md)                       | Consigliato, se questo oggetto rappresenta il contenuto di un servizio di sottoscrizione online.                                          |
| [NUMERO DI USI DEI FILE MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                                    | Consigliato.                                                                                                                 |
| [NUMERO DI SKIP MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                                  | facoltativo.                                                                                                                    |
| [ORA \_ DELL'ULTIMO ACCESSO AI FILE MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                 | facoltativo.                                                                                                                    |
| [WPD \_ MEDIA \_ PARENT \_ RATING](media-properties.md)                                        | facoltativo.                                                                                                                    |
| [META-GENERE \_ \_ MULTIMEDIALE WPD \_](media-properties.md)                                                  | facoltativo.                                                                                                                    |
| [WPD \_ MEDIA \_ COMPOSER](media-properties.md)                                                       | facoltativo.                                                                                                                    |
| [CLASSIFICAZIONE MEDIA EFFECTIVE WPD \_ \_ \_](media-properties.md)                                      | facoltativo.                                                                                                                    |
| [TITOLO SECONDARIO \_ FILE \_ MULTIMEDIALI \_ WPD](media-properties.md)                                                    | facoltativo.                                                                                                                    |
| [DATA DI RILASCIO DEI FILE MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                              | Consigliato.                                                                                                                 |
| [FREQUENZA DI \_ CAMPIONAMENTO DEI FILE \_ MULTIMEDIALI WPD \_](media-properties.md)                                                | facoltativo.                                                                                                                    |
| [CLASSIFICAZIONE MEDIA STAR WPD \_ \_ \_](media-properties.md)                                                | Consigliato.                                                                                                                 |
| [WPD \_ MEDIA \_ USER \_ EFFECTIVE \_ RATING](media-properties.md)                           | Consigliato.                                                                                                                 |
| [TITOLO MULTIMEDIALE WPD \_ \_](media-properties.md)                                                             | Obbligatorio.                                                                                                                    |
| [DURATA DEI SUPPORTI WPD \_ \_](media-properties.md)                                                       | Obbligatorio.                                                                                                                    |
| [ACQUISTO DI SUPPORTI WPD \_ \_ \_](media-properties.md)                                                        | Consigliato.                                                                                                                 |
| [PROFILO DI CODIFICA \_ MULTIMEDIALE \_ \_ WPD](media-properties.md)                                      | facoltativo.                                                                                                                    |
| [LARGHEZZA DEI SUPPORTI WPD \_ \_](media-properties.md)                                                             | Obbligatorio.                                                                                                                    |
| [ALTEZZA DEI SUPPORTI WPD \_ \_](media-properties.md)                                                           | Obbligatorio.                                                                                                                    |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                                           | Consigliato.                                                                                                                 |
| [URL ORIGINE SUPPORTO WPD \_ \_ \_](media-properties.md)                                                  | Consigliato.                                                                                                                 |
| [URL DESTINAZIONE SUPPORTI WPD \_ \_ \_](media-properties.md)                                        | facoltativo.                                                                                                                    |
| [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)                                                 | facoltativo.                                                                                                                    |
| [GENERE MULTIMEDIALE WPD \_ \_](media-properties.md)                                                             | facoltativo.                                                                                                                    |
| [SEGNALIBRO ORA SUPPORTO WPD \_ \_ \_](media-properties.md)                                            | facoltativo.                                                                                                                    |
| [SEGNALIBRO BYTE MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                            | facoltativo.                                                                                                                    |
| [GUID SUPPORTO WPD \_ \_](media-properties.md)                                                               | facoltativo.                                                                                                                    |
| [DESCRIZIONE DELLA \_ SOTTOSOD MEDIA \_ \_ WPD](media-properties.md)                                        | facoltativo.                                                                                                                    |
| [AUTORE \_ DI VIDEO WPD \_](video-properties.md)                                                           | facoltativo.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ STATION \_ NAME](video-properties.md)                       | facoltativo.                                                                                                                    |
| [NUMERO DI \_ CANALE WPD VIDEO \_ REGISTRATOTV \_ \_](video-properties.md)                   | facoltativo.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT](video-properties.md)                                    | facoltativo.                                                                                                                    |
| [DIMENSIONI DEL \_ BUFFER VIDEO WPD \_ \_](video-properties.md)                                                | facoltativo.                                                                                                                    |
| [CREDITI VIDEO WPD \_ \_](video-properties.md)                                                         | facoltativo.                                                                                                                    |
| [DISTANZA DEL \_ FOTOGRAMMA CHIAVE VIDEO WPD \_ \_ \_](video-properties.md)                                 | facoltativo.                                                                                                                    |
| [IMPOSTAZIONE QUALITÀ VIDEO WPD \_ \_ \_](video-properties.md)                                        | facoltativo.                                                                                                                    |
| [TIPO DI ANALISI VIDEO WPD \_ \_ \_](video-properties.md)                                                    | Obbligatorio.                                                                                                                    |
| [VELOCITÀ IN \_ BIT VIDEO WPD \_](video-properties.md)                                                         | Obbligatorio.                                                                                                                    |
| [WPD \_ VIDEO \_ FOURCC \_ CODE](video-properties.md)                                                | Obbligatorio se il codec è supportato da Microsoft Video per Windows (VFW), Microsoft DirectShow e Windows Media Format. |
| [FREQUENZA \_ FOTOGRAMMI VIDEO WPD \_](video-properties.md)                                                     | facoltativo.                                                                                                                    |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                              | Obbligatorio o facoltativo       | Descrizione                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**RISORSA WPD \_ \_ PREDEFINITA**](wpd-resource-default.md)     | Obbligatorio.                  | Contiene i dati video (file).                                      |
| [**ANTEPRIMA DELLE RISORSE WPD \_ \_**](wpd-resource-thumbnail.md) | Consigliato, se disponibile. | Contiene il fotogramma chiave o un altro fotogramma di esempio non vuota per il video. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



