---
title: Funzioni di configurazione del metodo peer EAPHost
description: Informazioni sulle funzioni di configurazione del metodo peer EAPHost. Visualizzare un elenco delle funzioni di configurazione e visualizzare altre risorse disponibili.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355784647be6c6e13d4110303d544670e80ce09e7f9f99be02b662205e8ead82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785196"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Funzioni di configurazione del metodo peer EAPHost

Le funzioni di configurazione dell'API del metodo peer EAP sono le seguenti.



| Funzione                                                                                                  | Descrizione                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Converte il BLOB di configurazione in XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Converte XML nel BLOB di configurazione.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Converte le credenziali XML in un BLOB.                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Libera tutta la memoria specifica dell'errore EAP restituita dalle API peer EapHost.                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Rilascia tutta la memoria allocata dai parametri OUT del metodo EAP.                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Genera la finestra di dialogo dell'interfaccia utente di configurazione della connessione specifica del metodo EAP nel client.                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Genera una finestra di dialogo dell'interfaccia utente interattiva personalizzata per ottenere informazioni sull'identità utente per il metodo EAP nel client.                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Genera una finestra di dialogo dell'interfaccia utente interattiva personalizzata per il metodo EAP nel client.                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Definisce l'implementazione di una funzione specifica del metodo EAP che ottiene i campi di input delle credenziali Single Sign-On (SSO) EAP per tale metodo EAP                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Definisce l'implementazione di una funzione supplicante EAP che ottiene i campi di input per i componenti interattivi dell'interfaccia utente da generare sul supplicant.                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Converte le informazioni utente in un BLOB utente che può essere utilizzato dalle funzioni di run-time EAPHost.                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Definisce l'implementazione di una funzione specifica del metodo EAP che genera un BLOB di credenziali utente EAP da una [**struttura EAP \_ CONFIG INPUT \_ FIELD \_ \_ ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) che contiene i dati delle credenziali forniti da un utente supplicato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di Run-Time peer EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




