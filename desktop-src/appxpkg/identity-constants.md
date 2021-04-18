---
title: Costanti Identity (AppModel. h)
description: Specifica la lunghezza delle stringhe per i campi Identity del pacchetto.
ms.assetid: C4F81822-B502-4360-AEA4-829F1AB926BF
topic_type:
- apiref
api_name:
- APPLICATION_USER_MODEL_ID_MAX_LENGTH
- APPLICATION_USER_MODEL_ID_MIN_LENGTH
- PACKAGE_ARCHITECTURE_MAX_LENGTH
- PACKAGE_ARCHITECTURE_MIN_LENGTH
- PACKAGE_FAMILY_NAME_MAX_LENGTH
- PACKAGE_FAMILY_NAME_MIN_LENGTH
- PACKAGE_FULL_NAME_MAX_LENGTH
- PACKAGE_FULL_NAME_MIN_LENGTH
- PACKAGE_NAME_MAX_LENGTH
- PACKAGE_NAME_MIN_LENGTH
- PACKAGE_PUBLISHERID_MAX_LENGTH
- PACKAGE_PUBLISHERID_MIN_LENGTH
- PACKAGE_PUBLISHER_MAX_LENGTH
- PACKAGE_PUBLISHER_MIN_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH
- PACKAGE_RESOURCEID_MAX_LENGTH
- PACKAGE_RESOURCEID_MIN_LENGTH
- PACKAGE_VERSION_MAX_LENGTH
- PACKAGE_VERSION_MIN_LENGTH
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681a0aef767afe92cdb93eee3849df8ed6a5f080
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301286"
---
# <a name="identity-constants"></a>Costanti Identity

Specifica la lunghezza delle stringhe per i campi Identity del pacchetto. La lunghezza viene misurata in caratteri e può includere o meno lo spazio per il terminatore NULL.

> [!Note]  
> Costanti nel formato: la lunghezza dell'ID del **\_ \_ modello utente \_ \_ \* \_ dell'applicazione** e la **\_ \_ \_ \_ \* \_ lunghezza dell'ID applicazione relativa del pacchetto** includono lo spazio per un carattere di terminazione null, ma le costanti nel formato: la **\_ \* \_ lunghezza del pacchetto** non include lo spazio per un carattere di terminazione null.

 



| Costante/valore                                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**Applicazione \_ di \_ \_ \_ \_ Lunghezza massima ID modello utente**</dt> <dt>130</dt> </dl>                  | Lunghezza massima dell'ID del modello utente dell'applicazione. Per il terminatore NULL è incluso uno spazio.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**Applicazione \_ di \_ID modello \_ utente \_ minimo \_ lunghezza**</dt> <dt>21</dt> </dl>                   | Lunghezza minima dell'ID del modello utente dell'applicazione. Per il terminatore NULL è incluso uno spazio.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza massima architettura**</dt> <dt>7</dt> </dl>                                     | Lunghezza massima dell'architettura. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza minima architettura**</dt> <dt>3</dt> </dl>                                     | Lunghezza minima dell'architettura. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ \_ Lunghezza massima del nome della famiglia**</dt> <dt>64</dt> </dl>                                      | Lunghezza massima del nome della famiglia. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**Pacchetto \_ di \_Nome famiglia \_ Min \_ length**</dt> <dt>17</dt> </dl>                                      | Lunghezza minima del nome della famiglia. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ \_ Lunghezza massima del nome completo**</dt> <dt>127</dt> </dl>                                           | Lunghezza massima del nome completo. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**Pacchetto \_ di \_Nome completo \_ Min \_ length**</dt> <dt>30</dt> </dl>                                            | Lunghezza minima del nome completo. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza massima del nome**</dt> <dt>50</dt> </dl>                                                            | Lunghezza massima del nome. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**Pacchetto \_ di NOME \_ Min \_ length**</dt> <dt>3</dt> </dl>                                                             | Lunghezza minima del nome. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza massima PUBLISHERID**</dt> <dt>13</dt> </dl>                                       | Lunghezza massima dell'ID del server di pubblicazione. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza minima PUBLISHERID**</dt> <dt>13</dt> </dl>                                       | Lunghezza minima dell'ID del server di pubblicazione. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza massima server di pubblicazione**</dt> <dt>8192</dt> </dl>                                           | Lunghezza massima del server di pubblicazione. Ad esempio, CN =*Publisher*. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza minima server di pubblicazione**</dt> <dt>4</dt> </dl>                                              | Lunghezza minima del server di pubblicazione. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ \_ \_ Lunghezza massima ID applicazione relativa**</dt> <dt>65</dt> </dl> | Lunghezza massima dell'ID applicazione relativa del pacchetto. Per il terminatore NULL è incluso uno spazio.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**Pacchetto \_ di \_ID applicazione \_ relativo \_ \_ lunghezza minima**</dt> <dt>2</dt> </dl>  | Lunghezza minima dell'ID applicazione relativa del pacchetto. Per il terminatore NULL è incluso uno spazio.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza massima RESOURCEID**</dt> <dt>30</dt> </dl>                                          | Lunghezza massima dell'ID risorsa. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza minima RESOURCEID**</dt> <dt>0</dt> </dl>                                           | Lunghezza minima dell'ID risorsa. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza massima versione**</dt> <dt>23</dt> </dl>                                                   | Lunghezza massima della versione. Ad esempio, *xxxxx*. *xxxxx*. *xxxxx*. *xxxxx*. Nessuno spazio incluso per il terminatore NULL/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**Pacchetto \_ di \_ \_ Lunghezza minima versione**</dt> <dt>7</dt> </dl>                                                    | Lunghezza minima della versione. Ad esempio *x*. *x*. *x*. *x*. Non è stato incluso alcuno spazio per il carattere di terminazione NULL.<br/>                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>AppModel. h</dt> </dl> |



 

 





