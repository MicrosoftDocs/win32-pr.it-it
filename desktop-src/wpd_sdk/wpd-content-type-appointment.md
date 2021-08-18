---
description: APPUNTAMENTO CON TIPO DI CONTENUTO WPD \_ \_ \_
ms.assetid: d41c26ef-9f51-4ba7-b1a4-57abec91925e
title: WPD_CONTENT_TYPE_APPOINTMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159f80246b14c121e386f1122a70dce27e717481ec02897c06b9061821a8c0fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193545"
---
# <a name="wpd_content_type_appointment"></a>APPUNTAMENTO CON TIPO DI CONTENUTO WPD \_ \_ \_

Un oggetto che descrive il tipo come WPD \_ CONTENT TYPE APPOINTMENT rappresenta un appuntamento in un \_ \_ calendario.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                         | Obbligatorio o facoltativo                                                           |
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
| [GENERAZIONE \_ DELL'ANTEPRIMA \_ \_ DELL'OGGETTO \_ WPD DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                                      |
| [POSIZIONE APPUNTAMENTO WPD \_ \_](appointment-properties.md)                                     | Obbligatorio.                                                                      |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                     | Obbligatorio se l'oggetto può essere eliminato.                                         |
| [IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                | facoltativo.                                                                      |
| [WPD \_ COMMON \_ INFORMATION \_ SUBJECT](object-properties.md)                                                            | Obbligatorio.                                                                      |
| [TESTO DEL CORPO \_ DELLE INFORMAZIONI COMUNI \_ WPD \_ \_](object-properties.md)                                                         | Consigliato.                                                                   |
| [PRIORITÀ DELLE INFORMAZIONI COMUNI WPD \_ \_ \_](object-properties.md)                                                           | Consigliato.                                                                   |
| [DATETIME DI INIZIO \_ \_ DELLE INFORMAZIONI COMUNI \_ \_ WPD](object-properties.md)                                                    | Consigliato.                                                                   |
| [DATETIME DI \_ FINE \_ DELLE INFORMAZIONI COMUNI \_ WPD \_](object-properties.md)                                                      | Consigliato.                                                                   |
| [NOTE SULLE INFORMAZIONI \_ COMUNI WPD \_ \_](object-properties.md)                                                              | facoltativo.                                                                      |
| [POSIZIONE APPUNTAMENTO WPD \_ \_](object-properties.md)                                                                   | Obbligatorio.                                                                      |
| [TIPO DI APPUNTAMENTO WPD \_ \_](appointment-properties.md)                                             | facoltativo.                                                                      |
| [PARTECIPANTI RICHIESTI \_ PER \_ \_ L'APPUNTAMENTO WPD](appointment-properties.md)                | facoltativo.                                                                      |
| [PARTECIPANTI \_ FACOLTATIVI \_ DELL'APPUNTAMENTO WPD \_](appointment-properties.md)                | facoltativo.                                                                      |
| [PARTECIPANTI \_ ACCETTATI PER \_ \_ L'APPUNTAMENTO WPD](appointment-properties.md)                | facoltativo.                                                                      |
| [RISORSE PER APPUNTAMENTI \_ WPD \_](appointment-properties.md)                                   | facoltativo.                                                                      |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti in genere non ospitano risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



