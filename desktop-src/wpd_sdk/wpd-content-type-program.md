---
description: '\_ \_ programma tipo di contenuto WPD \_'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0187d4e87f47e8210e94a676ca9ccd1e1364cf1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758438"
---
# <a name="wpd_content_type_program"></a>\_ \_ programma tipo di contenuto WPD \_

Un oggetto che descrive il tipo come WPD \_ Content \_ Type \_ Program rappresenta un programma eseguibile.

Questo tipo di oggetto supporta le proprietà seguenti.



|                                                                                                                       |                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Nome della proprietà**                                                                                                     | **Obbligatorio o facoltativo**                                                           |
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, ma di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                          |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                          |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà anche al momento della creazione.      |
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
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                          |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | facoltativo.                                                                          |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo | Descrizione                |
|--------------------------------------------------------|----------------------|----------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md) | Obbligatorio.            | Contiene il file di programma. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



