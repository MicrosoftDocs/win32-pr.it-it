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

Un oggetto funzionale WPD FUNCTIONAL CATEGORY DEVICE incapsula il dispositivo, ovvero l'oggetto più \_ \_ in alto del \_ dispositivo. Se un dispositivo implementa questa categoria funzionale, deve supportare queste proprietà oltre alle proprietà elencate per [l'oggetto dispositivo](device-object.md).



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                      |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                                                                           |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio.                                                                                                           |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                      |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                                                           |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                                                           |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                                   |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                               |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto dispone di almeno una risorsa.                                                                   |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                                           |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo.                                               |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                                             |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                                                           |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                                                           |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                              |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                                                           |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                                                        |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                         | facoltativo.                                                                                                           |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                                                | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.                                                          |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                                                           |
| [GENERAZIONE \_ DELL'ANTEPRIMA \_ \_ DELL'OGGETTO \_ WPD DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                                                           |
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](miscellaneous-properties.md)                      | Obbligatorio.                                                                                                           |
| [PARTNER DI SINCRONIZZAZIONE DISPOSITIVI WPD \_ \_ \_](device-properties.md)                                           | facoltativo.                                                                                                           |
| [VERSIONE DEL \_ FIRMWARE DEL \_ DISPOSITIVO WPD \_](device-properties.md)                                   | Obbligatorio.                                                                                                           |
| [LIVELLO DI ALIMENTAZIONE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                             | Consigliato se il dispositivo ha una batteria.                                                                                |
| [ORIGINE ALIMENTAZIONE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                           | Consigliato.                                                                                                        |
| [PROTOCOLLO DEL DISPOSITIVO WPD \_ \_](device-properties.md)                                                    | Consigliato.                                                                                                        |
| [PRODUTTORE DEL DISPOSITIVO WPD \_ \_](device-properties.md)                                            | Obbligatorio.                                                                                                           |
| [MODELLO DI DISPOSITIVO WPD \_ \_](device-properties.md)                                                          | Obbligatorio.                                                                                                           |
| [NUMERO DI SERIE DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                         | Obbligatorio.                                                                                                           |
| [IL DISPOSITIVO WPD \_ \_ SUPPORTA NON \_ \_ UTILIZZABILI](device-properties.md)                    | Obbligatorio se il dispositivo supporta oggetti non consumabili. in altri parole, se il dispositivo può essere usato per l'archiviazione dati semplice. |
| [DATETIME DEL DISPOSITIVO WPD \_ \_](device-properties.md)                                                    | facoltativo.                                                                                                           |
| [NOME DESCRITTIVO DEL DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                         | Consigliato.                                                                                                        |
| [SCHEMI \_ DRM SUPPORTATI \_ DAI DISPOSITIVI \_ WPD \_](device-properties.md)                        | Consigliato se il dispositivo supporta la tecnologia DRM.                                                                  |
| [I FORMATI SUPPORTATI DAI DISPOSITIVI WPD \_ \_ SONO \_ \_ \_ ORDINATI](device-properties.md)       | Consigliato se il dispositivo supporta l'ordinamento del formato preferito.                                                       |
| [TIPO DI DISPOSITIVO WPD \_ \_](device-properties.md)                                                            | Consigliato.                                                                                                        |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



