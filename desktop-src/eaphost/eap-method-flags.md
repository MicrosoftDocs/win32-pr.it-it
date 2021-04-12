---
title: Flag del metodo EAP (Eaptypes. h)
description: I flag del metodo EAP vengono utilizzati all'interno delle funzioni di supplicant, Authenticator e peer per specificare i comportamenti di una sessione di autenticazione EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475022"
---
# <a name="eap-method-flags"></a><span data-ttu-id="06c6e-103">Flag del metodo EAP</span><span class="sxs-lookup"><span data-stu-id="06c6e-103">EAP Method Flags</span></span>

<span data-ttu-id="06c6e-104">I flag del metodo EAP vengono utilizzati all'interno delle funzioni di supplicant, Authenticator e peer per specificare i comportamenti di una sessione di autenticazione EAP.</span><span class="sxs-lookup"><span data-stu-id="06c6e-104">The EAP method flags are used within the supplicant, authenticator, and peer functions to specify behaviors of an EAP authentication session.</span></span>

<dl> <dt>

<span data-ttu-id="06c6e-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Flag EAP \_ Reserved1**</span><span class="sxs-lookup"><span data-stu-id="06c6e-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP\_FLAG\_Reserved1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="06c6e-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-107">Non usare.</span><span class="sxs-lookup"><span data-stu-id="06c6e-107">Do not use.</span></span> <span data-ttu-id="06c6e-108">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="06c6e-108">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**\_flag EAP \_ non \_ interattivo**</span><span class="sxs-lookup"><span data-stu-id="06c6e-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP\_FLAG\_NON\_INTERACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="06c6e-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-111">Non visualizzare un'interfaccia utente (UI).</span><span class="sxs-lookup"><span data-stu-id="06c6e-111">Do not display a user interface (UI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**\_accesso al flag EAP \_**</span><span class="sxs-lookup"><span data-stu-id="06c6e-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP\_FLAG\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-113">0x00000004</span><span class="sxs-lookup"><span data-stu-id="06c6e-113">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-114">I dati utente sono stati ottenuti dall'accesso di Windows.</span><span class="sxs-lookup"><span data-stu-id="06c6e-114">User data was obtained from Windows logon.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**\_anteprima del flag EAP \_**</span><span class="sxs-lookup"><span data-stu-id="06c6e-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP\_FLAG\_PREVIEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-116">0x00000008</span><span class="sxs-lookup"><span data-stu-id="06c6e-116">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-117">Mostra l'interfaccia utente delle credenziali prima di eseguire l'autenticazione, anche se sono presenti credenziali memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="06c6e-117">Show credentials UI before authenticating, even if cached credentials are present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ FLAG \_ Reserved2**</span><span class="sxs-lookup"><span data-stu-id="06c6e-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span> **EAP\_FLAG\_Reserved2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06c6e-119">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-120">Non usare.</span><span class="sxs-lookup"><span data-stu-id="06c6e-120">Do not use.</span></span> <span data-ttu-id="06c6e-121">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="06c6e-121">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**\_ \_ autenticazione computer del flag EAP \_**</span><span class="sxs-lookup"><span data-stu-id="06c6e-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP\_FLAG\_MACHINE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-123">0x00000020</span><span class="sxs-lookup"><span data-stu-id="06c6e-123">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-124">Usa autenticazione a livello di computer; la mancata impostazione di questo flag indica che è in uso l'autenticazione a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="06c6e-124">Use machine level authentication; not setting this flag indicates user level authentication is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**\_ \_ accesso Guest del flag EAP \_**</span><span class="sxs-lookup"><span data-stu-id="06c6e-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP\_FLAG\_GUEST\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="06c6e-126">0x00000040</span><span class="sxs-lookup"><span data-stu-id="06c6e-126">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-127">Indica una richiesta di fornire l'accesso guest.</span><span class="sxs-lookup"><span data-stu-id="06c6e-127">Indicates a request to provide guest access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Flag EAP \_ Reserved3**</span><span class="sxs-lookup"><span data-stu-id="06c6e-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP\_FLAG\_Reserved3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-129">0x00000080</span><span class="sxs-lookup"><span data-stu-id="06c6e-129">0x00000080</span></span> 
</dt> <dt>



