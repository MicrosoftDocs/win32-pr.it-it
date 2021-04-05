---
title: Costanti di errore e informazioni correlate a EAP (Eaphosterror. h)
description: Singoli gruppi di costanti di errore e informazioni correlate a EAP comuni a tutte le tecnologie API EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048454"
---
# <a name="eap-related-error-and-information-constants"></a><span data-ttu-id="04865-103">Costanti di errore e informazioni correlate a EAP</span><span class="sxs-lookup"><span data-stu-id="04865-103">EAP Related Error and Information Constants</span></span>

<span data-ttu-id="04865-104">Singoli gruppi di costanti di errore e informazioni correlate a EAP comuni a tutte le tecnologie API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="04865-104">Individual groups of EAP related error and information constants common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="04865-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**\_prima EAP E \_ EAPHost \_**</span><span class="sxs-lookup"><span data-stu-id="04865-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP\_E\_EAPHOST\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-106">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="04865-106">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="04865-107">Definisce il limite dei report di errore. si verificherà un errore relativo a EAPHost tra **EAP e \_ \_ EAPHost \_ prima** e **EAP e EAPHost per \_ \_ \_ ultimo**.</span><span class="sxs-lookup"><span data-stu-id="04865-107">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST per \_ ultimi**</span><span class="sxs-lookup"><span data-stu-id="04865-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP\_E\_EAPHOST\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-109">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="04865-109">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="04865-110">Definisce il limite dei report di errore. si verificherà un errore relativo a EAPHost tra **EAP e \_ \_ EAPHost \_ prima** e **EAP e EAPHost per \_ \_ \_ ultimo**.</span><span class="sxs-lookup"><span data-stu-id="04865-110">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHost \_ prima**</span><span class="sxs-lookup"><span data-stu-id="04865-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP\_I\_EAPHOST\_FIRST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-112">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="04865-112">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="04865-113">Definisce il limite dei report informazioni; eventuali registrazioni di eventi informativi correlati a EAPHost si verificheranno **prima tra EAP \_ i \_ EAPHost \_** e **EAP \_ i \_ EAPHost \_**.</span><span class="sxs-lookup"><span data-stu-id="04865-113">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHost per \_ ultimi**</span><span class="sxs-lookup"><span data-stu-id="04865-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP\_I\_EAPHOST\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-115">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="04865-115">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="04865-116">Definisce il limite dei report informazioni; eventuali registrazioni di eventi informativi correlati a EAPHost si verificheranno **prima tra EAP \_ i \_ EAPHost \_** e **EAP \_ i \_ EAPHost \_**.</span><span class="sxs-lookup"><span data-stu-id="04865-116">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_archivio certificati EAP E non \_ \_ \_ accessibile**</span><span class="sxs-lookup"><span data-stu-id="04865-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP\_E\_CERT\_STORE\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-118">0x80420011</span><span class="sxs-lookup"><span data-stu-id="04865-118">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="04865-119">L'autenticatore o il peer non è in grado di accedere all'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="04865-119">Neither the authenticator or peer can access the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_metodo EAP \_ E \_ EAPHost \_ non \_ installato**</span><span class="sxs-lookup"><span data-stu-id="04865-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP\_E\_EAPHOST\_METHOD\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-121">0x80420011</span><span class="sxs-lookup"><span data-stu-id="04865-121">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="04865-122">Il metodo EAP richiesto non è installato.</span><span class="sxs-lookup"><span data-stu-id="04865-122">The requested EAP method is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**\_reimpostazione \_ \_ \_ host metodo thirdparty \_ EAP E EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="04865-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP\_E\_EAPHOST\_THIRDPARTY\_METHOD\_HOST\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-124">0x80420012</span><span class="sxs-lookup"><span data-stu-id="04865-124">0x80420012</span></span>
</dt> <dt>



