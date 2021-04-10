---
description: '\_sezione del \_ tipo di contenuto WPD \_'
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fbb63821f75115c5855653dc811067891652615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058078"
---
# <a name="wpd_content_type_section"></a>\_sezione del \_ tipo di contenuto WPD \_

Un oggetto che descrive il tipo come \_ \_ \_ sezione del tipo di contenuto WPD rappresenta una sezione di dati contenuta in un altro oggetto. Un file audio di grandi dimensioni, ad esempio, può essere descritto come una raccolta di più capitoli e ogni capitolo potrebbe essere un \_ oggetto della sezione del tipo di contenuto WPD \_ \_ .

La \_ \_ Proprietà References dell'oggetto WPD identifica l'oggetto padre di una sezione specificata.

Questo tipo di oggetto supporta le proprietà seguenti.



|                                                                                                                                  |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Nome della proprietà**                                                                                                                | **Obbligatorio o facoltativo**                                              |
| [\_ID oggetto \_ WPD](object-properties.md)                                                                           | Obbligatorio.                                                             |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio.                                                             |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                                       | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                                     | Obbligatorio.                                                             |
| [\_formato oggetto \_ WPD](object-properties.md)                                                                   | Obbligatorio.                                                             |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                                      | Obbligatorio.                                                             |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                               | Obbligatorio se l'oggetto è nascosto.                                     |
| [\_oggetto WPD \_](object-properties.md)                                                               | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                                       | Obbligatorio se l'oggetto ha almeno una risorsa.                     |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                                         | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                                  | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo. |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                           | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                               | facoltativo.                                                             |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                                | facoltativo.                                                             |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                             | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                                      | facoltativo.                                                             |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                                    | Consigliato.                                                          |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                                    | facoltativo.                                                             |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                | Consigliato se l'oggetto contiene riferimenti ad altri oggetti.            |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)                | facoltativo.                                                             |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md)            | facoltativo.                                                             |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                          | Obbligatorio se l'oggetto non può essere eliminato.                             |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                           | facoltativo.                                                             |
| [\_ \_ offset dati della sezione WPD \_](section-attribute-properties.md)                                           | Obbligatorio.                                                             |
| [\_ \_ lunghezza dei dati della sezione WPD \_](section-attribute-properties.md)                                           | Obbligatorio.                                                             |
| [\_ \_ unità dati della sezione WPD \_](section-attribute-properties.md)                                             | Consigliato.                                                          |
| [\_ \_ \_ risorsa oggetto a cui si fa riferimento dati \_ della sezione WPD \_](section-attribute-properties.md) | Consigliato.                                                          |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



