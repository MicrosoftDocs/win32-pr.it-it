---
description: '\_immagine del \_ tipo di contenuto WPD \_'
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d547a6190df01f495c0a340010b4305f5c77bf5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316344"
---
# <a name="wpd_content_type_image"></a>\_immagine del \_ tipo di contenuto WPD \_

Un oggetto che descrive il tipo come \_ immagine del tipo di contenuto WPD \_ \_ rappresenta un'immagine ancora.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                   |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                                        |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                                        |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                   |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                                        |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                                        |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                            |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                                |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                        |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                            |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                          |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                                        |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                                        |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                           |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                                        |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                                     |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                                        |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                                       |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                                        |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                                        |
| [immagine di WPD \_ \_ BITDEPTH](image-properties.md)                                                       | Consigliato.                                                                                     |
| [\_ \_ stato ritagliato immagine WPD \_](image-properties.md)                                          | facoltativo.                                                                                        |
| [\_ \_ \_ stato correzione colore immagine \_ WPD](image-properties.md)                         | facoltativo.                                                                                        |
| [immagine di WPD \_ \_ FNUMBER](image-properties.md)                                                                           | facoltativo.                                                                                        |
| [WPD \_ \_ tempo di esposizione immagine \_](image-properties.md)                                                                    | facoltativo.                                                                                        |
| [\_indice di \_ esposizione \_ Immagini WPD](image-properties.md)                                                                   | facoltativo.                                                                                        |
| [\_ \_ risoluzione orizzontale immagine \_ WPD](image-properties.md)                                                            | facoltativo.                                                                                        |
| [\_ \_ risoluzione verticale dell'immagine WPD \_](image-properties.md)                                                              | facoltativo.                                                                                        |
| [\_copyright per supporti WPD \_](media-properties.md)                                                     | facoltativo.                                                                                        |
| [\_Larghezza supporto \_ WPD](media-properties.md)                                                             | Obbligatorio.                                                                                        |
| [\_altezza supporto \_ WPD](media-properties.md)                                                           | Obbligatorio.                                                                                        |
| [WPD \_ media \_ Artist](media-properties.md)                                                                            | Consigliato.                                                                                     |
| [WPD \_ media \_ album \_ Artist](media-properties.md)                                                                     | Consigliato. Questa proprietà identifica la persona, o persone, che ha originariamente creato questo oggetto. |
| [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)                                                                       | facoltativo.                                                                                        |
| [\_ \_ URL destinazione supporto \_ WPD](media-properties.md)                                                                  | facoltativo.                                                                                        |
| [\_Descrizione supporto \_ WPD](media-properties.md)                                                                       | facoltativo.                                                                                        |
| [\_genere multimediale \_ WPD](media-properties.md)                                                                             | facoltativo.                                                                                        |
| [\_ \_ segnalibro WPD Media byte \_](media-properties.md)                                                                    | facoltativo.                                                                                        |
| [\_GUID del supporto WPD \_](media-properties.md)                                                                              | facoltativo.                                                                                        |
| [\_ \_ Descrizione secondaria supporti \_ WPD](media-properties.md)                                                                  | facoltativo.                                                                                        |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                                 | Obbligatorio o facoltativo | Descrizione                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md)        | Obbligatorio.            | Contiene i dati dell'immagine.                                                                 |
| [**\_anteprima della risorsa WPD \_**](wpd-resource-thumbnail.md)    | Consigliato.         | Contiene l'anteprima dell'immagine.                                                    |
| [**\_ \_ clip audio della risorsa WPD \_**](wpd-resource-audio-clip.md) | facoltativo.            | Se questa immagine ha un'annotazione audio associata, questa risorsa contiene i dati audio. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



