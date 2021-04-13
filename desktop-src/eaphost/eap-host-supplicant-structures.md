---
title: Strutture supplicant EAPHost
description: Informazioni sulle strutture dell'API del richiedente EAPHost, ad esempio la matrice di proprietà del metodo EAP e di EAP \_ cred \_ \_ \_ \_ .
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7121e123fd790a54a95dafb59c080f435ca917
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399711"
---
# <a name="eaphost-supplicant-structures"></a>Strutture supplicant EAPHost

Di seguito sono riportate le strutture dell'API supplicant di EAPHost.



| Struttura                                                                        | Descrizione                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_req creda EAP \_**](eap-cred-req.md)                                           | Contiene le credenziali EAP precedenti e nuove per le operazioni di modifica delle credenziali.                                    |
| [**\_creda \_ EAP**](eap-cred-resp.md)                                         | Contiene le credenziali EAP precedenti e nuove per le operazioni di modifica delle credenziali.                                    |
| [**REQ di scadenza di EAP \_ cred \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Contiene le credenziali EAP precedenti e nuove per le operazioni di scadenza delle credenziali                                     |
| [**la \_ scadenza del credito EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Contiene le credenziali EAP precedenti e nuove per le operazioni di scadenza delle credenziali.                                    |
| [**richiesta di accesso di EAP \_ cred \_ \_**](eap-cred-logon-req.md)                              | Contiene le credenziali EAP per l'autenticazione di rete.                                                                 |
| [**\_ \_ accesso \_ resp EAP**](eap-cred-logon-resp.md)                            | Contiene le credenziali EAP per l'autenticazione di rete.                                                                 |
| [**\_ \_ dati dell'interfaccia utente interattiva EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Contiene le informazioni di configurazione per i componenti interattivi dell'interfaccia utente generati in un supplicant EAP.            |
| [**\_proprietà del metodo EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 o versioni successive: rappresenta una proprietà del metodo.                                                                    |
| [**\_matrice di \_ proprietà del metodo EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 o versioni successive: contiene una matrice di strutture di proprietà del metodo.                                                 |
| [**\_valore della \_ proprietà del metodo EAP \_**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 o versioni successive: contiene un valore della proprietà del metodo.                                                                |
| [**\_valore della proprietà del metodo EAP \_ \_ \_ bool**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 o versioni successive: contiene un valore della proprietà del metodo del tipo di dati BOOL.                                                 |
| [**\_ \_ \_ valore DWORD della proprietà del metodo EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 o versioni successive: contiene un valore della proprietà del metodo con tipo di dati DWORD.                                                |
| [**\_stringa del \_ valore della proprietà del metodo EAP \_ \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 o versioni successive: contiene un valore della proprietà del metodo con tipo di dati String.                                               |
| [**\_informazioni di autenticazione EAPHOST \_**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Descrive le informazioni di autenticazione correnti per le varie fasi del processo di autenticazione EAP.          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Contiene i dati dei risultati generati da EAPHost durante una sessione di autenticazione che viene quindi passata a un metodo EAP. |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 o versioni successive: contiene le informazioni di protezione accesso alla rete (NAP) su un supplicant EAP.                   |



 

 

 