<span data-ttu-id="04865-125">L'host del metodo di terze parti non risponde ed è stato riavviato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="04865-125">The host of the third party method is not responding and was restarted automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**\_EAPQEC EAP \_ E \_ EAPHOST \_ inaccessibili**</span><span class="sxs-lookup"><span data-stu-id="04865-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP\_E\_EAPHOST\_EAPQEC\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-127">0x80420013</span><span class="sxs-lookup"><span data-stu-id="04865-127">0x80420013</span></span>
</dt> <dt>



<span data-ttu-id="04865-128">EAPHost non è in grado di comunicare con il [client di imposizione di quarantena](/windows/desktop/NAP/nap-client-architecture) EAP (QeC) in un client abilitato per [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span><span class="sxs-lookup"><span data-stu-id="04865-128">EAPHost not able to communicate with EAP [quarantine enforcement client](/windows/desktop/NAP/nap-client-architecture) (QEC) on a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) enabled client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_identità EAP \_ E \_ EAPHOST \_ sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="04865-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP\_E\_EAPHOST\_IDENTITY\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-130">0x80420014</span><span class="sxs-lookup"><span data-stu-id="04865-130">0x80420014</span></span>
</dt> <dt>



<span data-ttu-id="04865-131">EAPHost restituisce questo errore se l'autenticatore non riesce a eseguire l'autenticazione dopo l'invio dell'identità peer.</span><span class="sxs-lookup"><span data-stu-id="04865-131">EAPHost returns this error if the authenticator fails the authentication after the peer identity was submitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_autenticazione EAP \_ E \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="04865-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP\_E\_AUTHENTICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-133">0x80420015</span><span class="sxs-lookup"><span data-stu-id="04865-133">0x80420015</span></span> 
</dt> <dt>



<span data-ttu-id="04865-134">EAPHost restituisce questo errore in caso di errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="04865-134">EAPHost returns this error on authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_ \_ \_ negoziazione EAP EAP EAPHost \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="04865-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP\_I\_EAPHOST\_EAP\_NEGOTIATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-136">0x40420016</span><span class="sxs-lookup"><span data-stu-id="04865-136">0x40420016</span></span>
</dt> <dt>



<span data-ttu-id="04865-137">EAPHost registra questo evento informativo quando il client e il server non sono configurati con tipi EAP compatibili.</span><span class="sxs-lookup"><span data-stu-id="04865-137">EAPHost logs this information event when the client and server aren't configured with compatible EAP types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_ \_ \_ \_ pacchetto non valido nel metodo EAP E EAPHost \_**</span><span class="sxs-lookup"><span data-stu-id="04865-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-139">0x80420017</span><span class="sxs-lookup"><span data-stu-id="04865-139">0x80420017</span></span>
</dt> <dt>



<span data-ttu-id="04865-140">Un metodo EAP ha ricevuto un pacchetto EAP che non può essere elaborato.</span><span class="sxs-lookup"><span data-stu-id="04865-140">An EAP method received an EAP packet that cannot be processed.</span></span> <span data-ttu-id="04865-141">Un altro nome per il **\_ pacchetto EAP E \_ EAPHOST \_ Method \_ non valido \_** è il **\_ \_ \_ pacchetto EAP non valido**.</span><span class="sxs-lookup"><span data-stu-id="04865-141">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_ \_ pacchetto remoto EAP E EAPHost \_ \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="04865-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-143">0x80420018</span><span class="sxs-lookup"><span data-stu-id="04865-143">0x80420018</span></span>
</dt> <dt>



<span data-ttu-id="04865-144">EAPHost ha ricevuto un pacchetto che non può essere elaborato.</span><span class="sxs-lookup"><span data-stu-id="04865-144">EAPHost received a packet that cannot be processed.</span></span> <span data-ttu-id="04865-145">Un altro nome per **EAP \_ E \_ EAPHOST \_ Remote \_ \_ Packet** è un **\_ \_ pacchetto EAP non valido**.</span><span class="sxs-lookup"><span data-stu-id="04865-145">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**\_ \_ formato XML EAP E EAPHost non \_ \_ valido**</span><span class="sxs-lookup"><span data-stu-id="04865-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP\_E\_EAPHOST\_XML\_MALFORMED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-147">0x80420019</span><span class="sxs-lookup"><span data-stu-id="04865-147">0x80420019</span></span>
</dt> <dt>



