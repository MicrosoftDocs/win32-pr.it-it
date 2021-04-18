---
description: '\_ \_ archiviazione categoria funzionale \_ WPD'
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3000c63207286bc1dae153e3f930231909e92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316801"
---
# <a name="wpd_functional_category_storage"></a>\_ \_ archiviazione categoria funzionale \_ WPD

Un \_ \_ \_ oggetto funzionale archiviazione categoria funzionale WPD incapsula l'archiviazione di file fisici nel dispositivo.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                                                         |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                                                                                              |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio.                                                                                                                                              |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                                                         |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                                                                                              |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                                                                                              |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                                                      |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                                                                  |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                                                                                      |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                                                              |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                                                                                  |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                                                                                |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                                                                                              |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                                                                                              |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                                                                 |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                                                                                              |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                                                                                           |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                                                                                              |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                                                                                             |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                                                                                              |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                                                                                              |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                                                                                              |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | facoltativo.                                                                                                                                              |
| [\_ \_ categoria oggetto funzionale \_ WPD](miscellaneous-properties.md)                      | Obbligatorio. Vedere [**\_ \_ \_ \_ oggetto funzionale del tipo di contenuto WPD**](wpd-content-type-functional-object.md) per le categorie definite da dispositivi portatili Windows. |
| [\_tipo di archiviazione WPD \_](storage-properties.md)                                                         | Obbligatorio.                                                                                                                                              |
| [\_tipo di \_ file \_ System di archiviazione \_ WPD](storage-properties.md)                               | facoltativo.                                                                                                                                              |
| [\_capacità di archiviazione WPD \_](storage-properties.md)                                                 | Obbligatorio.                                                                                                                                              |
| [\_ \_ spazio libero di archiviazione WPD \_ \_ in \_ byte](storage-properties.md)                        | facoltativo.                                                                                                                                              |
| [\_ \_ spazio libero di archiviazione WPD \_ \_ negli \_ oggetti](storage-properties.md)                    | facoltativo.                                                                                                                                              |
| [\_Descrizione archiviazione \_ WPD](storage-properties.md)                                           | facoltativo.                                                                                                                                              |
| [\_numero di \_ serie di archiviazione WPD \_](storage-properties.md)                                      | facoltativo.                                                                                                                                              |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                    | Obbligatorio o facoltativo | Descrizione                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**\_icona della risorsa WPD \_**](wpd-resource-icon.md) | facoltativo.            | Contiene la rappresentazione dell'icona per questa risorsa di archiviazione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_ \_ oggetto funzionale del tipo di contenuto WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



