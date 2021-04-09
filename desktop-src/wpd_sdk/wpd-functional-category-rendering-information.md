---
description: '\_ \_ \_ informazioni sul rendering della categoria funzionale WPD \_'
ms.assetid: 84ec6f14-fe90-42a5-ba2b-6c4cc406935c
title: WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf2a5b981b75820b566e3133faab22c2f35860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968150"
---
# <a name="wpd_functional_category_rendering_information"></a>\_ \_ \_ informazioni sul rendering della categoria funzionale WPD \_

Un \_ \_ \_ \_ oggetto funzionale delle informazioni di rendering della categoria funzionale WPD descrive il tipo di file multimediali che il dispositivo è in grado di eseguire il rendering.



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
| [\_ \_ profili informazioni di rendering WPD \_](miscellaneous-properties.md)              | Obbligatorio.                                                                                                                                              |
| [\_tipo di \_ \_ voce del profilo informazioni di rendering \_ WPD \_](miscellaneous-properties.md)                                     | facoltativo.                                                                                                                                              |
| [\_ \_ \_ \_ \_ risorsa creabile voce profilo informazioni rendering \_ WPD](miscellaneous-properties.md)                      | facoltativo.                                                                                                                                              |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_ \_ oggetto funzionale del tipo di contenuto WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



