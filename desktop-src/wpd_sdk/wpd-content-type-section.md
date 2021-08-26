---
description: SEZIONE TIPO DI \_ CONTENUTO WPD \_ \_
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be521313b2401166e4af1be06bf0e5bbe611de3a247a202177d7564f0c759bc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927701"
---
# <a name="wpd_content_type_section"></a>SEZIONE TIPO DI \_ CONTENUTO WPD \_ \_

Un oggetto che descrive il tipo come WPD CONTENT TYPE SECTION rappresenta una sezione di dati contenuta \_ \_ in un altro \_ oggetto. Ad esempio, un file audio di grandi dimensioni può essere descritto come una raccolta di più capitoli e ogni capitolo potrebbe essere un oggetto WPD \_ CONTENT \_ TYPE \_ SECTION.

La proprietà WPD \_ OBJECT \_ REFERENCES identifica l'oggetto padre di una determinata sezione.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà       | Obbligatorio o facoltativo             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                           | Obbligatorio.                                                             |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                            | Obbligatorio.                                                             |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                                       | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                     | Obbligatorio.                                                             |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                   | Obbligatorio.                                                             |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                      | Obbligatorio.                                                             |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                               | Obbligatorio se l'oggetto è nascosto.                                     |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                               | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                       | Obbligatorio se l'oggetto dispone di almeno una risorsa.                     |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                                         | Obbligatorio se l'oggetto rappresenta un file.                             |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                                  | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo. |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                           | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                               | facoltativo.                                                             |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                                | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                             | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                      | facoltativo.                                                             |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                    | Consigliato.                                                          |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                                    | facoltativo.                                                             |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                                | Consigliato se l'oggetto contiene riferimenti ad altri oggetti.            |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)                | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ GENERA \_ \_ L'ANTEPRIMA DALLA \_ RISORSA](object-properties.md)            | facoltativo.                                                             |
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

 

 



