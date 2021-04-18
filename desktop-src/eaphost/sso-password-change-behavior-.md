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
# <a name="sso-password-change-behavior"></a><span data-ttu-id="feb30-103">Comportamento di modifica della password SSO</span><span class="sxs-lookup"><span data-stu-id="feb30-103">SSO Password Change Behavior</span></span>

<span data-ttu-id="feb30-104">In questo argomento viene fornito un approccio dettagliato per la risoluzione del comportamento di modifica della password SSO.</span><span class="sxs-lookup"><span data-stu-id="feb30-104">This topic provides a step-by-step approach for resolving SSO password change behavior.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="feb30-105">Approccio dettagliato</span><span class="sxs-lookup"><span data-stu-id="feb30-105">Step-By-Step Approach</span></span>

<span data-ttu-id="feb30-106">L'elenco seguente rappresenta un approccio dettagliato per la risoluzione del comportamento di modifica della password SSO.</span><span class="sxs-lookup"><span data-stu-id="feb30-106">The following list represents a step-by-step approach for resolving SSO password change behavior.</span></span>

-   <span data-ttu-id="feb30-107">Una volta che il metodo EAP riceve una notifica relativa a una modifica della password, il metodo notifica a EAPHost; EAPHost a sua volta invia una notifica al supplicante restituendo il codice dell'azione, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="feb30-107">Once the EAP method is notified about a password change, the method notifies EAPHost; EAPHost in turn notifies the supplicant by returning the action code, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="feb30-108">Dopo la ricezione del codice dell'azione [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) da EAPHost, il supplicant ottiene il contesto dell'interfaccia utente dal metodo EAP chiamando la funzione [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) ; EAPHost ottiene quindi il contesto dell'interfaccia utente dal metodo EAP chiamando la funzione del metodo corrispondente</span><span class="sxs-lookup"><span data-stu-id="feb30-108">After receiving the [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) action code from EAPHost, the supplicant obtains the UI context from the EAP method by calling the [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) function; EAPHost then obtains the UI context from the EAP method by calling the corresponding method function</span></span>
-   <span data-ttu-id="feb30-109">Il supplicant passa il contesto dell'interfaccia utente al processo dell'interfaccia utente (usando una forma di comunicazione tra processi).</span><span class="sxs-lookup"><span data-stu-id="feb30-109">The supplicant passes the UI context to the UI process (using some form of inter-process communication).</span></span>
-   <span data-ttu-id="feb30-110">Il processo dell'interfaccia utente chiama [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) in EAPHost.</span><span class="sxs-lookup"><span data-stu-id="feb30-110">The UI process calls [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) on EAPHost.</span></span>
-   <span data-ttu-id="feb30-111">EAPHost raccoglie il contesto dell'interfaccia utente chiamando [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) sul metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="feb30-111">EAPHost collects the UI context by calling [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) on the EAP method.</span></span>
-   <span data-ttu-id="feb30-112">Il metodo EAP fornisce le informazioni sul contesto dell'interfaccia utente necessarie nella struttura [**\_ \_ \_ dei dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , in cui *DwDataType* è impostato su *EapCredExpiryReq* e *pbUiData* punta a una struttura di tipo [**EAP \_ cred \_ req**](eap-cred-req.md).</span><span class="sxs-lookup"><span data-stu-id="feb30-112">The EAP method provides any necessary UI context information in the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, where *dwDataType* is set to *EapCredExpiryReq* and *pbUiData* points to a structure of type [**EAP\_CRED\_REQ**](eap-cred-req.md).</span></span>
-   <span data-ttu-id="feb30-113">Durante il popolamento della struttura [**\_ \_ \_ dei dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , questo metodo EAP compilerà solo il parametro *curCreds* e non imposterà il flag di [**\_ \_ \_ \_ \_ sola lettura \_ del campo di input dell'interfaccia utente EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) nella struttura **\_ \_ \_ \_ dei dati del campo di input della configurazione EAP** .</span><span class="sxs-lookup"><span data-stu-id="feb30-113">While populating the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, this EAP method will only fill in the *curCreds* parameter, and not set the [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag in the **EAP\_CONFIG\_INPUT\_FIELD\_DATA** structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="feb30-114">Il flag di [**\_ \_ \_ \_ \_ sola lettura \_ del campo di input dell'interfaccia utente EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) è per i campi dei membri che devono essere modificati.</span><span class="sxs-lookup"><span data-stu-id="feb30-114">The [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag is for member field(s) which need to be changed.</span></span>

     

-   <span data-ttu-id="feb30-115">Se è stato raccolto il contesto dell'interfaccia utente informazioni, il processo dell'interfaccia utente esegue il rendering di un'interfaccia utente per raccogliere informazioni sulle modifiche della password dall'utente.</span><span class="sxs-lookup"><span data-stu-id="feb30-115">Having collected the UI context informtion, the UI process renders a UI to collect change password information from the user.</span></span> <span data-ttu-id="feb30-116">Queste informazioni vengono popolate nel parametro *NewCreds* della struttura di richiesta di [**scadenza di EAP \_ \_ \_ cred**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .</span><span class="sxs-lookup"><span data-stu-id="feb30-116">This information is populated in the *NewCreds* parameter of the [**EAP\_CRED\_EXPIRY\_REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) structure.</span></span>
-   <span data-ttu-id="feb30-117">Il processo dell'interfaccia utente passa nuovamente la struttura [**EAP \_ \_ creda**](eap-cred-resp.md) a EAPHost tramite [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span><span class="sxs-lookup"><span data-stu-id="feb30-117">The UI process passes the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure back to EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span></span>
-   <span data-ttu-id="feb30-118">Il processo dell'interfaccia utente passa questo BLOB utente al supplicant e il supplicant continua con le funzioni di runtime di EAPHost come di consueto.</span><span class="sxs-lookup"><span data-stu-id="feb30-118">The UI process passes this user BLOB to the supplicant, and the supplicant continues with EAPHost run-time functions as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="feb30-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="feb30-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb30-120">Scenari EAPHost SSO</span><span class="sxs-lookup"><span data-stu-id="feb30-120">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="feb30-121">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="feb30-121">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