<span data-ttu-id="04865-148">Convalida dello schema di configurazione EAPHost non riuscita.</span><span class="sxs-lookup"><span data-stu-id="04865-148">The EAPHost configuration schema validation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**\_la configurazione del metodo EAP E non \_ \_ \_ \_ \_ supporta \_ SSO**</span><span class="sxs-lookup"><span data-stu-id="04865-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP\_E\_METHOD\_CONFIG\_DOES\_NOT\_SUPPORT\_SSO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-150">0x8042001A</span><span class="sxs-lookup"><span data-stu-id="04865-150">0x8042001A</span></span>
</dt> <dt>



<span data-ttu-id="04865-151">Windows 7 o versioni successive: il metodo EAP non supporta Single Sign-on (SSO) per la configurazione specificata.</span><span class="sxs-lookup"><span data-stu-id="04865-151">Windows 7 or later: The EAP method does not support single sign on (SSO) for the provided configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_operazione del metodo EAP E \_ EAPHost \_ \_ \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="04865-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**EAP\_E\_EAPHOST\_METHOD\_OPERATION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-153">0x80420020</span><span class="sxs-lookup"><span data-stu-id="04865-153">0x80420020</span></span>
</dt> <dt>



<span data-ttu-id="04865-154">EAPHost restituisce questo errore quando un metodo EAP configurato non supporta un'operazione richiesta (chiamata di procedura).</span><span class="sxs-lookup"><span data-stu-id="04865-154">EAPHost returns this error when a configured EAP method does not support a requested operation (procedure call).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**\_ \_ prima utente EAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="04865-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP\_E\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-156">0x80420100L</span><span class="sxs-lookup"><span data-stu-id="04865-156">0x80420100L</span></span>
</dt> <dt>



<span data-ttu-id="04865-157">Definisce il limite dei report di errore. si verificherà un errore correlato all'utente tra il **\_ \_ \_ primo utente** e EAP e **\_ \_ \_ l'** utente.</span><span class="sxs-lookup"><span data-stu-id="04865-157">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**\_ \_ ultimo utente EAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="04865-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP\_E\_USER\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-159">0x804201FFL</span><span class="sxs-lookup"><span data-stu-id="04865-159">0x804201FFL</span></span>
</dt> <dt>



<span data-ttu-id="04865-160">Definisce il limite dei report di errore. si verificherà un errore correlato all'utente tra il **\_ \_ \_ primo utente** e EAP e **\_ \_ \_ l'** utente.</span><span class="sxs-lookup"><span data-stu-id="04865-160">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**\_ \_ prima utente EAP \_ I**</span><span class="sxs-lookup"><span data-stu-id="04865-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP\_I\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-162">0x40420100L</span><span class="sxs-lookup"><span data-stu-id="04865-162">0x40420100L</span></span>
</dt> <dt>



<span data-ttu-id="04865-163">Definisce il limite dei report informazioni; eventuali registrazioni di eventi informativi correlati a EAP si verificheranno tra l' **\_ \_ utente EAP \_ prima** e **\_ \_ \_ l'ultimo utente EAP i**.</span><span class="sxs-lookup"><span data-stu-id="04865-163">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**\_ \_ ultimo utente EAP \_ I**</span><span class="sxs-lookup"><span data-stu-id="04865-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP\_I\_USER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-165">0x404201FFL</span><span class="sxs-lookup"><span data-stu-id="04865-165">0x404201FFL</span></span>
</dt> <dt>



