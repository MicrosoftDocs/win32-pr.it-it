---
description: DISPOSITIVO CATEGORIA \_ FUNZIONALE WPD \_ \_
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f39cf60e247c0abbbcc66f7fad52099a2a83a93f348b1ac9636bb790b9354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842217"
---
# <a name="wpd_functional_category_device"></a>DISPOSITIVO CATEGORIA \_ FUNZIONALE WPD \_ \_

Un oggetto funzionale WPD FUNCTIONAL CATEGORY DEVICE incapsula il dispositivo, ovvero \_ \_ \_ l'oggetto più in alto del dispositivo. Se un dispositivo implementa questa categoria funzionale, deve supportare queste proprietà oltre alle proprietà elencate per [l'oggetto dispositivo](device-object.md).



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                      |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                 | Obbligatorio.                                                                                                           |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio.                                                                                                           |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                      |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                                                           |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                                                           |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                   |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                               |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                                                                   |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                           |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                                               |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                                             |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                                                           |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                                                           |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                              |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                                                           |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                                                        |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                         | facoltativo.                                                                                                           |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                | Consigliato se un altro oggetto fa riferimento all'oggetto.                                                          |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                                                           |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                                                           |
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](miscellaneous-properties.md)                      | Obbligatorio.                                                                                                           |
| [PARTNER DI SINCRONIZZAZIONE \_ \_ DEI DISPOSITIVI WPD \_](device-properties.md)                                           | facoltativo.                                                                                                           |
| [VERSIONE \_ DEL FIRMWARE DEL \_ DISPOSITIVO WPD \_](device-properties.md)                                   | Obbligatorio.                                                                                                           |
| [LIVELLO DI ALIMENTAZIONE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                             | Consigliato se il dispositivo ha una batteria.                                                                                |
| [FONTE DI ALIMENTAZIONE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                           | Consigliato.                                                                                                        |
| [PROTOCOLLO DEL DISPOSITIVO WPD \_ \_](device-properties.md)                                                    | Consigliato.                                                                                                        |
| [PRODUTTORE DEL \_ DISPOSITIVO WPD \_](device-properties.md)                                            | Obbligatorio.                                                                                                           |
| [MODELLO DI DISPOSITIVO WPD \_ \_](device-properties.md)                                                          | Obbligatorio.                                                                                                           |
| [NUMERO DI SERIE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                         | Obbligatorio.                                                                                                           |
| [IL DISPOSITIVO WPD \_ \_ SUPPORTA NON \_ \_ UTILIZZABILE](device-properties.md)                    | Obbligatorio se il dispositivo supporta oggetti non utilizzabili. ad esempio se il dispositivo può essere usato per l'archiviazione dei dati semplice. |
| [DATETIME DEL DISPOSITIVO WPD \_ \_](device-properties.md)                                                    | facoltativo.                                                                                                           |
| [NOME \_ DESCRITTIVO DEL \_ DISPOSITIVO WPD \_](device-properties.md)                                         | Consigliato.                                                                                                        |
| [SCHEMI \_ DRM SUPPORTATI \_ DAI DISPOSITIVI \_ WPD \_](device-properties.md)                        | Consigliato se il dispositivo supporta la tecnologia DRM.                                                                  |
| [I FORMATI SUPPORTATI PER I DISPOSITIVI WPD \_ \_ SONO \_ \_ \_ ORDINATI](device-properties.md)       | Consigliato se il dispositivo supporta l'ordinamento del formato preferito.                                                       |
| [TIPO DI DISPOSITIVO WPD \_ \_](device-properties.md)                                                            | Consigliato.                                                                                                        |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



