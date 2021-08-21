---
title: Panoramica dell'API SSO EAPHost
description: Fornisce una panoramica delle API EAPHost che supportano l'accesso Single Sign-On (SSO).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a38c6dd35dd2506f8aa26412b09db0f9c9951241bd0f017ed5e55d7f5484b86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085875"
---
# <a name="sso-eaphost-api-overview"></a>Panoramica dell'API SSO EAPHost

Questo argomento offre una panoramica delle API EAPHost che supportano l'accesso Single Sign-On (SSO). Per scenari SSO specifici, vedere [Scenari SSO EAPHost](why-eaphost-sso.md).

## <a name="eaphost-enumerations"></a>Enumerazioni EAPHost

Le enumerazioni seguenti supportano l'accesso SSO.



| Nome                                                                    | Scopo                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**TIPO DI CAMPO \_ \_ DI INPUT \_ EAP CONFIG \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Definisce un set di possibili tipi di campo di input disponibili durante l'esecuzione di query per le credenziali utente.    |
| [**TIPO DI DATI \_ \_ DELL'INTERFACCIA \_ UTENTE INTERATTIVA \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Specifica i tipi di dati interattivi del contesto dell'interfaccia utente forniti a determinate chiamate API supplicanti. |



 

## <a name="eaphost-structures"></a>Strutture EAPHost

Le strutture di dati seguenti supportano l'accesso SSO.



| Nome                                                                     | Scopo                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATI DEI CAMPI \_ \_ DI INPUT \_ EAP CONFIG \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene i dati associati a un singolo campo di input.                                                                                                                         |
| [**MATRICE DI \_ CAMPI \_ DI INPUT \_ EAP CONFIG \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un set di [**strutture EAP \_ CONFIG INPUT \_ FIELD \_ \_ DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) che contengono collettivamente i dati dei campi di input utente ottenuti dall'utente. |
| [**DATI \_ DELL'INTERFACCIA \_ UTENTE INTERATTIVA EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Contiene informazioni di configurazione per i componenti interattivi dell'interfaccia utente generati in un supplicant EAP.                                                                                   |
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                   | Contiene sia le credenziali EAP vecchie che le nuove per le operazioni di modifica delle credenziali.                                                                                               |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                 | Contiene sia le credenziali EAP vecchie che le nuove per le operazioni di modifica delle credenziali.                                                                                               |
| [**EAP \_ CRED \_ EXPIRY \_ REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Contiene sia le credenziali EAP vecchie che le nuove per le operazioni di scadenza delle credenziali.                                                                                                 |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Contiene sia le credenziali EAP vecchie che le nuove per le operazioni di scadenza delle credenziali.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>API peer EAPHost (supplicant)

Le funzioni supplicant seguenti supportano l'accesso SSO.

Le [**funzioni EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) e [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) sono esclusive dell'accesso SSO.



| Nome                                                                                                             | Scopo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Ordine chiamato |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Ottiene i campi di input per i componenti interattivi dell'interfaccia utente da creare nel supplicant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Consente all'utente di determinare il tipo di credenziali richieste dai metodi per eseguire l'autenticazione in uno scenario SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Converte le informazioni utente in un BLOB utente che può essere utilizzato dalle funzioni di run-time EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Ottiene un BLOB di credenziali che può essere usato per avviare l'autenticazione dall'input dell'utente ricevuto dall'interfaccia utente SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | Il supplicant usa il flag **EAP \_ FLAG PRE \_ \_ LOGON** per indicare che EAPHost deve fornire l'accesso SSO. Se viene restituito il codice di azione [EapHostPeerResponseInvokeUI,](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) EAPHost chiama [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)e quindi [**chiama EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Se il codice di azione [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) non viene restituito, EAPHost procede con la normale sequenza di chiamate non SSO. Per altre informazioni, vedere [Sequenza di chiamate api supplicant.](supplicant-api-call-sequence.md)<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>API del metodo peer EAPHost

Le funzioni peer seguenti supportano l'accesso SSO.

Le [**funzioni EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) e [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) sono esclusive dell'accesso SSO.



| Nome                                                                                                      | Scopo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Ordine chiamato |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Definisce l'implementazione di un'API del metodo EAP che fornisce i campi di input per i componenti interattivi dell'interfaccia utente da creare nel supplicant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Definisce l'implementazione di una funzione specifica del metodo EAP che ottiene i campi di input delle credenziali SSO EAP per tale metodo EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Converte le informazioni utente in un BLOB utente che può essere utilizzato dalle funzioni di run-time EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Definisce l'implementazione di una funzione del metodo EAP che ottiene i dati BLOB utente forniti dall'interfaccia utente SSO interattiva generata sul supplicant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | Il flag **PRE LOGON flag EAP \_ FLAG \_ \_** indica che EAPHost deve fornire l'accesso SSO. In uno scenario SSO se viene restituito il codice di azione **EapPeerResponseInvokeUI,** EAPHost chiama [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)e quindi [**chiama EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Se il codice di azione **EapPeerResponseInvokeUI** non viene restituito, EAPHost procede con la normale sequenza di chiamate non SSO. Per altre informazioni, vedere Sequenza di [chiamate API del metodo peer](peer-method-api-call-sequence.md).<br/> | 3            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Scenari EAPHost per l'accesso Single Sign-On](why-eaphost-sso.md)
</dt> </dl>

 

