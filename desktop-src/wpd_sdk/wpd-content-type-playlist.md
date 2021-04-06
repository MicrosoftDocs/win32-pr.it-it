---
description: '\_playlist del \_ tipo di contenuto WPD \_'
ms.assetid: 4223970d-8c37-4326-a2df-bec558f8ac5e
title: WPD_CONTENT_TYPE_PLAYLIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b650527d92d2b3523654b3445aaf60496aae3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758441"
---
# <a name="wpd_content_type_playlist"></a>\_playlist del \_ tipo di contenuto WPD \_

Un oggetto che descrive il tipo come \_ playlist del tipo di contenuto WPD \_ \_ rappresenta una playlist. Una playlist può essere rappresentata da un file fisico oppure può essere costituita da riferimenti archiviati come metadati.

Questo tipo di oggetto supporta le proprietà seguenti.



|                                                                                                                       |                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome della proprietà**                                                                                                     | **Obbligatorio o facoltativo**                                                                                                                       |
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà anche al momento della creazione.                                                                  |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                                                                                      |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                                                                                      |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                                                 |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                                                                                      |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                                                                                      |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                                              |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                                                          |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                                                                              |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                                                      |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                                                                          |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti; ovvero se i riferimenti vengono archiviati come metadati anziché come dati fisici in un file. |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                                                                                      |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                                                                                      |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                                                         |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                                                                                      |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                                                                                   |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                                                                                      |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                                                                                     |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                                                                                      |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                                                                                      |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                                                                                      |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | facoltativo.                                                                                                                                      |
| [\_ \_ segnalibro oggetto multimediale WPD \_](object-properties.md)                                                                 | Consigliato.                                                                                                                                   |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo | Descrizione                                                                                                                  |
|--------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md) | facoltativo.            | Se la playlist è un file fisico, ad esempio un file XML che elenca i file multimediali da riprodurre, si tratta dei byte di file effettivi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



