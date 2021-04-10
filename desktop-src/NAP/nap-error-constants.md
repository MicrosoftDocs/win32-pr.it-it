---
title: Costanti di errore NAP (WinError. h)
description: Le costanti di errore NAP seguenti sono definite in WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964716"
---
# <a name="nap-error-constants"></a><span data-ttu-id="577f6-103">Costanti di errore NAP</span><span class="sxs-lookup"><span data-stu-id="577f6-103">NAP Error Constants</span></span>

> [!Note]  
> <span data-ttu-id="577f6-104">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="577f6-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="577f6-105">Le costanti di errore NAP seguenti sono definite in WinError. h.</span><span class="sxs-lookup"><span data-stu-id="577f6-105">The following NAP error constants are defined in WinError.h.</span></span>

<dl> <dt>

<span data-ttu-id="577f6-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP \_ E \_ pacchetto non valido \_**</span><span class="sxs-lookup"><span data-stu-id="577f6-106"><span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP\_E\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-107">\_HRESULT \_ \_ (0x80270001L)</span><span class="sxs-lookup"><span data-stu-id="577f6-107">\_HRESULT\_TYPEDEF\_(0x80270001L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-108">Il pacchetto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) NAP non è valido.</span><span class="sxs-lookup"><span data-stu-id="577f6-108">The NAP [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E rapporto di \_ \_ integrità mancante**</span><span class="sxs-lookup"><span data-stu-id="577f6-109"><span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP\_E\_MISSING\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-110">\_HRESULT \_ \_ (0x80270002L)</span><span class="sxs-lookup"><span data-stu-id="577f6-110">\_HRESULT\_TYPEDEF\_(0x80270002L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-111">Nel pacchetto NAP manca un rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="577f6-111">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) was missing from the NAP packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**protezione accesso alla rete \_ E \_ ID in conflitto \_**</span><span class="sxs-lookup"><span data-stu-id="577f6-112"><span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP\_E\_CONFLICTING\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-113">\_HRESULT \_ \_ (0x80270003L)</span><span class="sxs-lookup"><span data-stu-id="577f6-113">\_HRESULT\_TYPEDEF\_(0x80270003L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-114">L'ID entità è in conflitto con un ID entità già registrato.</span><span class="sxs-lookup"><span data-stu-id="577f6-114">The entity ID conflicts with an already-registered entity ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ nessun rapporto di \_ integrità memorizzato nella cache \_**</span><span class="sxs-lookup"><span data-stu-id="577f6-115"><span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP\_E\_NO\_CACHED\_SOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-116">\_HRESULT \_ \_ (0x80270004L)</span><span class="sxs-lookup"><span data-stu-id="577f6-116">\_HRESULT\_TYPEDEF\_(0x80270004L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-117">Non è presente alcun rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="577f6-117">No cached [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ ancora \_ associato**</span><span class="sxs-lookup"><span data-stu-id="577f6-118"><span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP\_E\_STILL\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-119">\_HRESULT \_ \_ (0x80270005L)</span><span class="sxs-lookup"><span data-stu-id="577f6-119">\_HRESULT\_TYPEDEF\_(0x80270005L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-120">L'entità è ancora associata al sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="577f6-120">The entity is still bound to the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ non \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="577f6-121"><span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP\_E\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-122">\_HRESULT \_ \_ (0x80270006L)</span><span class="sxs-lookup"><span data-stu-id="577f6-122">\_HRESULT\_TYPEDEF\_(0x80270006L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-123">L'entità non è registrata nel sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="577f6-123">The entity is not registered with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ non \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="577f6-124"><span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP\_E\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-125">\_HRESULT \_ \_ (0x80270007L)</span><span class="sxs-lookup"><span data-stu-id="577f6-125">\_HRESULT\_TYPEDEF\_(0x80270007L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-126">L'entità non è inizializzata con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="577f6-126">The entity is not initialized with the NAP system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**\_ID NAP E non \_ corrispondente \_**</span><span class="sxs-lookup"><span data-stu-id="577f6-127"><span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**NAP\_E\_MISMATCHED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-128">\_HRESULT \_ \_ (0x80270008L)</span><span class="sxs-lookup"><span data-stu-id="577f6-128">\_HRESULT\_TYPEDEF\_(0x80270008L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-129">Gli ID di correlazione nella **richiesta e nella** risposta di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="577f6-129">The correlation IDs in the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) request and **SoH** response do not match up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ non \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="577f6-130"><span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP\_E\_NOT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-131">\_HRESULT \_ \_ (0x80270009L)</span><span class="sxs-lookup"><span data-stu-id="577f6-131">\_HRESULT\_TYPEDEF\_(0x80270009L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-132">Il completamento è stato indicato in una richiesta che non è attualmente in sospeso.</span><span class="sxs-lookup"><span data-stu-id="577f6-132">Completion was indicated on a request that is not currently pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP \_ E \_ ID \_ non \_ trovati**</span><span class="sxs-lookup"><span data-stu-id="577f6-133"><span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP\_E\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-134">\_HRESULT \_ \_ (0x8027000AL)</span><span class="sxs-lookup"><span data-stu-id="577f6-134">\_HRESULT\_TYPEDEF\_(0x8027000AL)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-135">ID del componente NAP non trovato.</span><span class="sxs-lookup"><span data-stu-id="577f6-135">The NAP component's ID was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MaxSize \_ troppo \_ piccoli**</span><span class="sxs-lookup"><span data-stu-id="577f6-136"><span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP\_E\_MAXSIZE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-137">\_HRESULT \_ \_ (0x8027000BL)</span><span class="sxs-lookup"><span data-stu-id="577f6-137">\_HRESULT\_TYPEDEF\_(0x8027000BL)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-138">La dimensione massima della connessione è troppo piccola per un pacchetto di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="577f6-138">The maximum size of the connection is too small for an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**\_servizio NAP \_ E \_ non \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="577f6-139"><span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**NAP\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-140">\_HRESULT \_ \_ (0x8027000CL)</span><span class="sxs-lookup"><span data-stu-id="577f6-140">\_HRESULT\_TYPEDEF\_(0x8027000CL)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-141">Il servizio NapAgent non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="577f6-141">The NapAgent service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**il \_ certificato NAP S è \_ \_ già \_ presente**</span><span class="sxs-lookup"><span data-stu-id="577f6-142"><span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**NAP\_S\_CERT\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-143">\_HRESULT \_ \_ (0x0027000DL)</span><span class="sxs-lookup"><span data-stu-id="577f6-143">\_HRESULT\_TYPEDEF\_(0x0027000DL)</span></span> 
</dt> <dt>



<span data-ttu-id="577f6-144">Un certificato è già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="577f6-144">A certificate is already present in the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**protezione accesso alla rete \_ E \_ entità \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="577f6-145"><span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**NAP\_E\_ENTITY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-146">\_HRESULT \_ \_ (0x8027000EL)</span><span class="sxs-lookup"><span data-stu-id="577f6-146">\_HRESULT\_TYPEDEF\_(0x8027000EL)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-147">L'entità è disabilitata con il servizio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="577f6-147">The entity is disabled with the NapAgent service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**errore di protezione accesso alla rete \_ E \_ netsh \_ GROUPPOLICY \_**</span><span class="sxs-lookup"><span data-stu-id="577f6-148"><span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**NAP\_E\_NETSH\_GROUPPOLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-149">\_HRESULT \_ \_ (0x8027000FL)</span><span class="sxs-lookup"><span data-stu-id="577f6-149">\_HRESULT\_TYPEDEF\_(0x8027000FL)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-150">Criteri di gruppo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="577f6-150">Group Policy is not configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ numero eccessivo di \_ \_ chiamate**</span><span class="sxs-lookup"><span data-stu-id="577f6-151"><span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP\_E\_TOO\_MANY\_CALLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-152">\_HRESULT \_ \_ (0x80270010L)</span><span class="sxs-lookup"><span data-stu-id="577f6-152">\_HRESULT\_TYPEDEF\_(0x80270010L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-153">Troppe chiamate simultanee.</span><span class="sxs-lookup"><span data-stu-id="577f6-153">Too many simultaneous calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="577f6-154"><span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**NAP\_E\_SHV\_CONFIG\_EXISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-155">\_HRESULT \_ \_ (0x80270011L)</span><span class="sxs-lookup"><span data-stu-id="577f6-155">\_HRESULT\_TYPEDEF\_(0x80270011L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-156">La configurazione di convalida integrità sistema esiste già.</span><span class="sxs-lookup"><span data-stu-id="577f6-156">SHV configuration already exists.</span></span>

> [!Note]  
> <span data-ttu-id="577f6-157">Supportato in Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="577f6-157">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="577f6-158"><span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-159">\_HRESULT \_ \_ (0x80270012L)</span><span class="sxs-lookup"><span data-stu-id="577f6-159">\_HRESULT\_TYPEDEF\_(0x80270012L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-160">Configurazione di convalida integrità sistema non trovata.</span><span class="sxs-lookup"><span data-stu-id="577f6-160">SHV configuration is not found.</span></span>

> [!Note]  
> <span data-ttu-id="577f6-161">Supportato in Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="577f6-161">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="577f6-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**TIMEOUT di protezione accesso alla rete \_ E di \_ integrità \_**</span><span class="sxs-lookup"><span data-stu-id="577f6-162"><span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**NAP\_E\_SHV\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="577f6-163">\_HRESULT \_ \_ (0x80270013L)</span><span class="sxs-lookup"><span data-stu-id="577f6-163">\_HRESULT\_TYPEDEF\_(0x80270013L)</span></span>
</dt> <dt>



<span data-ttu-id="577f6-164">Timeout di convalida integrità di sistema nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="577f6-164">SHV timed out on the request.</span></span>

> [!Note]  
> <span data-ttu-id="577f6-165">Supportato in Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="577f6-165">Supported in Windows 7 or later.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="577f6-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="577f6-166">Requirements</span></span>



| <span data-ttu-id="577f6-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="577f6-167">Requirement</span></span> | <span data-ttu-id="577f6-168">Valore</span><span class="sxs-lookup"><span data-stu-id="577f6-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="577f6-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="577f6-169">Minimum supported client</span></span><br/> | <span data-ttu-id="577f6-170">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="577f6-170">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="577f6-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="577f6-171">Minimum supported server</span></span><br/> | <span data-ttu-id="577f6-172">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="577f6-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="577f6-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="577f6-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="577f6-174"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="577f6-174"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577f6-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="577f6-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577f6-176">**Costanti NAP**</span><span class="sxs-lookup"><span data-stu-id="577f6-176">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





