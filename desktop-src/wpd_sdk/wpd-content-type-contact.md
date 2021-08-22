---
description: CONTATTO DEL TIPO DI CONTENUTO WPD \_ \_ \_
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8354aa444f476e7c0b64d2e3d14d474c6eea02f90e8313c20073db2d0368fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083335"
---
# <a name="wpd_content_type_contact"></a>CONTATTO DEL TIPO DI CONTENUTO WPD \_ \_ \_

Un oggetto che descrive il tipo come WPD \_ CONTENT TYPE CONTACT rappresenta i dati di contatto \_ \_ personali.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà                                                                                                                   | Obbligatorio o facoltativo                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                          | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                           | Obbligatorio.                                                                      |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                                      | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                    | Obbligatorio, di sola lettura. Un client non può impostare questa proprietà, anche in fase di creazione. |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                  | Obbligatorio.                                                                      |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                     | Obbligatorio.                                                                      |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                              | Obbligatorio se l'oggetto è nascosto.                                              |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                              | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).          |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                      | Obbligatorio se l'oggetto dispone di almeno una risorsa.                              |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                                        | Obbligatorio se l'oggetto rappresenta un file.                                      |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                                 | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo.          |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                          | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.                        |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                              | facoltativo.                                                                      |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                               | facoltativo.                                                                      |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                            | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                         |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                                      |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                                   | Consigliato.                                                                   |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                                   | facoltativo.                                                                      |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                                                          | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.                     |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)               | facoltativo.                                                                      |
| [GENERAZIONE \_ DELL'ANTEPRIMA \_ \_ DELL'OGGETTO \_ WPD DALLA \_ RISORSA](object-properties.md)           | facoltativo.                                                                      |
| [NOME VISUALIZZATO DEL CONTATTO WPD \_ \_ \_](contact-properties.md)                                                  | Obbligatorio.                                                                      |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                                                               | Obbligatorio se l'oggetto non può essere eliminato.                                      |
| [IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                          | facoltativo.                                                                      |
| [NOME VISUALIZZATO DEL CONTATTO WPD \_ \_ \_](contact-properties.md)                                                                           | Obbligatorio.                                                                      |
| [NOME CONTATTO \_ WPD \_ \_](contact-properties.md)                                                      | Consigliato.                                                                   |
| [NOMI INTERMEDI DEI CONTATTI WPD \_ \_ \_](contact-properties.md)                                                  | Consigliato.                                                                   |
| [COGNOME CONTATTO WPD \_ \_ \_](contact-properties.md)                                                        | Consigliato.                                                                   |
| [PREFISSO CONTATTO WPD \_ \_](contact-properties.md)                                                               | Consigliato.                                                                   |
| [SUFFISSO CONTATTO WPD \_ \_](contact-properties.md)                                                               | Consigliato.                                                                   |
| [NOME FONETICO CONTATTO WPD \_ \_ \_ \_](contact-properties.md)                                   | facoltativo.                                                                      |
| [COGNOME FONETICO DEL CONTATTO WPD \_ \_ \_ \_](contact-properties.md)                                     | facoltativo.                                                                      |
| [WPD \_ CONTATTARE \_ \_ L'INDIRIZZO POSTALE COMPLETO \_ \_ PERSONALE](contact-properties.md)                | Consigliato.                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ LINE1](contact-properties.md)              | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ LINE2](contact-properties.md)              | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                | facoltativo.                                                                      |
| [AREA INDIRIZZO POSTALE PERSONALE CONTATTO WPD \_ \_ \_ \_ \_](contact-properties.md)            | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ POSTAL \_ CODE](contact-properties.md) | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ COUNTRY](contact-properties.md)          | facoltativo.                                                                      |
| [INDIRIZZO POSTALE COMPLETO WPD CONTACT \_ \_ BUSINESS \_ \_ \_](contact-properties.md)                | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ LINE1](contact-properties.md)              | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ LINE2](contact-properties.md)              | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ REGION](contact-properties.md)            | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ POSTAL \_ CODE](contact-properties.md) | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ COUNTRY](contact-properties.md)          | facoltativo.                                                                      |
| [WPD \_ CONTATTARE UN ALTRO INDIRIZZO POSTALE \_ \_ \_ \_ COMPLETO](contact-properties.md)                      | facoltativo.                                                                      |
| [WPD CONTATTARE ALTRI INDIRIZZI POSTALI \_ \_ RIGA \_ \_ \_ 1](contact-properties.md)                    | facoltativo.                                                                      |
| [WPD CONTATTARE ALTRI INDIRIZZI POSTALI \_ \_ RIGA \_ \_ \_ 2](contact-properties.md)                    | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                      | facoltativo.                                                                      |
| [WPD \_ CONTATTARE \_ UN'ALTRA \_ AREA INDIRIZZO \_ \_ POSTALE](contact-properties.md)                  | facoltativo.                                                                      |
| [WPD \_ CONTATTARE UN ALTRO \_ \_ CODICE \_ \_ \_ POSTALE](contact-properties.md)       | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ POSTAL \_ COUNTRY](contact-properties.md) | facoltativo.                                                                      |
| [INDIRIZZO DI POSTA ELETTRONICA \_ PRINCIPALE DEL CONTATTO WPD \_ \_ \_](contact-properties.md)                               | Consigliato.                                                                   |
| [WPD \_ CONTATTARE \_ L'INDIRIZZO DI POSTA ELETTRONICA \_ PERSONALE](contact-properties.md)                                              | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ EMAIL2](contact-properties.md)                                            | facoltativo.                                                                      |
| [WPD \_ CONTATTARE \_ L'INDIRIZZO DI POSTA ELETTRONICA \_ AZIENDALE](contact-properties.md)                                              | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ EMAIL2](contact-properties.md)                                            | facoltativo.                                                                      |
| [WPD \_ CONTATTARE ALTRI MESSAGGI DI POSTA \_ \_ ELETTRONICA](contact-properties.md)                                                  | facoltativo.                                                                      |
| [TELEFONO PRINCIPALE DEL CONTATTO WPD \_ \_ \_](contact-properties.md)                                                | Consigliato.                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ PHONE](contact-properties.md)                                              | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ PHONE2](contact-properties.md)                                            | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ PHONE](contact-properties.md)                                              | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ PHONE2](contact-properties.md)                                            | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ MOBILE \_ PHONE](contact-properties.md)                                                  | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ MOBILE \_ PHONE2](contact-properties.md)                                                | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ FAX](contact-properties.md)                                                  | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ FAX](contact-properties.md)                                                  | facoltativo.                                                                      |
| [PAGER DEI \_ CONTATTI WPD \_](contact-properties.md)                                                                 | facoltativo.                                                                      |
| [WPD \_ CONTATTARE \_ ALTRI \_ TELEFONI](contact-properties.md)                                                  | facoltativo.                                                                      |
| [INDIRIZZO WEB PRIMARIO DEL CONTATTO WPD \_ \_ \_ \_](contact-properties.md)                                   | Consigliato.                                                                   |
| [INDIRIZZO WEB PERSONALE DEL CONTATTO WPD \_ \_ \_ \_](contact-properties.md)                                 | facoltativo.                                                                      |
| [INDIRIZZO WEB AZIENDALE CONTATTO WPD \_ \_ \_ \_](contact-properties.md)                                 | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER](contact-properties.md)                                        | Consigliato                                                                    |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER2](contact-properties.md)                                      | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER3](contact-properties.md)                                      | facoltativo.                                                                      |
| [NOME SOCIETÀ CONTATTO WPD \_ \_ \_](contact-properties.md)                                                  | facoltativo.                                                                      |
| [NOME \_ FONETICO DEL CONTATTO WPD \_ \_ \_](contact-properties.md)                               | Facoltativo                                                                       |
| [RUOLO CONTATTO \_ WPD \_](contact-properties.md)                                                                   | facoltativo.                                                                      |
| [DATA DI NASCITA DEL CONTATTO WPD \_ \_](contact-properties.md)                                                         | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ PRIMARY \_ FAX](contact-properties.md)                                                                            | facoltativo.                                                                      |
| [PARTNER DI CONTATTO WPD \_ \_](contact-properties.md)                                                                                  | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ CHILDREN](contact-properties.md)                                                                                | facoltativo.                                                                      |
| [ASSISTENTE CONTATTO \_ WPD \_](contact-properties.md)                                                                               | facoltativo.                                                                      |
| [DATA \_ \_ DELL'ANNIVERSARIO DEL CONTATTO WPD \_](contact-properties.md)                                                                       | facoltativo.                                                                      |
| [WPD \_ CONTACT \_ RINGTONE](contact-properties.md)                                                                                | facoltativo.                                                                      |
| [NOTE SULLE INFORMAZIONI \_ COMUNI WPD \_ \_](object-properties.md)                                                                        | facoltativo.                                                                      |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                                       | Obbligatorio o facoltativo       | Descrizione                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**IMPOSTAZIONE PREDEFINITA DELLA RISORSA WPD \_ \_**](wpd-resource-default.md)              | facoltativo.                  | Contiene i dati del contatto.         |
| [**FOTO DI CONTATTO DELLA RISORSA WPD \_ \_ \_**](wpd-resource-contact-photo.md) | Consigliato, se disponibile. | Contiene un'immagine del contatto. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 



