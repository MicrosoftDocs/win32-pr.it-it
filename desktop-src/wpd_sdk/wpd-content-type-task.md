---
description: ATTIVITÀ TIPO DI CONTENUTO WPD \_ \_ \_
ms.assetid: 503d0b11-2113-4df4-8b6b-250f24d09b1f
title: WPD_CONTENT_TYPE_TASK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d42761fa8cbd96b4ce5b4085544906d2333b9d1317181b397140468145a4b37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193535"
---
# <a name="wpd_content_type_task"></a>ATTIVITÀ TIPO DI CONTENUTO WPD \_ \_ \_

Un oggetto che descrive il tipo come ATTIVITÀ TIPO DI CONTENUTO WPD rappresenta un'attività, ad esempio un \_ elemento in un elenco \_ \_ attività.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà       | Obbligatorio o facoltativo         |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio.                                                                      |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                      |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                      |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                              |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).          |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                              |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.          |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                        |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                      |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                      |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                         |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                      |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                   |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                         | facoltativo.                                                                      |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                     |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                      |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                      |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                      |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                | facoltativo.                                                                      |
| [SOGGETTO DELLE INFORMAZIONI COMUNI WPD \_ \_ \_](object-properties.md)                                                            | Obbligatorio.                                                                      |
| [TESTO DEL CORPO \_ DELLE \_ INFORMAZIONI COMUNI \_ \_ WPD](object-properties.md)                                                         | Consigliato.                                                                   |
| [PRIORITÀ DELLE INFORMAZIONI \_ COMUNI WPD \_ \_](object-properties.md)                                                           | Consigliato.                                                                   |
| [DATETIME DI \_ INIZIO \_ DELLE INFORMAZIONI \_ COMUNI \_ WPD](object-properties.md)                                                    | Consigliato.                                                                   |
| [DATETIME DI \_ FINE \_ DELLE INFORMAZIONI \_ COMUNI \_ WPD](object-properties.md)                                                      | Consigliato.                                                                   |
| [NOTE SULLE INFORMAZIONI \_ COMUNI WPD \_ \_](object-properties.md)                                                              | facoltativo.                                                                      |
| [STATO ATTIVITÀ \_ WPD \_](task-properties.md)                                                              | facoltativo.                                                                      |
| [PERCENTUALE DI COMPLETAMENTO ATTIVITÀ WPD \_ \_ \_](task-properties.md)                                         | facoltativo.                                                                      |
| [DATA PROMEMORIA ATTIVITÀ WPD \_ \_ \_](task-properties.md)                                               | facoltativo.                                                                      |
| [PROPRIETARIO ATTIVITÀ \_ WPD \_](task-properties.md)                                                                | facoltativo.                                                                      |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



