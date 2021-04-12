---
description: Descrive i codici di errore 1300-1699 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Codici di errore di sistema (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483317"
---
# <a name="system-error-codes-1300-1699"></a><span data-ttu-id="c0548-103">Codici di errore di sistema (1300-1699)</span><span class="sxs-lookup"><span data-stu-id="c0548-103">System Error Codes (1300-1699)</span></span>

> [!NOTE]
> <span data-ttu-id="c0548-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="c0548-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="c0548-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c0548-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="c0548-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 1300 a 1699.</span><span class="sxs-lookup"><span data-stu-id="c0548-106">The following list describes [system error codes](system-error-codes.md) for errors 1300 to 1699.</span></span> <span data-ttu-id="c0548-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c0548-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="c0548-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="c0548-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="c0548-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERRORE \_ non \_ tutti \_ assegnati**</span><span class="sxs-lookup"><span data-stu-id="c0548-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERROR\_NOT\_ALL\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-110">1300 (0x514)</span><span class="sxs-lookup"><span data-stu-id="c0548-110">1300 (0x514)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-111">Non tutti i privilegi o i gruppi a cui viene fatto riferimento vengono assegnati al chiamante.</span><span class="sxs-lookup"><span data-stu-id="c0548-111">Not all privileges or groups referenced are assigned to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERRORE per \_ alcuni \_ non \_ mappato**</span><span class="sxs-lookup"><span data-stu-id="c0548-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR\_SOME\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-113">1301 (0x515)</span><span class="sxs-lookup"><span data-stu-id="c0548-113">1301 (0x515)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-114">Non è stato possibile eseguire il mapping tra i nomi di account e gli ID di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0548-114">Some mapping between account names and security IDs was not done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERRORE \_ Nessuna \_ quota \_ per l' \_ account**</span><span class="sxs-lookup"><span data-stu-id="c0548-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR\_NO\_QUOTAS\_FOR\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-116">1302 (0x516)</span><span class="sxs-lookup"><span data-stu-id="c0548-116">1302 (0x516)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-117">Nessun limite di quota di sistema impostato in modo specifico per questo account.</span><span class="sxs-lookup"><span data-stu-id="c0548-117">No system quota limits are specifically set for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERRORE \_ \_ chiave della \_ sessione \_ utente locale**</span><span class="sxs-lookup"><span data-stu-id="c0548-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR\_LOCAL\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-119">1303 (0x517)</span><span class="sxs-lookup"><span data-stu-id="c0548-119">1303 (0x517)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-120">Non è disponibile alcuna chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="c0548-120">No encryption key is available.</span></span> <span data-ttu-id="c0548-121">È stata restituita una chiave di crittografia nota.</span><span class="sxs-lookup"><span data-stu-id="c0548-121">A well-known encryption key was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERRORE \_ \_ password LM \_ null**</span><span class="sxs-lookup"><span data-stu-id="c0548-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR\_NULL\_LM\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-123">1304 (0x518)</span><span class="sxs-lookup"><span data-stu-id="c0548-123">1304 (0x518)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-124">La password è troppo complessa per essere convertita in una password di LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="c0548-124">The password is too complex to be converted to a LAN Manager password.</span></span> <span data-ttu-id="c0548-125">La password di LAN Manager restituita è una stringa **null** .</span><span class="sxs-lookup"><span data-stu-id="c0548-125">The LAN Manager password returned is a **NULL** string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERRORE \_ \_ Revisione sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="c0548-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR\_UNKNOWN\_REVISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-127">1305 (0x519)</span><span class="sxs-lookup"><span data-stu-id="c0548-127">1305 (0x519)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-128">Il livello di revisione è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c0548-128">The revision level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**Revisione errore non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="c0548-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR\_REVISION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-130">1306 (0x51A)</span><span class="sxs-lookup"><span data-stu-id="c0548-130">1306 (0x51A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-131">Indica che due livelli di revisione non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="c0548-131">Indicates two revision levels are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERRORE \_ proprietario non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR\_INVALID\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-133">1307 (0x51B)</span><span class="sxs-lookup"><span data-stu-id="c0548-133">1307 (0x51B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-134">Questo ID di sicurezza non può essere assegnato come proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0548-134">This security ID may not be assigned as the owner of this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERRORE \_ \_ gruppo primario non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR\_INVALID\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-136">1308 (0x51C)</span><span class="sxs-lookup"><span data-stu-id="c0548-136">1308 (0x51C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-137">Questo ID di sicurezza non può essere assegnato come gruppo primario di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0548-137">This security ID may not be assigned as the primary group of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERRORE \_ nessun \_ token di rappresentazione \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR\_NO\_IMPERSONATION\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-139">1309 (0x51D)</span><span class="sxs-lookup"><span data-stu-id="c0548-139">1309 (0x51D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-140">È stato effettuato un tentativo di operare su un token di rappresentazione da un thread che non rappresenta attualmente un client.</span><span class="sxs-lookup"><span data-stu-id="c0548-140">An attempt has been made to operate on an impersonation token by a thread that is not currently impersonating a client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERRORE \_ di \_ disabilitazione del cant \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="c0548-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR\_CANT\_DISABLE\_MANDATORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-142">1310 (0x51E)</span><span class="sxs-lookup"><span data-stu-id="c0548-142">1310 (0x51E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-143">Il gruppo potrebbe non essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c0548-143">The group may not be disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERRORE \_ nessun \_ server di accesso \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR\_NO\_LOGON\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-145">1311 (0x51F)</span><span class="sxs-lookup"><span data-stu-id="c0548-145">1311 (0x51F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-146">Attualmente non sono disponibili server di accesso per il servizio della richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="c0548-146">There are currently no logon servers available to service the logon request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERRORE \_ \_ : nessuna \_ sessione di accesso \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR\_NO\_SUCH\_LOGON\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-148">1312 (0x520)</span><span class="sxs-lookup"><span data-stu-id="c0548-148">1312 (0x520)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-149">Una sessione di accesso specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="c0548-149">A specified logon session does not exist.</span></span> <span data-ttu-id="c0548-150">È possibile che sia già stata terminata.</span><span class="sxs-lookup"><span data-stu-id="c0548-150">It may already have been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERRORE \_ nessun \_ privilegio di questo tipo \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERROR\_NO\_SUCH\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-152">1313 (0x521)</span><span class="sxs-lookup"><span data-stu-id="c0548-152">1313 (0x521)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-153">Il privilegio specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="c0548-153">A specified privilege does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**\_privilegio errore \_ non \_ mantenuto**</span><span class="sxs-lookup"><span data-stu-id="c0548-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**ERROR\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-155">1314 (0x522)</span><span class="sxs-lookup"><span data-stu-id="c0548-155">1314 (0x522)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-156">Il client non dispone di un privilegio necessario.</span><span class="sxs-lookup"><span data-stu-id="c0548-156">A required privilege is not held by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERRORE \_ \_ nome account non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR\_INVALID\_ACCOUNT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-158">1315 (0x523)</span><span class="sxs-lookup"><span data-stu-id="c0548-158">1315 (0x523)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-159">Il nome specificato non è un nome di account formulato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c0548-159">The name provided is not a properly formed account name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERRORE \_ utente \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="c0548-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERROR\_USER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-161">1316 (0x524)</span><span class="sxs-lookup"><span data-stu-id="c0548-161">1316 (0x524)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-162">L'account specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="c0548-162">The specified account already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERRORE \_ \_ \_ dell'utente**</span><span class="sxs-lookup"><span data-stu-id="c0548-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERROR\_NO\_SUCH\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-164">1317 (0x525)</span><span class="sxs-lookup"><span data-stu-id="c0548-164">1317 (0x525)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-165">L'account specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="c0548-165">The specified account does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**\_gruppo errore \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="c0548-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**ERROR\_GROUP\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-167">1318 (0x526)</span><span class="sxs-lookup"><span data-stu-id="c0548-167">1318 (0x526)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-168">Il gruppo specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="c0548-168">The specified group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERRORE \_ di \_ questo \_ gruppo**</span><span class="sxs-lookup"><span data-stu-id="c0548-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERROR\_NO\_SUCH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-170">1319 (0x527)</span><span class="sxs-lookup"><span data-stu-id="c0548-170">1319 (0x527)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-171">Il gruppo specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="c0548-171">The specified group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_membro Error \_ nel \_ gruppo**</span><span class="sxs-lookup"><span data-stu-id="c0548-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**ERROR\_MEMBER\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-173">1320 (0x528)</span><span class="sxs-lookup"><span data-stu-id="c0548-173">1320 (0x528)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-174">L'account utente specificato è già membro del gruppo specificato oppure non è possibile eliminare il gruppo specificato perché contiene un membro.</span><span class="sxs-lookup"><span data-stu-id="c0548-174">Either the specified user account is already a member of the specified group, or the specified group cannot be deleted because it contains a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**\_membro errore \_ non \_ nel \_ gruppo**</span><span class="sxs-lookup"><span data-stu-id="c0548-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**ERROR\_MEMBER\_NOT\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-176">1321 (0x529)</span><span class="sxs-lookup"><span data-stu-id="c0548-176">1321 (0x529)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-177">L'account utente specificato non è un membro dell'account di gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="c0548-177">The specified user account is not a member of the specified group account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERRORE \_ ultimo \_ amministratore**</span><span class="sxs-lookup"><span data-stu-id="c0548-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERROR\_LAST\_ADMIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-179">1322 (0x52A)</span><span class="sxs-lookup"><span data-stu-id="c0548-179">1322 (0x52A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-180">Questa operazione non è consentita perché potrebbe causare la disabilitazione, l'eliminazione o l'accesso di un account di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-180">This operation is disallowed as it could result in an administration account being disabled, deleted or unable to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERRORE \_ di \_ password errata**</span><span class="sxs-lookup"><span data-stu-id="c0548-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR\_WRONG\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-182">1323 (0x52B)</span><span class="sxs-lookup"><span data-stu-id="c0548-182">1323 (0x52B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-183">Non è possibile aggiornare la password.</span><span class="sxs-lookup"><span data-stu-id="c0548-183">Unable to update the password.</span></span> <span data-ttu-id="c0548-184">Il valore specificato come password corrente non è corretto.</span><span class="sxs-lookup"><span data-stu-id="c0548-184">The value provided as the current password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**PASSWORD di errore formato non valido \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR\_ILL\_FORMED\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-186">1324 (0x52C)</span><span class="sxs-lookup"><span data-stu-id="c0548-186">1324 (0x52C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-187">Non è possibile aggiornare la password.</span><span class="sxs-lookup"><span data-stu-id="c0548-187">Unable to update the password.</span></span> <span data-ttu-id="c0548-188">Il valore specificato per la nuova password contiene valori non consentiti nelle password.</span><span class="sxs-lookup"><span data-stu-id="c0548-188">The value provided for the new password contains values that are not allowed in passwords.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_ \_ restrizione password errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**ERROR\_PASSWORD\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-190">1325 (0x52D)</span><span class="sxs-lookup"><span data-stu-id="c0548-190">1325 (0x52D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-191">Non è possibile aggiornare la password.</span><span class="sxs-lookup"><span data-stu-id="c0548-191">Unable to update the password.</span></span> <span data-ttu-id="c0548-192">Il valore specificato per la nuova password non soddisfa i requisiti di lunghezza, complessità o cronologia del dominio.</span><span class="sxs-lookup"><span data-stu-id="c0548-192">The value provided for the new password does not meet the length, complexity, or history requirements of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERRORE di \_ accesso non \_ riuscito**</span><span class="sxs-lookup"><span data-stu-id="c0548-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR\_LOGON\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-194">1326 (0x52E)</span><span class="sxs-lookup"><span data-stu-id="c0548-194">1326 (0x52E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-195">Il nome utente o la password non sono corretti.</span><span class="sxs-lookup"><span data-stu-id="c0548-195">The user name or password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_restrizione dell'account errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**ERROR\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-197">1327 (0x52F)</span><span class="sxs-lookup"><span data-stu-id="c0548-197">1327 (0x52F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-198">Le restrizioni degli account impediscono a questo utente di accedere.</span><span class="sxs-lookup"><span data-stu-id="c0548-198">Account restrictions are preventing this user from signing in.</span></span> <span data-ttu-id="c0548-199">Ad esempio: le password vuote non sono consentite, i tempi di accesso sono limitati oppure è stata applicata una restrizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c0548-199">For example: blank passwords aren't allowed, sign-in times are limited, or a policy restriction has been enforced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERRORE \_ di \_ accesso non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR\_INVALID\_LOGON\_HOURS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-201">1328 (0x530)</span><span class="sxs-lookup"><span data-stu-id="c0548-201">1328 (0x530)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-202">Per l'account sono previste restrizioni temporali che impediscono l'accesso al momento.</span><span class="sxs-lookup"><span data-stu-id="c0548-202">Your account has time restrictions that keep you from signing in right now.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERRORE \_ di \_ workstation non valido**</span><span class="sxs-lookup"><span data-stu-id="c0548-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR\_INVALID\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-204">1329 (0x531)</span><span class="sxs-lookup"><span data-stu-id="c0548-204">1329 (0x531)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-205">Questo utente non è autorizzato ad accedere a questo computer.</span><span class="sxs-lookup"><span data-stu-id="c0548-205">This user isn't allowed to sign in to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**PASSWORD di errore \_ \_ scaduta**</span><span class="sxs-lookup"><span data-stu-id="c0548-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERROR\_PASSWORD\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-207">1330 (0x532)</span><span class="sxs-lookup"><span data-stu-id="c0548-207">1330 (0x532)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-208">La password per questo account è scaduta.</span><span class="sxs-lookup"><span data-stu-id="c0548-208">The password for this account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**\_account errore \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="c0548-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**ERROR\_ACCOUNT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-210">1331 (0x533)</span><span class="sxs-lookup"><span data-stu-id="c0548-210">1331 (0x533)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-211">Questo utente non può accedere perché questo account è attualmente disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c0548-211">This user can't sign in because this account is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERRORE \_ nessuno \_ mappato**</span><span class="sxs-lookup"><span data-stu-id="c0548-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR\_NONE\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-213">1332 (0x534)</span><span class="sxs-lookup"><span data-stu-id="c0548-213">1332 (0x534)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-214">Non è stato eseguito alcun mapping tra nomi di account e ID di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0548-214">No mapping between account names and security IDs was done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERRORE \_ numero eccessivo di \_ \_ gli LUID \_ richieste**</span><span class="sxs-lookup"><span data-stu-id="c0548-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR\_TOO\_MANY\_LUIDS\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-216">1333 (0x535)</span><span class="sxs-lookup"><span data-stu-id="c0548-216">1333 (0x535)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-217">Troppi identificatori utente locali (gli LUID) richiesti in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="c0548-217">Too many local user identifiers (LUIDs) were requested at one time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERRORE \_ gli LUID \_ esaurito**</span><span class="sxs-lookup"><span data-stu-id="c0548-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR\_LUIDS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-219">1334 (0x536)</span><span class="sxs-lookup"><span data-stu-id="c0548-219">1334 (0x536)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-220">Non sono disponibili altri identificatori utente locali (gli LUID).</span><span class="sxs-lookup"><span data-stu-id="c0548-220">No more local user identifiers (LUIDs) are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERRORE \_ di \_ \_ sottoautorità non valida**</span><span class="sxs-lookup"><span data-stu-id="c0548-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR\_INVALID\_SUB\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-222">1335 (0x537)</span><span class="sxs-lookup"><span data-stu-id="c0548-222">1335 (0x537)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-223">La parte della sottocreazione di un ID di sicurezza non è valida per questo particolare utilizzo.</span><span class="sxs-lookup"><span data-stu-id="c0548-223">The subauthority part of a security ID is invalid for this particular use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERRORE \_ ACL non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR\_INVALID\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-225">1336 (0x538)</span><span class="sxs-lookup"><span data-stu-id="c0548-225">1336 (0x538)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-226">La struttura dell'elenco di controllo di accesso (ACL) non è valida.</span><span class="sxs-lookup"><span data-stu-id="c0548-226">The access control list (ACL) structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERRORE \_ SID non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR\_INVALID\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-228">1337 (0x539)</span><span class="sxs-lookup"><span data-stu-id="c0548-228">1337 (0x539)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-229">La struttura dell'ID di sicurezza non è valida.</span><span class="sxs-lookup"><span data-stu-id="c0548-229">The security ID structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERRORE \_ del \_ Descr di sicurezza non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR\_INVALID\_SECURITY\_DESCR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-231">1338 (0x53A)</span><span class="sxs-lookup"><span data-stu-id="c0548-231">1338 (0x53A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-232">La struttura del descrittore di sicurezza non è valida.</span><span class="sxs-lookup"><span data-stu-id="c0548-232">The security descriptor structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERRORE \_ \_ ACL ereditarietà non valida \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR\_BAD\_INHERITANCE\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-234">1340 (0x53C)</span><span class="sxs-lookup"><span data-stu-id="c0548-234">1340 (0x53C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-235">Non è stato possibile compilare l'elenco di controllo di accesso (ACL) ereditato o la voce di controllo di accesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="c0548-235">The inherited access control list (ACL) or access control entry (ACE) could not be built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**SERVER degli errori \_ \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="c0548-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR\_SERVER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-237">1341 (0x53D)</span><span class="sxs-lookup"><span data-stu-id="c0548-237">1341 (0x53D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-238">Il server è attualmente disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c0548-238">The server is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERRORE del \_ server \_ non \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="c0548-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERROR\_SERVER\_NOT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-240">1342 (0x53E)</span><span class="sxs-lookup"><span data-stu-id="c0548-240">1342 (0x53E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-241">Il server è attualmente abilitato.</span><span class="sxs-lookup"><span data-stu-id="c0548-241">The server is currently enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERRORE \_ di \_ autorità ID non valida \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR\_INVALID\_ID\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-243">1343 (0x53F)</span><span class="sxs-lookup"><span data-stu-id="c0548-243">1343 (0x53F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-244">Il valore specificato non è valido per un'autorità di identificazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-244">The value provided was an invalid value for an identifier authority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**\_ \_ superamento dello spazio allocato per l'errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERROR\_ALLOTTED\_SPACE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-246">1344 (0x540)</span><span class="sxs-lookup"><span data-stu-id="c0548-246">1344 (0x540)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-247">Memoria non disponibile per gli aggiornamenti delle informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0548-247">No more memory is available for security information updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERRORE \_ degli \_ attributi di gruppo non validi \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR\_INVALID\_GROUP\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-249">1345 (0x541)</span><span class="sxs-lookup"><span data-stu-id="c0548-249">1345 (0x541)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-250">Gli attributi specificati non sono validi o sono incompatibili con gli attributi per il gruppo nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="c0548-250">The specified attributes are invalid, or incompatible with the attributes for the group as a whole.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERRORE \_ del \_ livello di rappresentazione \_ errato**</span><span class="sxs-lookup"><span data-stu-id="c0548-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR\_BAD\_IMPERSONATION\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-252">1346 (0x542)</span><span class="sxs-lookup"><span data-stu-id="c0548-252">1346 (0x542)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-253">Non è stato fornito il livello richiesto di rappresentazione di client oppure il livello di rappresentazione fornito non è valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-253">Either a required impersonation level was not provided, or the provided impersonation level is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERRORE \_ di \_ apertura \_ anonima del cant**</span><span class="sxs-lookup"><span data-stu-id="c0548-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR\_CANT\_OPEN\_ANONYMOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-255">1347 (0x543)</span><span class="sxs-lookup"><span data-stu-id="c0548-255">1347 (0x543)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-256">Non è possibile aprire un token di sicurezza a livello anonimo.</span><span class="sxs-lookup"><span data-stu-id="c0548-256">Cannot open an anonymous level security token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERRORE \_ \_ classe di convalida non valida \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR\_BAD\_VALIDATION\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-258">1348 (0x544)</span><span class="sxs-lookup"><span data-stu-id="c0548-258">1348 (0x544)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-259">La classe di informazioni di convalida richiesta non è valida.</span><span class="sxs-lookup"><span data-stu-id="c0548-259">The validation information class requested was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERRORE \_ \_ tipo di token non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR\_BAD\_TOKEN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-261">1349 (0x545)</span><span class="sxs-lookup"><span data-stu-id="c0548-261">1349 (0x545)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-262">Il tipo del token non è appropriato per il tentativo di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="c0548-262">The type of the token is inappropriate for its attempted use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERRORE \_ Nessuna \_ sicurezza \_ per l' \_ oggetto**</span><span class="sxs-lookup"><span data-stu-id="c0548-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR\_NO\_SECURITY\_ON\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-264">1350 (0x546)</span><span class="sxs-lookup"><span data-stu-id="c0548-264">1350 (0x546)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-265">Impossibile eseguire un'operazione di sicurezza su un oggetto a cui non è associata alcuna sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0548-265">Unable to perform a security operation on an object that has no associated security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**errore \_ durante \_ l'accesso alle \_ informazioni sul dominio \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR\_CANT\_ACCESS\_DOMAIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-267">1351 (0x547)</span><span class="sxs-lookup"><span data-stu-id="c0548-267">1351 (0x547)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-268">Impossibile leggere le informazioni di configurazione dal controller di dominio perché il computer non è disponibile o l'accesso è stato negato.</span><span class="sxs-lookup"><span data-stu-id="c0548-268">Configuration information could not be read from the domain controller, either because the machine is unavailable, or access has been denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERRORE \_ \_ stato server non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR\_INVALID\_SERVER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-270">1352 (0x548)</span><span class="sxs-lookup"><span data-stu-id="c0548-270">1352 (0x548)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-271">Il server di sicurezza account Manager (SAM) o dell'autorità di protezione locale (LSA) non è in stato di errore per eseguire l'operazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0548-271">The security account manager (SAM) or local security authority (LSA) server was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERRORE \_ \_ stato del dominio non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR\_INVALID\_DOMAIN\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-273">1353 (0x549)</span><span class="sxs-lookup"><span data-stu-id="c0548-273">1353 (0x549)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-274">Lo stato del dominio non è corretto per eseguire l'operazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0548-274">The domain was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERRORE \_ \_ ruolo di dominio non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR\_INVALID\_DOMAIN\_ROLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-276">1354 (0x54A)</span><span class="sxs-lookup"><span data-stu-id="c0548-276">1354 (0x54A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-277">Questa operazione è consentita solo per il controller di dominio primario del dominio.</span><span class="sxs-lookup"><span data-stu-id="c0548-277">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERRORE \_ nessun \_ dominio di questo tipo \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERROR\_NO\_SUCH\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-279">1355 (0x54B)</span><span class="sxs-lookup"><span data-stu-id="c0548-279">1355 (0x54B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-280">Il dominio specificato non esiste o non è possibile contattarlo.</span><span class="sxs-lookup"><span data-stu-id="c0548-280">The specified domain either does not exist or could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**il \_ dominio di errore \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="c0548-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**ERROR\_DOMAIN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-282">1356 (0x54C)</span><span class="sxs-lookup"><span data-stu-id="c0548-282">1356 (0x54C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-283">Il dominio specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="c0548-283">The specified domain already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**\_superato il \_ limite di domini di errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**ERROR\_DOMAIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-285">1357 (0x54D)</span><span class="sxs-lookup"><span data-stu-id="c0548-285">1357 (0x54D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-286">È stato effettuato un tentativo di superare il limite per il numero di domini per server.</span><span class="sxs-lookup"><span data-stu-id="c0548-286">An attempt was made to exceed the limit on the number of domains per server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERRORE \_ di \_ danneggiamento interno del database \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR\_INTERNAL\_DB\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-288">1358 (0x54E)</span><span class="sxs-lookup"><span data-stu-id="c0548-288">1358 (0x54E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-289">Non è possibile completare l'operazione richiesta a causa di un errore irreversibile del supporto o di una struttura di dati danneggiata sul disco.</span><span class="sxs-lookup"><span data-stu-id="c0548-289">Unable to complete the requested operation because of either a catastrophic media failure or a data structure corruption on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**errore \_ interno \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERROR\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-291">1359 (0x54F)</span><span class="sxs-lookup"><span data-stu-id="c0548-291">1359 (0x54F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-292">An internal error occurred.</span><span class="sxs-lookup"><span data-stu-id="c0548-292">An internal error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERRORE \_ generico \_ non \_ mappato**</span><span class="sxs-lookup"><span data-stu-id="c0548-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR\_GENERIC\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-294">1360 (0x550)</span><span class="sxs-lookup"><span data-stu-id="c0548-294">1360 (0x550)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-295">I tipi di accesso generici erano contenuti in una maschera di accesso che dovrebbe essere già mappata a tipi non generici.</span><span class="sxs-lookup"><span data-stu-id="c0548-295">Generic access types were contained in an access mask which should already be mapped to nongeneric types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERRORE \_ nel \_ formato del descrittore errato \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR\_BAD\_DESCRIPTOR\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-297">1361 (0x551)</span><span class="sxs-lookup"><span data-stu-id="c0548-297">1361 (0x551)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-298">Il formato di un descrittore di sicurezza non è corretto (assoluto o relativo).</span><span class="sxs-lookup"><span data-stu-id="c0548-298">A security descriptor is not in the right format (absolute or self-relative).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**errore durante il \_ \_ processo di accesso \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR\_NOT\_LOGON\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-300">1362 (0x552)</span><span class="sxs-lookup"><span data-stu-id="c0548-300">1362 (0x552)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-301">L'azione richiesta è limitata per l'utilizzo solo da parte dei processi di accesso.</span><span class="sxs-lookup"><span data-stu-id="c0548-301">The requested action is restricted for use by logon processes only.</span></span> <span data-ttu-id="c0548-302">Il processo chiamante non è stato registrato come processo di accesso.</span><span class="sxs-lookup"><span data-stu-id="c0548-302">The calling process has not registered as a logon process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**la \_ sessione di accesso agli errori \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="c0548-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERROR\_LOGON\_SESSION\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-304">1363 (0x553)</span><span class="sxs-lookup"><span data-stu-id="c0548-304">1363 (0x553)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-305">Impossibile avviare una nuova sessione di accesso con un ID già in uso.</span><span class="sxs-lookup"><span data-stu-id="c0548-305">Cannot start a new logon session with an ID that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERRORE \_ di \_ questo \_ pacchetto**</span><span class="sxs-lookup"><span data-stu-id="c0548-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERROR\_NO\_SUCH\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-307">1364 (0x554)</span><span class="sxs-lookup"><span data-stu-id="c0548-307">1364 (0x554)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-308">Un pacchetto di autenticazione specificato è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c0548-308">A specified authentication package is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERRORE \_ \_ stato sessione di accesso non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR\_BAD\_LOGON\_SESSION\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-310">1365 (0x555)</span><span class="sxs-lookup"><span data-stu-id="c0548-310">1365 (0x555)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-311">La sessione di accesso non si trova in uno stato coerente con l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="c0548-311">The logon session is not in a state that is consistent with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**\_ \_ collisione della sessione di accesso agli errori \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERROR\_LOGON\_SESSION\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-313">1366 (0x556)</span><span class="sxs-lookup"><span data-stu-id="c0548-313">1366 (0x556)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-314">L'ID sessione di accesso è già in uso.</span><span class="sxs-lookup"><span data-stu-id="c0548-314">The logon session ID is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERRORE \_ \_ tipo di accesso non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR\_INVALID\_LOGON\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-316">1367 (0x557)</span><span class="sxs-lookup"><span data-stu-id="c0548-316">1367 (0x557)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-317">Una richiesta di accesso contiene un valore di tipo di accesso non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-317">A logon request contained an invalid logon type value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERRORE \_ non è possibile \_ rappresentare**</span><span class="sxs-lookup"><span data-stu-id="c0548-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR\_CANNOT\_IMPERSONATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-319">1368 (0x558)</span><span class="sxs-lookup"><span data-stu-id="c0548-319">1368 (0x558)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-320">Non è possibile rappresentare usando un named pipe fino a quando i dati non sono stati letti dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="c0548-320">Unable to impersonate using a named pipe until data has been read from that pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERRORE \_ RXACT \_ stato non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR\_RXACT\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-322">1369 (0x559)</span><span class="sxs-lookup"><span data-stu-id="c0548-322">1369 (0x559)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-323">Lo stato della transazione di un sottoalbero del registro di sistema non è compatibile con l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="c0548-323">The transaction state of a registry subtree is incompatible with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**errore \_ RXACT \_ commit \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR\_RXACT\_COMMIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-325">1370 (0x55A)</span><span class="sxs-lookup"><span data-stu-id="c0548-325">1370 (0x55A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-326">È stato rilevato un danneggiamento del database di sicurezza interno.</span><span class="sxs-lookup"><span data-stu-id="c0548-326">An internal security database corruption has been encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_account speciale \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERROR\_SPECIAL\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-328">1371 (0x55B)</span><span class="sxs-lookup"><span data-stu-id="c0548-328">1371 (0x55B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-329">Non è possibile eseguire questa operazione sugli account predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c0548-329">Cannot perform this operation on built-in accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**\_gruppo speciale \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERROR\_SPECIAL\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-331">1372 (0x55C)</span><span class="sxs-lookup"><span data-stu-id="c0548-331">1372 (0x55C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-332">Non è possibile eseguire questa operazione in questo gruppo speciale incorporato.</span><span class="sxs-lookup"><span data-stu-id="c0548-332">Cannot perform this operation on this built-in special group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERRORE \_ \_ utente speciale**</span><span class="sxs-lookup"><span data-stu-id="c0548-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR\_SPECIAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-334">1373 (0x55D)</span><span class="sxs-lookup"><span data-stu-id="c0548-334">1373 (0x55D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-335">Non è possibile eseguire questa operazione su questo utente speciale incorporato.</span><span class="sxs-lookup"><span data-stu-id="c0548-335">Cannot perform this operation on this built-in special user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**\_ \_ gruppo primario membri \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**ERROR\_MEMBERS\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-337">1374 (0x55E)</span><span class="sxs-lookup"><span data-stu-id="c0548-337">1374 (0x55E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-338">Non è possibile rimuovere l'utente da un gruppo perché il gruppo è attualmente il gruppo primario dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c0548-338">The user cannot be removed from a group because the group is currently the user's primary group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**il \_ token \_ di errore è già \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="c0548-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**ERROR\_TOKEN\_ALREADY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-340">1375 (0x55F)</span><span class="sxs-lookup"><span data-stu-id="c0548-340">1375 (0x55F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-341">Il token è già in uso come token primario.</span><span class="sxs-lookup"><span data-stu-id="c0548-341">The token is already in use as a primary token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERRORE \_ di \_ questo \_ alias**</span><span class="sxs-lookup"><span data-stu-id="c0548-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERROR\_NO\_SUCH\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-343">1376 (0x560)</span><span class="sxs-lookup"><span data-stu-id="c0548-343">1376 (0x560)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-344">Il gruppo locale specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="c0548-344">The specified local group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**\_membro errore \_ non presente \_ nell' \_ alias**</span><span class="sxs-lookup"><span data-stu-id="c0548-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**ERROR\_MEMBER\_NOT\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-346">1377 (0x561)</span><span class="sxs-lookup"><span data-stu-id="c0548-346">1377 (0x561)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-347">Il nome dell'account specificato non è un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="c0548-347">The specified account name is not a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_membro Error \_ nell' \_ alias**</span><span class="sxs-lookup"><span data-stu-id="c0548-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**ERROR\_MEMBER\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-349">1378 (0x562)</span><span class="sxs-lookup"><span data-stu-id="c0548-349">1378 (0x562)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-350">Il nome dell'account specificato è già membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="c0548-350">The specified account name is already a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ALIAS di errore \_ \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="c0548-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ERROR\_ALIAS\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-352">1379 (0x563)</span><span class="sxs-lookup"><span data-stu-id="c0548-352">1379 (0x563)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-353">Il gruppo locale specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="c0548-353">The specified local group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERRORE di \_ accesso \_ non \_ concesso**</span><span class="sxs-lookup"><span data-stu-id="c0548-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR\_LOGON\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-355">1380 (0x564)</span><span class="sxs-lookup"><span data-stu-id="c0548-355">1380 (0x564)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-356">Errore di accesso: all'utente non è stato concesso il tipo di accesso richiesto nel computer.</span><span class="sxs-lookup"><span data-stu-id="c0548-356">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERRORE di \_ troppi \_ \_ segreti**</span><span class="sxs-lookup"><span data-stu-id="c0548-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR\_TOO\_MANY\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-358">1381 (0x565)</span><span class="sxs-lookup"><span data-stu-id="c0548-358">1381 (0x565)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-359">È stato superato il numero massimo di segreti che possono essere archiviati in un singolo sistema.</span><span class="sxs-lookup"><span data-stu-id="c0548-359">The maximum number of secrets that may be stored in a single system has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**\_segreto errore \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="c0548-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR\_SECRET\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-361">1382 (0x566)</span><span class="sxs-lookup"><span data-stu-id="c0548-361">1382 (0x566)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-362">La lunghezza di un segreto supera la lunghezza massima consentita.</span><span class="sxs-lookup"><span data-stu-id="c0548-362">The length of a secret exceeds the maximum length allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**errore \_ interno \_ DB \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERROR\_INTERNAL\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-364">1383 (0x567)</span><span class="sxs-lookup"><span data-stu-id="c0548-364">1383 (0x567)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-365">Il database dell'autorità di sicurezza locale contiene un'incoerenza interna.</span><span class="sxs-lookup"><span data-stu-id="c0548-365">The local security authority database contains an internal inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERRORE di un \_ numero eccessivo di \_ \_ \_ ID contesto**</span><span class="sxs-lookup"><span data-stu-id="c0548-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR\_TOO\_MANY\_CONTEXT\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-367">1384 (0x568)</span><span class="sxs-lookup"><span data-stu-id="c0548-367">1384 (0x568)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-368">Durante un tentativo di accesso, il contesto di sicurezza dell'utente ha accumulato un numero eccessivo di ID di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0548-368">During a logon attempt, the user's security context accumulated too many security IDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_tipo di accesso errore \_ \_ non \_ concesso**</span><span class="sxs-lookup"><span data-stu-id="c0548-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**ERROR\_LOGON\_TYPE\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-370">1385 (0x569)</span><span class="sxs-lookup"><span data-stu-id="c0548-370">1385 (0x569)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-371">Errore di accesso: all'utente non è stato concesso il tipo di accesso richiesto nel computer.</span><span class="sxs-lookup"><span data-stu-id="c0548-371">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERRORE \_ NT \_ Cross \_ Encryption \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="c0548-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR\_NT\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-373">1386 (0x56A)</span><span class="sxs-lookup"><span data-stu-id="c0548-373">1386 (0x56A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-374">Per modificare la password di un utente, è necessaria una password crittografata in modo incrociato.</span><span class="sxs-lookup"><span data-stu-id="c0548-374">A cross-encrypted password is necessary to change a user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERRORE \_ nessun \_ membro di questo tipo \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR\_NO\_SUCH\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-376">1387 (0x56B)</span><span class="sxs-lookup"><span data-stu-id="c0548-376">1387 (0x56B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-377">Impossibile aggiungere o rimuovere un membro dal gruppo locale perché il membro non esiste.</span><span class="sxs-lookup"><span data-stu-id="c0548-377">A member could not be added to or removed from the local group because the member does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERRORE \_ membro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR\_INVALID\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-379">1388 (0x56C)</span><span class="sxs-lookup"><span data-stu-id="c0548-379">1388 (0x56C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-380">Non è stato possibile aggiungere un nuovo membro a un gruppo locale perché il tipo di account del membro non è corretto.</span><span class="sxs-lookup"><span data-stu-id="c0548-380">A new member could not be added to a local group because the member has the wrong account type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERRORE \_ troppi \_ \_ SID**</span><span class="sxs-lookup"><span data-stu-id="c0548-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR\_TOO\_MANY\_SIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-382">1389 (0x56D)</span><span class="sxs-lookup"><span data-stu-id="c0548-382">1389 (0x56D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-383">Sono stati specificati troppi ID di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c0548-383">Too many security IDs have been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERRORE \_ di \_ crittografia incrociata LM \_ \_ richiesta**</span><span class="sxs-lookup"><span data-stu-id="c0548-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR\_LM\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-385">1390 (0x56E)</span><span class="sxs-lookup"><span data-stu-id="c0548-385">1390 (0x56E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-386">Per modificare la password dell'utente, è necessaria una password crittografata in modo incrociato.</span><span class="sxs-lookup"><span data-stu-id="c0548-386">A cross-encrypted password is necessary to change this user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERRORE \_ senza \_ ereditarietà**</span><span class="sxs-lookup"><span data-stu-id="c0548-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR\_NO\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-388">1391 (0x56F)</span><span class="sxs-lookup"><span data-stu-id="c0548-388">1391 (0x56F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-389">Indica che un ACL non contiene componenti ereditabili.</span><span class="sxs-lookup"><span data-stu-id="c0548-389">Indicates an ACL contains no inheritable components.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**FILE di errore \_ \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="c0548-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**ERROR\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-391">1392 (0x570)</span><span class="sxs-lookup"><span data-stu-id="c0548-391">1392 (0x570)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-392">Il file o la directory è danneggiato e illeggibile.</span><span class="sxs-lookup"><span data-stu-id="c0548-392">The file or directory is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**disco di errore \_ \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="c0548-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR\_DISK\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-394">1393 (0x571)</span><span class="sxs-lookup"><span data-stu-id="c0548-394">1393 (0x571)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-395">La struttura del disco è danneggiata e illeggibile.</span><span class="sxs-lookup"><span data-stu-id="c0548-395">The disk structure is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERRORE \_ Nessuna \_ \_ chiave della sessione utente \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR\_NO\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-397">1394 (0x572)</span><span class="sxs-lookup"><span data-stu-id="c0548-397">1394 (0x572)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-398">Nessuna chiave della sessione utente per la sessione di accesso specificata.</span><span class="sxs-lookup"><span data-stu-id="c0548-398">There is no user session key for the specified logon session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**\_ \_ superata la quota di licenze di errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**ERROR\_LICENSE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-400">1395 (0x573)</span><span class="sxs-lookup"><span data-stu-id="c0548-400">1395 (0x573)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-401">The service being accessed is licensed for a particular number of connections.</span><span class="sxs-lookup"><span data-stu-id="c0548-401">The service being accessed is licensed for a particular number of connections.</span></span> <span data-ttu-id="c0548-402">Al momento non è possibile eseguire altre connessioni al servizio perché sono già presenti tutte le connessioni che il servizio può accettare.</span><span class="sxs-lookup"><span data-stu-id="c0548-402">No more connections can be made to the service at this time because there are already as many connections as the service can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERRORE \_ \_ Nome destinazione \_ errato**</span><span class="sxs-lookup"><span data-stu-id="c0548-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR\_WRONG\_TARGET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-404">1396 (0x574)</span><span class="sxs-lookup"><span data-stu-id="c0548-404">1396 (0x574)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-405">Il nome dell'account di destinazione non è corretto.</span><span class="sxs-lookup"><span data-stu-id="c0548-405">The target account name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERRORE di \_ autenticazione reciproca \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="c0548-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR\_MUTUAL\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-407">1397 (0x575)</span><span class="sxs-lookup"><span data-stu-id="c0548-407">1397 (0x575)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-408">Autenticazione reciproca non riuscita.</span><span class="sxs-lookup"><span data-stu-id="c0548-408">Mutual Authentication failed.</span></span> <span data-ttu-id="c0548-409">La password del server non è aggiornata nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="c0548-409">The server's password is out of date at the domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**\_sfasamento dell'ora di errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**ERROR\_TIME\_SKEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-411">1398 (0x576)</span><span class="sxs-lookup"><span data-stu-id="c0548-411">1398 (0x576)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-412">Esiste una differenza di data e ora tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="c0548-412">There is a time and/or date difference between the client and server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERRORE \_ \_ dominio corrente \_ non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="c0548-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR\_CURRENT\_DOMAIN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-414">1399 (0x577)</span><span class="sxs-lookup"><span data-stu-id="c0548-414">1399 (0x577)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-415">Non è possibile eseguire questa operazione sul dominio corrente.</span><span class="sxs-lookup"><span data-stu-id="c0548-415">This operation cannot be performed on the current domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERRORE \_ dell' \_ handle di finestra non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR\_INVALID\_WINDOW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-417">1400 (0x578)</span><span class="sxs-lookup"><span data-stu-id="c0548-417">1400 (0x578)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-418">Handle di finestra non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-418">Invalid window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERRORE \_ di \_ handle di menu non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR\_INVALID\_MENU\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-420">1401 (0x579)</span><span class="sxs-lookup"><span data-stu-id="c0548-420">1401 (0x579)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-421">Handle di menu non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-421">Invalid menu handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERRORE \_ di \_ handle cursore non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR\_INVALID\_CURSOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-423">1402 (0x57A)</span><span class="sxs-lookup"><span data-stu-id="c0548-423">1402 (0x57A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-424">Handle di cursore non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-424">Invalid cursor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERRORE \_ \_ handle accelerazione non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR\_INVALID\_ACCEL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-426">1403 (0x57B)</span><span class="sxs-lookup"><span data-stu-id="c0548-426">1403 (0x57B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-427">Handle della tabella di tasti di scelta rapida non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-427">Invalid accelerator table handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERRORE \_ dell' \_ handle di hook non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR\_INVALID\_HOOK\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-429">1404 (0x57C)</span><span class="sxs-lookup"><span data-stu-id="c0548-429">1404 (0x57C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-430">Handle di hook non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-430">Invalid hook handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERRORE \_ dell' \_ handle dwp non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR\_INVALID\_DWP\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-432">1405 (0x57D)</span><span class="sxs-lookup"><span data-stu-id="c0548-432">1405 (0x57D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-433">Handle non valido per una struttura di posizione a più finestre.</span><span class="sxs-lookup"><span data-stu-id="c0548-433">Invalid handle to a multiple-window position structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERRORE \_ TLW \_ con \_ WSCHILD**</span><span class="sxs-lookup"><span data-stu-id="c0548-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR\_TLW\_WITH\_WSCHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-435">1406 (0x57E)</span><span class="sxs-lookup"><span data-stu-id="c0548-435">1406 (0x57E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-436">Impossibile creare una finestra figlio di primo livello.</span><span class="sxs-lookup"><span data-stu-id="c0548-436">Cannot create a top-level child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**errore durante la \_ \_ ricerca della \_ \_ classe WND**</span><span class="sxs-lookup"><span data-stu-id="c0548-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR\_CANNOT\_FIND\_WND\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-438">1407 (0x57F)</span><span class="sxs-lookup"><span data-stu-id="c0548-438">1407 (0x57F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-439">Impossibile trovare la classe Window.</span><span class="sxs-lookup"><span data-stu-id="c0548-439">Cannot find window class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_finestra \_ di errore dell' \_ altro \_ thread**</span><span class="sxs-lookup"><span data-stu-id="c0548-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**ERROR\_WINDOW\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-441">1408 (0x580)</span><span class="sxs-lookup"><span data-stu-id="c0548-441">1408 (0x580)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-442">Finestra non valida; appartiene ad altro thread.</span><span class="sxs-lookup"><span data-stu-id="c0548-442">Invalid window; it belongs to other thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**\_tasto di scelta rapida errore \_ già \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="c0548-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERROR\_HOTKEY\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-444">1409 (0x581)</span><span class="sxs-lookup"><span data-stu-id="c0548-444">1409 (0x581)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-445">Il tasto di scelta è già registrato.</span><span class="sxs-lookup"><span data-stu-id="c0548-445">Hot key is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**la \_ classe \_ Error \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="c0548-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**ERROR\_CLASS\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-447">1410 (0x582)</span><span class="sxs-lookup"><span data-stu-id="c0548-447">1410 (0x582)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-448">Classe già esistente.</span><span class="sxs-lookup"><span data-stu-id="c0548-448">Class already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**\_la classe Error non \_ \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="c0548-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**ERROR\_CLASS\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-450">1411 (0x583)</span><span class="sxs-lookup"><span data-stu-id="c0548-450">1411 (0x583)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-451">La classe non esiste.</span><span class="sxs-lookup"><span data-stu-id="c0548-451">Class does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**\_classe Error \_ con \_ Windows**</span><span class="sxs-lookup"><span data-stu-id="c0548-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR\_CLASS\_HAS\_WINDOWS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-453">1412 (0x584)</span><span class="sxs-lookup"><span data-stu-id="c0548-453">1412 (0x584)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-454">La classe dispone ancora di finestre aperte.</span><span class="sxs-lookup"><span data-stu-id="c0548-454">Class still has open windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERRORE \_ indice non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR\_INVALID\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-456">1413 (0x585)</span><span class="sxs-lookup"><span data-stu-id="c0548-456">1413 (0x585)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-457">Indice non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-457">Invalid index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERRORE \_ di \_ handle icona non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR\_INVALID\_ICON\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-459">1414 (0x586)</span><span class="sxs-lookup"><span data-stu-id="c0548-459">1414 (0x586)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-460">Handle icona non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-460">Invalid icon handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**\_ \_ Indice finestra di dialogo di errore privato \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR\_PRIVATE\_DIALOG\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-462">1415 (0x587)</span><span class="sxs-lookup"><span data-stu-id="c0548-462">1415 (0x587)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-463">Uso delle parole della finestra di dialogo privata.</span><span class="sxs-lookup"><span data-stu-id="c0548-463">Using private DIALOG window words.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**\_ID casella di riepilogo errore \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="c0548-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ERROR\_LISTBOX\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-465">1416 (0x588)</span><span class="sxs-lookup"><span data-stu-id="c0548-465">1416 (0x588)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-466">Impossibile trovare l'identificatore della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="c0548-466">The list box identifier was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERRORE \_ senza \_ \_ caratteri jolly**</span><span class="sxs-lookup"><span data-stu-id="c0548-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR\_NO\_WILDCARD\_CHARACTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-468">1417 (0x589)</span><span class="sxs-lookup"><span data-stu-id="c0548-468">1417 (0x589)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-469">Non sono stati trovati caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="c0548-469">No wildcards were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**gli \_ Appunti di errore \_ non sono \_ aperti**</span><span class="sxs-lookup"><span data-stu-id="c0548-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR\_CLIPBOARD\_NOT\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-471">1418 (0x58A)</span><span class="sxs-lookup"><span data-stu-id="c0548-471">1418 (0x58A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-472">Per il thread non sono aperti gli Appunti.</span><span class="sxs-lookup"><span data-stu-id="c0548-472">Thread does not have a clipboard open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**\_tasto di scelta rapida errore \_ non \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="c0548-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERROR\_HOTKEY\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-474">1419 (0x58B)</span><span class="sxs-lookup"><span data-stu-id="c0548-474">1419 (0x58B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-475">Il tasto di scelta non è registrato.</span><span class="sxs-lookup"><span data-stu-id="c0548-475">Hot key is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**finestra di errore \_ non finestra di \_ \_ dialogo**</span><span class="sxs-lookup"><span data-stu-id="c0548-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**ERROR\_WINDOW\_NOT\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-477">1420 (0x58C)</span><span class="sxs-lookup"><span data-stu-id="c0548-477">1420 (0x58C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-478">La finestra non è una finestra di dialogo valida.</span><span class="sxs-lookup"><span data-stu-id="c0548-478">The window is not a valid dialog window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**\_ID controllo \_ errore \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="c0548-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ERROR\_CONTROL\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-480">1421 (0x58D)</span><span class="sxs-lookup"><span data-stu-id="c0548-480">1421 (0x58D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-481">ID controllo non trovato.</span><span class="sxs-lookup"><span data-stu-id="c0548-481">Control ID not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERRORE \_ \_ messaggio ComboBox non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR\_INVALID\_COMBOBOX\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-483">1422 (0x58E)</span><span class="sxs-lookup"><span data-stu-id="c0548-483">1422 (0x58E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-484">Messaggio non valido per una casella combinata perché non contiene un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c0548-484">Invalid message for a combo box because it does not have an edit control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**finestra di errore \_ \_ non \_ ComboBox**</span><span class="sxs-lookup"><span data-stu-id="c0548-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ERROR\_WINDOW\_NOT\_COMBOBOX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-486">1423 (0x58F)</span><span class="sxs-lookup"><span data-stu-id="c0548-486">1423 (0x58F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-487">La finestra non è una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="c0548-487">The window is not a combo box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERRORE \_ di \_ modifica \_ altezza non valida**</span><span class="sxs-lookup"><span data-stu-id="c0548-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR\_INVALID\_EDIT\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-489">1424 (0x590)</span><span class="sxs-lookup"><span data-stu-id="c0548-489">1424 (0x590)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-490">L'altezza deve essere minore di 256.</span><span class="sxs-lookup"><span data-stu-id="c0548-490">Height must be less than 256.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERRORE \_ DC \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="c0548-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERROR\_DC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-492">1425 (0x591)</span><span class="sxs-lookup"><span data-stu-id="c0548-492">1425 (0x591)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-493">Handle del contesto di dispositivo (DC) non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-493">Invalid device context (DC) handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERRORE \_ di \_ filtro hook non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR\_INVALID\_HOOK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-495">1426 (0x592)</span><span class="sxs-lookup"><span data-stu-id="c0548-495">1426 (0x592)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-496">Tipo di routine hook non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-496">Invalid hook procedure type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERRORE \_ \_ processo filtro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR\_INVALID\_FILTER\_PROC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-498">1427 (0x593)</span><span class="sxs-lookup"><span data-stu-id="c0548-498">1427 (0x593)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-499">Routine hook non valida.</span><span class="sxs-lookup"><span data-stu-id="c0548-499">Invalid hook procedure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**l' \_ hook di errore \_ richiede \_ HMOD**</span><span class="sxs-lookup"><span data-stu-id="c0548-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**ERROR\_HOOK\_NEEDS\_HMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-501">1428 (0x594)</span><span class="sxs-lookup"><span data-stu-id="c0548-501">1428 (0x594)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-502">Impossibile impostare un hook non locale senza un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="c0548-502">Cannot set nonlocal hook without a module handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**\_ \_ Hook solo globale \_ errori**</span><span class="sxs-lookup"><span data-stu-id="c0548-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR\_GLOBAL\_ONLY\_HOOK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-504">1429 (0x595)</span><span class="sxs-lookup"><span data-stu-id="c0548-504">1429 (0x595)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-505">Questa procedura di hook può essere impostata solo a livello globale.</span><span class="sxs-lookup"><span data-stu-id="c0548-505">This hook procedure can only be set globally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_set di \_ hook del journal degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**ERROR\_JOURNAL\_HOOK\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-507">1430 (0x596)</span><span class="sxs-lookup"><span data-stu-id="c0548-507">1430 (0x596)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-508">La procedura di hook del journal è già installata.</span><span class="sxs-lookup"><span data-stu-id="c0548-508">The journal hook procedure is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**HOOK di errore \_ \_ non \_ installato**</span><span class="sxs-lookup"><span data-stu-id="c0548-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR\_HOOK\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-510">1431 (0x597)</span><span class="sxs-lookup"><span data-stu-id="c0548-510">1431 (0x597)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-511">La procedura hook non è installata.</span><span class="sxs-lookup"><span data-stu-id="c0548-511">The hook procedure is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERRORE \_ del \_ messaggio LB non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR\_INVALID\_LB\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-513">1432 (0x598)</span><span class="sxs-lookup"><span data-stu-id="c0548-513">1432 (0x598)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-514">Messaggio non valido per la casella di riepilogo a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="c0548-514">Invalid message for single-selection list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERRORE \_ di conteggio \_ su \_ LB non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR\_SETCOUNT\_ON\_BAD\_LB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-516">1433 (0x599)</span><span class="sxs-lookup"><span data-stu-id="c0548-516">1433 (0x599)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-517">Il conteggio LB è stato \_ inviato a una casella di riepilogo non lazy.</span><span class="sxs-lookup"><span data-stu-id="c0548-517">LB\_SETCOUNT sent to non-lazy list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERRORE \_ lb \_ senza \_ TABSTOPS**</span><span class="sxs-lookup"><span data-stu-id="c0548-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR\_LB\_WITHOUT\_TABSTOPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-519">1434 (0x59A)</span><span class="sxs-lookup"><span data-stu-id="c0548-519">1434 (0x59A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-520">Questa casella di riepilogo non supporta le tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="c0548-520">This list box does not support tab stops.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**errore durante l' \_ eliminazione \_ \_ dell'oggetto di un \_ altro \_ thread**</span><span class="sxs-lookup"><span data-stu-id="c0548-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR\_DESTROY\_OBJECT\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-522">1435 (0x59B)</span><span class="sxs-lookup"><span data-stu-id="c0548-522">1435 (0x59B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-523">Non è possibile eliminare definitivamente l'oggetto creato da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="c0548-523">Cannot destroy object created by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_ \_ menu finestra figlio di errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**ERROR\_CHILD\_WINDOW\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-525">1436 (0x59C)</span><span class="sxs-lookup"><span data-stu-id="c0548-525">1436 (0x59C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-526">Le finestre figlio non possono disporre di menu.</span><span class="sxs-lookup"><span data-stu-id="c0548-526">Child windows cannot have menus.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERRORE \_ nessun \_ menu di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR\_NO\_SYSTEM\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-528">1437 (0x59D)</span><span class="sxs-lookup"><span data-stu-id="c0548-528">1437 (0x59D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-529">La finestra non dispone di un menu di sistema.</span><span class="sxs-lookup"><span data-stu-id="c0548-529">The window does not have a system menu.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERRORE \_ di \_ tipo MsgBox non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR\_INVALID\_MSGBOX\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-531">1438 (0x59E)</span><span class="sxs-lookup"><span data-stu-id="c0548-531">1438 (0x59E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-532">Stile della finestra di messaggio non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-532">Invalid message box style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERRORE \_ \_ valore SPI non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR\_INVALID\_SPI\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-534">1439 (0x59F)</span><span class="sxs-lookup"><span data-stu-id="c0548-534">1439 (0x59F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-535">Parametro non valido a livello di sistema (SPI \_ \* ).</span><span class="sxs-lookup"><span data-stu-id="c0548-535">Invalid system-wide (SPI\_\*) parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**schermata di errore \_ \_ già \_ bloccata**</span><span class="sxs-lookup"><span data-stu-id="c0548-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**ERROR\_SCREEN\_ALREADY\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-537">1440 (0x5A0)</span><span class="sxs-lookup"><span data-stu-id="c0548-537">1440 (0x5A0)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-538">Schermata già bloccata.</span><span class="sxs-lookup"><span data-stu-id="c0548-538">Screen already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**gli \_ HWND degli errori \_ hanno un \_ \_ elemento padre diff**</span><span class="sxs-lookup"><span data-stu-id="c0548-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR\_HWNDS\_HAVE\_DIFF\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-540">1441 (0x5A1)</span><span class="sxs-lookup"><span data-stu-id="c0548-540">1441 (0x5A1)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-541">Tutti gli handle di Windows in una struttura di posizione a più finestre devono avere lo stesso elemento padre.</span><span class="sxs-lookup"><span data-stu-id="c0548-541">All handles to windows in a multiple-window position structure must have the same parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERRORE \_ non \_ \_ finestra figlio**</span><span class="sxs-lookup"><span data-stu-id="c0548-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR\_NOT\_CHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-543">1442 (0x5A2)</span><span class="sxs-lookup"><span data-stu-id="c0548-543">1442 (0x5A2)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-544">La finestra non è una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="c0548-544">The window is not a child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERRORE \_ del \_ comando GW non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR\_INVALID\_GW\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-546">1443 (0x5A3)</span><span class="sxs-lookup"><span data-stu-id="c0548-546">1443 (0x5A3)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-547">Comando GW non valido \_ \* .</span><span class="sxs-lookup"><span data-stu-id="c0548-547">Invalid GW\_\* command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERRORE \_ \_ ID thread non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR\_INVALID\_THREAD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-549">1444 (0x5A4)</span><span class="sxs-lookup"><span data-stu-id="c0548-549">1444 (0x5A4)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-550">Identificatore thread non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-550">Invalid thread identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERRORE \_ non \_ MDIChild \_ finestra**</span><span class="sxs-lookup"><span data-stu-id="c0548-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR\_NON\_MDICHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-552">1445 (0x5A5)</span><span class="sxs-lookup"><span data-stu-id="c0548-552">1445 (0x5A5)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-553">Impossibile elaborare un messaggio da una finestra che non è una finestra con interfaccia a documenti multipli (MDI).</span><span class="sxs-lookup"><span data-stu-id="c0548-553">Cannot process a message from a window that is not a multiple document interface (MDI) window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**\_popup errore \_ già \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="c0548-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR\_POPUP\_ALREADY\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-555">1446 (0x5A6)</span><span class="sxs-lookup"><span data-stu-id="c0548-555">1446 (0x5A6)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-556">Menu popup già attivo.</span><span class="sxs-lookup"><span data-stu-id="c0548-556">Popup menu already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERRORE \_ Nessuna \_ barra di scorrimento**</span><span class="sxs-lookup"><span data-stu-id="c0548-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR\_NO\_SCROLLBARS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-558">1447 (0x5A7)</span><span class="sxs-lookup"><span data-stu-id="c0548-558">1447 (0x5A7)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-559">Per la finestra non sono disponibili barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="c0548-559">The window does not have scroll bars.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERRORE \_ nell' \_ intervallo della barra di scorrimento non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR\_INVALID\_SCROLLBAR\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-561">1448 (0x5A8)</span><span class="sxs-lookup"><span data-stu-id="c0548-561">1448 (0x5A8)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-562">L'intervallo della barra di scorrimento non può essere maggiore di MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="c0548-562">Scroll bar range cannot be greater than MAXLONG.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERRORE \_ \_ comando SHOWWIN non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR\_INVALID\_SHOWWIN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-564">1449 (0x5A9)</span><span class="sxs-lookup"><span data-stu-id="c0548-564">1449 (0x5A9)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-565">Impossibile visualizzare o rimuovere la finestra nel modo specificato.</span><span class="sxs-lookup"><span data-stu-id="c0548-565">Cannot show or remove the window in the way specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERRORE \_ senza \_ risorse di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR\_NO\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-567">1450 (0x5AA)</span><span class="sxs-lookup"><span data-stu-id="c0548-567">1450 (0x5AA)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-568">Risorse di sistema insufficienti per completare il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="c0548-568">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERRORE di risorse di sistema non di \_ paging \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR\_NONPAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-570">1451 (0x5AB)</span><span class="sxs-lookup"><span data-stu-id="c0548-570">1451 (0x5AB)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-571">Risorse di sistema insufficienti per completare il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="c0548-571">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERRORE di \_ paging \_ \_ delle risorse di sistema**</span><span class="sxs-lookup"><span data-stu-id="c0548-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERROR\_PAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-573">1452 (0x5AC)</span><span class="sxs-lookup"><span data-stu-id="c0548-573">1452 (0x5AC)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-574">Risorse di sistema insufficienti per completare il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="c0548-574">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**\_quota working \_ set di errori \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERROR\_WORKING\_SET\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-576">1453 (0x5AD)</span><span class="sxs-lookup"><span data-stu-id="c0548-576">1453 (0x5AD)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-577">Quota insufficiente per completare il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="c0548-577">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**\_quota di paging degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERROR\_PAGEFILE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-579">1454 (0x5AE)</span><span class="sxs-lookup"><span data-stu-id="c0548-579">1454 (0x5AE)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-580">Quota insufficiente per completare il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="c0548-580">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_Limite impegno \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**ERROR\_COMMITMENT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-582">1455 (0x5AF)</span><span class="sxs-lookup"><span data-stu-id="c0548-582">1455 (0x5AF)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-583">Il file di paging è troppo piccolo per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-583">The paging file is too small for this operation to complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**\_ \_ \_ Impossibile trovare la voce di menu di errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ERROR\_MENU\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-585">1456 (0x5B0)</span><span class="sxs-lookup"><span data-stu-id="c0548-585">1456 (0x5B0)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-586">Una voce di menu non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="c0548-586">A menu item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERRORE \_ di \_ handle di tastiera non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR\_INVALID\_KEYBOARD\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-588">1457 (0x5B1)</span><span class="sxs-lookup"><span data-stu-id="c0548-588">1457 (0x5B1)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-589">Handle layout tastiera non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-589">Invalid keyboard layout handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**\_tipo di hook errore \_ \_ non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="c0548-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**ERROR\_HOOK\_TYPE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-591">1458 (0x5B2)</span><span class="sxs-lookup"><span data-stu-id="c0548-591">1458 (0x5B2)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-592">Il tipo di hook non è consentito.</span><span class="sxs-lookup"><span data-stu-id="c0548-592">Hook type not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**per errore è \_ necessario \_ Interactive \_ WINDOWSTATION**</span><span class="sxs-lookup"><span data-stu-id="c0548-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERROR\_REQUIRES\_INTERACTIVE\_WINDOWSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-594">1459 (0x5B3)</span><span class="sxs-lookup"><span data-stu-id="c0548-594">1459 (0x5B3)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-595">Questa operazione richiede una stazione finestra interattiva.</span><span class="sxs-lookup"><span data-stu-id="c0548-595">This operation requires an interactive window station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**\_timeout errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**ERROR\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-597">1460 (0x5B4)</span><span class="sxs-lookup"><span data-stu-id="c0548-597">1460 (0x5B4)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-598">Questa operazione è stata restituita perché il periodo di timeout è scaduto.</span><span class="sxs-lookup"><span data-stu-id="c0548-598">This operation returned because the timeout period expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERRORE \_ di \_ handle di monitoraggio non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR\_INVALID\_MONITOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-600">1461 (0x5B5)</span><span class="sxs-lookup"><span data-stu-id="c0548-600">1461 (0x5B5)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-601">Handle di monitoraggio non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-601">Invalid monitor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERRORE \_ di \_ dimensioni errate**</span><span class="sxs-lookup"><span data-stu-id="c0548-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR\_INCORRECT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-603">1462 (0x5B6)</span><span class="sxs-lookup"><span data-stu-id="c0548-603">1462 (0x5B6)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-604">Argomento di dimensione errato.</span><span class="sxs-lookup"><span data-stu-id="c0548-604">Incorrect size argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**\_classe del collegamento simbolico Error \_ \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="c0548-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR\_SYMLINK\_CLASS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-606">1463 (0x5B7)</span><span class="sxs-lookup"><span data-stu-id="c0548-606">1463 (0x5B7)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-607">Non è possibile seguire il collegamento simbolico perché il tipo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c0548-607">The symbolic link cannot be followed because its type is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**\_collegamento simbolico errore \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="c0548-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR\_SYMLINK\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-609">1464 (0x5B8)</span><span class="sxs-lookup"><span data-stu-id="c0548-609">1464 (0x5B8)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-610">Questa applicazione non supporta l'operazione corrente sui collegamenti simbolici.</span><span class="sxs-lookup"><span data-stu-id="c0548-610">This application does not support the current operation on symbolic links.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**errore \_ di \_ analisi XML errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR\_XML\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-612">1465 (0x5B9)</span><span class="sxs-lookup"><span data-stu-id="c0548-612">1465 (0x5B9)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-613">Windows non è riuscito ad analizzare i dati XML richiesti.</span><span class="sxs-lookup"><span data-stu-id="c0548-613">Windows was unable to parse the requested XML data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**errore \_ XMLDSIG \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERROR\_XMLDSIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-615">1466 (0x5BA)</span><span class="sxs-lookup"><span data-stu-id="c0548-615">1466 (0x5BA)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-616">Si è verificato un errore durante l'elaborazione di una firma digitale XML.</span><span class="sxs-lookup"><span data-stu-id="c0548-616">An error was encountered while processing an XML digital signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**errore durante il \_ riavvio \_ dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="c0548-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR\_RESTART\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-618">1467 (0x5BB)</span><span class="sxs-lookup"><span data-stu-id="c0548-618">1467 (0x5BB)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-619">Questa applicazione deve essere riavviata.</span><span class="sxs-lookup"><span data-stu-id="c0548-619">This application must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERRORE \_ nel \_ raggruppamento**</span><span class="sxs-lookup"><span data-stu-id="c0548-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERROR\_WRONG\_COMPARTMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-621">1468 (0x5BC)</span><span class="sxs-lookup"><span data-stu-id="c0548-621">1468 (0x5BC)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-622">Il chiamante ha effettuato la richiesta di connessione nel raggruppamento di routing errato.</span><span class="sxs-lookup"><span data-stu-id="c0548-622">The caller made the connection request in the wrong routing compartment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERRORE \_ AUTHIP non \_ riuscito**</span><span class="sxs-lookup"><span data-stu-id="c0548-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR\_AUTHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-624">1469 (0x5BD)</span><span class="sxs-lookup"><span data-stu-id="c0548-624">1469 (0x5BD)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-625">Si è verificato un errore AuthIP durante il tentativo di connessione all'host remoto.</span><span class="sxs-lookup"><span data-stu-id="c0548-625">There was an AuthIP failure when attempting to connect to the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERRORE \_ Nessuna \_ \_ risorsa NVRAM**</span><span class="sxs-lookup"><span data-stu-id="c0548-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR\_NO\_NVRAM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-627">1470 (0x5BE)</span><span class="sxs-lookup"><span data-stu-id="c0548-627">1470 (0x5BE)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-628">Per completare il servizio richiesto sono disponibili risorse NVRAM insufficienti.</span><span class="sxs-lookup"><span data-stu-id="c0548-628">Insufficient NVRAM resources exist to complete the requested service.</span></span> <span data-ttu-id="c0548-629">Potrebbe essere necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="c0548-629">A reboot might be required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**errore durante il \_ \_ processo di GUI \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR\_NOT\_GUI\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-631">1471 (0x5BF)</span><span class="sxs-lookup"><span data-stu-id="c0548-631">1471 (0x5BF)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-632">Non è possibile completare l'operazione richiesta perché il processo specificato non è un processo GUI.</span><span class="sxs-lookup"><span data-stu-id="c0548-632">Unable to finish the requested operation because the specified process is not a GUI process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERRORE \_ del \_ file EventLog \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="c0548-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERROR\_EVENTLOG\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-634">1500 (0x5DC)</span><span class="sxs-lookup"><span data-stu-id="c0548-634">1500 (0x5DC)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-635">Il file di registro eventi è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="c0548-635">The event log file is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**\_ \_ Impossibile avviare il log eventi di errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR\_EVENTLOG\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-637">1501 (0x5DD)</span><span class="sxs-lookup"><span data-stu-id="c0548-637">1501 (0x5DD)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-638">Non è stato possibile aprire alcun file di registro eventi, quindi il servizio di registrazione eventi non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="c0548-638">No event log file could be opened, so the event logging service did not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**FILE di log degli errori \_ \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="c0548-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**ERROR\_LOG\_FILE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-640">1502 (0x5DE)</span><span class="sxs-lookup"><span data-stu-id="c0548-640">1502 (0x5DE)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-641">Il file del registro eventi è pieno.</span><span class="sxs-lookup"><span data-stu-id="c0548-641">The event log file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERRORE \_ del \_ file EventLog \_ modificato**</span><span class="sxs-lookup"><span data-stu-id="c0548-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERROR\_EVENTLOG\_FILE\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-643">1503 (0x5DF)</span><span class="sxs-lookup"><span data-stu-id="c0548-643">1503 (0x5DF)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-644">Il file di registro eventi è stato modificato tra le operazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="c0548-644">The event log file has changed between read operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERRORE \_ \_ nome attività non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR\_INVALID\_TASK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-646">1550 (0x60E)</span><span class="sxs-lookup"><span data-stu-id="c0548-646">1550 (0x60E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-647">Il nome dell'attività specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-647">The specified task name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERRORE \_ \_ Indice attività non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR\_INVALID\_TASK\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-649">1551 (0x60F)</span><span class="sxs-lookup"><span data-stu-id="c0548-649">1551 (0x60F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-650">L'indice dell'attività specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-650">The specified task index is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_thread \_ di errore già presente \_ nell' \_ attività**</span><span class="sxs-lookup"><span data-stu-id="c0548-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**ERROR\_THREAD\_ALREADY\_IN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-652">1552 (0x610)</span><span class="sxs-lookup"><span data-stu-id="c0548-652">1552 (0x610)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-653">Il thread specificato è già Unito in join a un'attività.</span><span class="sxs-lookup"><span data-stu-id="c0548-653">The specified thread is already joining a task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERRORE di \_ installazione del \_ servizio \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR\_INSTALL\_SERVICE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-655">1601 (0x641)</span><span class="sxs-lookup"><span data-stu-id="c0548-655">1601 (0x641)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-656">Impossibile accedere al servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0548-656">The Windows Installer Service could not be accessed.</span></span> <span data-ttu-id="c0548-657">Questo problema può verificarsi se la Windows Installer non è installata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c0548-657">This can occur if the Windows Installer is not correctly installed.</span></span> <span data-ttu-id="c0548-658">Per assistenza, contattare il personale di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0548-658">Contact your support personnel for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERRORE di \_ installazione di \_ USEREXIT**</span><span class="sxs-lookup"><span data-stu-id="c0548-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR\_INSTALL\_USEREXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-660">1602 (0x642)</span><span class="sxs-lookup"><span data-stu-id="c0548-660">1602 (0x642)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-661">Installazione annullata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c0548-661">User cancelled installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERRORE di \_ installazione \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR\_INSTALL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-663">1603 (0x643)</span><span class="sxs-lookup"><span data-stu-id="c0548-663">1603 (0x643)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-664">Errore irreversibile durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-664">Fatal error during installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERRORE \_ installazione \_ sospensione**</span><span class="sxs-lookup"><span data-stu-id="c0548-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR\_INSTALL\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-666">1604 (0x644)</span><span class="sxs-lookup"><span data-stu-id="c0548-666">1604 (0x644)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-667">Installazione sospesa, incompleta.</span><span class="sxs-lookup"><span data-stu-id="c0548-667">Installation suspended, incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERRORE \_ \_ prodotto sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="c0548-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR\_UNKNOWN\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-669">1605 (0x645)</span><span class="sxs-lookup"><span data-stu-id="c0548-669">1605 (0x645)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-670">Questa azione è valida solo per i prodotti attualmente installati.</span><span class="sxs-lookup"><span data-stu-id="c0548-670">This action is only valid for products that are currently installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**\_funzionalità sconosciuta di errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR\_UNKNOWN\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-672">1606 (0x646)</span><span class="sxs-lookup"><span data-stu-id="c0548-672">1606 (0x646)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-673">ID funzionalità non registrato.</span><span class="sxs-lookup"><span data-stu-id="c0548-673">Feature ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERRORE \_ \_ componente sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="c0548-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR\_UNKNOWN\_COMPONENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-675">1607 (0x647)</span><span class="sxs-lookup"><span data-stu-id="c0548-675">1607 (0x647)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-676">ID componente non registrato.</span><span class="sxs-lookup"><span data-stu-id="c0548-676">Component ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERRORE \_ \_ proprietà sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="c0548-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR\_UNKNOWN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-678">1608 (0x648)</span><span class="sxs-lookup"><span data-stu-id="c0548-678">1608 (0x648)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-679">Proprietà sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="c0548-679">Unknown property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERRORE \_ di \_ handle non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR\_INVALID\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-681">1609 (0x649)</span><span class="sxs-lookup"><span data-stu-id="c0548-681">1609 (0x649)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-682">Lo stato dell'handle non è valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-682">Handle is in an invalid state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERRORE \_ configurazione errata \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR\_BAD\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-684">1610 (0x64A)</span><span class="sxs-lookup"><span data-stu-id="c0548-684">1610 (0x64A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-685">I dati di configurazione per questo prodotto sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="c0548-685">The configuration data for this product is corrupt.</span></span> <span data-ttu-id="c0548-686">Contattare il personale di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0548-686">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**\_indice errore \_ assente**</span><span class="sxs-lookup"><span data-stu-id="c0548-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**ERROR\_INDEX\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-688">1611 (0x64B)</span><span class="sxs-lookup"><span data-stu-id="c0548-688">1611 (0x64B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-689">Qualificatore componente non presente.</span><span class="sxs-lookup"><span data-stu-id="c0548-689">Component qualifier not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERRORE \_ di \_ origine installazione \_ assente**</span><span class="sxs-lookup"><span data-stu-id="c0548-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERROR\_INSTALL\_SOURCE\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-691">1612 (0x64C)</span><span class="sxs-lookup"><span data-stu-id="c0548-691">1612 (0x64C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-692">L'origine di installazione per questo prodotto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="c0548-692">The installation source for this product is not available.</span></span> <span data-ttu-id="c0548-693">Verificare che l'origine esista e che sia possibile accedervi.</span><span class="sxs-lookup"><span data-stu-id="c0548-693">Verify that the source exists and that you can access it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERRORE di \_ installazione della \_ versione del pacchetto \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR\_INSTALL\_PACKAGE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-695">1613 (0x64D)</span><span class="sxs-lookup"><span data-stu-id="c0548-695">1613 (0x64D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-696">Questo pacchetto di installazione non può essere installato dal servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0548-696">This installation package cannot be installed by the Windows Installer service.</span></span> <span data-ttu-id="c0548-697">È necessario installare un Service Pack Windows che contenga una versione più recente del servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0548-697">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERRORE \_ prodotto \_ disinstallato**</span><span class="sxs-lookup"><span data-stu-id="c0548-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERROR\_PRODUCT\_UNINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-699">1614 (0x64E)</span><span class="sxs-lookup"><span data-stu-id="c0548-699">1614 (0x64E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-700">Il prodotto viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="c0548-700">Product is uninstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**\_sintassi di \_ query ERRAta errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR\_BAD\_QUERY\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-702">1615 (0x64F)</span><span class="sxs-lookup"><span data-stu-id="c0548-702">1615 (0x64F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-703">Sintassi di query SQL non valida o non supportata.</span><span class="sxs-lookup"><span data-stu-id="c0548-703">SQL query syntax invalid or unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERRORE \_ campo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR\_INVALID\_FIELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-705">1616 (0x650)</span><span class="sxs-lookup"><span data-stu-id="c0548-705">1616 (0x650)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-706">Il campo del record non esiste.</span><span class="sxs-lookup"><span data-stu-id="c0548-706">Record field does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**dispositivo di errore \_ \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="c0548-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**ERROR\_DEVICE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-708">1617 (0x651)</span><span class="sxs-lookup"><span data-stu-id="c0548-708">1617 (0x651)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-709">Il dispositivo è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="c0548-709">The device has been removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERRORE di \_ installazione \_ già \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="c0548-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERROR\_INSTALL\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-711">1618 (0x652)</span><span class="sxs-lookup"><span data-stu-id="c0548-711">1618 (0x652)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-712">È già in corso un'altra installazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-712">Another installation is already in progress.</span></span> <span data-ttu-id="c0548-713">Completare l'installazione prima di procedere con questa installazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-713">Complete that installation before proceeding with this install.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERRORE \_ di \_ installazione \_ apertura pacchetto \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="c0548-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR\_INSTALL\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-715">1619 (0x653)</span><span class="sxs-lookup"><span data-stu-id="c0548-715">1619 (0x653)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-716">Non è stato possibile aprire questo pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-716">This installation package could not be opened.</span></span> <span data-ttu-id="c0548-717">Verificare che il pacchetto esista e che sia possibile accedervi oppure contattare il fornitore dell'applicazione per verificare che si tratta di un pacchetto di Windows Installer valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-717">Verify that the package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERRORE di \_ installazione \_ pacchetto \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="c0548-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR\_INSTALL\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-719">1620 (0x654)</span><span class="sxs-lookup"><span data-stu-id="c0548-719">1620 (0x654)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-720">Non è stato possibile aprire questo pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-720">This installation package could not be opened.</span></span> <span data-ttu-id="c0548-721">Contattare il fornitore dell'applicazione per verificare che si tratta di un pacchetto di Windows Installer valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-721">Contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERRORE di \_ installazione \_ dell'interfaccia utente \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR\_INSTALL\_UI\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-723">1621 (0x655)</span><span class="sxs-lookup"><span data-stu-id="c0548-723">1621 (0x655)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-724">Si è verificato un errore durante l'avvio dell'interfaccia utente del servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0548-724">There was an error starting the Windows Installer service user interface.</span></span> <span data-ttu-id="c0548-725">Contattare il personale di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0548-725">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**errore durante l' \_ installazione del \_ log \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR\_INSTALL\_LOG\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-727">1622 (0x656)</span><span class="sxs-lookup"><span data-stu-id="c0548-727">1622 (0x656)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-728">Errore durante l'apertura del file di log dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="c0548-728">Error opening installation log file.</span></span> <span data-ttu-id="c0548-729">Verificare che il percorso del file di log specificato esista e che sia possibile scrivervi.</span><span class="sxs-lookup"><span data-stu-id="c0548-729">Verify that the specified log file location exists and that you can write to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERRORE di \_ installazione della \_ lingua non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="c0548-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERROR\_INSTALL\_LANGUAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-731">1623 (0x657)</span><span class="sxs-lookup"><span data-stu-id="c0548-731">1623 (0x657)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-732">La lingua del pacchetto di installazione non è supportata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c0548-732">The language of this installation package is not supported by your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**errore durante l' \_ installazione della \_ trasformazione \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR\_INSTALL\_TRANSFORM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-734">1624 (0x658)</span><span class="sxs-lookup"><span data-stu-id="c0548-734">1624 (0x658)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-735">Errore durante l'applicazione delle trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="c0548-735">Error applying transforms.</span></span> <span data-ttu-id="c0548-736">Verificare che i percorsi di trasformazione specificati siano validi.</span><span class="sxs-lookup"><span data-stu-id="c0548-736">Verify that the specified transform paths are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERRORE di \_ installazione del \_ pacchetto \_ rifiutato**</span><span class="sxs-lookup"><span data-stu-id="c0548-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR\_INSTALL\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-738">1625 (0x659)</span><span class="sxs-lookup"><span data-stu-id="c0548-738">1625 (0x659)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-739">Questa installazione non è consentita dai criteri di sistema.</span><span class="sxs-lookup"><span data-stu-id="c0548-739">This installation is forbidden by system policy.</span></span> <span data-ttu-id="c0548-740">Contattare l'amministratore del sistema.</span><span class="sxs-lookup"><span data-stu-id="c0548-740">Contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**funzione di errore \_ \_ non \_ chiamata**</span><span class="sxs-lookup"><span data-stu-id="c0548-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**ERROR\_FUNCTION\_NOT\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-742">1626 (0x65A)</span><span class="sxs-lookup"><span data-stu-id="c0548-742">1626 (0x65A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-743">Non è stato possibile eseguire la funzione.</span><span class="sxs-lookup"><span data-stu-id="c0548-743">Function could not be executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**\_funzione Error \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="c0548-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR\_FUNCTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-745">1627 (0x65B)</span><span class="sxs-lookup"><span data-stu-id="c0548-745">1627 (0x65B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-746">Funzione non riuscita durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c0548-746">Function failed during execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERRORE \_ di \_ tabella non valida**</span><span class="sxs-lookup"><span data-stu-id="c0548-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR\_INVALID\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-748">1628 (0x65C)</span><span class="sxs-lookup"><span data-stu-id="c0548-748">1628 (0x65C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-749">La tabella specificata non è valida o è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="c0548-749">Invalid or unknown table specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERRORE \_ di \_ MANCAta corrispondenza del tipo di dati**</span><span class="sxs-lookup"><span data-stu-id="c0548-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-751">1629 (0x65D)</span><span class="sxs-lookup"><span data-stu-id="c0548-751">1629 (0x65D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-752">Il tipo dei dati forniti non è corretto.</span><span class="sxs-lookup"><span data-stu-id="c0548-752">Data supplied is of wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERRORE \_ tipo non supportato \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-754">1630 (0x65E)</span><span class="sxs-lookup"><span data-stu-id="c0548-754">1630 (0x65E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-755">I dati di questo tipo non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="c0548-755">Data of this type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**\_creazione errore \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="c0548-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-757">1631 (0x65F)</span><span class="sxs-lookup"><span data-stu-id="c0548-757">1631 (0x65F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-758">Impossibile avviare il servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0548-758">The Windows Installer service failed to start.</span></span> <span data-ttu-id="c0548-759">Contattare il personale di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0548-759">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERRORE di \_ installazione \_ Temp non \_ scrivibile**</span><span class="sxs-lookup"><span data-stu-id="c0548-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR\_INSTALL\_TEMP\_UNWRITABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-761">1632 (0x660)</span><span class="sxs-lookup"><span data-stu-id="c0548-761">1632 (0x660)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-762">La cartella Temp si trova in un'unità completa o inaccessibile.</span><span class="sxs-lookup"><span data-stu-id="c0548-762">The Temp folder is on a drive that is full or is inaccessible.</span></span> <span data-ttu-id="c0548-763">Liberare spazio nell'unità o verificare di disporre dell'autorizzazione di scrittura per la cartella Temp.</span><span class="sxs-lookup"><span data-stu-id="c0548-763">Free up space on the drive or verify that you have write permission on the Temp folder.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERRORE di \_ installazione della \_ piattaforma non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="c0548-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR\_INSTALL\_PLATFORM\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-765">1633 (0x661)</span><span class="sxs-lookup"><span data-stu-id="c0548-765">1633 (0x661)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-766">Questo pacchetto di installazione non è supportato da questo tipo di processore.</span><span class="sxs-lookup"><span data-stu-id="c0548-766">This installation package is not supported by this processor type.</span></span> <span data-ttu-id="c0548-767">Contattare il fornitore del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c0548-767">Contact your product vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERRORE di \_ installazione di \_ abituata**</span><span class="sxs-lookup"><span data-stu-id="c0548-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR\_INSTALL\_NOTUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-769">1634 (0x662)</span><span class="sxs-lookup"><span data-stu-id="c0548-769">1634 (0x662)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-770">Componente non usato in questo computer.</span><span class="sxs-lookup"><span data-stu-id="c0548-770">Component not used on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERRORE \_ di \_ apertura del pacchetto di patch \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR\_PATCH\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-772">1635 (0x663)</span><span class="sxs-lookup"><span data-stu-id="c0548-772">1635 (0x663)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-773">Non è stato possibile aprire il pacchetto di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c0548-773">This update package could not be opened.</span></span> <span data-ttu-id="c0548-774">Verificare che il pacchetto di aggiornamento esista e che sia possibile accedervi oppure contattare il fornitore dell'applicazione per verificare che si tratta di un pacchetto di aggiornamento Windows Installer valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-774">Verify that the update package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERRORE \_ \_ pacchetto patch \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="c0548-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERROR\_PATCH\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-776">1636 (0x664)</span><span class="sxs-lookup"><span data-stu-id="c0548-776">1636 (0x664)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-777">Non è stato possibile aprire il pacchetto di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c0548-777">This update package could not be opened.</span></span> <span data-ttu-id="c0548-778">Contattare il fornitore dell'applicazione per verificare che si tratta di un pacchetto di aggiornamento Windows Installer valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-778">Contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**pacchetto di patch di errore non \_ \_ \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="c0548-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERROR\_PATCH\_PACKAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-780">1637 (0x665)</span><span class="sxs-lookup"><span data-stu-id="c0548-780">1637 (0x665)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-781">Il pacchetto di aggiornamento non può essere elaborato dal servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0548-781">This update package cannot be processed by the Windows Installer service.</span></span> <span data-ttu-id="c0548-782">È necessario installare un Service Pack Windows che contenga una versione più recente del servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0548-782">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_versione prodotto \_ errore**</span><span class="sxs-lookup"><span data-stu-id="c0548-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERROR\_PRODUCT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-784">1638 (0x666)</span><span class="sxs-lookup"><span data-stu-id="c0548-784">1638 (0x666)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-785">È già installata un'altra versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c0548-785">Another version of this product is already installed.</span></span> <span data-ttu-id="c0548-786">Non è possibile continuare l'installazione di questa versione.</span><span class="sxs-lookup"><span data-stu-id="c0548-786">Installation of this version cannot continue.</span></span> <span data-ttu-id="c0548-787">Per configurare o rimuovere la versione esistente di questo prodotto, utilizzare Installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="c0548-787">To configure or remove the existing version of this product, use Add/Remove Programs on the Control Panel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERRORE \_ della \_ riga di comando non valida \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR\_INVALID\_COMMAND\_LINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-789">1639 (0x667)</span><span class="sxs-lookup"><span data-stu-id="c0548-789">1639 (0x667)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-790">Argomento della riga di comando non valido.</span><span class="sxs-lookup"><span data-stu-id="c0548-790">Invalid command line argument.</span></span> <span data-ttu-id="c0548-791">Per informazioni dettagliate sulla riga di comando, vedere l'SDK Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0548-791">Consult the Windows Installer SDK for detailed command line help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERRORE di \_ installazione \_ remota non \_ consentita**</span><span class="sxs-lookup"><span data-stu-id="c0548-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR\_INSTALL\_REMOTE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-793">1640 (0x668)</span><span class="sxs-lookup"><span data-stu-id="c0548-793">1640 (0x668)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-794">Solo gli amministratori dispongono dell'autorizzazione per aggiungere, rimuovere o configurare il software server durante una sessione remota di Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="c0548-794">Only administrators have permission to add, remove, or configure server software during a Terminal services remote session.</span></span> <span data-ttu-id="c0548-795">Se si desidera installare o configurare il software sul server, contattare l'amministratore di rete.</span><span class="sxs-lookup"><span data-stu-id="c0548-795">If you want to install or configure software on the server, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERRORE \_ \_ avviato riavvio \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR\_SUCCESS\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-797">1641 (0x669)</span><span class="sxs-lookup"><span data-stu-id="c0548-797">1641 (0x669)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-798">L'operazione richiesta è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c0548-798">The requested operation completed successfully.</span></span> <span data-ttu-id="c0548-799">Il sistema verrà riavviato per rendere effettive le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c0548-799">The system will be restarted so the changes can take effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**destinazione della patch di errore \_ \_ \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="c0548-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERROR\_PATCH\_TARGET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-801">1642 (0x66A)</span><span class="sxs-lookup"><span data-stu-id="c0548-801">1642 (0x66A)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-802">Non è possibile installare l'aggiornamento dal servizio Windows Installer perché il programma da aggiornare potrebbe essere mancante o l'aggiornamento può aggiornare una versione diversa del programma.</span><span class="sxs-lookup"><span data-stu-id="c0548-802">The upgrade cannot be installed by the Windows Installer service because the program to be upgraded may be missing, or the upgrade may update a different version of the program.</span></span> <span data-ttu-id="c0548-803">Verificare che il programma da aggiornare esista nel computer in uso e che l'aggiornamento sia corretto.</span><span class="sxs-lookup"><span data-stu-id="c0548-803">Verify that the program to be upgraded exists on your computer and that you have the correct upgrade.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERRORE \_ \_ pacchetto patch \_ rifiutato**</span><span class="sxs-lookup"><span data-stu-id="c0548-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERROR\_PATCH\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-805">1643 (0x66B)</span><span class="sxs-lookup"><span data-stu-id="c0548-805">1643 (0x66B)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-806">Il pacchetto di aggiornamento non è consentito dai criteri di restrizione software.</span><span class="sxs-lookup"><span data-stu-id="c0548-806">The update package is not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERRORE di \_ installazione della \_ trasformazione \_ rifiutata**</span><span class="sxs-lookup"><span data-stu-id="c0548-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR\_INSTALL\_TRANSFORM\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-808">1644 (0x66C)</span><span class="sxs-lookup"><span data-stu-id="c0548-808">1644 (0x66C)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-809">Una o più personalizzazioni non sono consentite dai criteri di restrizione software.</span><span class="sxs-lookup"><span data-stu-id="c0548-809">One or more customizations are not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERRORE di \_ installazione \_ remota non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="c0548-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR\_INSTALL\_REMOTE\_PROHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-811">1645 (0x66D)</span><span class="sxs-lookup"><span data-stu-id="c0548-811">1645 (0x66D)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-812">Il Windows Installer non consente l'installazione da una Connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c0548-812">The Windows Installer does not permit installation from a Remote Desktop Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**rimozione della patch di errore non \_ \_ \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="c0548-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERROR\_PATCH\_REMOVAL\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-814">1646 (0x66E)</span><span class="sxs-lookup"><span data-stu-id="c0548-814">1646 (0x66E)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-815">La disinstallazione del pacchetto di aggiornamento non è supportata.</span><span class="sxs-lookup"><span data-stu-id="c0548-815">Uninstallation of the update package is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**PATCH di errore \_ sconosciuta \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR\_UNKNOWN\_PATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-817">1647 (0x66F)</span><span class="sxs-lookup"><span data-stu-id="c0548-817">1647 (0x66F)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-818">L'aggiornamento non viene applicato al prodotto.</span><span class="sxs-lookup"><span data-stu-id="c0548-818">The update is not applied to this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERRORE \_ patch \_ Nessuna \_ sequenza**</span><span class="sxs-lookup"><span data-stu-id="c0548-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR\_PATCH\_NO\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-820">1648 (0x670)</span><span class="sxs-lookup"><span data-stu-id="c0548-820">1648 (0x670)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-821">Impossibile trovare una sequenza valida per il set di aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="c0548-821">No valid sequence could be found for the set of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**rimozione della patch di errore non \_ \_ \_ consentita**</span><span class="sxs-lookup"><span data-stu-id="c0548-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERROR\_PATCH\_REMOVAL\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-823">1649 (0x671)</span><span class="sxs-lookup"><span data-stu-id="c0548-823">1649 (0x671)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-824">La rimozione degli aggiornamenti non è consentita dai criteri.</span><span class="sxs-lookup"><span data-stu-id="c0548-824">Update removal was disallowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERRORE \_ \_ XML patch non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR\_INVALID\_PATCH\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-826">1650 (0x672)</span><span class="sxs-lookup"><span data-stu-id="c0548-826">1650 (0x672)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-827">I dati dell'aggiornamento XML non sono validi.</span><span class="sxs-lookup"><span data-stu-id="c0548-827">The XML update data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**\_ \_ \_ prodotto annunciato gestito dalla patch di errore \_**</span><span class="sxs-lookup"><span data-stu-id="c0548-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERROR\_PATCH\_MANAGED\_ADVERTISED\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-829">1651 (0x673)</span><span class="sxs-lookup"><span data-stu-id="c0548-829">1651 (0x673)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-830">Windows Installer non consente l'aggiornamento dei prodotti pubblicizzati gestiti.</span><span class="sxs-lookup"><span data-stu-id="c0548-830">Windows Installer does not permit updating of managed advertised products.</span></span> <span data-ttu-id="c0548-831">Prima di applicare l'aggiornamento, è necessario installare almeno una funzionalità del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c0548-831">At least one feature of the product must be installed before applying the update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERRORE di \_ installazione \_ servizio \_ SafeBoot**</span><span class="sxs-lookup"><span data-stu-id="c0548-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR\_INSTALL\_SERVICE\_SAFEBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-833">1652 (0x674)</span><span class="sxs-lookup"><span data-stu-id="c0548-833">1652 (0x674)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-834">Il servizio Windows Installer non è accessibile in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="c0548-834">The Windows Installer service is not accessible in Safe Mode.</span></span> <span data-ttu-id="c0548-835">Riprovare quando il computer non è in modalità provvisoria oppure è possibile usare Ripristino configurazione di sistema per riportare il computer a uno stato valido precedente.</span><span class="sxs-lookup"><span data-stu-id="c0548-835">Please try again when your computer is not in Safe Mode or you can use System Restore to return your machine to a previous good state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**errore \_ errore \_ veloce \_ eccezione**</span><span class="sxs-lookup"><span data-stu-id="c0548-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR\_FAIL\_FAST\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-837">1653 (0x675)</span><span class="sxs-lookup"><span data-stu-id="c0548-837">1653 (0x675)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-838">Si è verificata un'eccezione di errore veloce.</span><span class="sxs-lookup"><span data-stu-id="c0548-838">A fail fast exception occurred.</span></span> <span data-ttu-id="c0548-839">I gestori di eccezioni non verranno richiamati e il processo verrà terminato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="c0548-839">Exception handlers will not be invoked and the process will be terminated immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0548-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERRORE di \_ installazione \_ rifiutato**</span><span class="sxs-lookup"><span data-stu-id="c0548-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERROR\_INSTALL\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0548-841">1654 (0x676)</span><span class="sxs-lookup"><span data-stu-id="c0548-841">1654 (0x676)</span></span>
</dt> <dt>



<span data-ttu-id="c0548-842">L'app che si sta tentando di eseguire non è supportata in questa versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="c0548-842">The app that you are trying to run is not supported on this version of Windows.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0548-843">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0548-843">Requirements</span></span>



| <span data-ttu-id="c0548-844">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0548-844">Requirement</span></span> | <span data-ttu-id="c0548-845">Valore</span><span class="sxs-lookup"><span data-stu-id="c0548-845">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0548-846">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0548-846">Minimum supported client</span></span><br/> | <span data-ttu-id="c0548-847">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c0548-847">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c0548-848">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0548-848">Minimum supported server</span></span><br/> | <span data-ttu-id="c0548-849">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0548-849">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0548-850">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0548-850">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0548-851"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0548-851"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0548-852">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0548-852">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0548-853">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="c0548-853">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




