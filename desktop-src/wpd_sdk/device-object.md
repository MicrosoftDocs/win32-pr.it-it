---
description: Oggetto dispositivo
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Oggetto dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef76dbe26b1fd2c8d2bfd6da708728c9eb2177b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525909"
---
# <a name="device-object"></a>Oggetto dispositivo

L'oggetto dispositivo supporta le seguenti proprietà. Un'applicazione può richiedere queste proprietà eseguendo una query sull'oggetto radice, specificando l'ID oggetto costante **\_ \_ \_ ID oggetto dispositivo WPD** . Tutti i valori dell'oggetto dispositivo sono di sola lettura.

Se un determinato dispositivo implementa la categoria di [ \_ \_ \_ dispositivi della categoria funzionale WPD](wpd-functional-category-device.md) , deve supportare anche le proprietà associate a tale categoria.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio. Il valore è **WPD \_ \_ \_ ID oggetto dispositivo**.                                                         |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio. Il valore è una stringa vuota.                                                                     |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                                                   |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio.                                                                                                   |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto dispositivo non deve essere visualizzato all'utente.                                              |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto dispositivo contiene riferimenti ad altri oggetti.                                              |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                                                                   |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                                                                   |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                                                                   |
| [\_ \_ partner sincronizzazione dispositivi \_ WPD](device-properties.md)                                           | facoltativo.                                                                                                   |
| [\_versione del \_ firmware del dispositivo WPD \_](device-properties.md)                                   | Obbligatorio.                                                                                                   |
| [\_livello di \_ alimentazione del dispositivo WPD \_](device-properties.md)                                             | Consigliato se il dispositivo ha una batteria.                                                                    |
| [\_ \_ origine alimentazione dispositivo \_ WPD](device-properties.md)                                           | Consigliato.                                                                                                |
| [\_protocollo del dispositivo WPD \_](device-properties.md)                                                    | Consigliato.                                                                                                |
| [\_produttore del dispositivo WPD \_](device-properties.md)                                            | Obbligatorio.                                                                                                   |
| [\_modello di dispositivo WPD \_](device-properties.md)                                                          | Obbligatorio.                                                                                                   |
| [\_numero di \_ serie del dispositivo WPD \_](device-properties.md)                                         | Obbligatorio.                                                                                                   |
| [il \_ dispositivo WPD \_ supporta \_ non \_ utilizzabile](device-properties.md)                    | Obbligatorio se il dispositivo supporta oggetti non utilizzabili; ovvero, se può essere usato per l'archiviazione semplice dei dati. |
| [\_DateTime del dispositivo WPD \_](device-properties.md)                                                    | facoltativo.                                                                                                   |
| [\_ \_ nome descrittivo del dispositivo WPD \_](device-properties.md)                                         | Consigliato.                                                                                                |
| [\_ \_ \_ schema DRM supportato dal dispositivo WPD \_](device-properties.md)                          | Consigliato se il dispositivo supporta la Rights Management digitale (DRM).                                         |
| [\_ \_ \_ \_ sono ordinati i formati supportati per il dispositivo WPD \_](device-properties.md)       | Consigliato se il dispositivo supporta l'ordinamento del formato preferito.                                               |
| [\_tipo di dispositivo WPD \_](device-properties.md)                                                            | Consigliato.                                                                                                |
| [\_ \_ \_ ID univoco funzionale del dispositivo WPD \_](device-properties.md)                          | facoltativo.                                                                                                   |
| [\_ \_ ID univoco del modello di dispositivo WPD \_ \_](device-properties.md)                                    | facoltativo.                                                                                                   |
| [\_trasporto di dispositivi WPD \_](device-properties.md)                                                  | Consigliato.                                                                                                |
| [\_fase di \_ utilizzo \_ del \_ dispositivo WPD](device-properties.md)                                  | facoltativo.                                                                                                   |
| [\_ \_ categoria oggetto funzionale \_ WPD](device-properties.md)                             | Obbligatorio.                                                                                                   |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="commands"></a>Comandi

Oltre alle proprietà, i dispositivi devono supportare un set di comandi specifico definito da dispositivi portatili Windows. I comandi supportati da un oggetto o da un dispositivo dipendono dal tipo, dalle funzionalità e dalle funzionalità.

La tabella seguente descrive le classi di comando che si applicano ai dispositivi, in base alla funzionalità. In genere, un dispositivo rientra in diverse categorie e deve supportare i comandi per tutte le categorie applicabili. Ad esempio, un telefono cellulare con una fotocamera dovrebbe rientrare in tre categorie: tutti i dispositivi, i dispositivi SMS e i dispositivi di acquisizione immagini ancora. Un driver personalizzato e un'applicazione client possono supportare comandi o proprietà aggiuntivi definiti dall'utente, ma devono supportare i comandi seguenti. Per una descrizione dei comandi specifici che rientrano in ogni categoria di comandi, vedere [comandi](commands.md).



| Descrizione                                                                                                                                                                                                                      | Categorie di comandi                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tutti i dispositivi.                                                                                                                                                                                                                     | **categoria \_ WPD \_ categoria \_ CAPABILITIESWPD \_ comuni**<br/> **\_ \_ enumerazione oggetto categoria \_ WPD**<br/> **\_gestione degli \_ oggetti di categoria WPD \_**<br/> **\_proprietà dell' \_ oggetto \_ categoria WPD**<br/> **\_Proprietà oggetto categoria WPD in \_ \_ \_ blocco**<br/> **\_ \_ risorse oggetto categoria \_ WPD**<br/> |
| Dispositivi che possono acquisire immagini ancora, ad esempio fotocamere digitali.                                                                                                                                                                  | **\_acquisizione di \_ \_ Immagini ancora della categoria \_ WPD**                                                                                                                                                                                                                                                                                   |
| Dispositivi che possono inviare messaggi SMS (Short Message Service), ad esempio telefoni cellulari. L'invio di messaggi SMS viene spesso definito "messaggistica testuale".                                                                                      | **\_SMS della categoria WPD \_**                                                                                                                                                                                                                                                                                                     |
| Dispositivi che funzionano come dispositivi di archiviazione. Sono incluse le unità esterne. Se un dispositivo supporta la possibilità di formattare un archivio o di spostare gli oggetti da una posizione a un'altra, il driver deve supportare questa categoria.<br/> | **\_archiviazione categoria \_ WPD**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 




