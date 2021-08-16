---
description: AUDIO DEL TIPO DI CONTENUTO WPD \_ \_ \_
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd4aa78b7fa546fab9fe186265ca721e441860a2fc55c2ba0b384df377e1344b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842355"
---
# <a name="wpd_content_type_audio"></a>AUDIO DEL TIPO DI CONTENUTO WPD \_ \_ \_

Un oggetto che ne descrive il tipo come WPD CONTENT TYPE AUDIO rappresenta un file audio, ad esempio \_ un file Windows Media Audio \_ \_ (WMA) o MP3.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.     |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio.                                                                          |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                          |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.     |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                          |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                          |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                  |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).              |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                  |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                          |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.              |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                            |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                          |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                          |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                             |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                          |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                       |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                         | facoltativo.                                                                          |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                         |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                          |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                          |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto può essere eliminato.                                             |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                | facoltativo.                                                                          |
| [VELOCITÀ IN \_ BIT TOTALE DEI FILE MULTIMEDIALI WPD \_ \_](media-properties.md)                                            | Consigliato.                                                                       |
| [TIPO DI VELOCITÀ IN \_ \_ BIT MULTIMEDIALE WPD \_](media-properties.md)                                              | facoltativo.                                                                          |
| [COPYRIGHT MULTIMEDIALE WPD \_ \_](media-properties.md)                                                     | facoltativo.                                                                          |
| [ID CONTENUTO SOTTOSCRIZIONE MULTIMEDIALE WPD \_ \_ \_ \_](media-properties.md)                       | Consigliato se questo oggetto rappresenta il contenuto di un servizio di sottoscrizione online. |
| [WPD \_ MEDIA USE COUNT (CONTEGGIO USO SUPPORTI WPD) \_ \_](media-properties.md)                                                    | Consigliato.                                                                       |
| [NUMERO DI SKIP MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                                  | facoltativo.                                                                          |
| [ORA \_ DELL'ULTIMO ACCESSO AI FILE MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                 | facoltativo.                                                                          |
| [WPD \_ MEDIA \_ PARENT \_ RATING](media-properties.md)                                        | facoltativo.                                                                          |
| [META-GENERE \_ \_ MULTIMEDIALE WPD \_](media-properties.md)                                                  | facoltativo.                                                                          |
| [WPD \_ MEDIA \_ COMPOSER](media-properties.md)                                                       | facoltativo.                                                                          |
| [CLASSIFICAZIONE MEDIA EFFECTIVE WPD \_ \_ \_](media-properties.md)                                      | facoltativo.                                                                          |
| [TITOLO SECONDARIO \_ \_ SUPPORTI WPD \_](media-properties.md)                                                    | facoltativo.                                                                          |
| [DATA DI RILASCIO DEI FILE MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                              | Consigliato.                                                                       |
| [FREQUENZA DI \_ CAMPIONAMENTO DEI FILE \_ MULTIMEDIALI WPD \_](media-properties.md)                                                | facoltativo.                                                                          |
| [CLASSIFICAZIONE MEDIA STAR WPD \_ \_ \_](media-properties.md)                                                | Consigliato.                                                                       |
| [WPD \_ MEDIA \_ USER \_ EFFECTIVE \_ RATING](media-properties.md)                           | Consigliato.                                                                       |
| [TITOLO \_ MULTIMEDIALE \_ WPD](media-properties.md)                                                             | Obbligatorio.                                                                          |
| [DURATA DEI FILE \_ MULTIMEDIALI \_ WPD](media-properties.md)                                                       | Obbligatorio.                                                                          |
| [WPD \_ MEDIA \_ BUY \_ NOW](media-properties.md)                                                        | Consigliato.                                                                       |
| [PROFILO DI CODIFICA \_ MULTIMEDIALE \_ \_ WPD](media-properties.md)                                      | facoltativo.                                                                          |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                                                            | Consigliato.                                                                       |
| [WPD \_ MEDIA \_ ALBUM \_ ARTIST](media-properties.md)                                                                     | Consigliato.                                                                       |
| [URL ORIGINE MULTIMEDIALE WPD \_ \_ \_](media-properties.md)                                                                       | facoltativo.                                                                          |
| [URL DESTINAZIONE SUPPORTO WPD \_ \_ \_](media-properties.md)                                                                  | facoltativo.                                                                          |
| [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)                                                                       | facoltativo.                                                                          |
| [GENERE MULTIMEDIALE WPD \_ \_](media-properties.md)                                                                             | facoltativo.                                                                          |
| [SEGNALIBRO ORA \_ \_ MULTIMEDIALE WPD \_](media-properties.md)                                                                    | facoltativo.                                                                          |
| [SEGNALIBRO MEDIA BYTE WPD \_ \_ \_](media-properties.md)                                                                    | facoltativo.                                                                          |
| [GUID SUPPORTO WPD \_ \_](media-properties.md)                                                                              | facoltativo.                                                                          |
| [DESCRIZIONE SECONDARIA \_ DEI \_ SUPPORTI WPD \_](media-properties.md)                                                                  | facoltativo.                                                                          |
| [ALBUM MUSICALE \_ WPD \_](music-properties.md)                                                             | Consigliato.                                                                       |
| [TRACCIA MUSICALE \_ WPD \_](music-properties.md)                                                             | Consigliato.                                                                       |
| [WPD \_ MUSIC \_ LYRICS](music-properties.md)                                                           | facoltativo.                                                                          |
| [WPD \_ MUSIC \_ MOOD](music-properties.md)                                                               | facoltativo.                                                                          |
| [VELOCITÀ IN \_ BIT AUDIO WPD \_](audio-properties.md)                                                         | Consigliato.                                                                       |
| [NUMERO DI CANALI \_ AUDIO WPD \_ \_](audio-properties.md)                                            | facoltativo.                                                                          |
| [CODICE DI FORMATO AUDIO WPD \_ \_ \_](audio-properties.md)                                                | facoltativo.                                                                          |
| [PROFONDITÀ IN \_ BIT AUDIO WPD \_ \_](audio-properties.md)                                                    | facoltativo.                                                                          |
| [ALLINEAMENTO DEI BLOCCHI AUDIO WPD \_ \_ \_](audio-properties.md)                                        | facoltativo.                                                                          |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                               | Obbligatorio o facoltativo       | Descrizione                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**RISORSA WPD \_ \_ PREDEFINITA**](wpd-resource-default.md)      | facoltativo.                  | Contiene il file audio completo.                  |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md) | Consigliato, se disponibile. | Contiene l'immagine dell'album.                |
| [**AUDIOCLIP \_ DELLA \_ RISORSA WPD**](wpd-resource-audio-clip.md) | facoltativo.                  | Contiene un clip di esempio del file audio completo. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



