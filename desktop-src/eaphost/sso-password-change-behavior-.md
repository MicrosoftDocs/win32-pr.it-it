---
title: Comportamento di modifica della password SSO
description: Fornisce un approccio dettagliata per la risoluzione del comportamento di modifica della password SSO.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d438dd41466809805f159fde4a2db698d11b1f7899e48e1f96ccce2c811111cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042799"
---
# <a name="sso-password-change-behavior"></a>Comportamento di modifica della password SSO

In questo argomento viene fornito un approccio dettagliata per la risoluzione del comportamento di modifica della password SSO.

## <a name="step-by-step-approach"></a>Approccio step-by-step

L'elenco seguente rappresenta un approccio step-by-step per la risoluzione del comportamento di modifica della password SSO.

-   Dopo che il metodo EAP ha notificato una modifica della password, il metodo invia una notifica a EAPHost. EAPHost a sua volta notifica al supplicant la restituzione del codice di [azione, EapHostPeerResponseInvokeUI.](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)
-   Dopo aver ricevuto il codice di azione [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) da EAPHost, il supplicante ottiene il contesto dell'interfaccia utente dal metodo EAP chiamando la [**funzione EapHostPeerGetUIContext.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) EAPHost ottiene quindi il contesto dell'interfaccia utente dal metodo EAP chiamando la funzione del metodo corrispondente
-   Il supplicant passa il contesto dell'interfaccia utente al processo dell'interfaccia utente (usando una qualche forma di comunicazione tra processi).
-   Il processo dell'interfaccia [**utente chiama EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) in EAPHost.
-   EAPHost raccoglie il contesto dell'interfaccia utente chiamando [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) nel metodo EAP.
-   Il metodo EAP fornisce tutte le informazioni necessarie sul contesto dell'interfaccia utente nella struttura [**EAP \_ INTERACTIVE UI \_ \_ DATA,**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) in cui *dwDataType* è impostato su *EapCredExpiryReq* e *pbUiData* punta a una struttura di tipo [**EAP \_ CRED \_ REQ.**](eap-cred-req.md)
-   Durante il popolamento della struttura [**EAP \_ INTERACTIVE UI \_ \_ DATA,**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) questo metodo EAP compila solo il parametro *curCreds* e non imposta il flag [**EAP UI INPUT FIELD \_ \_ \_ \_ \_ PROPS READ \_ ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) nella struttura **EAP CONFIG INPUT FIELD \_ \_ \_ \_ DATA.**
    > [!Note]  
    > Il flag [**EAP \_ INPUT FIELD \_ \_ \_ PROPS READ \_ \_ ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) dell'interfaccia utente è per i campi membro che devono essere modificati.

     

-   Dopo aver raccolto le informazioni sul contesto dell'interfaccia utente, il processo dell'interfaccia utente esegue il rendering di un'interfaccia utente per raccogliere le informazioni sulla modifica della password dall'utente. Queste informazioni vengono popolate nel *parametro NewCreds* della [**struttura EAP \_ CRED \_ EXPIRY \_ REQ.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
-   Il processo dell'interfaccia utente passa la struttura [**EAP \_ CRED \_ RESP**](eap-cred-resp.md) a EAPHost tramite [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).
-   Il processo dell'interfaccia utente passa questo BLOB utente al supplicant e il supplicant continua con le funzioni di run-time EAPHost come di consueto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scenari EAPHost per l'accesso Single Sign-On](why-eaphost-sso.md)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