<span data-ttu-id="06c6e-130">Non usare.</span><span class="sxs-lookup"><span data-stu-id="06c6e-130">Do not use.</span></span> <span data-ttu-id="06c6e-131">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="06c6e-131">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ FLAG \_ Reserved4**</span><span class="sxs-lookup"><span data-stu-id="06c6e-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span> **EAP\_FLAG\_Reserved4**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-133">0x00000100</span><span class="sxs-lookup"><span data-stu-id="06c6e-133">0x00000100</span></span> 
</dt> <dt>



<span data-ttu-id="06c6e-134">Non usare.</span><span class="sxs-lookup"><span data-stu-id="06c6e-134">Do not use.</span></span> <span data-ttu-id="06c6e-135">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="06c6e-135">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**il \_ flag EAP \_ riprende \_ dalla modalità di \_ ibernazione**</span><span class="sxs-lookup"><span data-stu-id="06c6e-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP\_FLAG\_RESUME\_FROM\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-137">0x00000200</span><span class="sxs-lookup"><span data-stu-id="06c6e-137">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-138">Indica che si tratta della prima chiamata dopo che l'attività del computer è stata ripresa da un periodo di ibernazione.</span><span class="sxs-lookup"><span data-stu-id="06c6e-138">Indicates this is the first call after machine activity has resumed from a period of hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ FLAG \_ Reserved5**</span><span class="sxs-lookup"><span data-stu-id="06c6e-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span> **EAP\_FLAG\_Reserved5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-140">0x00000400</span><span class="sxs-lookup"><span data-stu-id="06c6e-140">0x00000400</span></span> 
</dt> <dt>



<span data-ttu-id="06c6e-141">Non usare.</span><span class="sxs-lookup"><span data-stu-id="06c6e-141">Do not use.</span></span> <span data-ttu-id="06c6e-142">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="06c6e-142">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Flag EAP \_ Reserved6**</span><span class="sxs-lookup"><span data-stu-id="06c6e-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP\_FLAG\_Reserved6**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-144">0x00000800</span><span class="sxs-lookup"><span data-stu-id="06c6e-144">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-145">Non usare.</span><span class="sxs-lookup"><span data-stu-id="06c6e-145">Do not use.</span></span> <span data-ttu-id="06c6e-146">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="06c6e-146">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_autenticazione del flag EAP \_ completa \_**</span><span class="sxs-lookup"><span data-stu-id="06c6e-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP\_FLAG\_FULL\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-148">0x00001000</span><span class="sxs-lookup"><span data-stu-id="06c6e-148">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-149">Indica che i metodi tunnel devono eseguire un'autenticazione completa anziché una versione abbreviata, ad esempio la [riconnessione rapida PEAP (Protected EAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="06c6e-149">Indicates that tunnel methods should perform a full authentication instead of an abbreviated version, such as [Protected EAP (PEAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**il \_ flag EAP \_ preferisce le \_ \_ credenziali Alt**</span><span class="sxs-lookup"><span data-stu-id="06c6e-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP\_FLAG\_PREFER\_ALT\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="06c6e-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-152">Indica che le credenziali passate a [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) sono preferite per tutte le altre forme di recupero delle credenziali, anche se i dati di configurazione passati nella funzione corrente richiedono una modalità diversa di recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="06c6e-152">Indicates credentials passed into [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) are preferred to all other forms of credential retrieval, even if configuration data passed into the current function requests a different mode of credential retrieval.</span></span>

