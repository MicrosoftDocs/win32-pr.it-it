---
description: ASSOCIAZIONE DI RETE \_ DEL TIPO \_ DI \_ CONTENUTO \_ WPD
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c383ac251d410e03fc5d26dd969d4161ae555ebf2cdd3802ca7228b1739ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842291"
---
# <a name="wpd_content_type_network_association"></a>ASSOCIAZIONE DI RETE \_ DEL TIPO \_ DI \_ CONTENUTO \_ WPD

Un oggetto che descrive il tipo come ASSOCIAZIONE DI RETE DEL TIPO DI CONTENUTO WPD \_ \_ rappresenta \_ un'associazione tra un host e un \_ dispositivo.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà         | Obbligatorio o facoltativo        |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                                       | Obbligatorio.                                                             |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                                        | Obbligatorio.                                                             |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                                                   | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio.                                                             |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                                               | Obbligatorio.                                                             |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                                  | Obbligatorio.                                                             |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                                           | Obbligatorio se l'oggetto è nascosto.                                     |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                           | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                                                   | Obbligatorio se l'oggetto ha almeno una risorsa.                     |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                                                     | Obbligatorio se l'oggetto rappresenta un file.                             |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                                              | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo. |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                                       | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                                           | facoltativo.                                                             |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                                            | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                                         | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                                  | facoltativo.                                                             |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                                | Consigliato.                                                          |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                                | facoltativo.                                                             |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                                       | Consigliato se un altro oggetto fa riferimento all'oggetto.            |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)                            | facoltativo.                                                             |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md)                        | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                      | Obbligatorio se l'oggetto non può essere eliminato.                             |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCAL](object-properties.md)                                                                                        | facoltativo.                                                             |
| [IDENTIFICATORI DI RETE \_ HOST DI ASSOCIAZIONE DI \_ \_ \_ \_ RETE WPD](network-association-properties.md) | Obbligatorio.                                                             |
| [ASSOCIAZIONE DI RETE WPD \_ \_ \_ X509V3SEQUENCE](network-association-properties.md)                       | facoltativo.                                                             |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



