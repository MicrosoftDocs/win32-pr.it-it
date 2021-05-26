---
description: TIPO DI \_ CONTENUTO WPD NON \_ \_ SPECIFICATO
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423681"
---
# <a name="wpd_content_type_unspecified"></a>TIPO DI \_ CONTENUTO WPD NON \_ \_ SPECIFICATO

Un oggetto che descrive il tipo come WPD \_ CONTENT \_ TYPE UNSPECIFIED rappresenta un oggetto generico che può avere o meno \_ un file fisico sottostante. La differenza tra questo tipo e WPD CONTENT TYPE GENERIC FILE è che gli oggetti \_ \_ \_ \_ WPD \_ CONTENT TYPE GENERIC FILE devono avere un file fisico \_ \_ \_ sottostante.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà       | Obbligatorio o facoltativo         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà anche in fase di creazione. |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                                     |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                     |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà anche in fase di creazione. |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                     |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                     |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                             |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).         |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto dispone di almeno una risorsa.                             |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                     |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo.         |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                       |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                     |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                     |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                        |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                     |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                  |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                         | facoltativo.                                                                     |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                                                | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.                    |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                     |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                     |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                     |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                | facoltativo.                                                                     |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo                             | Descrizione               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**RISORSA WPD \_ \_ PREDEFINITA**](wpd-resource-default.md) | Obbligatorio se l'oggetto è supportato da dati binari. | Contiene i dati binari. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



