---
description: '\_video del \_ tipo di contenuto WPD \_'
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afde065ef233ff64a4eb72af8be5f7308050ff75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316338"
---
# <a name="wpd_content_type_video"></a>\_video del \_ tipo di contenuto WPD \_

Un oggetto che descrive il tipo di \_ contenuto WPD \_ \_ video rappresenta un file video.

Questo tipo di oggetto supporta le proprietà seguenti.



|                                                                                                                       |                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Nome della proprietà**                                                                                                     | **Obbligatorio o facoltativo**                                                                                                     |
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                               |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                                                                    |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                                                                    |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                               |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                                                                    |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                                                                    |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                            |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                                        |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                                                            |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                                    |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                                                        |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                                                      |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                                                                    |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                                                                    |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                                       |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                                                                    |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                                                                 |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                                                                    |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                                                                   |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                                                                    |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                                                                    |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                                                                    |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | facoltativo.                                                                                                                    |
| [\_velocità in \_ bit totale media \_ WPD](media-properties.md)                                            | Consigliato.                                                                                                                 |
| [\_tipo di \_ bitrate WPD media \_](media-properties.md)                                              | facoltativo.                                                                                                                    |
| [\_copyright per supporti WPD \_](media-properties.md)                                                     | facoltativo.                                                                                                                    |
| [\_ \_ \_ ID contenuto sottoscrizione multimediale \_ WPD](media-properties.md)                       | Consigliato, se questo oggetto rappresenta il contenuto di un servizio di sottoscrizione online.                                          |
| [\_ \_ conteggio utilizzo supporti \_ WPD](media-properties.md)                                                    | Consigliato.                                                                                                                 |
| [\_conteggio elementi multimediali WPD \_ \_](media-properties.md)                                                  | facoltativo.                                                                                                                    |
| [\_ \_ \_ ora ultimo accesso \_ ai supporti WPD](media-properties.md)                                 | facoltativo.                                                                                                                    |
| [\_ \_ classificazione parentale media \_ WPD](media-properties.md)                                        | facoltativo.                                                                                                                    |
| [\_ \_ meta genere WPD \_ media](media-properties.md)                                                  | facoltativo.                                                                                                                    |
| [WPD \_ media \_ Composer](media-properties.md)                                                       | facoltativo.                                                                                                                    |
| [\_ \_ classificazione effettiva media \_ WPD](media-properties.md)                                      | facoltativo.                                                                                                                    |
| [\_sottotitolo supporto WPD \_ \_](media-properties.md)                                                    | facoltativo.                                                                                                                    |
| [\_Data di \_ rilascio del supporto WPD \_](media-properties.md)                                              | Consigliato.                                                                                                                 |
| [\_frequenza di \_ campionamento dei supporti WPD \_](media-properties.md)                                                | facoltativo.                                                                                                                    |
| [\_classificazione media \_ Star \_ WPD](media-properties.md)                                                | Consigliato.                                                                                                                 |
| [\_ \_ \_ valutazione efficace utente media \_ WPD](media-properties.md)                           | Consigliato.                                                                                                                 |
| [\_titolo supporto \_ WPD](media-properties.md)                                                             | Obbligatorio.                                                                                                                    |
| [\_durata supporto \_ WPD](media-properties.md)                                                       | Obbligatorio.                                                                                                                    |
| [WPD \_ media \_ Acquista \_ ora](media-properties.md)                                                        | Consigliato.                                                                                                                 |
| [\_profilo di \_ codifica \_ multimediale WPD](media-properties.md)                                      | facoltativo.                                                                                                                    |
| [\_Larghezza supporto \_ WPD](media-properties.md)                                                             | Obbligatorio.                                                                                                                    |
| [\_altezza supporto \_ WPD](media-properties.md)                                                           | Obbligatorio.                                                                                                                    |
| [WPD \_ media \_ Artist](media-properties.md)                                                           | Consigliato.                                                                                                                 |
| [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)                                                  | Consigliato.                                                                                                                 |
| [\_ \_ URL destinazione supporto \_ WPD](media-properties.md)                                        | facoltativo.                                                                                                                    |
| [\_Descrizione supporto \_ WPD](media-properties.md)                                                 | facoltativo.                                                                                                                    |
| [\_genere multimediale \_ WPD](media-properties.md)                                                             | facoltativo.                                                                                                                    |
| [\_ \_ segnalibro WPD tempo medio \_](media-properties.md)                                            | facoltativo.                                                                                                                    |
| [\_ \_ segnalibro WPD Media byte \_](media-properties.md)                                            | facoltativo.                                                                                                                    |
| [\_GUID del supporto WPD \_](media-properties.md)                                                               | facoltativo.                                                                                                                    |
| [\_ \_ Descrizione secondaria supporti \_ WPD](media-properties.md)                                        | facoltativo.                                                                                                                    |
| [\_autore video \_ WPD](video-properties.md)                                                           | facoltativo.                                                                                                                    |
| [\_nome della \_ \_ stazione RECORDEDTV del video \_ WPD](video-properties.md)                       | facoltativo.                                                                                                                    |
| [WPD \_ video \_ - \_ numero di canale RECORDEDTV \_](video-properties.md)                   | facoltativo.                                                                                                                    |
| [\_ \_ ripetizione RECORDEDTV video \_ WPD](video-properties.md)                                    | facoltativo.                                                                                                                    |
| [\_dimensioni del \_ buffer \_ video WPD](video-properties.md)                                                | facoltativo.                                                                                                                    |
| [\_crediti video \_ WPD](video-properties.md)                                                         | facoltativo.                                                                                                                    |
| [\_ \_ \_ distanza fotogramma chiave video WPD \_](video-properties.md)                                 | facoltativo.                                                                                                                    |
| [\_ \_ impostazione qualità video \_ WPD](video-properties.md)                                        | facoltativo.                                                                                                                    |
| [\_tipo di \_ analisi \_ video WPD](video-properties.md)                                                    | Obbligatorio.                                                                                                                    |
| [\_velocità in \_ bit video WPD](video-properties.md)                                                         | Obbligatorio.                                                                                                                    |
| [\_ \_ Codice FourCC video \_ WPD](video-properties.md)                                                | Obbligatorio se il codec è supportato da Microsoft video for Windows (VFW), Microsoft DirectShow e Windows Media Format. |
| [\_framerate video \_ WPD](video-properties.md)                                                     | facoltativo.                                                                                                                    |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                              | Obbligatorio o facoltativo       | Descrizione                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md)     | Obbligatorio.                  | Contiene i dati video (file).                                      |
| [**\_anteprima della risorsa WPD \_**](wpd-resource-thumbnail.md) | Consigliato, se disponibile. | Contiene il fotogramma chiave o un altro frame di esempio non vuoto per il video. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



