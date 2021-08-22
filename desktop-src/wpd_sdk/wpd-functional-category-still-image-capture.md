---
description: CATEGORIA FUNZIONALE WPD \_ \_ ACQUISIZIONE DI \_ \_ IMMAGINI \_
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fb0f6f19930780784083eaeddc1156bf55c99943aae8ad5850374c04211dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444811"
---
# <a name="wpd_functional_category_still_image_capture"></a>CATEGORIA FUNZIONALE WPD \_ \_ ACQUISIZIONE DI \_ \_ IMMAGINI \_

Un oggetto funzionale WPD FUNCTIONAL CATEGORY STILL IMAGE CAPTURE incapsula la funzionalità di acquisizione di immagini non ancorate in un dispositivo, ad esempio un allegato di \_ \_ fotocamera o \_ \_ \_ fotocamera.



| Nome della proprietà                                                                                                            | Obbligatorio o facoltativo                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                   | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                                                         |
| [ID PADRE \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio.                                                                                                                                              |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                               | Obbligatorio.                                                                                                                                              |
| [\_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD](object-properties.md)                             | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione.                                                                         |
| [FORMATO OGGETTO \_ WPD \_](object-properties.md)                                                           | Obbligatorio.                                                                                                                                              |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                              | Obbligatorio.                                                                                                                                              |
| [OGGETTO WPD \_ \_ ISHIDDEN](object-properties.md)                                                       | Obbligatorio se l'oggetto è nascosto.                                                                                                                      |
| [ISSYSTEM \_ DELL'OGGETTO WPD \_](object-properties.md)                                                       | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).                                                                                  |
| [DIMENSIONI DEGLI OGGETTI \_ \_ WPD](object-properties.md)                                                               | Obbligatorio se l'oggetto ha almeno una risorsa.                                                                                                      |
| [NOME FILE ORIGINALE \_ \_ \_ DELL'OGGETTO WPD \_](object-properties.md)                                 | Obbligatorio se l'oggetto rappresenta un file.                                                                                                              |
| [OGGETTO WPD \_ \_ NON \_ UTILIZZABILE](object-properties.md)                                          | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo.                                                                                  |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                   | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                                                                                                |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                       | facoltativo.                                                                                                                                              |
| [ID SINCRONIZZAZIONE OGGETTI WPD \_ \_ \_](object-properties.md)                                                        | facoltativo.                                                                                                                                              |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                     | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                                                                                                 |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                              | facoltativo.                                                                                                                                              |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                            | Consigliato.                                                                                                                                           |
| [DATA CREAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                            | facoltativo.                                                                                                                                              |
| [RIFERIMENTI AGLI \_ OGGETTI WPD \_ \_](object-properties.md)                                                                   | Consigliato se un altro oggetto fa riferimento all'oggetto.                                                                                             |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)        | facoltativo.                                                                                                                                              |
| [OGGETTO WPD \_ CHE \_ GENERA \_ \_ UN'ANTEPRIMA DALLA \_ RISORSA](object-properties.md)    | facoltativo.                                                                                                                                              |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                        | Obbligatorio se l'oggetto non può essere eliminato.                                                                                                              |
| [IMPOSTAZIONI LOCALI DELLA \_ LINGUA \_ DEGLI OGGETTI \_ WPD](object-properties.md)                                                                   | facoltativo.                                                                                                                                              |
| [CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_](miscellaneous-properties.md)                         | Obbligatorio. Vedere [**WPD \_ CONTENT TYPE FUNCTIONAL \_ OBJECT \_ \_ (OGGETTO FUNZIONALE**](wpd-content-type-functional-object.md) DEL TIPO DI CONTENUTO WPD) per le categorie Windows dispositivi portatili. |
| [RISOLUZIONE DELL'ACQUISIZIONE \_ DI \_ IMMAGINI ANCORA WPD \_ \_](still-image-properties.md)                  | Obbligatorio.                                                                                                                                              |
| [FORMATO DI ACQUISIZIONE \_ DI \_ IMMAGINI ANCORA WPD \_ \_](still-image-properties.md)                          | Obbligatorio.                                                                                                                                              |
| [IMPOSTAZIONE DI COMPRESSIONE \_ DELLE IMMAGINI ANCORA \_ WPD \_ \_](still-image-properties.md)                | facoltativo.                                                                                                                                              |
| [BILANCIAMENTO DEL BIANCO \_ \_ DELL'IMMAGINE \_ ANCORA WPD \_](still-image-properties.md)                            | facoltativo.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ RGB \_ GAIN](still-image-properties.md)                                      | facoltativo.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FNUMBER](still-image-properties.md)                                         | facoltativo.                                                                                                                                              |
| [LUNGHEZZA FOCALE IMMAGINE FISSA WPD \_ \_ \_ \_](still-image-properties.md)                              | facoltativo.                                                                                                                                              |
| [DISTANZA DELLO STATO ATTIVO \_ \_ DELL'IMMAGINE ANCORA \_ WPD \_](still-image-properties.md)                          | facoltativo.                                                                                                                                              |
| [MODALITÀ MESSA A FUOCO \_ \_ DELL'IMMAGINE ANCORA WPD \_ \_](still-image-properties.md)                                  | facoltativo.                                                                                                                                              |
| [MODALITÀ DI MISURAZIONE \_ \_ DELL'ESPOSIZIONE \_ DELL'IMMAGINE \_ ANCORA WPD \_](still-image-properties.md)         | facoltativo.                                                                                                                                              |
| [WPD STILL IMAGE FLASH MODE (MODALITÀ FLASH IMMAGINE ANCORA \_ \_ \_ WPD) \_](still-image-properties.md)                                  | facoltativo.                                                                                                                                              |
| [TEMPO DI ESPOSIZIONE \_ \_ DELL'IMMAGINE WPD \_ \_](still-image-properties.md)                            | facoltativo.                                                                                                                                              |
| [WPD STILL IMAGE EXPOSURE PROGRAM MODE (MODALITÀ PROGRAMMA DI ESPOSIZIONE DI IMMAGINI ANCORA \_ WPD) \_ \_ \_ \_](still-image-properties.md)           | facoltativo.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ EXPOSURE \_ INDEX](still-image-properties.md)                          | facoltativo.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ EXPOSURE \_ BIAS \_ COMPENSATION](still-image-properties.md) | facoltativo.                                                                                                                                              |
| [RITARDO DI ACQUISIZIONE \_ DI \_ IMMAGINI ANCORA WPD \_ \_](still-image-properties.md)                            | facoltativo.                                                                                                                                              |
| [MODALITÀ DI ACQUISIZIONE \_ DI \_ IMMAGINI ANCORA WPD \_ \_](still-image-properties.md)                              | facoltativo.                                                                                                                                              |
| [CONTRASTO DELLE \_ IMMAGINI ANCORA \_ WPD \_](still-image-properties.md)                                       | facoltativo.                                                                                                                                              |
| [NITIDEZZA \_ DELLE IMMAGINI ANCORA \_ WPD \_](still-image-properties.md)                                     | facoltativo.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ DIGITAL \_ ZOOM](still-image-properties.md)                              | facoltativo.                                                                                                                                              |
| [MODALITÀ EFFETTO IMMAGINE CONTINUA WPD \_ \_ \_ \_](still-image-properties.md)                                | facoltativo.                                                                                                                                              |
| [WPD STILL IMAGE BURST NUMBER (NUMERO \_ \_ BURST IMMAGINE WPD) \_ \_](still-image-properties.md)                              | facoltativo.                                                                                                                                              |
| [INTERVALLO DI BURST \_ \_ DELL'IMMAGINE WPD \_ \_](still-image-properties.md)                          | facoltativo.                                                                                                                                              |
| [NUMERO \_ \_ TIMELAPSE DELL'IMMAGINE \_ WPD \_](still-image-properties.md)                      | facoltativo.                                                                                                                                              |
| [INTERVALLO \_ \_ \_ TIMELAPSE IMMAGINE WPD \_](still-image-properties.md)                  | facoltativo.                                                                                                                                              |
| [MODALITÀ DI MISURAZIONE \_ DELLO \_ STATO ATTIVO \_ DELL'IMMAGINE \_ \_ WPD](still-image-properties.md)               | facoltativo.                                                                                                                                              |
| [URL DI CARICAMENTO \_ IMMAGINE WPD \_ \_ \_](still-image-properties.md)                                  | facoltativo.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ ARTIST](still-image-properties.md)                                           | facoltativo.                                                                                                                                              |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

Molte di queste proprietà hanno effetti interconnessi. Ad esempio, se **WPD \_ STILL IMAGE EXPOSURE \_ \_ \_ METERING \_ MODE** è impostato su automatic, verranno collegati f-stop, tempo di esposizione e contatore dell'esposizione. In caso di variazione di uno, gli altri potrebbero variare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