<span data-ttu-id="04865-166">Definisce il limite dei report informazioni; eventuali registrazioni di eventi informativi correlati a EAP si verificheranno tra l' **\_ \_ utente EAP \_ prima** e **\_ \_ \_ l'ultimo utente EAP i**.</span><span class="sxs-lookup"><span data-stu-id="04865-166">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_ \_ certificato utente EAP \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="04865-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP\_E\_USER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-168">0x80420100</span><span class="sxs-lookup"><span data-stu-id="04865-168">0x80420100</span></span>
</dt> <dt>



<span data-ttu-id="04865-169">EAPHost non è riuscito a trovare un certificato utente per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="04865-169">EAPHost could not find a user certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**\_ \_ certificato utente EAP \_ E \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="04865-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP\_E\_USER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-171">0x80420101</span><span class="sxs-lookup"><span data-stu-id="04865-171">0x80420101</span></span>
</dt> <dt>



<span data-ttu-id="04865-172">Per il certificato utente utilizzato per l'autenticazione non è impostato l'utilizzo chiavi avanzato (EKU) appropriato.</span><span class="sxs-lookup"><span data-stu-id="04865-172">The user certificate being user for authentication does not have proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**\_ \_ certificato utente EAP \_ E \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="04865-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP\_E\_USER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-174">0x80420102</span><span class="sxs-lookup"><span data-stu-id="04865-174">0x80420102</span></span>
</dt> <dt>



<span data-ttu-id="04865-175">EAPhost ha rilevato un certificato utente scaduto.</span><span class="sxs-lookup"><span data-stu-id="04865-175">EAPhost found an expired user certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**\_ \_ certificato utente EAP \_ E \_ revocato**</span><span class="sxs-lookup"><span data-stu-id="04865-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP\_E\_USER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-177">0x80420103</span><span class="sxs-lookup"><span data-stu-id="04865-177">0x80420103</span></span>
</dt> <dt>



<span data-ttu-id="04865-178">Il certificato utente usato per l'autenticazione è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="04865-178">The user certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_errore del \_ \_ certificato utente \_ EAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="04865-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP\_E\_USER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-180">0x80420104</span><span class="sxs-lookup"><span data-stu-id="04865-180">0x80420104</span></span>
</dt> <dt>



<span data-ttu-id="04865-181">Si è verificato un errore sconosciuto con la certificazione utente utilizzata per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="04865-181">An unknown error occurred with the user certification being used for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**\_ \_ certificato utente EAP \_ E \_ rifiutato**</span><span class="sxs-lookup"><span data-stu-id="04865-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP\_E\_USER\_CERT\_REJECTED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-183">0x80420105</span><span class="sxs-lookup"><span data-stu-id="04865-183">0x80420105</span></span>
</dt> <dt>



<span data-ttu-id="04865-184">L'autenticatore ha rifiutato la certificazione utente.</span><span class="sxs-lookup"><span data-stu-id="04865-184">The authenticator rejected the user certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**\_ \_ \_ errore dell'account utente \_ EAP I \_**</span><span class="sxs-lookup"><span data-stu-id="04865-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP\_I\_USER\_ACCOUNT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-186">0x40420110</span><span class="sxs-lookup"><span data-stu-id="04865-186">0x40420110</span></span>
</dt> <dt>



<span data-ttu-id="04865-187">Si è verificato un errore EAP dopo uno scambio di identità, che indica la probabilità di un problema con l'account dell'utente che esegue l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="04865-187">An EAP failure was received after an identity exchange, indicating the likelihood of a problem with the authenticating user's account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_ \_ credenziali utente EAP \_ E \_ rifiutate**</span><span class="sxs-lookup"><span data-stu-id="04865-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP\_E\_USER\_CREDENTIALS\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-189">0x80420111</span><span class="sxs-lookup"><span data-stu-id="04865-189">0x80420111</span></span>
</dt> <dt>



