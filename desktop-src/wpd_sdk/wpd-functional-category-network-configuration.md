---
description: CONFIGURAZIONE DI RETE \_ DELLE \_ CATEGORIE FUNZIONALI \_ \_ WPD
ms.assetid: c5c93ebf-0072-49c2-a109-a2edb7e1bd8d
title: WPD_FUNCTIONAL_CATEGORY_NETWORK_CONFIGURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c87647e206ed8dfd95a2eb4ee6f8833724a1a8a645beefc67be9254030570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193059"
---
# <a name="wpd_functional_category_network_configuration"></a>CONFIGURAZIONE DI RETE \_ DELLE \_ CATEGORIE FUNZIONALI \_ \_ WPD

Un oggetto funzionale WPD FUNCTIONAL CATEGORY NETWORK CONFIGURATION incapsula la funzionalità di configurazione di rete per il dispositivo, ad esempio \_ \_ profili \_ \_ Wi-Fi o partnership.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                                                         |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio.                                                                                                                                              |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio.                                                                                                                                              |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                                                         |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                                                                                              |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                                                                                              |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                                                      |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                                                                  |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                                                                                      |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                                                              |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                                                                                  |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                                                                                |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                                                                                              |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                                                                                              |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                                                                 |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                                                                                              |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                                                                                           |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                         | facoltativo.                                                                                                                                              |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                                                                                             |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                                                                                              |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                                                                                              |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                                                                                              |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                | facoltativo.                                                                                                                                              |
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](miscellaneous-properties.md)                      | Obbligatorio. Vedere [**WPD \_ CONTENT TYPE FUNCTIONAL \_ OBJECT \_ \_ (OGGETTO**](wpd-content-type-functional-object.md) FUNZIONALE DEL TIPO DI CONTENUTO WPD) per le categorie definite Windows dispositivi portatili. |
| [TIPI DI CONTENUTO DELLA CARTELLA WPD \_ \_ \_ \_ CONSENTITI](miscellaneous-properties.md)                 | Consigliato.                                                                                                                                           |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



