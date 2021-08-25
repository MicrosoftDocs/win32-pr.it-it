---
description: CALENDARIO DEL TIPO \_ DI CONTENUTO WPD \_ \_
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819955c0554269deb26c6b6f7f7f3c74ee8715e2dca804b5d3d554b9657be524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927871"
---
# <a name="wpd_content_type_calendar"></a>CALENDARIO DEL TIPO \_ DI CONTENUTO WPD \_ \_

Un oggetto che ne descrive il tipo come WPD \_ CONTENT TYPE CALENDAR rappresenta un \_ \_ calendario. L'oggetto può essere un file che contiene informazioni sul calendario o una cartella che contiene altri oggetti correlati al calendario, ad esempio attività, appuntamenti e così via.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                  |
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
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo. |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                             |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                             |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                          |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                         | facoltativo.                                                             |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                     | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.            |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ GENERA \_ \_ L'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                               | Obbligatorio se l'oggetto può essere eliminato.                                |
| [IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                | facoltativo.                                                             |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo                             | Descrizione        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [**IMPOSTAZIONE PREDEFINITA DELLA RISORSA WPD \_ \_**](wpd-resource-default.md) | Obbligatorio se l'oggetto è supportato da dati binari. | Contiene i dati. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



