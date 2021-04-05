---
description: '\_ \_ servizio tipo di contenuto WPD \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968155"
---
# <a name="wpd_content_type_service"></a>\_ \_ servizio tipo di contenuto WPD \_

Un oggetto che descrive il tipo come \_ servizio del tipo di contenuto WPD \_ \_ rappresenta un servizio del dispositivo.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                        | Obbligatorio o facoltativo                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                               | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                | Obbligatorio.                                                                      |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)         | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                   | Obbligatorio se il servizio non deve essere visualizzato all'utente.                       |
| [\_oggetto WPD \_](object-properties.md)                                   | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).          |
| [\_ \_ categoria oggetto funzionale \_ WPD](object-properties.md) | Obbligatorio. Rappresenta il tipo di servizio del dispositivo.                             |
| [\_versione del servizio WPD \_](object-properties.md)           | Obbligatorio.                                                                      |
| [\_tipo di archiviazione WPD \_](object-properties.md)                                                          | Obbligatorio se il servizio viene utilizzato per archiviare gli oggetti.                              |
| [\_capacità di archiviazione WPD \_](object-properties.md)                                                      | Obbligatorio se il servizio viene utilizzato per archiviare gli oggetti.                              |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



