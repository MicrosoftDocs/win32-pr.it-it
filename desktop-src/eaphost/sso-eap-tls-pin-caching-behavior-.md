---
title: Comportamento del pin EAP-TLS Caching SSO
description: Fornisce un approccio passo per passo per risolvere gli aspetti relativi alla ripresa della sessione e alla ria autenticazione di un utente in roaming in un ambiente SSO EAP-TLS.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bc8cb112a6def55085cbd0b94068407320e4116a4b0161d7d923319257258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085885"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamento del pin EAP-TLS Caching SSO

Questo argomento fornisce un approccio passo per passo per risolvere gli aspetti relativi alla ripresa della sessione e alla ria autenticazione di un utente in roaming in un ambiente SSO EAP-TLS.

## <a name="step-by-step-approach"></a>Approccio passo per passo

L'elenco seguente rappresenta un approccio passo per passo per risolvere gli aspetti relativi alla ripresa della sessione e alla ria autenticazione di un utente in roaming in un ambiente SSO EAP-TLS.

-   Dopo la prima autenticazione riuscita in un ambiente SSO con EAP-TLS, il supplicato mantiene tutte le informazioni correlate alle credenziali utente per impostazione predefinita.
    > [!Note]  
    > Anche se soggetto all'implementazione supplicante specifica, è consigliabile che il supplicante manteni l'intera struttura [**EAP \_ CONFIG INPUT \_ FIELD \_ ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) usata per ultima nella chiamata [**di EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) a EAPHost.

     

-   Quando l'utente viene prima in roaming e viene avviata la nuova autenticazione, il supplicato chiama di nuovo [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) con la stessa struttura [**EAP \_ CONFIG INPUT \_ FIELD \_ ARRAY.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) Il supplicant deve anche passare lo stesso BLOB utente mantenuto dopo la prima autenticazione riuscita.
-   EAPHost passa quindi le informazioni nel BLOB dell'utente al metodo EAP.
-   Il metodo EAP aggiorna a sua volta il BLOB dell'utente con i campi delle credenziali, ad esempio il PIN fornito in *pEapConfigInputFieldArray,* e mantiene i valori rimanenti, ad esempio il certificato del server, come nel BLOB dell'utente originale.
-   Dopo aver completato questi passaggi, il supplicante può riprendere l'autenticazione in modo normale chiamando la funzione di run-time [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con questo BLOB utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scenari di EAPHost per l'accesso Single Sign-On](why-eaphost-sso.md)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




