---
title: Panoramica dell'API EAPHost SSO
description: Viene fornita una panoramica delle API EAPHost che supportano l'accesso Single Sign-on (SSO).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c047205946293c2116c1ab3537ad4d9250857d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046695"
---
# <a name="sso-eaphost-api-overview"></a>Panoramica dell'API EAPHost SSO

Questo argomento fornisce una panoramica delle API EAPHost che supportano l'accesso Single Sign-on (SSO). Per scenari SSO specifici, vedere [scenari EAPHost SSO](why-eaphost-sso.md).

## <a name="eaphost-enumerations"></a>Enumerazioni EAPHost

Le enumerazioni seguenti supportano SSO.



| Nome                                                                    | Scopo                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_tipo di \_ campo di input configurazione \_ EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Definisce un set di possibili tipi di campi di input disponibili quando si eseguono query per le credenziali utente.    |
| [**\_tipo di \_ dati dell'interfaccia utente interattiva EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Specifica i tipi di dati di contesto dell'interfaccia utente interattiva forniti a determinate chiamate API supplicant. |



 

## <a name="eaphost-structures"></a>Strutture EAPHost

Le strutture di dati seguenti supportano SSO.



| Nome                                                                     | Scopo                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_dati del \_ campo di input configurazione \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene i dati associati a un singolo campo di input.                                                                                                                         |
| [**\_matrice di \_ campi di input configurazione \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un set di strutture di [**dati del campo di \_ input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) che contengono collettivamente i dati del campo di input dell'utente ottenuti dall'utente. |
| [**\_ \_ dati dell'interfaccia utente interattiva EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Contiene informazioni di configurazione per i componenti dell'interfaccia utente interattivi generati in un supplicant EAP.                                                                                   |
| [**\_req creda EAP \_**](eap-cred-req.md)                                   | Contiene le credenziali EAP precedenti e nuove per le operazioni di modifica delle credenziali.                                                                                               |
| [**\_creda \_ EAP**](eap-cred-resp.md)                                 | Contiene le credenziali EAP precedenti e nuove per le operazioni di modifica delle credenziali.                                                                                               |
| [**REQ di scadenza di EAP \_ cred \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Contiene le credenziali EAP precedenti e nuove per le operazioni di scadenza delle credenziali.                                                                                                 |
| [**la \_ scadenza del credito EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Contiene le credenziali EAP precedenti e nuove per le operazioni di scadenza delle credenziali.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>API del peer EAPHost (supplicant)

Le funzioni supplicant seguenti supportano SSO.

Le funzioni [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) e [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) sono esclusive per SSO.



| Nome                                                                                                             | Scopo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Ordine chiamato |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Ottiene i campi di input per i componenti dell'interfaccia utente interattivi da generare nel supplicar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Consente all'utente di determinare il tipo di credenziali richieste dai metodi per eseguire l'autenticazione in uno scenario SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Converte le informazioni utente in un BLOB utente che può essere utilizzato dalle funzioni di runtime EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Ottiene un BLOB di credenziali che può essere utilizzato per avviare l'autenticazione dall'input dell'utente ricevuto dall'interfaccia utente SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | Il richiedente usa il flag **EAP \_ pre- \_ \_ Logon** flag per indicare che EAPHost deve fornire SSO. Se viene restituito il codice di azione [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) , EAPHost chiama [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)e quindi chiama [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Se il codice dell'azione [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) non viene restituito, EAPHost procede con la sequenza di chiamate normale non SSO. Per ulteriori informazioni, vedere [sequenza di chiamate API supplicant](supplicant-api-call-sequence.md).<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>API del metodo peer EAPHost

Le funzioni peer seguenti supportano SSO.

Le funzioni [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) e [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) sono esclusive per SSO.



| Nome                                                                                                      | Scopo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Ordine chiamato |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Definisce l'implementazione di un'API del metodo EAP che fornisce i campi di input per i componenti dell'interfaccia utente interattivi da generare nel supplicant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Definisce l'implementazione di una funzione specifica del metodo EAP che ottiene i campi di input delle credenziali SSO EAP per il metodo EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Converte le informazioni utente in un BLOB utente che può essere utilizzato dalle funzioni di runtime EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Definisce l'implementazione di una funzione del metodo EAP che ottiene i dati BLOB utente forniti dall'interfaccia utente interattiva Interactive SSO generata sul supplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | Il flag di **\_ pre- \_ \_ accesso del flag EAP** indica che EAPHost deve fornire SSO. In uno scenario SSO se viene restituito il codice di azione **EapPeerResponseInvokeUI** , EAPHost chiama [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)e quindi chiama [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Se il codice dell'azione **EapPeerResponseInvokeUI** non viene restituito, EAPHost procede con la sequenza di chiamate normale non SSO. Per ulteriori informazioni, vedere [sequenza di chiamate API del metodo peer](peer-method-api-call-sequence.md).<br/> | 3            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Scenari EAPHost SSO](why-eaphost-sso.md)
</dt> </dl>

 

