---
description: '\_audio del \_ tipo di contenuto WPD \_'
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83d43fcef539579fc0a687a97ba51e52278e4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316357"
---
# <a name="wpd_content_type_audio"></a>\_audio del \_ tipo di contenuto WPD \_

Un oggetto che descrive il tipo come \_ audio del tipo di contenuto WPD \_ \_ rappresenta un file audio, ad esempio un file di Windows Media Audio (WMA) o MP3.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.     |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                          |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                          |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.     |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                          |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                          |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                  |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).              |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                  |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                          |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.              |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                            |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                          |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                          |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                             |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                          |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                       |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                          |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                         |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                          |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                          |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                     | Obbligatorio se l'oggetto può essere eliminato.                                             |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | facoltativo.                                                                          |
| [\_velocità in \_ bit totale media \_ WPD](media-properties.md)                                            | Consigliato.                                                                       |
| [\_tipo di \_ bitrate WPD media \_](media-properties.md)                                              | facoltativo.                                                                          |
| [\_copyright per supporti WPD \_](media-properties.md)                                                     | facoltativo.                                                                          |
| [\_ \_ \_ ID contenuto sottoscrizione multimediale \_ WPD](media-properties.md)                       | Consigliato se questo oggetto rappresenta il contenuto di un servizio di sottoscrizione online. |
| [\_ \_ conteggio utilizzo supporti \_ WPD](media-properties.md)                                                    | Consigliato.                                                                       |
| [\_conteggio elementi multimediali WPD \_ \_](media-properties.md)                                                  | facoltativo.                                                                          |
| [\_ \_ \_ ora ultimo accesso \_ ai supporti WPD](media-properties.md)                                 | facoltativo.                                                                          |
| [\_ \_ classificazione parentale media \_ WPD](media-properties.md)                                        | facoltativo.                                                                          |
| [\_ \_ meta genere WPD \_ media](media-properties.md)                                                  | facoltativo.                                                                          |
| [WPD \_ media \_ Composer](media-properties.md)                                                       | facoltativo.                                                                          |
| [\_ \_ classificazione effettiva media \_ WPD](media-properties.md)                                      | facoltativo.                                                                          |
| [\_sottotitolo supporto WPD \_ \_](media-properties.md)                                                    | facoltativo.                                                                          |
| [\_Data di \_ rilascio del supporto WPD \_](media-properties.md)                                              | Consigliato.                                                                       |
| [\_frequenza di \_ campionamento dei supporti WPD \_](media-properties.md)                                                | facoltativo.                                                                          |
| [\_classificazione media \_ Star \_ WPD](media-properties.md)                                                | Consigliato.                                                                       |
| [\_ \_ \_ valutazione efficace utente media \_ WPD](media-properties.md)                           | Consigliato.                                                                       |
| [\_titolo supporto \_ WPD](media-properties.md)                                                             | Obbligatorio.                                                                          |
| [\_durata supporto \_ WPD](media-properties.md)                                                       | Obbligatorio.                                                                          |
| [WPD \_ media \_ Acquista \_ ora](media-properties.md)                                                        | Consigliato.                                                                       |
| [\_profilo di \_ codifica \_ multimediale WPD](media-properties.md)                                      | facoltativo.                                                                          |
| [WPD \_ media \_ Artist](media-properties.md)                                                                            | Consigliato.                                                                       |
| [WPD \_ media \_ album \_ Artist](media-properties.md)                                                                     | Consigliato.                                                                       |
| [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)                                                                       | facoltativo.                                                                          |
| [\_ \_ URL destinazione supporto \_ WPD](media-properties.md)                                                                  | facoltativo.                                                                          |
| [\_Descrizione supporto \_ WPD](media-properties.md)                                                                       | facoltativo.                                                                          |
| [\_genere multimediale \_ WPD](media-properties.md)                                                                             | facoltativo.                                                                          |
| [\_ \_ segnalibro WPD tempo medio \_](media-properties.md)                                                                    | facoltativo.                                                                          |
| [\_ \_ segnalibro WPD Media byte \_](media-properties.md)                                                                    | facoltativo.                                                                          |
| [\_GUID del supporto WPD \_](media-properties.md)                                                                              | facoltativo.                                                                          |
| [\_ \_ Descrizione secondaria supporti \_ WPD](media-properties.md)                                                                  | facoltativo.                                                                          |
| [\_album musica \_ WPD](music-properties.md)                                                             | Consigliato.                                                                       |
| [WPD \_ Music \_ Track](music-properties.md)                                                             | Consigliato.                                                                       |
| [WPD \_ Music \_ lyrics](music-properties.md)                                                           | facoltativo.                                                                          |
| [WPD \_ Music \_ Mood](music-properties.md)                                                               | facoltativo.                                                                          |
| [\_velocità in \_ bit audio WPD](audio-properties.md)                                                         | Consigliato.                                                                       |
| [\_numero di \_ canali \_ audio WPD](audio-properties.md)                                            | facoltativo.                                                                          |
| [\_codice del \_ formato \_ audio WPD](audio-properties.md)                                                | facoltativo.                                                                          |
| [\_ \_ profondità bit audio \_ WPD](audio-properties.md)                                                    | facoltativo.                                                                          |
| [\_ \_ allineamento blocchi audio \_ WPD](audio-properties.md)                                        | facoltativo.                                                                          |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                               | Obbligatorio o facoltativo       | Descrizione                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md)      | facoltativo.                  | Contiene il file audio completo.                  |
| [**\_Art album delle risorse WPD \_ \_**](wpd-resource-album-art.md) | Consigliato, se disponibile. | Contiene l'immagine per l'album.                |
| [**\_AUDIOCLIP risorse \_ WPD**](wpd-resource-audio-clip.md) | facoltativo.                  | Contiene una clip di esempio del file audio completo. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



