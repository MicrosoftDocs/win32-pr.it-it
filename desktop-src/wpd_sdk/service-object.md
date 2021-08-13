---
description: Oggetto service
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Oggetto service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587ca25e1e9fc225a0b555263bf3f3f4e725c83e5f9b01e716fd6fa191fc270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445585"
---
# <a name="service-object"></a>Oggetto service

L'oggetto servizio deve supportare le proprietà seguenti.



| Nome della proprietà                                                                                                                      | Obbligatorio o facoltativo                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Obbligatorio. .                                                                           |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Obbligatorio.                                                                             |
| [NOME OGGETTO \_ WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Obbligatorio.                                                                             |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Obbligatorio.                                                                             |
| [OGGETTO WPD \_ \_ ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obbligatorio se l'oggetto servizio non deve essere visualizzato all'utente.                       |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obbligatorio se l'oggetto è un oggetto di sistema, ad esempio rappresenta un file di sistema. |
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Obbligatorio. Rappresenta il tipo di servizio del dispositivo, ad esempio CONTATTI DEL SERVIZIO.          |
| [VERSIONE DEL SERVIZIO WPD \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obbligatorio.                                                                             |
| [TIPO DI ARCHIVIAZIONE WPD \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Obbligatorio se il servizio viene utilizzato per archiviare oggetti.                                     |
| [CAPACITÀ DI ARCHIVIAZIONE WPD \_ \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Obbligatorio se il servizio viene utilizzato per archiviare oggetti.                                     |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="typical-formats"></a>Formati tipici

L'elenco seguente identifica i formati tipici usati dall'oggetto Service. Tuttavia, questo oggetto non è limitato a questi formati.

-   FORMATO OGGETTO WPD \_ \_ NON \_ SPECIFICATO

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 
