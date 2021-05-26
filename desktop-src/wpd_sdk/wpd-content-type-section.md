---
description: SEZIONE TIPO DI \_ CONTENUTO WPD \_ \_
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84294ff9949418ecc12f55472da202dddcc8f06c
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423781"
---
# <a name="wpd_content_type_section"></a>SEZIONE TIPO DI \_ CONTENUTO WPD \_ \_

Un oggetto che descrive il tipo come WPD CONTENT TYPE SECTION rappresenta una sezione di dati contenuta \_ \_ in un altro \_ oggetto. Ad esempio, un file audio di grandi dimensioni può essere descritto come una raccolta di più capitoli e ogni capitolo può essere un oggetto WPD \_ CONTENT \_ TYPE \_ SECTION.

La proprietà WPD \_ OBJECT \_ REFERENCES identifica l'oggetto padre di una determinata sezione.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà       | Obbligatorio o facoltativo             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                           | Obbligatorio.                                                             |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                            | Obbligatorio.                                                             |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                                       | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                                     | Obbligatorio.                                                             |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                                   | Obbligatorio.                                                             |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                      | Obbligatorio.                                                             |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                               | Obbligatorio se l'oggetto è nascosto.                                     |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                               | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [DIMENSIONI \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                                       | Obbligatorio se l'oggetto ha almeno una risorsa.                     |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Obbligatorio se l'oggetto rappresenta un file.                             |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                                  | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo. |
| [RIFERIMENTI A OGGETTI WPD \_ \_](object-properties.md)                                                           | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                               | facoltativo.                                                             |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                                | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                             | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                      | facoltativo.                                                             |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                    | Consigliato.                                                          |
| [DATA DI \_ CREAZIONE \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | facoltativo.                                                             |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                | Consigliato se l'oggetto contiene riferimenti ad altri oggetti.            |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)                | facoltativo.                                                             |
| [OGGETTO WPD \_ \_ CHE GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md)            | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                          | Obbligatorio se l'oggetto non può essere eliminato.                             |
| [IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                           | facoltativo.                                                             |
| [OFFSET DEI DATI DELLA SEZIONE WPD \_ \_ \_](section-attribute-properties.md)                                           | Obbligatorio.                                                             |
| [LUNGHEZZA DEI DATI DELLA SEZIONE WPD \_ \_ \_](section-attribute-properties.md)                                           | Obbligatorio.                                                             |
| [UNITÀ DATI DELLA SEZIONE WPD \_ \_ \_](section-attribute-properties.md)                                             | Consigliato.                                                          |
| [RISORSA OGGETTO DI RIFERIMENTO \_ DEI \_ DATI DELLA \_ \_ SEZIONE \_ WPD](section-attribute-properties.md) | Consigliato.                                                          |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



