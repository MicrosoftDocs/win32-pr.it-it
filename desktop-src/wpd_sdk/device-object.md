---
description: Oggetto Device
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Oggetto Device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5279f63c7dabd8bd5b523d9234e33a60d9cf05608ac7b3f1b7601fd8c25024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083615"
---
# <a name="device-object"></a>Oggetto Device

L'oggetto dispositivo supporta le proprietà seguenti. Un'applicazione può richiedere queste proprietà tramite una query sull'oggetto radice (specificando l'ID oggetto **costante \_ WPD DEVICE OBJECT \_ \_ ID** definito). Tutti i valori dell'oggetto dispositivo sono di sola lettura.

Se un determinato dispositivo implementa la [categoria WPD \_ FUNCTIONAL CATEGORY \_ \_ DEVICE,](wpd-functional-category-device.md) deve supportare anche le proprietà associate a tale categoria.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio. Il valore è **WPD \_ DEVICE \_ OBJECT \_ ID**.                                                         |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio. Il valore è una stringa vuota.                                                                     |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                                                   |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio.                                                                                                   |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto dispositivo non deve essere visualizzato all'utente.                                              |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto dispositivo contiene riferimenti ad altri oggetti.                                              |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                                                   |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                                                   |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                                                   |
| [PARTNER DI SINCRONIZZAZIONE \_ \_ DEI DISPOSITIVI WPD \_](device-properties.md)                                           | facoltativo.                                                                                                   |
| [VERSIONE \_ DEL FIRMWARE DEL \_ DISPOSITIVO WPD \_](device-properties.md)                                   | Obbligatorio.                                                                                                   |
| [LIVELLO DI ALIMENTAZIONE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                             | Consigliato se il dispositivo ha una batteria.                                                                    |
| [FONTE DI ALIMENTAZIONE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                           | Consigliato.                                                                                                |
| [PROTOCOLLO DEL DISPOSITIVO WPD \_ \_](device-properties.md)                                                    | Consigliato.                                                                                                |
| [PRODUTTORE DEL \_ DISPOSITIVO WPD \_](device-properties.md)                                            | Obbligatorio.                                                                                                   |
| [MODELLO DI DISPOSITIVO WPD \_ \_](device-properties.md)                                                          | Obbligatorio.                                                                                                   |
| [NUMERO DI SERIE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                         | Obbligatorio.                                                                                                   |
| [IL DISPOSITIVO WPD \_ \_ SUPPORTA NON \_ \_ UTILIZZABILE](device-properties.md)                    | Obbligatorio se il dispositivo supporta oggetti non utilizzabili. ad esempio se può essere usato per l'archiviazione dati semplice. |
| [DATETIME DEL DISPOSITIVO WPD \_ \_](device-properties.md)                                                    | facoltativo.                                                                                                   |
| [NOME \_ DESCRITTIVO DEL \_ DISPOSITIVO WPD \_](device-properties.md)                                         | Consigliato.                                                                                                |
| [SCHEMA \_ DRM SUPPORTATO \_ DAL DISPOSITIVO \_ WPD \_](device-properties.md)                          | Consigliato se il dispositivo supporta DRM (Digital Rights Management).                                         |
| [I FORMATI SUPPORTATI PER I DISPOSITIVI WPD \_ \_ SONO \_ \_ \_ ORDINATI](device-properties.md)       | Consigliato se il dispositivo supporta l'ordinamento del formato preferito.                                               |
| [TIPO DI DISPOSITIVO WPD \_ \_](device-properties.md)                                                            | Consigliato.                                                                                                |
| [\_ID UNIVOCO FUNZIONALE \_ DEL \_ DISPOSITIVO \_ WPD](device-properties.md)                          | facoltativo.                                                                                                   |
| [\_ID UNIVOCO DEL MODELLO \_ DI \_ DISPOSITIVO \_ WPD](device-properties.md)                                    | facoltativo.                                                                                                   |
| [TRASPORTO DI DISPOSITIVI WPD \_ \_](device-properties.md)                                                  | Consigliato.                                                                                                |
| [FASE DI USO DEL DISPOSITIVO WPD \_ \_ \_ \_](device-properties.md)                                  | facoltativo.                                                                                                   |
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](device-properties.md)                             | Obbligatorio.                                                                                                   |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="commands"></a>Comandi

Oltre alle proprietà, i dispositivi devono supportare un set specifico di comandi definiti da Windows dispositivi portatili. I comandi supportati da un oggetto o un dispositivo dipendono dal tipo, dalla funzionalità e dalle funzionalità.

Nella tabella seguente vengono descritte le classi di comando che si applicano ai dispositivi, per funzionalità. In genere, un dispositivo rientra in diverse categorie e deve supportare i comandi per tutte le categorie applicabili. Ad esempio, un telefono cellulare con una fotocamera rientra in tre categorie: tutti i dispositivi, i dispositivi SMS e i dispositivi di acquisizione di immagini. Un driver personalizzato e un'applicazione client possono supportare comandi o proprietà aggiuntivi definiti dall'utente, ma devono supportare i comandi seguenti. Per una descrizione dei comandi specifici che rientrano in ogni categoria di comandi, vedere [Comandi](commands.md).



| Descrizione                                                                                                                                                                                                                      | Categorie di comandi                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tutti i dispositivi.                                                                                                                                                                                                                     | **FUNZIONALITÀ DELLE \_ CATEGORIE WPD COMUNI DELLA CATEGORIA \_ \_ \_ WPD**<br/> **ENUMERAZIONE DEGLI OGGETTI CATEGORIA WPD \_ \_ \_**<br/> **GESTIONE DEGLI OGGETTI DELLA CATEGORIA WPD \_ \_ \_**<br/> **PROPRIETÀ DELL'OGGETTO CATEGORIA WPD \_ \_ \_**<br/> **PROPRIETÀ DELL'OGGETTO CATEGORIA WPD \_ \_ IN \_ \_ BLOCCO**<br/> **RISORSE DELL'OGGETTO CATEGORIA WPD \_ \_ \_**<br/> |
| Dispositivi in grado di acquisire immagini fisse, ad esempio fotocamere digitali.                                                                                                                                                                  | **ACQUISIZIONE DI IMMAGINI \_ ANCORA \_ NELLA \_ CATEGORIA \_ WPD**                                                                                                                                                                                                                                                                                   |
| Dispositivi che possono inviare messaggi SMS (Short Message Service), ad esempio telefoni cellulari. L'invio di messaggi SMS viene spesso definito "SMS".                                                                                      | **SMS DI CATEGORIA \_ WPD \_**                                                                                                                                                                                                                                                                                                     |
| Dispositivi che funzionano come dispositivi di archiviazione. Sono incluse le unità esterne. Se un dispositivo supporta la possibilità di formattare un archivio o di spostare oggetti da una posizione a un'altra, il driver deve supportare questa categoria.<br/> | **ARCHIVIAZIONE DI CATEGORIE \_ WPD \_**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 