<span data-ttu-id="04865-190">L'autenticatore ha rifiutato le credenziali utente per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="04865-190">The authenticator rejected user credentials for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**\_ \_ password nome utente EAP E \_ \_ \_ rifiutata**</span><span class="sxs-lookup"><span data-stu-id="04865-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**EAP\_E\_USER\_NAME\_PASSWORD\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-192">0x80420112</span><span class="sxs-lookup"><span data-stu-id="04865-192">0x80420112</span></span>
</dt> <dt>



<span data-ttu-id="04865-193">Windows 7 o versioni successive: autenticazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="04865-193">Windows 7 or later: Authentication failed.</span></span> <span data-ttu-id="04865-194">L'autenticatore ha rifiutato le credenziali utente.</span><span class="sxs-lookup"><span data-stu-id="04865-194">The authenticator rejected the user credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ nessun \_ lettore di Smart \_ card \_**</span><span class="sxs-lookup"><span data-stu-id="04865-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP\_E\_NO\_SMART\_CARD\_READER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-196">0x80420113</span><span class="sxs-lookup"><span data-stu-id="04865-196">0x80420113</span></span>
</dt> <dt>



<span data-ttu-id="04865-197">Windows 7 o versioni successive: non è stato trovato alcun lettore di smart card.</span><span class="sxs-lookup"><span data-stu-id="04865-197">Windows 7 or later: No smart card reader found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**\_server EAP \_ E \_ prima**</span><span class="sxs-lookup"><span data-stu-id="04865-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP\_E\_SERVER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-199">0x80420200L</span><span class="sxs-lookup"><span data-stu-id="04865-199">0x80420200L</span></span>
</dt> <dt>



<span data-ttu-id="04865-200">Definisce il limite dei report di errore. si verificherà un errore relativo al server tra il **\_ \_ \_ primo** e il server EAP e il server per **\_ \_ \_ ultimo**.</span><span class="sxs-lookup"><span data-stu-id="04865-200">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**\_ \_ ultimo server EAP \_ E**</span><span class="sxs-lookup"><span data-stu-id="04865-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP\_E\_SERVER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-202">0x804202FFL</span><span class="sxs-lookup"><span data-stu-id="04865-202">0x804202FFL</span></span>
</dt> <dt>



<span data-ttu-id="04865-203">Definisce il limite dei report di errore. si verificherà un errore relativo al server tra il **\_ \_ \_ primo** e il server EAP e il server per **\_ \_ \_ ultimo**.</span><span class="sxs-lookup"><span data-stu-id="04865-203">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ certificato server EAP \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="04865-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP\_E\_SERVER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-205">0x80420200</span><span class="sxs-lookup"><span data-stu-id="04865-205">0x80420200</span></span>
</dt> <dt>



<span data-ttu-id="04865-206">EAPHost non è stato in grado di trovare il certificato del server per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="04865-206">EAPHost could not find the server certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_ \_ certificato server EAP \_ E \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="04865-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP\_E\_SERVER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-208">0x80420201</span><span class="sxs-lookup"><span data-stu-id="04865-208">0x80420201</span></span>
</dt> <dt>



<span data-ttu-id="04865-209">Il certificato del server utilizzato per l'autenticazione non dispone di un set di utilizzo chiavi avanzato (EKU) appropriato.</span><span class="sxs-lookup"><span data-stu-id="04865-209">The server certificate being user for authentication does not have a proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**\_ \_ certificato server EAP \_ E \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="04865-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP\_E\_SERVER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-211">0x80420202</span><span class="sxs-lookup"><span data-stu-id="04865-211">0x80420202</span></span>
</dt> <dt>



<span data-ttu-id="04865-212">EAPhost ha rilevato un certificato server scaduto.</span><span class="sxs-lookup"><span data-stu-id="04865-212">EAPhost found an expired server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**\_ \_ certificato server EAP \_ E \_ revocato**</span><span class="sxs-lookup"><span data-stu-id="04865-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP\_E\_SERVER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-214">0x80420203</span><span class="sxs-lookup"><span data-stu-id="04865-214">0x80420203</span></span>
</dt> <dt>



