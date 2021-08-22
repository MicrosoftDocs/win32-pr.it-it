---
description: ALBUM VIDEO \_ DEL TIPO DI \_ \_ CONTENUTO \_ WPD
ms.assetid: 0445a7de-1a2d-4369-b1f6-588fd6f2c999
title: WPD_CONTENT_TYPE_VIDEO_ALBUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727fc64639c52833142eb70b681c2e4f05bbb555f08b069011238deb0df0e3c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026759"
---
# <a name="wpd_content_type_video_album"></a>ALBUM VIDEO \_ DEL TIPO DI \_ \_ CONTENUTO \_ WPD

Un oggetto che descrive il tipo come WPD \_ CONTENT TYPE VIDEO ALBUM rappresenta una raccolta di file \_ \_ \_ video. Un album video è funzionalmente equivalente a una playlist di file video, ma viene usato per rappresentare un oggetto fisico per l'utente finale.

Questo tipo di oggetto supporta le proprietà seguenti.



|  Nome della proprietà                             | Obbligatorio o facoltativo              |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                                      |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                      |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                      |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                              |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).          |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto dispone di almeno una risorsa.                              |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo.          |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                        |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                      |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                      |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                         |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                      |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                   |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                         | facoltativo.                                                                      |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                                                | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.                     |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                      |
| [L'OGGETTO WPD \_ \_ GENERA \_ \_ L'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                      |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                      |
| [IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                | facoltativo.                                                                      |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



