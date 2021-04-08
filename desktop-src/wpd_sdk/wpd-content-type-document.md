---
description: '\_documento del \_ tipo di contenuto WPD \_'
ms.assetid: c3859590-7674-4315-b171-3747e5d9350b
title: WPD_CONTENT_TYPE_DOCUMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8a0a902fb30eb0343a3846eaf3668a4a005a82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058080"
---
# <a name="wpd_content_type_document"></a>\_documento del \_ tipo di contenuto WPD \_

Un oggetto che descrive il tipo come \_ documento del tipo di contenuto WPD \_ \_ rappresenta un documento. Gli esempi includono Microsoft Office file di Word, Microsoft Office file di Excel, file di testo normale e altri formati di documento proprietari.

Questo tipo di oggetto può ospitare le seguenti proprietà.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                      |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                      |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                      |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                              |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).          |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                              |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.          |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                        |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                      |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                      |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                         |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                      |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                   |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                      |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                     |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                      |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                      |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                      |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | facoltativo.                                                                      |
| [\_URL dell' \_ origine \_ multimediale WPD](object-properties.md)                                                                      | facoltativo.                                                                      |
| [\_ \_ URL destinazione supporto \_ WPD](object-properties.md)                                                                 | facoltativo.                                                                      |
| [\_Descrizione supporto \_ WPD](object-properties.md)                                                                      | facoltativo.                                                                      |
| [\_genere multimediale \_ WPD](object-properties.md)                                                                            | facoltativo.                                                                      |
| [\_ \_ segnalibro WPD Media byte \_](object-properties.md)                                                                   | facoltativo.                                                                      |
| [\_GUID del supporto WPD \_](object-properties.md)                                                                             | facoltativo.                                                                      |
| [\_ \_ Descrizione secondaria supporti \_ WPD](object-properties.md)                                                                 | facoltativo.                                                                      |
| [\_informazioni comuni di WPD \_](object-properties.md)                                                                     | Consigliato.                                                                   |
| [\_testo del \_ corpo delle informazioni comuni \_ WPD \_](object-properties.md)                                                         | Consigliato.                                                                   |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo | Descrizione                     |
|--------------------------------------------------------|----------------------|---------------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md) | Necessario             | Contiene il documento fisico. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