<span data-ttu-id="04865-215">Il certificato server usato per l'autenticazione è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="04865-215">The server certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_errore del \_ certificato del server EAP E \_ \_ altro \_**</span><span class="sxs-lookup"><span data-stu-id="04865-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP\_E\_SERVER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-217">0x80420204</span><span class="sxs-lookup"><span data-stu-id="04865-217">0x80420204</span></span>
</dt> <dt>



<span data-ttu-id="04865-218">Si è verificato un errore sconosciuto con il certificato del server.</span><span class="sxs-lookup"><span data-stu-id="04865-218">An unknown error occurred with the server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**\_ \_ \_ \_ primo certificato radice utente EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="04865-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP\_E\_USER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-220">0x80420300L</span><span class="sxs-lookup"><span data-stu-id="04865-220">0x80420300L</span></span>
</dt> <dt>



<span data-ttu-id="04865-221">Definisce il limite dei report di errore. qualsiasi errore relativo al certificato radice utente si verificherà prima tra il certificato **\_ \_ \_ radice utente \_ \_ EAP** e e il certificato **\_ \_ \_ radice \_ \_ utente EAP** e.</span><span class="sxs-lookup"><span data-stu-id="04865-221">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**\_ \_ \_ \_ ultimo certificato radice utente EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="04865-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP\_E\_USER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-223">0x804203FFL</span><span class="sxs-lookup"><span data-stu-id="04865-223">0x804203FFL</span></span>
</dt> <dt>



<span data-ttu-id="04865-224">Definisce il limite dei report di errore. qualsiasi errore relativo al certificato radice utente si verificherà prima tra il certificato **\_ \_ \_ radice utente \_ \_ EAP** e e il certificato **\_ \_ \_ radice \_ \_ utente EAP** e.</span><span class="sxs-lookup"><span data-stu-id="04865-224">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ certificato radice utente EAP E \_ \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="04865-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP\_E\_USER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-226">0x80420300</span><span class="sxs-lookup"><span data-stu-id="04865-226">0x80420300</span></span>
</dt> <dt>



<span data-ttu-id="04865-227">EAPHost non è riuscito a trovare un certificato in un archivio certificati radice attendibile per la convalida della certificazione utente.</span><span class="sxs-lookup"><span data-stu-id="04865-227">EAPHost could not find a certificate in a trusted root certificate store for user certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**\_ \_ certificato radice utente EAP E \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="04865-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP\_E\_USER\_ROOT\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-229">0x80420301</span><span class="sxs-lookup"><span data-stu-id="04865-229">0x80420301</span></span>
</dt> <dt>



<span data-ttu-id="04865-230">L'autenticazione non è riuscita perché il certificato radice usato per la rete non è valido.</span><span class="sxs-lookup"><span data-stu-id="04865-230">The authentication failed because the root certificate used for this network is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**\_ \_ \_ certificato radice utente EAP \_ E \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="04865-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP\_E\_USER\_ROOT\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-232">0x80420302</span><span class="sxs-lookup"><span data-stu-id="04865-232">0x80420302</span></span>
</dt> <dt>



<span data-ttu-id="04865-233">Il certificato radice attendibile necessario per la convalida del certificato utente è scaduto.</span><span class="sxs-lookup"><span data-stu-id="04865-233">The trusted root certificate needed for user certificate validation has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ \_ \_ primo certificato radice del server EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="04865-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-235">0x80420400L</span><span class="sxs-lookup"><span data-stu-id="04865-235">0x80420400L</span></span>
</dt> <dt>



<span data-ttu-id="04865-236">Definisce il limite dei report di errore. si verificherà un errore relativo al certificato radice del server tra il certificato **radice del server EAP e \_ \_ \_ \_ \_ prima** e il certificato **\_ \_ \_ radice \_ \_** del server EAP e.</span><span class="sxs-lookup"><span data-stu-id="04865-236">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ \_ \_ ultimo certificato radice server EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="04865-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-238">0x804204FFL</span><span class="sxs-lookup"><span data-stu-id="04865-238">0x804204FFL</span></span>
</dt> <dt>



