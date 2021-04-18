---
description: '\_ \_ dispositivo categoria funzionale \_ WPD'
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb179311af5fb3c3eef063157e3615b21eeb66a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316332"
---
# <a name="wpd_functional_category_device"></a>\_ \_ dispositivo categoria funzionale \_ WPD

Un \_ \_ \_ oggetto funzionale del dispositivo della categoria funzionale WPD incapsula il dispositivo, ovvero l'oggetto di primo livello del dispositivo. Se un dispositivo implementa questa categoria funzionale, deve supportare queste proprietà, oltre alle proprietà elencate per l' [oggetto dispositivo](device-object.md).



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                      |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                                                           |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio.                                                                                                           |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                      |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                                                           |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                                                           |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                   |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                               |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                                                   |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                           |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                                               |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                                             |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                                                           |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                                                           |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                              |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                                                           |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                                                        |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                                                           |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                                                          |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                                                           |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                                                           |
| [\_ \_ categoria oggetto funzionale \_ WPD](miscellaneous-properties.md)                      | Obbligatorio.                                                                                                           |
| [\_ \_ partner sincronizzazione dispositivi \_ WPD](device-properties.md)                                           | facoltativo.                                                                                                           |
| [\_versione del \_ firmware del dispositivo WPD \_](device-properties.md)                                   | Obbligatorio.                                                                                                           |
| [\_livello di \_ alimentazione del dispositivo WPD \_](device-properties.md)                                             | Consigliato se il dispositivo ha una batteria.                                                                                |
| [\_ \_ origine alimentazione dispositivo \_ WPD](device-properties.md)                                           | Consigliato.                                                                                                        |
| [\_protocollo del dispositivo WPD \_](device-properties.md)                                                    | Consigliato.                                                                                                        |
| [\_produttore del dispositivo WPD \_](device-properties.md)                                            | Obbligatorio.                                                                                                           |
| [\_modello di dispositivo WPD \_](device-properties.md)                                                          | Obbligatorio.                                                                                                           |
| [\_numero di \_ serie del dispositivo WPD \_](device-properties.md)                                         | Obbligatorio.                                                                                                           |
| [il \_ dispositivo WPD \_ supporta \_ non \_ utilizzabile](device-properties.md)                    | Obbligatorio se il dispositivo supporta oggetti non utilizzabili; ovvero, se il dispositivo può essere usato per l'archiviazione semplice dei dati. |
| [\_DateTime del dispositivo WPD \_](device-properties.md)                                                    | facoltativo.                                                                                                           |
| [\_ \_ nome descrittivo del dispositivo WPD \_](device-properties.md)                                         | Consigliato.                                                                                                        |
| [\_ \_ \_ schemi DRM supportati dal dispositivo WPD \_](device-properties.md)                        | Consigliato se il dispositivo supporta la tecnologia DRM.                                                                  |
| [\_ \_ \_ \_ sono ordinati i formati supportati per il dispositivo WPD \_](device-properties.md)       | Consigliato se il dispositivo supporta l'ordinamento del formato preferito.                                                       |
| [\_tipo di dispositivo WPD \_](device-properties.md)                                                            | Consigliato.                                                                                                        |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_ \_ oggetto funzionale del tipo di contenuto WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



