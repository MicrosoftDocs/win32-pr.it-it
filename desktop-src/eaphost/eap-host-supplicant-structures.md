---
title: Strutture supplicant EAPHost
description: Informazioni sulle strutture dell'API Supplicant EAPHost, ad esempio EAP \_ CRED \_ REQ e EAP \_ METHOD PROPERTY \_ \_ ARRAY.
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6703070eabbc571927569f28c39109bbe1eda2f1c70b621982dde3ab4ac3a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904618"
---
# <a name="eaphost-supplicant-structures"></a>Strutture supplicant EAPHost

Le strutture dell'API Supplicant EAPHost sono le seguenti.



| Struttura                                                                        | Descrizione                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                           | Contiene sia le credenziali EAP nuove che le credenziali per le operazioni di modifica delle credenziali.                                    |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                         | Contiene sia le credenziali EAP nuove che le credenziali per le operazioni di modifica delle credenziali.                                    |
| [**EAP \_ CRED \_ EXPIRY \_ REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Contiene sia le credenziali EAP nuove che le credenziali precedente per le operazioni di scadenza delle credenziali                                     |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Contiene sia le credenziali EAP nuove che le credenziali precedente per le operazioni di scadenza delle credenziali.                                    |
| [**EAP \_ CRED \_ LOGON \_ REQ**](eap-cred-logon-req.md)                              | Contiene le credenziali EAP per l'autenticazione di rete.                                                                 |
| [**EAP \_ CRED \_ LOGON \_ RESP**](eap-cred-logon-resp.md)                            | Contiene le credenziali EAP per l'autenticazione di rete.                                                                 |
| [**DATI \_ DELL'INTERFACCIA \_ UTENTE INTERATTIVA EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Contiene informazioni di configurazione per i componenti interattivi dell'interfaccia utente generati in una soluzione EAP flessibile.            |
| [**PROPRIETÀ DEL \_ METODO \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 o versione successiva: rappresenta una proprietà del metodo.                                                                    |
| [**MATRICE DI \_ PROPRIETÀ \_ DEL METODO \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 o versione successiva: contiene una matrice di strutture di proprietà del metodo.                                                 |
| [**VALORE DELLA \_ PROPRIETÀ \_ DEL METODO \_ EAP**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 o versione successiva: contiene un valore della proprietà del metodo.                                                                |
| [**VALORE DELLA PROPRIETÀ DEL METODO EAP \_ \_ \_ \_ BOOL**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 o versione successiva: contiene un valore della proprietà del metodo con tipo di dati BOOL.                                                 |
| [**VALORE DELLA \_ PROPRIETÀ \_ DEL METODO \_ \_ EAP DWORD**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 o versione successiva: contiene un valore della proprietà del metodo del tipo di dati DWORD.                                                |
| [**STRINGA DEL \_ VALORE DELLA PROPRIETÀ DEL \_ \_ METODO \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 o versione successiva: contiene un valore della proprietà del metodo con tipo di dati stringa.                                               |
| [**INFORMAZIONI DI AUTENTICAZIONE \_ \_ EAPHOST**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Descrive le informazioni di autenticazione correnti in diverse fasi del processo di autenticazione EAP.          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Contiene i dati dei risultati generati da EAPHost durante una sessione di autenticazione che viene quindi passata a un metodo EAP. |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 o versione successiva: contiene le informazioni di Protezione accesso alla rete (NAP) su un supplicante EAP.                   |



 

 

 