<span data-ttu-id="04865-239">Definisce il limite dei report di errore. si verificherà un errore relativo al certificato radice del server tra il certificato **radice del server EAP e \_ \_ \_ \_ \_ prima** e il certificato **\_ \_ \_ radice \_ \_** del server EAP e.</span><span class="sxs-lookup"><span data-stu-id="04865-239">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ certificato radice del server EAP E \_ \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="04865-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-241">0x80420400</span><span class="sxs-lookup"><span data-stu-id="04865-241">0x80420400</span></span>
</dt> <dt>



<span data-ttu-id="04865-242">EAPHost non è riuscito a trovare un certificato radice in un archivio certificati radice attendibile per la convalida della certificazione server.</span><span class="sxs-lookup"><span data-stu-id="04865-242">EAPHost could not find a root certificate in a trusted root certificate store for the server certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ certificato radice del server EAP E \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="04865-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_INVALID**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-244">0x80420401</span><span class="sxs-lookup"><span data-stu-id="04865-244">0x80420401</span></span>
</dt> <dt>



<span data-ttu-id="04865-245">L'autenticazione non è riuscita perché il certificato server richiesto per la rete nel computer server non è valido.</span><span class="sxs-lookup"><span data-stu-id="04865-245">The authentication failed because the server certificate required for this network on the server computer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="04865-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_ \_ \_ nome certificato radice server EAP E \_ \_ \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="04865-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04865-247">0x80420406</span><span class="sxs-lookup"><span data-stu-id="04865-247">0x80420406</span></span>
</dt> <dt>



<span data-ttu-id="04865-248">L'autenticazione non è riuscita perché il certificato nel computer server non ha un nome di server specificato.</span><span class="sxs-lookup"><span data-stu-id="04865-248">The authentication failed because the certificate on the server computer does not have a server name specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04865-249">Commenti</span><span class="sxs-lookup"><span data-stu-id="04865-249">Remarks</span></span>

<span data-ttu-id="04865-250">Esistono nomi alternativi per determinati errori:</span><span class="sxs-lookup"><span data-stu-id="04865-250">There are alternate names for certain errors:</span></span>

-   <span data-ttu-id="04865-251">Un altro nome per il **\_ pacchetto EAP E \_ EAPHOST \_ Method \_ non valido \_** è il **\_ \_ \_ pacchetto EAP non valido**.</span><span class="sxs-lookup"><span data-stu-id="04865-251">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>
-   <span data-ttu-id="04865-252">Un altro nome per **EAP \_ E \_ EAPHOST \_ Remote \_ \_ Packet** è un **\_ \_ pacchetto EAP non valido**.</span><span class="sxs-lookup"><span data-stu-id="04865-252">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>

## <a name="requirements"></a><span data-ttu-id="04865-253">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04865-253">Requirements</span></span>



| <span data-ttu-id="04865-254">Requisito</span><span class="sxs-lookup"><span data-stu-id="04865-254">Requirement</span></span> | <span data-ttu-id="04865-255">Valore</span><span class="sxs-lookup"><span data-stu-id="04865-255">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="04865-256">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04865-256">Minimum supported client</span></span><br/> | <span data-ttu-id="04865-257">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04865-257">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="04865-258">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04865-258">Minimum supported server</span></span><br/> | <span data-ttu-id="04865-259">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04865-259">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="04865-260">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04865-260">Header</span></span><br/>                   | <dl> <span data-ttu-id="04865-261"><dt>Eaphosterror. h</dt></span><span class="sxs-lookup"><span data-stu-id="04865-261"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04865-262">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04865-262">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04865-263">Costanti EAPHost comuni</span><span class="sxs-lookup"><span data-stu-id="04865-263">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

