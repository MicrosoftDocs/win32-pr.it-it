---
description: '\_album di \_ Immagini del tipo di contenuto WPD \_ \_'
ms.assetid: e2ae9f89-5a71-4443-b0c1-81e4c650e1bb
title: WPD_CONTENT_TYPE_IMAGE_ALBUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67a20f6a6628008e31b23a0ceb05fee4931793a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316345"
---
# <a name="wpd_content_type_image_album"></a>\_album di \_ Immagini del tipo di contenuto WPD \_ \_

Un oggetto che descrive il tipo come \_ \_ \_ album di tipo di contenuto WPD \_ rappresenta una raccolta di immagini ancora. Un album di immagini è equivalente dal punto di vista funzionale a una playlist di file di immagine, ma viene usato per rappresentare un album di foto fisico per l'utente finale.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                              |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.    |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                         |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                         |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà anche al momento della creazione.     |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                         |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                         |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                 |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema, ovvero rappresenta un file di sistema. |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                 |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                         |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.             |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                           |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                         |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                         |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                            |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                         |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                      |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                         |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                        |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                         |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | Facoltativo                                                                          |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                         |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | facoltativo.                                                                         |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