> [!Note]  
> <span data-ttu-id="06c6e-153">Questo flag viene utilizzato solo da [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="06c6e-153">This flag is only used by [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Flag EAP \_ Reserved7**</span><span class="sxs-lookup"><span data-stu-id="06c6e-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP\_FLAG\_Reserved7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-155">0x00004000</span><span class="sxs-lookup"><span data-stu-id="06c6e-155">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-156">Non usare.</span><span class="sxs-lookup"><span data-stu-id="06c6e-156">Do not use.</span></span> <span data-ttu-id="06c6e-157">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="06c6e-157">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**\_ \_ \_ \_ modifica dello stato di integrità del flag peer EAP \_**</span><span class="sxs-lookup"><span data-stu-id="06c6e-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP\_PEER\_FLAG\_HEALTH\_STATE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-159">0x00008000</span><span class="sxs-lookup"><span data-stu-id="06c6e-159">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-160">Indica che la riautenticazione è un callback di [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP); NAP ha avviato la sessione di autenticazione perché lo stato di integrità è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="06c6e-160">Indicates the cause of re-authentication is a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) callback; NAP initiated the authentication session because the health state changed.</span></span> <span data-ttu-id="06c6e-161">Questo flag deve essere inviato solo quando questa funzione viene chiamata da un callback [*NotificationHandler*](/previous-versions/windows/desktop/api) specifico di NAP fornito da una chiamata precedente a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="06c6e-161">This flag must be sent only when this function is called by a NAP-specific [*NotificationHandler*](/previous-versions/windows/desktop/api) callback provided by a previous call to this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_ \_ interfaccia utente eliminare flag EAP \_**</span><span class="sxs-lookup"><span data-stu-id="06c6e-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP\_FLAG\_SUPRESS\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-163">0x00010000</span><span class="sxs-lookup"><span data-stu-id="06c6e-163">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-164">Continuare l'autenticazione con le informazioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="06c6e-164">Continue authentication with available information.</span></span> <span data-ttu-id="06c6e-165">Se l'autenticazione non può continuare, non riesce.</span><span class="sxs-lookup"><span data-stu-id="06c6e-165">If the authentication cannot proceed then fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_flag EAP \_ pre- \_ accesso**</span><span class="sxs-lookup"><span data-stu-id="06c6e-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP\_FLAG\_PRE\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-167">0x00020000</span><span class="sxs-lookup"><span data-stu-id="06c6e-167">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-168">Indica che EAPHost deve fornire l'accesso Single Sign-on (SSO).</span><span class="sxs-lookup"><span data-stu-id="06c6e-168">Indicates that EAPHost should provide Single-Sign-On (SSO).</span></span> <span data-ttu-id="06c6e-169">Per ulteriori informazioni, vedere [SSO e PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="06c6e-169">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**\_ \_ autenticazione utente del flag EAP \_**</span><span class="sxs-lookup"><span data-stu-id="06c6e-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP\_FLAG\_USER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-171">0x00040000</span><span class="sxs-lookup"><span data-stu-id="06c6e-171">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-172">Indica l'autenticazione a livello di utente per i metodi legacy che non possono impostare l'autenticazione del **\_ computer del flag \_ \_ EAP**.</span><span class="sxs-lookup"><span data-stu-id="06c6e-172">Indicates user level authentication for legacy methods that cannot set **EAP\_FLAG\_MACHINE\_AUTH**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_flag EAP \_ config \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="06c6e-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP\_FLAG\_CONFG\_READONLY**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="06c6e-174">0x00080000</span><span class="sxs-lookup"><span data-stu-id="06c6e-174">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-175">Indica che la configurazione può essere visualizzata ma non aggiornata.</span><span class="sxs-lookup"><span data-stu-id="06c6e-175">Indicates the configuration can be viewed but not updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06c6e-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Flag EAP \_ Reserved8**</span><span class="sxs-lookup"><span data-stu-id="06c6e-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP\_FLAG\_Reserved8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c6e-177">0x00100000</span><span class="sxs-lookup"><span data-stu-id="06c6e-177">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="06c6e-178">Non usare.</span><span class="sxs-lookup"><span data-stu-id="06c6e-178">Do not use.</span></span> <span data-ttu-id="06c6e-179">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="06c6e-179">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06c6e-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06c6e-180">Requirements</span></span>



| <span data-ttu-id="06c6e-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c6e-181">Requirement</span></span> | <span data-ttu-id="06c6e-182">Valore</span><span class="sxs-lookup"><span data-stu-id="06c6e-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06c6e-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c6e-183">Minimum supported client</span></span><br/> | <span data-ttu-id="06c6e-184">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06c6e-184">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06c6e-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c6e-185">Minimum supported server</span></span><br/> | <span data-ttu-id="06c6e-186">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06c6e-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06c6e-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06c6e-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c6e-188"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c6e-188"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c6e-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06c6e-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c6e-190">Costanti EAPHost comuni</span><span class="sxs-lookup"><span data-stu-id="06c6e-190">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

