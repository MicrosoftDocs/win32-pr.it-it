---
description: PROGRAMMA DI TIPO \_ DI CONTENUTO WPD \_ \_
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ddf3c5d406c16891c692e84fb37c4d21757f702
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423771"
---
# <a name="wpd_content_type_program"></a>PROGRAMMA DI TIPO \_ DI CONTENUTO WPD \_ \_

Un oggetto che descrive il tipo come WPD \_ CONTENT TYPE PROGRAM rappresenta un programma \_ \_ eseguibile.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà     | Obbligatorio o facoltativo      |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, ma di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                                          |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                          |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà anche in fase di creazione.      |
| [FORMATO OGGETTO WPD \_ \_](object-properties.md)                                                        | Obbligatorio.                                                                          |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                          |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                  |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).              |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                  |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                          |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.              |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                            |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                          |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                          |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                             |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                          |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                       |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                         | facoltativo.                                                                          |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.                         |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                          |
| [OGGETTO WPD \_ \_ CHE GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                          |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                          |
| [IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                | facoltativo.                                                                          |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo | Descrizione                |
|--------------------------------------------------------|----------------------|----------------------------|
| [**IMPOSTAZIONE PREDEFINITA DELLA RISORSA WPD \_ \_**](wpd-resource-default.md) | Obbligatorio.            | Contiene il file di programma. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



