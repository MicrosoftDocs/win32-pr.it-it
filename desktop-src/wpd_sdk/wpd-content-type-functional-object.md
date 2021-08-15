---
description: OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58121d351219c246117106d578ed3672ebf25eecf9e159f957494b5c5eae9280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193525"
---
# <a name="wpd_content_type_functional_object"></a>OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_

Un oggetto che descrive il tipo come WPD CONTENT FUNCTIONAL OBJECT rappresenta un oggetto \_ \_ funzionale, incapsulando la funzionalità del \_ dispositivo.

Tutti gli oggetti funzionali, indipendentemente dal tipo, supportano le proprietà seguenti. Se si definisce un oggetto funzionale personalizzato, deve supportare anche queste proprietà.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.        |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio.                                                                             |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio.                                                                             |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.        |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                             |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                             |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                     |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                 |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                     |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                             |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                 |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                               |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                             |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                             |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                             |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                          |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                         | facoltativo.                                                                             |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                            |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                             |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                             |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                             |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                | facoltativo.                                                                             |
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](miscellaneous-properties.md)                      | Obbligatorio. Vedere la tabella seguente per le categorie definite da Windows dispositivi portatili. |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="functional-object-categories"></a>Categorie di oggetti funzionali

Gli oggetti funzionali possono essere raggruppati in categorie, a seconda delle relative funzioni. Una categoria è descritta dalla proprietà CATEGORY dell'oggetto FUNZIONALE WPD \_ \_ \_ (un valore GUID). La categoria determina quali proprietà aggiuntive sono supportate.

Nella tabella seguente vengono descritte le categorie definite Windows dispositivi portatili. Vedere la descrizione della categoria per informazioni sulle proprietà e le risorse aggiuntive supportate dall'oggetto.



| Categoria funzionale                                                                                        | Descrizione                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CATEGORIA FUNZIONALE WPD \_ \_ \_ ALL**](wpd-functional-category-all.md)                                      | Questa categoria funzionale è valida solo come parametro per determinate funzioni di query (per indicare che tutti i tipi di oggetto funzionali sono accettabili) e non è una categoria funzionale segnalata dal driver. |
| [**ACQUISIZIONE AUDIO CATEGORIA FUNZIONALE WPD \_ \_ \_ \_**](wpd-functional-category-audio-capture.md)                 | L'oggetto incapsula la funzionalità di acquisizione audio nel dispositivo, ad esempio un registratore vocale o un altro componente di registrazione audio.                                                                      |
| [**DISPOSITIVO CATEGORIA \_ FUNZIONALE WPD \_ \_**](wpd-functional-category-device.md)                                | L'oggetto incapsula il dispositivo, ovvero l'oggetto in primo piano del dispositivo.                                                                                                                          |
| [**CONFIGURAZIONE DI RETE \_ DELLE \_ CATEGORIE FUNZIONALI \_ \_ WPD**](wpd-functional-category-network-configuration.md) | L'oggetto incapsula la funzionalità di configurazione di rete per il dispositivo, ad esempio profili Wi-Fi o partnership.                                                                                   |
| [**INFORMAZIONI SUL \_ RENDERING DELLE \_ CATEGORIE FUNZIONALI \_ WPD \_**](wpd-functional-category-rendering-information.md) | L'oggetto descrive i tipi di file multimediali che il dispositivo è in grado di riprodurre.                                                                                                                            |
| [**SMS DELLA CATEGORIA \_ FUNZIONALE \_ WPD \_**](wpd-functional-category-sms.md)                                      | L'oggetto incapsula la funzionalità del servizio messaggi brevi (comunemente denominata "messaggistica di testo") nel dispositivo.                                                                                             |
| [**CATEGORIA FUNZIONALE WPD \_ \_ ACQUISIZIONE DI \_ \_ IMMAGINI \_**](wpd-functional-category-still-image-capture.md)    | L'oggetto incapsula la funzionalità di acquisizione di immagini ancora in un dispositivo, ad esempio una fotocamera o un allegato della fotocamera.                                                                                              |
| [**ARCHIVIAZIONE DELLE CATEGORIE FUNZIONALI WPD \_ \_ \_**](wpd-functional-category-storage.md)                              | L'oggetto incapsula l'archiviazione fisica dei file nel dispositivo.                                                                                                                                              |
| [**ACQUISIZIONE VIDEO DELLA CATEGORIA FUNZIONALE WPD \_ \_ \_ \_**](wpd-functional-category-video-capture.md)                 | L'oggetto incapsula la funzionalità di acquisizione video nel dispositivo, ad esempio un componente di registrazione video. Un'applicazione usa questo oggetto per ottenere il controllo a livello di codice.                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



