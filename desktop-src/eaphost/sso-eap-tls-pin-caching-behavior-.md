---
title: Comportamento della memorizzazione nella cache del PIN SSO EAP-TLS
description: Fornisce un approccio dettagliato per la risoluzione dei problemi di ripresa della sessione e di riautenticazione di un utente mobile in un ambiente EAP-TLS SSO.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7c4e3058598f98327570fbcd0347cfb84e5825
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104117237"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamento della memorizzazione nella cache del PIN SSO EAP-TLS

In questo argomento viene fornito un approccio dettagliato per la risoluzione dei problemi di ripresa della sessione e di riautenticazione di un utente mobile in un ambiente EAP-TLS SSO.

## <a name="step-by-step-approach"></a>Approccio dettagliato

L'elenco seguente rappresenta un approccio dettagliato per la risoluzione dei problemi di ripresa della sessione e di riautenticazione di un utente comune in un ambiente EAP-TLS SSO.

-   Dopo la prima autenticazione riuscita in un ambiente SSO con EAP-TLS, il supplicant conserva tutte le informazioni relative alle credenziali utente per impostazione predefinita.
    > [!Note]  
    > Anche se soggetto alla particolare implementazione del richiedente, è consigliabile che il richiedente mantenga l'intera struttura della [**\_ matrice di \_ \_ campi di input della configurazione EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) utilizzata per l'ultima volta nella chiamata [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) a EAPHost.

     

-   Quando l'utente si sposta per la prima volta e viene avviata la riautenticazione, il richiedente chiama di nuovo [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) con la stessa struttura della [**matrice di \_ \_ \_ campi di input della configurazione EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) . il richiedente deve anche passare lo stesso BLOB utente mantenuto dopo la prima autenticazione riuscita.
-   EAPHost passa quindi le informazioni nel BLOB utente al metodo EAP.
-   Il metodo EAP aggiorna a sua volta il BLOB utente con i campi delle credenziali, il PIN, ad esempio, fornito in *pEapConfigInputFieldArray*, e mantiene i valori rimanenti, il certificato del server, ad esempio, come nel BLOB utente originale.
-   Una volta completati questi passaggi, il richiedente può riprendere l'autenticazione in modo normale chiamando la funzione di runtime [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con questo blob utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scenari EAPHost SSO](why-eaphost-sso.md)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




