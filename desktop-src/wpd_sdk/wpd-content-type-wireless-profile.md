---
description: PROFILO WIRELESS \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999c8aec77c6ff046690e4c3450c0643d685e1db
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423701"
---
# <a name="wpd_content_type_wireless_profile"></a>PROFILO WIRELESS \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_

Un oggetto che ne descrive il tipo come WPD CONTENT TYPE WIRELESS PROFILE rappresenta le \_ informazioni usate per accedere a una rete \_ \_ \_ wireless.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà             | Obbligatorio o facoltativo                      |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio.                                                             |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                             |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                          | Obbligatorio.                                                             |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                                                        | Obbligatorio.                                                             |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                             |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                     |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto dispone di almeno una risorsa.                     |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                             |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo. |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                             |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                             |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                          |
| [DATA DI \_ CREAZIONE \_ DELL'OGGETTO \_ WPD](object-properties.md)                                         | facoltativo.                                                             |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.            |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                             |
| [OGGETTO WPD \_ \_ CHE GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                               | Obbligatorio se l'oggetto non può essere eliminato.                             |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                | facoltativo.                                                             |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo                                  | Descrizione               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [**IMPOSTAZIONE PREDEFINITA \_ DELLA RISORSA WPD \_**](wpd-resource-default.md) | Obbligatorio se l'oggetto è rappresentato da dati binari. | Contiene i dati binari. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



