---
title: Comportamento di modifica della password SSO
description: Fornisce un approccio dettagliato per la risoluzione del comportamento di modifica della password SSO.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299291"
---
# <a name="sso-password-change-behavior"></a>Comportamento di modifica della password SSO

In questo argomento viene fornito un approccio dettagliato per la risoluzione del comportamento di modifica della password SSO.

## <a name="step-by-step-approach"></a>Approccio dettagliato

L'elenco seguente rappresenta un approccio dettagliato per la risoluzione del comportamento di modifica della password SSO.

-   Una volta che il metodo EAP riceve una notifica relativa a una modifica della password, il metodo notifica a EAPHost; EAPHost a sua volta invia una notifica al supplicante restituendo il codice dell'azione, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   Dopo la ricezione del codice dell'azione [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) da EAPHost, il supplicant ottiene il contesto dell'interfaccia utente dal metodo EAP chiamando la funzione [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) ; EAPHost ottiene quindi il contesto dell'interfaccia utente dal metodo EAP chiamando la funzione del metodo corrispondente
-   Il supplicant passa il contesto dell'interfaccia utente al processo dell'interfaccia utente (usando una forma di comunicazione tra processi).
-   Il processo dell'interfaccia utente chiama [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) in EAPHost.
-   EAPHost raccoglie il contesto dell'interfaccia utente chiamando [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) sul metodo EAP.
-   Il metodo EAP fornisce le informazioni sul contesto dell'interfaccia utente necessarie nella struttura [**\_ \_ \_ dei dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , in cui *DwDataType* è impostato su *EapCredExpiryReq* e *pbUiData* punta a una struttura di tipo [**EAP \_ cred \_ req**](eap-cred-req.md).
-   Durante il popolamento della struttura [**\_ \_ \_ dei dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , questo metodo EAP compilerà solo il parametro *curCreds* e non imposterà il flag di [**\_ \_ \_ \_ \_ sola lettura \_ del campo di input dell'interfaccia utente EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) nella struttura **\_ \_ \_ \_ dei dati del campo di input della configurazione EAP** .
    > [!Note]  
    > Il flag di [**\_ \_ \_ \_ \_ sola lettura \_ del campo di input dell'interfaccia utente EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) è per i campi dei membri che devono essere modificati.

     

-   Se è stato raccolto il contesto dell'interfaccia utente informazioni, il processo dell'interfaccia utente esegue il rendering di un'interfaccia utente per raccogliere informazioni sulle modifiche della password dall'utente. Queste informazioni vengono popolate nel parametro *NewCreds* della struttura di richiesta di [**scadenza di EAP \_ \_ \_ cred**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .
-   Il processo dell'interfaccia utente passa nuovamente la struttura [**EAP \_ \_ creda**](eap-cred-resp.md) a EAPHost tramite [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).
-   Il processo dell'interfaccia utente passa questo BLOB utente al supplicant e il supplicant continua con le funzioni di runtime di EAPHost come di consueto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scenari EAPHost SSO](why-eaphost-sso.md)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




