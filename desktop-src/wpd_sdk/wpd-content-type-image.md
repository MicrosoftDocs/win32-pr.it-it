---
description: IMMAGINE DEL TIPO \_ DI CONTENUTO WPD \_ \_
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846347ac83345ed685a10739126028ca1728bb16a52fe7083fcc7dd823447c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193495"
---
# <a name="wpd_content_type_image"></a>IMMAGINE DEL TIPO \_ DI CONTENUTO WPD \_ \_

Un oggetto che ne descrive il tipo come WPD \_ CONTENT TYPE IMAGE rappresenta \_ \_ un'immagine ancorata.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                   |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                                                        |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                                                        |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                   |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                                                        | Obbligatorio.                                                                                        |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                                                        |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                                                |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                            |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto dispone di almeno una risorsa.                                                |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                                                        |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo.                            |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                          |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                                                        |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                                        |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                           |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                                                        |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                                                     |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                         | facoltativo.                                                                                        |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                                                | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.                                       |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                                                        |
| [GENERAZIONE \_ DELL'ANTEPRIMA \_ \_ DELL'OGGETTO \_ WPD DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                                        |
| [\_BITDEPTH IMMAGINE \_ WPD](image-properties.md)                                                       | Consigliato.                                                                                     |
| [STATO RITAGLIATO DELL'IMMAGINE WPD \_ \_ \_](image-properties.md)                                          | facoltativo.                                                                                        |
| [STATO CORRETTO \_ DEL \_ COLORE \_ DELL'IMMAGINE \_ WPD](image-properties.md)                         | facoltativo.                                                                                        |
| [FNUMBER \_ IMMAGINE WPD \_](image-properties.md)                                                                           | facoltativo.                                                                                        |
| [TEMPO DI ESPOSIZIONE DELL'IMMAGINE WPD \_ \_ \_](image-properties.md)                                                                    | facoltativo.                                                                                        |
| [INDICE DI ESPOSIZIONE DELLE IMMAGINI WPD \_ \_ \_](image-properties.md)                                                                   | facoltativo.                                                                                        |
| [RISOLUZIONE ORIZZONTALE DELL'IMMAGINE WPD \_ \_ \_](image-properties.md)                                                            | facoltativo.                                                                                        |
| [RISOLUZIONE VERTICALE \_ DELL'IMMAGINE WPD \_ \_](image-properties.md)                                                              | facoltativo.                                                                                        |
| [COPYRIGHT DEI SUPPORTI WPD \_ \_](media-properties.md)                                                     | facoltativo.                                                                                        |
| [LARGHEZZA DEI SUPPORTI WPD \_ \_](media-properties.md)                                                             | Obbligatorio.                                                                                        |
| [ALTEZZA DEI SUPPORTI WPD \_ \_](media-properties.md)                                                           | Obbligatorio.                                                                                        |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                                                            | Consigliato.                                                                                     |
| [WPD \_ MEDIA \_ ALBUM \_ ARTIST](media-properties.md)                                                                     | Consigliato. Questa proprietà identifica la persona o le persone che hanno creato l'oggetto. |
| [URL ORIGINE SUPPORTO WPD \_ \_ \_](media-properties.md)                                                                       | facoltativo.                                                                                        |
| [URL DESTINAZIONE SUPPORTI WPD \_ \_ \_](media-properties.md)                                                                  | facoltativo.                                                                                        |
| [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)                                                                       | facoltativo.                                                                                        |
| [GENERE MULTIMEDIALE WPD \_ \_](media-properties.md)                                                                             | facoltativo.                                                                                        |
| [SEGNALIBRO BYTE MULTIMEDIALI WPD \_ \_ \_](media-properties.md)                                                                    | facoltativo.                                                                                        |
| [GUID SUPPORTO WPD \_ \_](media-properties.md)                                                                              | facoltativo.                                                                                        |
| [DESCRIZIONE DELLA \_ SOTTOSOD MEDIA \_ \_ WPD](media-properties.md)                                                                  | facoltativo.                                                                                        |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                                 | Obbligatorio o facoltativo | Descrizione                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**IMPOSTAZIONE PREDEFINITA DELLA RISORSA WPD \_ \_**](wpd-resource-default.md)        | Obbligatorio.            | Contiene i dati dell'immagine.                                                                 |
| [**ANTEPRIMA DELLA RISORSA WPD \_ \_**](wpd-resource-thumbnail.md)    | Consigliato.         | Contiene l'anteprima dell'immagine.                                                    |
| [**CLIP AUDIO \_ DELLA \_ RISORSA WPD \_**](wpd-resource-audio-clip.md) | facoltativo.            | Se a questa immagine è associata un'annotazione audio, questa risorsa contiene i dati audio. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



