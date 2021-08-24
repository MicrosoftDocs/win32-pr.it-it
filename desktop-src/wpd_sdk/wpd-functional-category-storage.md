---
description: ARCHIVIAZIONE DELLE CATEGORIE FUNZIONALI WPD \_ \_ \_
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b16d70ebff4c61643b4d5ae0f8b333f5f9a7dc02103a32e14ded7a0ac4d8189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805939"
---
# <a name="wpd_functional_category_storage"></a>ARCHIVIAZIONE DELLE CATEGORIE FUNZIONALI WPD \_ \_ \_

Un oggetto funzionale \_ WPD FUNCTIONAL CATEGORY STORAGE incapsula \_ \_ l'archiviazione fisica dei file nel dispositivo.



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
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](miscellaneous-properties.md)                      | Obbligatorio. Vedere [**WPD \_ CONTENT TYPE FUNCTIONAL \_ OBJECT \_ \_ (OGGETTO FUNZIONALE**](wpd-content-type-functional-object.md) DEL TIPO DI CONTENUTO WPD) per le categorie definite Windows dispositivi portatili. |
| [TIPO DI ARCHIVIAZIONE WPD \_ \_](storage-properties.md)                                                         | Obbligatorio.                                                                                                                                              |
| [TIPO DI \_ \_ FILE SYSTEM DI ARCHIVIAZIONE \_ WPD \_](storage-properties.md)                               | facoltativo.                                                                                                                                              |
| [CAPACITÀ DI ARCHIVIAZIONE WPD \_ \_](storage-properties.md)                                                 | Obbligatorio.                                                                                                                                              |
| [SPAZIO DISPONIBILE DI \_ ARCHIVIAZIONE WPD \_ IN \_ \_ \_ BYTE](storage-properties.md)                        | facoltativo.                                                                                                                                              |
| [SPAZIO DISPONIBILE DI \_ ARCHIVIAZIONE WPD \_ NEGLI \_ \_ \_ OGGETTI](storage-properties.md)                    | facoltativo.                                                                                                                                              |
| [DESCRIZIONE \_ DELL'ARCHIVIAZIONE WPD \_](storage-properties.md)                                           | facoltativo.                                                                                                                                              |
| [NUMERO DI SERIE DI ARCHIVIAZIONE WPD \_ \_ \_](storage-properties.md)                                      | facoltativo.                                                                                                                                              |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                    | Obbligatorio o facoltativo | Descrizione                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**ICONA DELLA RISORSA \_ WPD \_**](wpd-resource-icon.md) | facoltativo.            | Contiene la rappresentazione dell'icona per questa archiviazione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



