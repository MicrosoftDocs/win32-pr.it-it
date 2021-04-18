---
description: '\_associazione di \_ rete del tipo di contenuto WPD \_ \_'
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab3fd2f76efef5b85991f1334977c17e34d06b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316342"
---
# <a name="wpd_content_type_network_association"></a>\_associazione di \_ rete del tipo di contenuto WPD \_ \_

Un oggetto che descrive il tipo come WPD \_ Content \_ Type \_ Network \_ Association rappresenta un'associazione tra un host e un dispositivo.

Questo tipo di oggetto supporta le proprietà seguenti.



|                                                                                                                                              |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Nome della proprietà**                                                                                                                            | **Obbligatorio o facoltativo**                                              |
| [\_ID oggetto \_ WPD](object-properties.md)                                                                                       | Obbligatorio.                                                             |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                                        | Obbligatorio.                                                             |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                                                   | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                             |
| [\_formato oggetto \_ WPD](object-properties.md)                                                                               | Obbligatorio.                                                             |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                                                  | Obbligatorio.                                                             |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                                           | Obbligatorio se l'oggetto è nascosto.                                     |
| [\_oggetto WPD \_](object-properties.md)                                                                           | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                                                   | Obbligatorio se l'oggetto ha almeno una risorsa.                     |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                                                     | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                                              | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo. |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                                       | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                                           | facoltativo.                                                             |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                                            | facoltativo.                                                             |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                                         | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                                                  | facoltativo.                                                             |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                                                | Consigliato.                                                          |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                                                | facoltativo.                                                             |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                                       | Consigliato se un altro oggetto fa riferimento all'oggetto.            |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)                            | facoltativo.                                                             |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md)                        | facoltativo.                                                             |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                      | Obbligatorio se l'oggetto non può essere eliminato.                             |
| [\_lingua dell'oggetto WPD \_ \_ locale](object-properties.md)                                                                                        | facoltativo.                                                             |
| [\_ \_ \_ \_ identificatori di rete dell'host di associazione di rete WPD \_](network-association-properties.md) | Obbligatorio.                                                             |
| [\_ \_ X509V3SEQUENCE associazione di rete WPD \_](network-association-properties.md)                       | facoltativo.                                                             |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



