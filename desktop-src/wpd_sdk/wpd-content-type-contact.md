---
description: '\_ \_ contatto tipo di contenuto WPD \_'
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fed10e0abb36a482141e5c796f5494b00b99f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316354"
---
# <a name="wpd_content_type_contact"></a>\_ \_ contatto tipo di contenuto WPD \_

Un oggetto che descrive il tipo come \_ contatto del tipo di contenuto WPD \_ \_ rappresenta i dati di contatto personali.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                                   | Obbligatorio o facoltativo                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                           | Obbligatorio.                                                                      |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                                      | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                                    | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [\_formato oggetto \_ WPD](object-properties.md)                                                                  | Obbligatorio.                                                                      |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                                     | Obbligatorio.                                                                      |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                              | Obbligatorio se l'oggetto è nascosto.                                              |
| [\_oggetto WPD \_](object-properties.md)                                                              | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).          |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                                      | Obbligatorio se l'oggetto ha almeno una risorsa.                              |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                                        | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                                 | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.          |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                          | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                        |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                              | facoltativo.                                                                      |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                               | facoltativo.                                                                      |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                            | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                         |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                                     | facoltativo.                                                                      |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                                   | Consigliato.                                                                   |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                                   | facoltativo.                                                                      |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                          | Consigliato se un altro oggetto fa riferimento all'oggetto.                     |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)               | facoltativo.                                                                      |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md)           | facoltativo.                                                                      |
| [\_ \_ nome visualizzato contatto \_ WPD](contact-properties.md)                                                  | Obbligatorio.                                                                      |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                               | Obbligatorio se l'oggetto non può essere eliminato.                                      |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                          | facoltativo.                                                                      |
| [\_ \_ nome visualizzato contatto \_ WPD](contact-properties.md)                                                                           | Obbligatorio.                                                                      |
| [\_nome contatto \_ WPD \_](contact-properties.md)                                                      | Consigliato.                                                                   |
| [\_ \_ nomi intermedi contatto \_ WPD](contact-properties.md)                                                  | Consigliato.                                                                   |
| [\_ \_ Cognome contatto \_ WPD](contact-properties.md)                                                        | Consigliato.                                                                   |
| [\_prefisso contatto \_ WPD](contact-properties.md)                                                               | Consigliato.                                                                   |
| [\_ \_ suffisso contatto WPD](contact-properties.md)                                                               | Consigliato.                                                                   |
| [WPD \_ contattare \_ il \_ primo \_ nome fonetico](contact-properties.md)                                   | facoltativo.                                                                      |
| [\_ \_ Cognome fonetico contatto WPD \_ \_](contact-properties.md)                                     | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ \_ Indirizzo postale \_ completo personale](contact-properties.md)                | Consigliato.                                                                   |
| [WPD \_ contattare \_ l' \_ Indirizzo postale personale \_ \_ riga 1](contact-properties.md)              | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ Indirizzo postale personale \_ \_ Riga2](contact-properties.md)              | facoltativo.                                                                      |
| [WPD \_ Contatta \_ la \_ \_ città dell'indirizzo postale personale \_](contact-properties.md)                | facoltativo.                                                                      |
| [\_ \_ \_ \_ area indirizzo postale personale contatto \_ WPD](contact-properties.md)            | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ \_ \_ codice postale per l'indirizzo postale personale \_](contact-properties.md) | facoltativo.                                                                      |
| [WPD \_ Contatta \_ il \_ \_ paese dell'indirizzo postale personale \_](contact-properties.md)          | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ \_ Indirizzo postale \_ completo aziendale](contact-properties.md)                | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ Indirizzo postale aziendale \_ \_ riga 1](contact-properties.md)              | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ Indirizzo postale aziendale \_ \_ Riga2](contact-properties.md)              | facoltativo.                                                                      |
| [WPD \_ Contatta \_ l' \_ Indirizzo postale aziendale \_ \_ città](contact-properties.md)                | facoltativo.                                                                      |
| [WPD \_ Contatta \_ l' \_ \_ area dell'indirizzo postale aziendale \_](contact-properties.md)            | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ Indirizzo postale aziendale \_ \_ Cap \_](contact-properties.md) | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ \_ paese dell'indirizzo postale aziendale \_](contact-properties.md)          | facoltativo.                                                                      |
| [WPD \_ contattare \_ altro \_ \_ Indirizzo postale \_ completo](contact-properties.md)                      | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ altro \_ Indirizzo postale \_ riga 1](contact-properties.md)                    | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ altro \_ Indirizzo postale \_ Riga2](contact-properties.md)                    | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ altro \_ Indirizzo postale \_ città](contact-properties.md)                      | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ altra \_ area dell'indirizzo postale \_](contact-properties.md)                  | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ \_ \_ codice postale di altro indirizzo postale \_](contact-properties.md)       | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ \_ \_ \_ paese postale di un altro indirizzo postale](contact-properties.md) | facoltativo.                                                                      |
| [\_indirizzo di \_ \_ posta elettronica \_ primario contatto WPD](contact-properties.md)                               | Consigliato.                                                                   |
| [WPD \_ contattare \_ la \_ posta elettronica personale](contact-properties.md)                                              | facoltativo.                                                                      |
| [WPD \_ contattare \_ Personal \_ Email2](contact-properties.md)                                            | facoltativo.                                                                      |
| [WPD \_ contattare \_ la \_ posta elettronica aziendale](contact-properties.md)                                              | facoltativo.                                                                      |
| [WPD \_ Contact \_ business \_ Email2](contact-properties.md)                                            | facoltativo.                                                                      |
| [WPD \_ Contatta \_ altri \_ messaggi di posta elettronica](contact-properties.md)                                                  | facoltativo.                                                                      |
| [\_ \_ telefono primario contatto \_ WPD](contact-properties.md)                                                | Consigliato.                                                                   |
| [WPD \_ contattare \_ il \_ telefono personale](contact-properties.md)                                              | facoltativo.                                                                      |
| [WPD \_ contattare \_ Personal \_ PHONE2](contact-properties.md)                                            | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ telefono aziendale](contact-properties.md)                                              | facoltativo.                                                                      |
| [WPD \_ Contact \_ business \_ PHONE2](contact-properties.md)                                            | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ telefono cellulare](contact-properties.md)                                                  | facoltativo.                                                                      |
| [WPD \_ contatto \_ mobile \_ PHONE2](contact-properties.md)                                                | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ fax personale](contact-properties.md)                                                  | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ fax aziendale](contact-properties.md)                                                  | facoltativo.                                                                      |
| [\_cercapersone contatto \_ WPD](contact-properties.md)                                                                 | facoltativo.                                                                      |
| [WPD \_ contattare \_ altri \_ telefoni](contact-properties.md)                                                  | facoltativo.                                                                      |
| [\_ \_ \_ indirizzo Web primario contatto \_ WPD](contact-properties.md)                                   | Consigliato.                                                                   |
| [\_ \_ \_ indirizzo Web personale contatto \_ WPD](contact-properties.md)                                 | facoltativo.                                                                      |
| [WPD \_ contattare \_ l' \_ indirizzo Web aziendale \_](contact-properties.md)                                 | facoltativo.                                                                      |
| [WPD \_ contatto \_ Instant \_ Messenger](contact-properties.md)                                        | Consigliato                                                                    |
| [WPD \_ contatto \_ istantaneo \_ MESSENGER2](contact-properties.md)                                      | facoltativo.                                                                      |
| [WPD \_ contatto \_ istantaneo \_ MESSENGER3](contact-properties.md)                                      | facoltativo.                                                                      |
| [\_ \_ nome società contatto \_ WPD](contact-properties.md)                                                  | facoltativo.                                                                      |
| [\_nome della \_ società fonetica del contatto \_ WPD \_](contact-properties.md)                               | Facoltativo                                                                       |
| [\_ruolo contatto \_ WPD](contact-properties.md)                                                                   | facoltativo.                                                                      |
| [WPD \_ di \_ nascita contatto](contact-properties.md)                                                         | facoltativo.                                                                      |
| [WPD \_ contattare \_ il \_ Fax primario](contact-properties.md)                                                                            | facoltativo.                                                                      |
| [\_partner contatto \_ WPD](contact-properties.md)                                                                                  | facoltativo.                                                                      |
| [WPD \_ contattare gli \_ elementi figlio](contact-properties.md)                                                                                | facoltativo.                                                                      |
| [\_Assistente contatto \_ WPD](contact-properties.md)                                                                               | facoltativo.                                                                      |
| [\_ \_ data anniversario contatto \_ WPD](contact-properties.md)                                                                       | facoltativo.                                                                      |
| [\_ \_ suoneria contatto WPD](contact-properties.md)                                                                                | facoltativo.                                                                      |
| [\_ \_ Note informative comuni di WPD \_](object-properties.md)                                                                        | facoltativo.                                                                      |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                                       | Obbligatorio o facoltativo       | Descrizione                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md)              | facoltativo.                  | Contiene i dati di contatto.         |
| [**\_ \_ Foto contatto risorse \_ WPD**](wpd-resource-contact-photo.md) | Consigliato, se disponibile. | Contiene un'immagine del contatto. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



