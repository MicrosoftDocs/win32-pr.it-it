---
description: '\_ \_ oggetto funzionale del tipo di contenuto WPD \_ \_'
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8516d29bf08b4873dc80c72b9a23de19dc50d0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316347"
---
# <a name="wpd_content_type_functional_object"></a>\_ \_ oggetto funzionale del tipo di contenuto WPD \_ \_

Un oggetto che descrive il tipo come \_ oggetto funzionale del contenuto WPD \_ \_ rappresenta un oggetto funzionale, incapsulando la funzionalità del dispositivo.

Tutti gli oggetti funzionali, a prescindere dal tipo, supportano le proprietà seguenti. (Se si definisce un oggetto funzionale personalizzato, è necessario che supporti anche queste proprietà).



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.        |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                                             |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio.                                                                             |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.        |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                                             |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                                             |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                     |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                 |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                     |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                             |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                 |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                               |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                             |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                             |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                                             |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                                          |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                                             |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                            |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                                             |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                             |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                             |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | facoltativo.                                                                             |
| [\_ \_ categoria oggetto funzionale \_ WPD](miscellaneous-properties.md)                      | Obbligatorio. Vedere la tabella seguente per le categorie definite da dispositivi portatili Windows. |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="functional-object-categories"></a>Categorie di oggetti funzionali

Gli oggetti funzionali possono essere raggruppati in categorie, a seconda delle rispettive funzioni. Una categoria viene descritta dalla proprietà di \_ categoria dell'oggetto funzionale WPD \_ \_ (un valore GUID). La categoria determina quali proprietà aggiuntive sono supportate.

Nella tabella seguente vengono descritte le categorie definite dai dispositivi portatili Windows. Per informazioni sulle proprietà e sulle risorse aggiuntive supportate dall'oggetto, vedere la descrizione della categoria.



| Categoria funzionale                                                                                        | Descrizione                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_categoria funzionale \_ WPD \_ All**](wpd-functional-category-all.md)                                      | Questa categoria funzionale è valida solo come parametro per determinate funzioni di query (per indicare che tutti i tipi di oggetto funzionali sono accettabili) e non è una categoria funzionale indicata dal driver. |
| [**\_ \_ acquisizione audio della categoria funzionale \_ WPD \_**](wpd-functional-category-audio-capture.md)                 | L'oggetto incapsula la funzionalità di acquisizione audio sul dispositivo, ad esempio, un registratore vocale o un altro componente di registrazione audio.                                                                      |
| [**\_ \_ dispositivo categoria funzionale \_ WPD**](wpd-functional-category-device.md)                                | L'oggetto incapsula il dispositivo, ovvero l'oggetto di primo livello del dispositivo.                                                                                                                          |
| [**\_configurazione di \_ rete della categoria funzionale \_ WPD \_**](wpd-functional-category-network-configuration.md) | L'oggetto incapsula la funzionalità di configurazione di rete per il dispositivo, ad esempio i profili Wi-Fi o le relazioni.                                                                                   |
| [**\_ \_ \_ informazioni sul rendering della categoria funzionale WPD \_**](wpd-functional-category-rendering-information.md) | L'oggetto descrive i tipi di file multimediali che il dispositivo è in grado di riprodurre.                                                                                                                            |
| [**\_SMS della \_ categoria \_ funzionale WPD**](wpd-functional-category-sms.md)                                      | L'oggetto incapsula la funzionalità di breve messaggio del servizio, denominata comunemente "messaggistica testuale", sul dispositivo.                                                                                             |
| [**\_ \_ \_ \_ acquisizione immagini ancora della categoria funzionale WPD \_**](wpd-functional-category-still-image-capture.md)    | L'oggetto incapsula ancora la funzionalità di acquisizione delle immagini in un dispositivo, ad esempio un allegato della fotocamera o della fotocamera.                                                                                              |
| [**\_ \_ archiviazione categoria funzionale \_ WPD**](wpd-functional-category-storage.md)                              | L'oggetto incapsula l'archiviazione fisica dei file nel dispositivo.                                                                                                                                              |
| [**\_ \_ acquisizione video della categoria funzionale \_ WPD \_**](wpd-functional-category-video-capture.md)                 | L'oggetto incapsula la funzionalità di acquisizione video nel dispositivo, ad esempio un componente registratore video. Un'applicazione utilizza questo oggetto per ottenere il controllo a livello di codice.                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



