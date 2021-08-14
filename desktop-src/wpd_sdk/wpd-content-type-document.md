---
description: DOCUMENTO DEL TIPO \_ DI CONTENUTO WPD \_ \_
ms.assetid: c3859590-7674-4315-b171-3747e5d9350b
title: WPD_CONTENT_TYPE_DOCUMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47684fa261b3455adba371c81095dea5cc5243266a662a922da7108e0d3b07c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193510"
---
# <a name="wpd_content_type_document"></a>DOCUMENTO DEL TIPO \_ DI CONTENUTO WPD \_ \_

Un oggetto che descrive il tipo come DOCUMENTO DI TIPO DI CONTENUTO WPD \_ \_ rappresenta un \_ documento. Ad esempio Microsoft Office file di Word, Microsoft Office Excel, file di testo normale e altri formati di documenti proprietari.

Questo tipo di oggetto può ospitare le proprietà seguenti.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio.                                                                      |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                      |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                      |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                              |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).          |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                              |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.          |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                        |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                      |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                      |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                         |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                      |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                   |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                         | facoltativo.                                                                      |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                     |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                      |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                      |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto non può essere eliminato.                                      |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                | facoltativo.                                                                      |
| [URL ORIGINE MULTIMEDIALE WPD \_ \_ \_](object-properties.md)                                                                      | facoltativo.                                                                      |
| [URL DESTINAZIONE SUPPORTO WPD \_ \_ \_](object-properties.md)                                                                 | facoltativo.                                                                      |
| [DESCRIZIONE DEI SUPPORTI WPD \_ \_](object-properties.md)                                                                      | facoltativo.                                                                      |
| [GENERE MULTIMEDIALE WPD \_ \_](object-properties.md)                                                                            | facoltativo.                                                                      |
| [SEGNALIBRO MEDIA BYTE WPD \_ \_ \_](object-properties.md)                                                                   | facoltativo.                                                                      |
| [GUID SUPPORTO WPD \_ \_](object-properties.md)                                                                             | facoltativo.                                                                      |
| [DESCRIZIONE SECONDARIA \_ DEI \_ SUPPORTI WPD \_](object-properties.md)                                                                 | facoltativo.                                                                      |
| [INFORMAZIONI COMUNI SULLA WPD \_ \_](object-properties.md)                                                                     | Consigliato.                                                                   |
| [TESTO DEL CORPO \_ DELLE \_ INFORMAZIONI COMUNI \_ \_ WPD](object-properties.md)                                                         | Consigliato.                                                                   |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                          | Obbligatorio o facoltativo | Descrizione                     |
|--------------------------------------------------------|----------------------|---------------------------------|
| [**RISORSA WPD \_ \_ PREDEFINITA**](wpd-resource-default.md) | Necessario             | Contiene il documento fisico. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



