---
description: INFORMAZIONI SUL \_ RENDERING DELLE \_ CATEGORIE FUNZIONALI \_ WPD \_
ms.assetid: 84ec6f14-fe90-42a5-ba2b-6c4cc406935c
title: WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0665d9918726495d72b318b60a39a4713c01c9ad3a80ab0dbe15be5fc87576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083245"
---
# <a name="wpd_functional_category_rendering_information"></a>INFORMAZIONI SUL \_ RENDERING DELLE \_ CATEGORIE FUNZIONALI \_ WPD \_

Un oggetto funzionale WPD FUNCTIONAL CATEGORY RENDERING INFORMATION descrive il tipo di file multimediali di cui il \_ dispositivo è in grado di eseguire il \_ \_ \_ rendering.



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
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](miscellaneous-properties.md)                      | Obbligatorio. Vedere [**WPD \_ CONTENT TYPE FUNCTIONAL \_ OBJECT \_ \_ (OGGETTO FUNZIONALE**](wpd-content-type-functional-object.md) DEL TIPO DI CONTENUTO WPD) per le categorie Windows dispositivi portatili. |
| [PROFILI DI INFORMAZIONI SUL RENDERING WPD \_ \_ \_](miscellaneous-properties.md)              | Obbligatorio.                                                                                                                                              |
| [TIPO DI VOCE DEL PROFILO \_ \_ DI INFORMAZIONI SUL \_ \_ RENDERING \_ WPD](miscellaneous-properties.md)                                     | facoltativo.                                                                                                                                              |
| [RISORSA CREABILE \_ VOCE DEL PROFILO INFORMAZIONI RENDERING \_ \_ \_ WPD \_ \_](miscellaneous-properties.md)                      | facoltativo.                                                                                                                                              |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



