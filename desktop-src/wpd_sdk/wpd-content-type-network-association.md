---
description: ASSOCIAZIONE DI RETE \_ DEL TIPO \_ DI \_ CONTENUTO \_ WPD
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c92f76080db4167a12578c58e9d85c9506c28b
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423720"
---
# <a name="wpd_content_type_network_association"></a>ASSOCIAZIONE DI RETE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_

Un oggetto che descrive il tipo come ASSOCIAZIONE DI RETE DEL TIPO DI CONTENUTO WPD \_ \_ rappresenta \_ un'associazione tra un host e un \_ dispositivo.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà         | Obbligatorio o facoltativo        |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                                       | Obbligatorio.                                                             |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                                        | Obbligatorio.                                                             |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                                                   | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio.                                                             |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                                               | Obbligatorio.                                                             |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                                  | Obbligatorio.                                                             |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                                           | Obbligatorio se l'oggetto è nascosto.                                     |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                           | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [DIMENSIONI \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                                                   | Obbligatorio se l'oggetto ha almeno una risorsa.                     |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | Obbligatorio se l'oggetto rappresenta un file.                             |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                                              | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo. |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                                       | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                                           | facoltativo.                                                             |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                                            | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                                         | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                                  | facoltativo.                                                             |
| [DATA DI \_ MODIFICA DELL'OGGETTO WPD \_ \_](object-properties.md)                                                                | Consigliato.                                                          |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                                                | facoltativo.                                                             |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                                                                       | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.            |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)                            | facoltativo.                                                             |
| [GENERAZIONE \_ DELL'ANTEPRIMA \_ \_ DELL'OGGETTO \_ WPD DALLA \_ RISORSA](object-properties.md)                        | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                      | Obbligatorio se l'oggetto non può essere eliminato.                             |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCAL](object-properties.md)                                                                                        | facoltativo.                                                             |
| [IDENTIFICATORI DI RETE HOST ASSOCIAZIONE DI RETE WPD \_ \_ \_ \_ \_](network-association-properties.md) | Obbligatorio.                                                             |
| [ASSOCIAZIONE DI RETE WPD \_ \_ \_ X509V3SEQUENCE](network-association-properties.md)                       | facoltativo.                                                             |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



