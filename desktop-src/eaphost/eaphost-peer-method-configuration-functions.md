---
title: Funzioni di configurazione del metodo peer EAPHost
description: Informazioni sulle funzioni di configurazione del metodo peer EAPHost. Vedere un elenco delle funzioni di configurazione e visualizzare altre risorse disponibili.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3081f8a54482c48c7c506a25bfaf7f18cf3193ff
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300460"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Funzioni di configurazione del metodo peer EAPHost

Di seguito sono riportate le funzioni di configurazione dell'API del metodo peer EAP.



| Funzione                                                                                                  | Descrizione                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Converte il BLOB di configurazione in XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Converte il codice XML nel BLOB di configurazione.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Converte le credenziali XML in un BLOB.                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Libera tutta la memoria specifica dell'errore EAP restituita dalle API peer EapHost.                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Rilascia tutta la memoria allocata dai parametri OUT del metodo EAP.                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Genera la finestra di dialogo dell'interfaccia utente di configurazione della connessione specifica del metodo EAP nel client.                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Genera una finestra di dialogo personalizzata dell'interfaccia utente interattiva per ottenere informazioni sull'identità utente per il metodo EAP nel client.                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Genera una finestra di dialogo personalizzata dell'interfaccia utente interattiva per il metodo EAP nel client.                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Definisce l'implementazione di una funzione specifica del metodo EAP che ottiene i campi di input delle credenziali Single Sign-on (SSO) EAP per il metodo EAP                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Definisce l'implementazione di una funzione di supplicant EAP che ottiene i campi di input per i componenti interattivi dell'interfaccia utente da generare sul supplicante.                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Converte le informazioni utente in un BLOB utente che può essere utilizzato dalle funzioni di runtime EAPHost.                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Definisce l'implementazione di una funzione specifica del metodo EAP che genera un BLOB di credenziali utente EAP da una struttura di [**matrice di campi di \_ input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) che contiene i dati delle credenziali forniti da un utente del richiedente. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di Run-Time del metodo peer EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




