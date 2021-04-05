---
description: Oggetto servizio
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Oggetto servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885314"
---
# <a name="service-object"></a>Oggetto servizio

L'oggetto servizio deve supportare le seguenti proprietà.



| Nome della proprietà                                                                                                                      | Obbligatorio o facoltativo                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Obbligatorio. .                                                                           |
| [\_ \_ ID padre dell'oggetto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Obbligatorio.                                                                             |
| [\_nome dell'oggetto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Obbligatorio.                                                                             |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Obbligatorio.                                                                             |
| [\_oggetto WPD \_ nascosto](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obbligatorio se l'oggetto servizio non deve essere visualizzato all'utente.                       |
| [\_oggetto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obbligatorio se l'oggetto è un oggetto di sistema (ad esempio, rappresenta un file di sistema). |
| [\_ \_ categoria oggetto funzionale \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Obbligatorio. Rappresenta il tipo di servizio del dispositivo, ad esempio i contatti del servizio.          |
| [\_versione del servizio WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obbligatorio.                                                                             |
| [\_tipo di archiviazione WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Obbligatorio se il servizio viene utilizzato per archiviare gli oggetti.                                     |
| [\_capacità di archiviazione WPD \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Obbligatorio se il servizio viene utilizzato per archiviare gli oggetti.                                     |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="typical-formats"></a>Formati tipici

Nell'elenco seguente vengono identificati i formati tipici utilizzati dall'oggetto servizio. Questo oggetto, tuttavia, non è limitato a questi formati.

-   \_formato oggetto WPD non \_ \_ specificato

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 
