---
description: PLAYLIST DEL TIPO DI CONTENUTO WPD \_ \_ \_
ms.assetid: 4223970d-8c37-4326-a2df-bec558f8ac5e
title: WPD_CONTENT_TYPE_PLAYLIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de97169b4858b48b9bf8e8a0dc7fc365961cc519
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423761"
---
# <a name="wpd_content_type_playlist"></a>PLAYLIST DEL TIPO DI CONTENUTO WPD \_ \_ \_

Un oggetto che descrive il tipo come PLAYLIST TIPO DI CONTENUTO WPD \_ \_ rappresenta una \_ playlist. Una playlist può essere rappresentata da un file fisico oppure può essere costituita da riferimenti archiviati come metadati.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà           | Obbligatorio o facoltativo                 |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà anche in fase di creazione.                                                                  |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                                                                                                      |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                                                                                      |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                                                 |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                                                                                      |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                                                                                      |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                                              |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                                                          |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                                                                              |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                                                      |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                                                                          |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti. ad esempio se i riferimenti vengono archiviati come metadati anziché come dati fisici in un file. |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                                                                                      |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                                                                                      |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                                                         |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                                                                                      |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                                                                                   |
| [DATA DI \_ CREAZIONE \_ DELL'OGGETTO \_ WPD](object-properties.md)                                         | facoltativo.                                                                                                                                      |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.                                                                                     |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                                                                                      |
| [GENERAZIONE \_ DELL'ANTEPRIMA \_ \_ DELL'OGGETTO \_ WPD DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                                                                                      |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                                                                                      |
| [IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                | facoltativo.                                                                                                                                      |
| [SEGNALIBRO DELL'OGGETTO \_ \_ MULTIMEDIALE WPD \_](object-properties.md)                                                                 | Consigliato.                                                                                                                                   |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo | Descrizione                                                                                                                  |
|--------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IMPOSTAZIONE PREDEFINITA \_ DELLA RISORSA WPD \_**](wpd-resource-default.md) | facoltativo.            | Se la playlist è un file fisico, ad esempio un file XML che elenca i file multimediali da riprodurre, si tratta dei byte effettivi del file. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



