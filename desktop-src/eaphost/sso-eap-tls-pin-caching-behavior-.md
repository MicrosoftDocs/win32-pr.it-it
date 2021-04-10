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
# <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="80b3d-103">Comportamento della memorizzazione nella cache del PIN SSO EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="80b3d-103">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="80b3d-104">In questo argomento viene fornito un approccio dettagliato per la risoluzione dei problemi di ripresa della sessione e di riautenticazione di un utente mobile in un ambiente EAP-TLS SSO.</span><span class="sxs-lookup"><span data-stu-id="80b3d-104">This topic provides a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="80b3d-105">Approccio dettagliato</span><span class="sxs-lookup"><span data-stu-id="80b3d-105">Step-By-Step Approach</span></span>

<span data-ttu-id="80b3d-106">L'elenco seguente rappresenta un approccio dettagliato per la risoluzione dei problemi di ripresa della sessione e di riautenticazione di un utente comune in un ambiente EAP-TLS SSO.</span><span class="sxs-lookup"><span data-stu-id="80b3d-106">The following list represents a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

-   <span data-ttu-id="80b3d-107">Dopo la prima autenticazione riuscita in un ambiente SSO con EAP-TLS, il supplicant conserva tutte le informazioni relative alle credenziali utente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="80b3d-107">After the first successful authentication in an SSO environment with EAP-TLS, the supplicant retains all user credential related information by default.</span></span>
    > [!Note]  
    > <span data-ttu-id="80b3d-108">Anche se soggetto alla particolare implementazione del richiedente, è consigliabile che il richiedente mantenga l'intera struttura della [**\_ matrice di \_ \_ campi di input della configurazione EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) utilizzata per l'ultima volta nella chiamata [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) a EAPHost.</span><span class="sxs-lookup"><span data-stu-id="80b3d-108">Although subject to the particular supplicant implementation, it's advisable for the supplicant to retain the entire [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure that the supplicant last used in the [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) call to EAPHost.</span></span>

     

-   <span data-ttu-id="80b3d-109">Quando l'utente si sposta per la prima volta e viene avviata la riautenticazione, il richiedente chiama di nuovo [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) con la stessa struttura della [**matrice di \_ \_ \_ campi di input della configurazione EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) . il richiedente deve anche passare lo stesso BLOB utente mantenuto dopo la prima autenticazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="80b3d-109">As the user first roams and the re-authentication begins, the supplicant calls [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) again with the same [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure; the supplicant must also pass in the same user BLOB retained after the first successful authentication.</span></span>
-   <span data-ttu-id="80b3d-110">EAPHost passa quindi le informazioni nel BLOB utente al metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="80b3d-110">EAPHost then passes the information in the user BLOB to the EAP method.</span></span>
-   <span data-ttu-id="80b3d-111">Il metodo EAP aggiorna a sua volta il BLOB utente con i campi delle credenziali, il PIN, ad esempio, fornito in *pEapConfigInputFieldArray*, e mantiene i valori rimanenti, il certificato del server, ad esempio, come nel BLOB utente originale.</span><span class="sxs-lookup"><span data-stu-id="80b3d-111">The EAP method in turn updates the user BLOB with credential fields - the PIN for example - provided in *pEapConfigInputFieldArray*, and keeps the remaining values - the server certificate for example - as it was in the original user BLOB.</span></span>
-   <span data-ttu-id="80b3d-112">Una volta completati questi passaggi, il richiedente può riprendere l'autenticazione in modo normale chiamando la funzione di runtime [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) con questo blob utente.</span><span class="sxs-lookup"><span data-stu-id="80b3d-112">After completing these steps, the supplicant can resume authentication in a normal way by calling the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) run-time function with this user BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80b3d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80b3d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80b3d-114">Scenari EAPHost SSO</span><span class="sxs-lookup"><span data-stu-id="80b3d-114">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="80b3d-115">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="80b3d-115">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




