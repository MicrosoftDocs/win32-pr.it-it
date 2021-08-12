---
title: Costanti identity (AppModel.h)
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
ms.openlocfilehash: 4590e62397ac069cb0fc9661f615288c2d8df36ba41304fff71e4ef0293f9f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552213"
---
# <a name="identity-constants"></a>Costanti di identità

Specifica la lunghezza delle stringhe per i campi Identity del pacchetto. La lunghezza viene misurata in caratteri e può includere o meno spazio per il carattere di terminazione NULL.

> [!Note]  
> Le costanti nel formato: **APPLICATION USER MODEL ID \_ \_ \_ \_ \* \_ LENGTH** e PACKAGE RELATIVE APPLICATION **ID \_ \_ \_ \_ \* \_ LENGTH** includono lo spazio per un carattere di terminazione NULL, ma le costanti nel formato PACKAGE **\_ \* \_ LENGTH** non includono spazio per un carattere di terminazione NULL.

 



| Costante/valore                                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**APPLICAZIONE \_ LUNGHEZZA \_ MASSIMA ID MODELLO \_ \_ \_ UTENTE**</dt> <dt>130</dt> </dl>                  | Lunghezza massima dell'ID modello utente dell'applicazione. Lo spazio è incluso per il carattere di terminazione NULL.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**APPLICAZIONE \_ USER \_ MODEL ID MIN \_ \_ \_ LENGTH**</dt> <dt>21</dt> </dl>                   | Lunghezza minima dell'ID modello utente dell'applicazione. Lo spazio è incluso per il carattere di terminazione NULL.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**PACCHETTO \_ ARCHITETTURA \_ LUNGHEZZA \_ MASSIMA**</dt> <dt>7</dt> </dl>                                     | Lunghezza massima dell'architettura. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**PACCHETTO \_ ARCHITETTURA \_ LUNGHEZZA \_ MINIMA**</dt> <dt>3</dt> </dl>                                     | Lunghezza minima dell'architettura. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**PACCHETTO \_ NOME \_ FAMIGLIA \_ LUNGHEZZA \_ MASSIMA**</dt> <dt>64</dt> </dl>                                      | Lunghezza massima del nome della famiglia. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**PACCHETTO \_ NOME \_ FAMIGLIA \_ LUNGHEZZA \_ MINIMA**</dt> <dt>17</dt> </dl>                                      | Lunghezza minima del nome della famiglia. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**PACCHETTO \_ FULL \_ NAME \_ MAX \_ LENGTH**</dt> <dt>127</dt> </dl>                                           | Lunghezza massima del nome completo. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**PACCHETTO \_ NOME \_ COMPLETO \_ LUNGHEZZA \_ MINIMA**</dt> <dt>30</dt> </dl>                                            | Lunghezza minima del nome completo. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**PACCHETTO \_ NOME \_ LUNGHEZZA \_ MASSIMA**</dt> <dt>50</dt> </dl>                                                            | Lunghezza massima del nome. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**PACCHETTO \_ NOME \_ LUNGHEZZA \_ MINIMA**</dt> <dt>3</dt> </dl>                                                             | Lunghezza minima del nome. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**PACCHETTO \_ LUNGHEZZA \_ MASSIMA \_ PUBLISHERID**</dt> <dt>13</dt> </dl>                                       | Lunghezza massima dell'ID del server di pubblicazione. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**PACCHETTO \_ PUBLISHERID \_ MIN \_ LENGTH**</dt> <dt>13</dt> </dl>                                       | Lunghezza minima dell'ID editore. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**PACCHETTO \_ LUNGHEZZA \_ MASSIMA SERVER DI \_ PUBBLICAZIONE**</dt> <dt>8192</dt> </dl>                                           | Lunghezza massima del server di pubblicazione. Ad esempio, CN=*publisher*. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**PACCHETTO \_ LUNGHEZZA \_ MINIMA SERVER DI \_ PUBBLICAZIONE**</dt> <dt>4</dt> </dl>                                              | Lunghezza minima del server di pubblicazione. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**PACCHETTO \_ LUNGHEZZA \_ MASSIMA ID APPLICAZIONE \_ \_ \_ RELATIVA**</dt> <dt>65</dt> </dl> | Lunghezza massima dell'ID applicazione relativo del pacchetto. Lo spazio è incluso per il carattere di terminazione NULL.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**PACCHETTO \_ ID \_ APPLICAZIONE RELATIVO LUNGHEZZA \_ \_ \_ MINIMA**</dt> <dt>2</dt> </dl>  | Lunghezza minima dell'ID applicazione relativo del pacchetto. Lo spazio è incluso per il carattere di terminazione NULL.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**PACCHETTO \_ LUNGHEZZA \_ MASSIMA \_ RESOURCEID**</dt> <dt>30</dt> </dl>                                          | Lunghezza massima dell'ID risorsa. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**PACCHETTO \_ RESOURCEID \_ MIN \_ LENGTH**</dt> <dt>0</dt> </dl>                                           | Lunghezza minima dell'ID risorsa. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**PACCHETTO \_ VERSIONE \_ LUNGHEZZA \_ MASSIMA**</dt> <dt>23</dt> </dl>                                                   | Lunghezza massima della versione. Ad esempio, *xxxxx*. *xxxxx*. *xxxxx*. *xxxxx*. Nessuno spazio incluso per il carattere di terminazione NULL/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**PACCHETTO \_ VERSIONE \_ LUNGHEZZA \_ MINIMA**</dt> <dt>7</dt> </dl>                                                    | Lunghezza minima della versione. Ad esempio, *x*. *x*. *x*. *x*. Nessuno spazio incluso per il carattere di terminazione NULL.<br/>                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>AppModel.h</dt> </dl> |



 

 





