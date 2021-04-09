---
description: Descrive i codici di errore 6000-8199 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Codici di errore di sistema (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878021"
---
# <a name="system-error-codes-6000-8199"></a><span data-ttu-id="65444-103">Codici di errore di sistema (6000-8199)</span><span class="sxs-lookup"><span data-stu-id="65444-103">System Error Codes (6000-8199)</span></span>

> [!NOTE]
> <span data-ttu-id="65444-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="65444-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="65444-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="65444-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 6000 a 8199).</span><span class="sxs-lookup"><span data-stu-id="65444-106">The following list describes [system error codes](system-error-codes.md) (errors 6000 to 8199).</span></span> <span data-ttu-id="65444-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="65444-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="65444-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="65444-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="65444-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**crittografia degli errori \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="65444-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR\_ENCRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-110">6000 (0x1770)</span><span class="sxs-lookup"><span data-stu-id="65444-110">6000 (0x1770)</span></span>
</dt> <dt>



<span data-ttu-id="65444-111">Impossibile crittografare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="65444-111">The specified file could not be encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**\_decrittografia errore \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="65444-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERROR\_DECRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-113">6001 (0x1771)</span><span class="sxs-lookup"><span data-stu-id="65444-113">6001 (0x1771)</span></span>
</dt> <dt>



<span data-ttu-id="65444-114">Non è stato possibile decrittografare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="65444-114">The specified file could not be decrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**FILE di errore \_ \_ crittografato**</span><span class="sxs-lookup"><span data-stu-id="65444-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**ERROR\_FILE\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-116">6002 (0x1772)</span><span class="sxs-lookup"><span data-stu-id="65444-116">6002 (0x1772)</span></span>
</dt> <dt>



<span data-ttu-id="65444-117">Il file specificato è crittografato e l'utente non è in grado di decrittografarlo.</span><span class="sxs-lookup"><span data-stu-id="65444-117">The specified file is encrypted and the user does not have the ability to decrypt it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERRORE \_ nessun \_ criterio di ripristino \_**</span><span class="sxs-lookup"><span data-stu-id="65444-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR\_NO\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-119">6003 (0x1773)</span><span class="sxs-lookup"><span data-stu-id="65444-119">6003 (0x1773)</span></span>
</dt> <dt>



<span data-ttu-id="65444-120">Non sono stati configurati criteri di recupero della crittografia validi per questo sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-120">There is no valid encryption recovery policy configured for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERRORE \_ senza \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="65444-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR\_NO\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-122">6004 (0x1774)</span><span class="sxs-lookup"><span data-stu-id="65444-122">6004 (0x1774)</span></span>
</dt> <dt>



<span data-ttu-id="65444-123">Il driver di crittografia necessario non è stato caricato per questo sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-123">The required encryption driver is not loaded for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERRORE \_ \_ EFS errato**</span><span class="sxs-lookup"><span data-stu-id="65444-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR\_WRONG\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-125">6005 (0x1775)</span><span class="sxs-lookup"><span data-stu-id="65444-125">6005 (0x1775)</span></span>
</dt> <dt>



<span data-ttu-id="65444-126">Il file è stato crittografato con un driver di crittografia diverso da quello attualmente caricato.</span><span class="sxs-lookup"><span data-stu-id="65444-126">The file was encrypted with a different encryption driver than is currently loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERRORE \_ nessun \_ \_ tasto utente**</span><span class="sxs-lookup"><span data-stu-id="65444-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR\_NO\_USER\_KEYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-128">6006 (0x1776)</span><span class="sxs-lookup"><span data-stu-id="65444-128">6006 (0x1776)</span></span>
</dt> <dt>



<span data-ttu-id="65444-129">Non sono state definite chiavi EFS per l'utente.</span><span class="sxs-lookup"><span data-stu-id="65444-129">There are no EFS keys defined for the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**FILE di errore \_ \_ non \_ crittografato**</span><span class="sxs-lookup"><span data-stu-id="65444-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**ERROR\_FILE\_NOT\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-131">6007 (0x1777)</span><span class="sxs-lookup"><span data-stu-id="65444-131">6007 (0x1777)</span></span>
</dt> <dt>



<span data-ttu-id="65444-132">Il file specificato non è crittografato.</span><span class="sxs-lookup"><span data-stu-id="65444-132">The specified file is not encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERRORE \_ di \_ esportazione del \_ formato**</span><span class="sxs-lookup"><span data-stu-id="65444-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERROR\_NOT\_EXPORT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-134">6008 (0x1778)</span><span class="sxs-lookup"><span data-stu-id="65444-134">6008 (0x1778)</span></span>
</dt> <dt>



<span data-ttu-id="65444-135">Il file specificato non è nel formato di esportazione EFS definito.</span><span class="sxs-lookup"><span data-stu-id="65444-135">The specified file is not in the defined EFS export format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**FILE di errore di sola \_ \_ lettura \_**</span><span class="sxs-lookup"><span data-stu-id="65444-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**ERROR\_FILE\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-137">6009 (0x1779)</span><span class="sxs-lookup"><span data-stu-id="65444-137">6009 (0x1779)</span></span>
</dt> <dt>



<span data-ttu-id="65444-138">Il file specificato è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="65444-138">The specified file is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERRORE \_ dir \_ non \_ consentito di EFS**</span><span class="sxs-lookup"><span data-stu-id="65444-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR\_DIR\_EFS\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-140">6010 (0x177A)</span><span class="sxs-lookup"><span data-stu-id="65444-140">6010 (0x177A)</span></span>
</dt> <dt>



<span data-ttu-id="65444-141">La directory è stata disabilitata per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="65444-141">The directory has been disabled for encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERRORE \_ del \_ Server EFS \_ non \_ attendibile**</span><span class="sxs-lookup"><span data-stu-id="65444-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR\_EFS\_SERVER\_NOT\_TRUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-143">6011 (0x177B)</span><span class="sxs-lookup"><span data-stu-id="65444-143">6011 (0x177B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-144">Il server non è considerato attendibile per l'operazione di crittografia remota.</span><span class="sxs-lookup"><span data-stu-id="65444-144">The server is not trusted for remote encryption operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERRORE \_ \_ criterio di recupero errato \_**</span><span class="sxs-lookup"><span data-stu-id="65444-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR\_BAD\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-146">6012 (0x177C)</span><span class="sxs-lookup"><span data-stu-id="65444-146">6012 (0x177C)</span></span>
</dt> <dt>



<span data-ttu-id="65444-147">I criteri di ripristino configurati per questo sistema contengono un certificato di ripristino non valido.</span><span class="sxs-lookup"><span data-stu-id="65444-147">Recovery policy configured for this system contains invalid recovery certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERRORE \_ EFS \_ ALG \_ BLOB \_ troppo \_ grande**</span><span class="sxs-lookup"><span data-stu-id="65444-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR\_EFS\_ALG\_BLOB\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-149">6013 (0x177D)</span><span class="sxs-lookup"><span data-stu-id="65444-149">6013 (0x177D)</span></span>
</dt> <dt>



<span data-ttu-id="65444-150">L'algoritmo di crittografia utilizzato nel file di origine richiede un buffer di chiave più grande rispetto a quello del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="65444-150">The encryption algorithm used on the source file needs a bigger key buffer than the one on the destination file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**il \_ volume degli errori \_ non \_ supporta \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="65444-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**ERROR\_VOLUME\_NOT\_SUPPORT\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-152">6014 (0x177E)</span><span class="sxs-lookup"><span data-stu-id="65444-152">6014 (0x177E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-153">La partizione del disco non supporta la crittografia dei file.</span><span class="sxs-lookup"><span data-stu-id="65444-153">The disk partition does not support file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERRORE \_ EFS \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="65444-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR\_EFS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-155">6015 (0x177F)</span><span class="sxs-lookup"><span data-stu-id="65444-155">6015 (0x177F)</span></span>
</dt> <dt>



<span data-ttu-id="65444-156">Questo computer è disabilitato per la crittografia dei file.</span><span class="sxs-lookup"><span data-stu-id="65444-156">This machine is disabled for file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERRORE \_ della \_ versione EFS \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="65444-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR\_EFS\_VERSION\_NOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-158">6016 (0x1780)</span><span class="sxs-lookup"><span data-stu-id="65444-158">6016 (0x1780)</span></span>
</dt> <dt>



<span data-ttu-id="65444-159">Per decrittografare il file crittografato, è necessario un sistema più recente.</span><span class="sxs-lookup"><span data-stu-id="65444-159">A newer system is required to decrypt this encrypted file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERRORE \_ di \_ crittografia cs- \_ \_ risposta server non valida \_**</span><span class="sxs-lookup"><span data-stu-id="65444-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR\_CS\_ENCRYPTION\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-161">6017 (0x1781)</span><span class="sxs-lookup"><span data-stu-id="65444-161">6017 (0x1781)</span></span>
</dt> <dt>



<span data-ttu-id="65444-162">Il server remoto ha inviato una risposta non valida per un file aperto con la crittografia lato client.</span><span class="sxs-lookup"><span data-stu-id="65444-162">The remote server sent an invalid response for a file being opened with Client Side Encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERRORE \_ di \_ crittografia cs \_ Server non supportato \_**</span><span class="sxs-lookup"><span data-stu-id="65444-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR\_CS\_ENCRYPTION\_UNSUPPORTED\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-164">6018 (0x1782)</span><span class="sxs-lookup"><span data-stu-id="65444-164">6018 (0x1782)</span></span>
</dt> <dt>



<span data-ttu-id="65444-165">La crittografia lato client non è supportata dal server remoto anche se attesta per supportarla.</span><span class="sxs-lookup"><span data-stu-id="65444-165">Client Side Encryption is not supported by the remote server even though it claims to support it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERRORE \_ di \_ crittografia CS crittografia \_ esistente \_ file crittografato \_**</span><span class="sxs-lookup"><span data-stu-id="65444-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_EXISTING\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-167">6019 (0x1783)</span><span class="sxs-lookup"><span data-stu-id="65444-167">6019 (0x1783)</span></span>
</dt> <dt>



<span data-ttu-id="65444-168">Il file è crittografato e deve essere aperto nella modalità di crittografia lato client.</span><span class="sxs-lookup"><span data-stu-id="65444-168">File is encrypted and should be opened in Client Side Encryption mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERRORE \_ di \_ crittografia \_ cs \_ nuovo \_ file crittografato**</span><span class="sxs-lookup"><span data-stu-id="65444-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_NEW\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-170">6020 (0x1784)</span><span class="sxs-lookup"><span data-stu-id="65444-170">6020 (0x1784)</span></span>
</dt> <dt>



<span data-ttu-id="65444-171">È in corso la creazione di un nuovo file crittografato ed è necessario fornire un $EFS.</span><span class="sxs-lookup"><span data-stu-id="65444-171">A new encrypted file is being created and a $EFS needs to be provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERRORE \_ \_ file di crittografia cs \_ \_ non \_ CSE**</span><span class="sxs-lookup"><span data-stu-id="65444-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR\_CS\_ENCRYPTION\_FILE\_NOT\_CSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-173">6021 (0x1785)</span><span class="sxs-lookup"><span data-stu-id="65444-173">6021 (0x1785)</span></span>
</dt> <dt>



<span data-ttu-id="65444-174">Il client SMB ha richiesto un FSCTL CSE in un file non CSE.</span><span class="sxs-lookup"><span data-stu-id="65444-174">The SMB client requested a CSE FSCTL on a non-CSE file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**il \_ criterio di crittografia degli errori \_ Nega l' \_ \_ operazione**</span><span class="sxs-lookup"><span data-stu-id="65444-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERROR\_ENCRYPTION\_POLICY\_DENIES\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-176">6022 (0x1786)</span><span class="sxs-lookup"><span data-stu-id="65444-176">6022 (0x1786)</span></span>
</dt> <dt>



<span data-ttu-id="65444-177">L'operazione richiesta è stata bloccata dai criteri.</span><span class="sxs-lookup"><span data-stu-id="65444-177">The requested operation was blocked by policy.</span></span> <span data-ttu-id="65444-178">Per ulteriori informazioni, contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-178">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERRORE \_ non sono stati \_ \_ trovati server browser \_**</span><span class="sxs-lookup"><span data-stu-id="65444-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR\_NO\_BROWSER\_SERVERS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-180">6118 (0x17E6)</span><span class="sxs-lookup"><span data-stu-id="65444-180">6118 (0x17E6)</span></span>
</dt> <dt>



<span data-ttu-id="65444-181">L'elenco dei server per questo gruppo di lavoro non è attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="65444-181">The list of servers for this workgroup is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**Pianifica \_ E \_ servizio \_ non \_ LocalSystem**</span><span class="sxs-lookup"><span data-stu-id="65444-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED\_E\_SERVICE\_NOT\_LOCALSYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-183">6200 (0x1838)</span><span class="sxs-lookup"><span data-stu-id="65444-183">6200 (0x1838)</span></span>
</dt> <dt>



<span data-ttu-id="65444-184">Per il corretto funzionamento, è necessario configurare il servizio Utilità di pianificazione per l'esecuzione nell'account di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-184">The Task Scheduler service must be configured to run in the System account to function properly.</span></span> <span data-ttu-id="65444-185">Le singole attività possono essere configurate per l'esecuzione in altri account.</span><span class="sxs-lookup"><span data-stu-id="65444-185">Individual tasks may be configured to run in other accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**\_settore log degli errori \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**ERROR\_LOG\_SECTOR\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-187">6600 (0x19C8)</span><span class="sxs-lookup"><span data-stu-id="65444-187">6600 (0x19C8)</span></span>
</dt> <dt>



<span data-ttu-id="65444-188">Il servizio di log ha rilevato un settore di log non valido.</span><span class="sxs-lookup"><span data-stu-id="65444-188">Log service encountered an invalid log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**\_parità di settore log degli errori \_ \_ \_ non valida**</span><span class="sxs-lookup"><span data-stu-id="65444-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**ERROR\_LOG\_SECTOR\_PARITY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-190">6601 (0x19C9)</span><span class="sxs-lookup"><span data-stu-id="65444-190">6601 (0x19C9)</span></span>
</dt> <dt>



<span data-ttu-id="65444-191">Il servizio di log ha rilevato un settore di log con parità di blocco non valida.</span><span class="sxs-lookup"><span data-stu-id="65444-191">Log service encountered a log sector with invalid block parity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**\_RImappato il settore log degli errori \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65444-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**ERROR\_LOG\_SECTOR\_REMAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-193">6602 (0x19CA)</span><span class="sxs-lookup"><span data-stu-id="65444-193">6602 (0x19CA)</span></span>
</dt> <dt>



<span data-ttu-id="65444-194">Il servizio di log ha rilevato un settore di log rimappato.</span><span class="sxs-lookup"><span data-stu-id="65444-194">Log service encountered a remapped log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**blocco del log degli errori \_ \_ \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="65444-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**ERROR\_LOG\_BLOCK\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-196">6603 (0x19CB)</span><span class="sxs-lookup"><span data-stu-id="65444-196">6603 (0x19CB)</span></span>
</dt> <dt>



<span data-ttu-id="65444-197">Il servizio di log ha rilevato un blocco di log parziale o incompleto.</span><span class="sxs-lookup"><span data-stu-id="65444-197">Log service encountered a partial or incomplete log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ intervallo non valido per il log degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="65444-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**ERROR\_LOG\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-199">6604 (0x19CC)</span><span class="sxs-lookup"><span data-stu-id="65444-199">6604 (0x19CC)</span></span>
</dt> <dt>



<span data-ttu-id="65444-200">Il servizio di log ha rilevato un tentativo di accesso ai dati al di fuori dell'intervallo di log attivo.</span><span class="sxs-lookup"><span data-stu-id="65444-200">Log service encountered an attempt access data outside the active log range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**\_blocchi log degli errori \_ \_ esauriti**</span><span class="sxs-lookup"><span data-stu-id="65444-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**ERROR\_LOG\_BLOCKS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-202">6605 (0x19CD)</span><span class="sxs-lookup"><span data-stu-id="65444-202">6605 (0x19CD)</span></span>
</dt> <dt>



<span data-ttu-id="65444-203">I buffer di marshalling degli utenti del servizio di log sono esauriti.</span><span class="sxs-lookup"><span data-stu-id="65444-203">Log service user marshalling buffers are exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**\_contesto di lettura log degli errori \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**ERROR\_LOG\_READ\_CONTEXT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-205">6606 (0x19CE)</span><span class="sxs-lookup"><span data-stu-id="65444-205">6606 (0x19CE)</span></span>
</dt> <dt>



<span data-ttu-id="65444-206">Il servizio di log ha rilevato un tentativo di lettura da un'area di marshalling con un contesto di lettura non valido.</span><span class="sxs-lookup"><span data-stu-id="65444-206">Log service encountered an attempt read from a marshalling area with an invalid read context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**riavvio del log degli errori \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**ERROR\_LOG\_RESTART\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-208">6607 (0x19CF)</span><span class="sxs-lookup"><span data-stu-id="65444-208">6607 (0x19CF)</span></span>
</dt> <dt>



<span data-ttu-id="65444-209">Il servizio di log ha rilevato un'area di riavvio del log non valida.</span><span class="sxs-lookup"><span data-stu-id="65444-209">Log service encountered an invalid log restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_versione del \_ blocco del log degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="65444-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**ERROR\_LOG\_BLOCK\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-211">6608 (0x19D0)</span><span class="sxs-lookup"><span data-stu-id="65444-211">6608 (0x19D0)</span></span>
</dt> <dt>



<span data-ttu-id="65444-212">Il servizio di log ha rilevato una versione non valida del blocco del log.</span><span class="sxs-lookup"><span data-stu-id="65444-212">Log service encountered an invalid log block version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**blocco del log degli errori \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**ERROR\_LOG\_BLOCK\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-214">6609 (0x19D1)</span><span class="sxs-lookup"><span data-stu-id="65444-214">6609 (0x19D1)</span></span>
</dt> <dt>



<span data-ttu-id="65444-215">Il servizio di log ha rilevato un blocco del log non valido.</span><span class="sxs-lookup"><span data-stu-id="65444-215">Log service encountered an invalid log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**\_modalità di lettura log degli errori \_ \_ \_ non valida**</span><span class="sxs-lookup"><span data-stu-id="65444-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**ERROR\_LOG\_READ\_MODE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-217">6610 (0x19D2)</span><span class="sxs-lookup"><span data-stu-id="65444-217">6610 (0x19D2)</span></span>
</dt> <dt>



<span data-ttu-id="65444-218">Il servizio di log ha rilevato un tentativo di lettura del log con una modalità di lettura non valida.</span><span class="sxs-lookup"><span data-stu-id="65444-218">Log service encountered an attempt to read the log with an invalid read mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**LOG degli errori \_ \_ senza \_ riavvio**</span><span class="sxs-lookup"><span data-stu-id="65444-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**ERROR\_LOG\_NO\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-220">6611 (0x19D3)</span><span class="sxs-lookup"><span data-stu-id="65444-220">6611 (0x19D3)</span></span>
</dt> <dt>



<span data-ttu-id="65444-221">Il servizio di log ha rilevato un flusso di log senza area di riavvio.</span><span class="sxs-lookup"><span data-stu-id="65444-221">Log service encountered a log stream with no restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**metadati del log degli errori \_ \_ \_ danneggiati**</span><span class="sxs-lookup"><span data-stu-id="65444-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**ERROR\_LOG\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-223">6612 (0x19D4)</span><span class="sxs-lookup"><span data-stu-id="65444-223">6612 (0x19D4)</span></span>
</dt> <dt>



<span data-ttu-id="65444-224">Il servizio di log ha rilevato un file di metadati danneggiato.</span><span class="sxs-lookup"><span data-stu-id="65444-224">Log service encountered a corrupted metadata file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**metadati del log degli errori \_ \_ \_ non validi**</span><span class="sxs-lookup"><span data-stu-id="65444-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**ERROR\_LOG\_METADATA\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-226">6613 (0x19D5)</span><span class="sxs-lookup"><span data-stu-id="65444-226">6613 (0x19D5)</span></span>
</dt> <dt>



<span data-ttu-id="65444-227">Il servizio di log ha rilevato un file di metadati che non è stato possibile creare tramite il file system di log.</span><span class="sxs-lookup"><span data-stu-id="65444-227">Log service encountered a metadata file that could not be created by the log file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**metadati del log degli errori \_ \_ \_ incoerenti**</span><span class="sxs-lookup"><span data-stu-id="65444-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**ERROR\_LOG\_METADATA\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-229">6614 (0x19D6)</span><span class="sxs-lookup"><span data-stu-id="65444-229">6614 (0x19D6)</span></span>
</dt> <dt>



<span data-ttu-id="65444-230">Il servizio di log ha rilevato un file di metadati con dati incoerenti.</span><span class="sxs-lookup"><span data-stu-id="65444-230">Log service encountered a metadata file with inconsistent data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**\_prenotazione log degli errori \_ \_ non valida**</span><span class="sxs-lookup"><span data-stu-id="65444-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**ERROR\_LOG\_RESERVATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-232">6615 (0x19D7)</span><span class="sxs-lookup"><span data-stu-id="65444-232">6615 (0x19D7)</span></span>
</dt> <dt>



<span data-ttu-id="65444-233">Il servizio di log ha rilevato un tentativo di allocare o eliminare uno spazio di prenotazione errato.</span><span class="sxs-lookup"><span data-stu-id="65444-233">Log service encountered an attempt to erroneous allocate or dispose reservation space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**\_ \_ Impossibile eliminare il log degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="65444-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**ERROR\_LOG\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-235">6616 (0x19D8)</span><span class="sxs-lookup"><span data-stu-id="65444-235">6616 (0x19D8)</span></span>
</dt> <dt>



<span data-ttu-id="65444-236">Il servizio log non è in grado di eliminare il file di log o il contenitore file system</span><span class="sxs-lookup"><span data-stu-id="65444-236">Log service cannot delete log file or file system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**limite del contenitore del log degli errori \_ \_ \_ \_ superato**</span><span class="sxs-lookup"><span data-stu-id="65444-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**ERROR\_LOG\_CONTAINER\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-238">6617 (0x19D9)</span><span class="sxs-lookup"><span data-stu-id="65444-238">6617 (0x19D9)</span></span>
</dt> <dt>



<span data-ttu-id="65444-239">Il servizio di log ha raggiunto il numero massimo consentito di contenitori allocati a un file di log.</span><span class="sxs-lookup"><span data-stu-id="65444-239">Log service has reached the maximum allowable containers allocated to a log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_inizio log \_ degli errori \_ di \_ log**</span><span class="sxs-lookup"><span data-stu-id="65444-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**ERROR\_LOG\_START\_OF\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-241">6618 (0x19DA)</span><span class="sxs-lookup"><span data-stu-id="65444-241">6618 (0x19DA)</span></span>
</dt> <dt>



<span data-ttu-id="65444-242">Il servizio di log ha eseguito un tentativo di lettura o scrittura indietro oltre l'inizio del log.</span><span class="sxs-lookup"><span data-stu-id="65444-242">Log service has attempted to read or write backward past the start of the log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**criterio del log degli errori \_ \_ \_ già \_ installato**</span><span class="sxs-lookup"><span data-stu-id="65444-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**ERROR\_LOG\_POLICY\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-244">6619 (0x19DB)</span><span class="sxs-lookup"><span data-stu-id="65444-244">6619 (0x19DB)</span></span>
</dt> <dt>



<span data-ttu-id="65444-245">Impossibile installare i criteri di log perché è già presente un criterio dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="65444-245">Log policy could not be installed because a policy of the same type is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**criterio del log degli errori \_ \_ \_ non \_ installato**</span><span class="sxs-lookup"><span data-stu-id="65444-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**ERROR\_LOG\_POLICY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-247">6620 (0x19DC)</span><span class="sxs-lookup"><span data-stu-id="65444-247">6620 (0x19DC)</span></span>
</dt> <dt>



<span data-ttu-id="65444-248">Il criterio di log in questione non è stato installato al momento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="65444-248">Log policy in question was not installed at the time of the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**criterio del log degli errori \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**ERROR\_LOG\_POLICY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-250">6621 (0x19DD)</span><span class="sxs-lookup"><span data-stu-id="65444-250">6621 (0x19DD)</span></span>
</dt> <dt>



<span data-ttu-id="65444-251">Il set di criteri installato nel log non è valido.</span><span class="sxs-lookup"><span data-stu-id="65444-251">The installed set of policies on the log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_conflitto del \_ criterio del log degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="65444-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**ERROR\_LOG\_POLICY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-253">6622 (0x19DE)</span><span class="sxs-lookup"><span data-stu-id="65444-253">6622 (0x19DE)</span></span>
</dt> <dt>



<span data-ttu-id="65444-254">Un criterio per il log in questione ha impedito il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="65444-254">A policy on the log in question prevented the operation from completing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_coda di \_ \_ archiviazione bloccata nel log \_ degli errori**</span><span class="sxs-lookup"><span data-stu-id="65444-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**ERROR\_LOG\_PINNED\_ARCHIVE\_TAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-256">6623 (0x19DF)</span><span class="sxs-lookup"><span data-stu-id="65444-256">6623 (0x19DF)</span></span>
</dt> <dt>



<span data-ttu-id="65444-257">Non è possibile recuperare lo spazio del log perché il log è bloccato dalla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65444-257">Log space cannot be reclaimed because the log is pinned by the archive tail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**RECORD del log degli errori \_ \_ \_ inesistente**</span><span class="sxs-lookup"><span data-stu-id="65444-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**ERROR\_LOG\_RECORD\_NONEXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-259">6624 (0x19E0)</span><span class="sxs-lookup"><span data-stu-id="65444-259">6624 (0x19E0)</span></span>
</dt> <dt>



<span data-ttu-id="65444-260">Il record del log non è un record nel file di log.</span><span class="sxs-lookup"><span data-stu-id="65444-260">Log record is not a record in the log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**record del log degli errori \_ \_ \_ riservati \_ non validi**</span><span class="sxs-lookup"><span data-stu-id="65444-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**ERROR\_LOG\_RECORDS\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-262">6625 (0x19E1)</span><span class="sxs-lookup"><span data-stu-id="65444-262">6625 (0x19E1)</span></span>
</dt> <dt>



<span data-ttu-id="65444-263">Il numero di record di log riservati o la modifica del numero di record di log riservati non è valido.</span><span class="sxs-lookup"><span data-stu-id="65444-263">Number of reserved log records or the adjustment of the number of reserved log records is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**spazio del log degli errori \_ \_ \_ riservato \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**ERROR\_LOG\_SPACE\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-265">6626 (0x19E2)</span><span class="sxs-lookup"><span data-stu-id="65444-265">6626 (0x19E2)</span></span>
</dt> <dt>



<span data-ttu-id="65444-266">Lo spazio del log riservato o la modifica dello spazio del log non è valido.</span><span class="sxs-lookup"><span data-stu-id="65444-266">Reserved log space or the adjustment of the log space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**coda del log degli errori \_ \_ \_ non valida**</span><span class="sxs-lookup"><span data-stu-id="65444-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**ERROR\_LOG\_TAIL\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-268">6627 (0x19E3)</span><span class="sxs-lookup"><span data-stu-id="65444-268">6627 (0x19E3)</span></span>
</dt> <dt>



<span data-ttu-id="65444-269">Una coda o una base di archivio nuova o esistente del log attivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="65444-269">An new or existing archive tail or base of the active log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**LOG degli errori \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="65444-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**ERROR\_LOG\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-271">6628 (0x19E4)</span><span class="sxs-lookup"><span data-stu-id="65444-271">6628 (0x19E4)</span></span>
</dt> <dt>



<span data-ttu-id="65444-272">Lo spazio del log è esaurito.</span><span class="sxs-lookup"><span data-stu-id="65444-272">Log space is exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**errore durante il \_ \_ \_ ridimensionamento del \_ log**</span><span class="sxs-lookup"><span data-stu-id="65444-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR\_COULD\_NOT\_RESIZE\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-274">6629 (0x19E5)</span><span class="sxs-lookup"><span data-stu-id="65444-274">6629 (0x19E5)</span></span>
</dt> <dt>



<span data-ttu-id="65444-275">Impossibile impostare il log sulla dimensione richiesta.</span><span class="sxs-lookup"><span data-stu-id="65444-275">The log could not be set to the requested size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**LOG degli errori \_ \_ multiplexed**</span><span class="sxs-lookup"><span data-stu-id="65444-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**ERROR\_LOG\_MULTIPLEXED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-277">6630 (0x19E6)</span><span class="sxs-lookup"><span data-stu-id="65444-277">6630 (0x19E6)</span></span>
</dt> <dt>



<span data-ttu-id="65444-278">Il log è multiplexato, non sono consentite Scritture dirette nel log fisico.</span><span class="sxs-lookup"><span data-stu-id="65444-278">Log is multiplexed, no direct writes to the physical log is allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**LOG degli errori \_ \_ dedicato**</span><span class="sxs-lookup"><span data-stu-id="65444-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**ERROR\_LOG\_DEDICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-280">6631 (0x19E7)</span><span class="sxs-lookup"><span data-stu-id="65444-280">6631 (0x19E7)</span></span>
</dt> <dt>



<span data-ttu-id="65444-281">L'operazione non è riuscita perché il log è un log dedicato.</span><span class="sxs-lookup"><span data-stu-id="65444-281">The operation failed because the log is a dedicated log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_archivio log degli errori \_ \_ non \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="65444-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-283">6632 (0x19E8)</span><span class="sxs-lookup"><span data-stu-id="65444-283">6632 (0x19E8)</span></span>
</dt> <dt>



<span data-ttu-id="65444-284">Per l'operazione è necessario un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65444-284">The operation requires an archive context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_archivio log degli errori \_ \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="65444-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-286">6633 (0x19E9)</span><span class="sxs-lookup"><span data-stu-id="65444-286">6633 (0x19E9)</span></span>
</dt> <dt>



<span data-ttu-id="65444-287">Archiviazione del log in corso.</span><span class="sxs-lookup"><span data-stu-id="65444-287">Log archival is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**LOG degli errori \_ \_ effimero**</span><span class="sxs-lookup"><span data-stu-id="65444-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR\_LOG\_EPHEMERAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-289">6634 (0x19EA)</span><span class="sxs-lookup"><span data-stu-id="65444-289">6634 (0x19EA)</span></span>
</dt> <dt>



<span data-ttu-id="65444-290">Per l'operazione è necessario un log non temporaneo, ma il log è temporaneo.</span><span class="sxs-lookup"><span data-stu-id="65444-290">The operation requires a non-ephemeral log, but the log is ephemeral.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**LOG degli errori \_ \_ non sufficiente per i \_ \_ contenitori**</span><span class="sxs-lookup"><span data-stu-id="65444-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**ERROR\_LOG\_NOT\_ENOUGH\_CONTAINERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-292">6635 (0x19EB)</span><span class="sxs-lookup"><span data-stu-id="65444-292">6635 (0x19EB)</span></span>
</dt> <dt>



<span data-ttu-id="65444-293">Il log deve avere almeno due contenitori per poter essere letto o scritto.</span><span class="sxs-lookup"><span data-stu-id="65444-293">The log must have at least two containers before it can be read from or written to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**\_client log degli errori \_ \_ già \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="65444-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**ERROR\_LOG\_CLIENT\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-295">6636 (0x19EC)</span><span class="sxs-lookup"><span data-stu-id="65444-295">6636 (0x19EC)</span></span>
</dt> <dt>



<span data-ttu-id="65444-296">Un client di log è già registrato nel flusso.</span><span class="sxs-lookup"><span data-stu-id="65444-296">A log client has already registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**\_client log degli errori \_ \_ non \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="65444-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**ERROR\_LOG\_CLIENT\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-298">6637 (0x19ED)</span><span class="sxs-lookup"><span data-stu-id="65444-298">6637 (0x19ED)</span></span>
</dt> <dt>



<span data-ttu-id="65444-299">Un client di log non è stato registrato nel flusso.</span><span class="sxs-lookup"><span data-stu-id="65444-299">A log client has not been registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_gestore completo log degli errori \_ \_ \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="65444-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**ERROR\_LOG\_FULL\_HANDLER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-301">6638 (0x19EE)</span><span class="sxs-lookup"><span data-stu-id="65444-301">6638 (0x19EE)</span></span>
</dt> <dt>



<span data-ttu-id="65444-302">È già stata effettuata una richiesta per gestire la condizione di log full.</span><span class="sxs-lookup"><span data-stu-id="65444-302">A request has already been made to handle the log full condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**lettura del contenitore del log degli errori \_ \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="65444-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**ERROR\_LOG\_CONTAINER\_READ\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-304">6639 (0x19EF)</span><span class="sxs-lookup"><span data-stu-id="65444-304">6639 (0x19EF)</span></span>
</dt> <dt>



<span data-ttu-id="65444-305">Si è verificato un errore del servizio log durante il tentativo di lettura da un contenitore di log.</span><span class="sxs-lookup"><span data-stu-id="65444-305">Log service encountered an error when attempting to read from a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**scrittura del contenitore del log degli errori \_ \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="65444-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**ERROR\_LOG\_CONTAINER\_WRITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-307">6640 (0x19F0)</span><span class="sxs-lookup"><span data-stu-id="65444-307">6640 (0x19F0)</span></span>
</dt> <dt>



<span data-ttu-id="65444-308">Il servizio di log ha rilevato un errore durante il tentativo di scrittura in un contenitore di log.</span><span class="sxs-lookup"><span data-stu-id="65444-308">Log service encountered an error when attempting to write to a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**apertura del contenitore del log degli errori \_ \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="65444-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**ERROR\_LOG\_CONTAINER\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-310">6641 (0x19F1)</span><span class="sxs-lookup"><span data-stu-id="65444-310">6641 (0x19F1)</span></span>
</dt> <dt>



<span data-ttu-id="65444-311">Si è verificato un errore del servizio log durante il tentativo di aprire un contenitore di log.</span><span class="sxs-lookup"><span data-stu-id="65444-311">Log service encountered an error when attempting open a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**stato del contenitore del log degli errori \_ \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**ERROR\_LOG\_CONTAINER\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-313">6642 (0x19F2)</span><span class="sxs-lookup"><span data-stu-id="65444-313">6642 (0x19F2)</span></span>
</dt> <dt>



<span data-ttu-id="65444-314">Il servizio di log ha rilevato uno stato del contenitore non valido quando si tenta di eseguire un'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="65444-314">Log service encountered an invalid container state when attempting a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**stato del log degli errori \_ \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**ERROR\_LOG\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-316">6643 (0x19F3)</span><span class="sxs-lookup"><span data-stu-id="65444-316">6643 (0x19F3)</span></span>
</dt> <dt>



<span data-ttu-id="65444-317">Il servizio di log non è nello stato corretto per eseguire un'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="65444-317">Log service is not in the correct state to perform a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**LOG degli errori \_ \_ aggiunto**</span><span class="sxs-lookup"><span data-stu-id="65444-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**ERROR\_LOG\_PINNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-319">6644 (0x19F4)</span><span class="sxs-lookup"><span data-stu-id="65444-319">6644 (0x19F4)</span></span>
</dt> <dt>



<span data-ttu-id="65444-320">Non è possibile recuperare lo spazio del log perché il log è bloccato.</span><span class="sxs-lookup"><span data-stu-id="65444-320">Log space cannot be reclaimed because the log is pinned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_scaricamento metadati del log degli errori \_ \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="65444-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**ERROR\_LOG\_METADATA\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-322">6645 (0x19F5)</span><span class="sxs-lookup"><span data-stu-id="65444-322">6645 (0x19F5)</span></span>
</dt> <dt>



<span data-ttu-id="65444-323">Scaricamento metadati del log non riuscito.</span><span class="sxs-lookup"><span data-stu-id="65444-323">Log metadata flush failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**\_ \_ sicurezza incoerente log degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="65444-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**ERROR\_LOG\_INCONSISTENT\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-325">6646 (0x19F6)</span><span class="sxs-lookup"><span data-stu-id="65444-325">6646 (0x19F6)</span></span>
</dt> <dt>



<span data-ttu-id="65444-326">La sicurezza nel log e nei relativi contenitori è incoerente.</span><span class="sxs-lookup"><span data-stu-id="65444-326">Security on the log and its containers is inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**svuotamento del log degli errori \_ \_ accodato \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="65444-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**ERROR\_LOG\_APPENDED\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-328">6647 (0x19F7)</span><span class="sxs-lookup"><span data-stu-id="65444-328">6647 (0x19F7)</span></span>
</dt> <dt>



<span data-ttu-id="65444-329">I record sono stati accodati al log o sono state apportate modifiche alla prenotazione, ma non è stato possibile scaricare il log.</span><span class="sxs-lookup"><span data-stu-id="65444-329">Records were appended to the log or reservation changes were made, but the log could not be flushed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**\_ \_ prenotazione bloccata log degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="65444-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**ERROR\_LOG\_PINNED\_RESERVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-331">6648 (0x19F8)</span><span class="sxs-lookup"><span data-stu-id="65444-331">6648 (0x19F8)</span></span>
</dt> <dt>



<span data-ttu-id="65444-332">Il log è bloccato a causa di una prenotazione che utilizza la maggior parte dello spazio di log.</span><span class="sxs-lookup"><span data-stu-id="65444-332">The log is pinned due to reservation consuming most of the log space.</span></span> <span data-ttu-id="65444-333">Liberare alcuni record riservati per rendere disponibile spazio.</span><span class="sxs-lookup"><span data-stu-id="65444-333">Free some reserved records to make space available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERRORE \_ transazione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="65444-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR\_INVALID\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-335">6700 (0x1A2C)</span><span class="sxs-lookup"><span data-stu-id="65444-335">6700 (0x1A2C)</span></span>
</dt> <dt>



<span data-ttu-id="65444-336">L'handle di transazione associato a questa operazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="65444-336">The transaction handle associated with this operation is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**transazione di errore \_ \_ non \_ attiva**</span><span class="sxs-lookup"><span data-stu-id="65444-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR\_TRANSACTION\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-338">6701 (0x1A2D)</span><span class="sxs-lookup"><span data-stu-id="65444-338">6701 (0x1A2D)</span></span>
</dt> <dt>



<span data-ttu-id="65444-339">L'operazione richiesta è stata eseguita nel contesto di una transazione che non è più attiva.</span><span class="sxs-lookup"><span data-stu-id="65444-339">The requested operation was made in the context of a transaction that is no longer active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**\_richiesta transazione di errore \_ \_ non \_ valida**</span><span class="sxs-lookup"><span data-stu-id="65444-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR\_TRANSACTION\_REQUEST\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-341">6702 (0x1A2E)</span><span class="sxs-lookup"><span data-stu-id="65444-341">6702 (0x1A2E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-342">L'operazione richiesta non è valida per l'oggetto transazione nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="65444-342">The requested operation is not valid on the Transaction object in its current state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**transazione di errore \_ \_ non \_ richiesta**</span><span class="sxs-lookup"><span data-stu-id="65444-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ERROR\_TRANSACTION\_NOT\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-344">6703 (0x1A2F)</span><span class="sxs-lookup"><span data-stu-id="65444-344">6703 (0x1A2F)</span></span>
</dt> <dt>



<span data-ttu-id="65444-345">Il chiamante ha chiamato un'API di risposta, ma la risposta non è prevista perché la TM non ha emesso la richiesta corrispondente al chiamante.</span><span class="sxs-lookup"><span data-stu-id="65444-345">The caller has called a response API, but the response is not expected because the TM did not issue the corresponding request to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**transazione di errore \_ \_ già \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="65444-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**ERROR\_TRANSACTION\_ALREADY\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-347">6704 (0x1A30)</span><span class="sxs-lookup"><span data-stu-id="65444-347">6704 (0x1A30)</span></span>
</dt> <dt>



<span data-ttu-id="65444-348">È troppo tardi per eseguire l'operazione richiesta, perché la transazione è già stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="65444-348">It is too late to perform the requested operation, since the Transaction has already been aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**transazione di errore già sottoposta a \_ \_ \_ commit**</span><span class="sxs-lookup"><span data-stu-id="65444-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**ERROR\_TRANSACTION\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-350">6705 (0x1A31)</span><span class="sxs-lookup"><span data-stu-id="65444-350">6705 (0x1A31)</span></span>
</dt> <dt>



<span data-ttu-id="65444-351">È troppo tardi per eseguire l'operazione richiesta, perché è già stato eseguito il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-351">It is too late to perform the requested operation, since the Transaction has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**\_ \_ inizializzazione TM errore \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="65444-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR\_TM\_INITIALIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-353">6706 (0x1A32)</span><span class="sxs-lookup"><span data-stu-id="65444-353">6706 (0x1A32)</span></span>
</dt> <dt>



<span data-ttu-id="65444-354">Impossibile inizializzare la gestione transazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-354">The Transaction Manager was unable to be successfully initialized.</span></span> <span data-ttu-id="65444-355">Le operazioni transazionali non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="65444-355">Transacted operations are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERRORE \_ RESOURCEMANAGER di \_ sola lettura \_**</span><span class="sxs-lookup"><span data-stu-id="65444-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR\_RESOURCEMANAGER\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-357">6707 (0x1A33)</span><span class="sxs-lookup"><span data-stu-id="65444-357">6707 (0x1A33)</span></span>
</dt> <dt>



<span data-ttu-id="65444-358">Il ResourceManager specificato non ha apportato modifiche o aggiornamenti alla risorsa in questa transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-358">The specified ResourceManager made no changes or updates to the resource under this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**transazione di errore \_ \_ non \_ unita in join**</span><span class="sxs-lookup"><span data-stu-id="65444-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR\_TRANSACTION\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-360">6708 (0x1A34)</span><span class="sxs-lookup"><span data-stu-id="65444-360">6708 (0x1A34)</span></span>
</dt> <dt>



<span data-ttu-id="65444-361">Resource Manager ha tentato di preparare una transazione a cui non è stato aggiunto correttamente.</span><span class="sxs-lookup"><span data-stu-id="65444-361">The resource manager has attempted to prepare a transaction that it has not successfully joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERRORE di \_ transazione \_ superiore \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="65444-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERROR\_TRANSACTION\_SUPERIOR\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-363">6709 (0x1A35)</span><span class="sxs-lookup"><span data-stu-id="65444-363">6709 (0x1A35)</span></span>
</dt> <dt>



<span data-ttu-id="65444-364">L'oggetto transazione dispone già di un elenco superiore e il chiamante ha tentato di eseguire un'operazione che avrebbe creato un nuovo livello superiore.</span><span class="sxs-lookup"><span data-stu-id="65444-364">The Transaction object already has a superior enlistment, and the caller attempted an operation that would have created a new superior.</span></span> <span data-ttu-id="65444-365">È consentita solo una singola integrazione superiore.</span><span class="sxs-lookup"><span data-stu-id="65444-365">Only a single superior enlistment is allow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**il \_ protocollo CRM con errori \_ \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="65444-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR\_CRM\_PROTOCOL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-367">6710 (0x1A36)</span><span class="sxs-lookup"><span data-stu-id="65444-367">6710 (0x1A36)</span></span>
</dt> <dt>



<span data-ttu-id="65444-368">Il RM ha tentato di registrare un protocollo già esistente.</span><span class="sxs-lookup"><span data-stu-id="65444-368">The RM tried to register a protocol that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERRORE \_ \_ propagazione transazioni \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="65444-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR\_TRANSACTION\_PROPAGATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-370">6711 (0x1A37)</span><span class="sxs-lookup"><span data-stu-id="65444-370">6711 (0x1A37)</span></span>
</dt> <dt>



<span data-ttu-id="65444-371">Il tentativo di propagare la transazione non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="65444-371">The attempt to propagate the Transaction failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERRORE \_ del \_ protocollo CRM \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="65444-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR\_CRM\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-373">6712 (0x1A38)</span><span class="sxs-lookup"><span data-stu-id="65444-373">6712 (0x1A38)</span></span>
</dt> <dt>



<span data-ttu-id="65444-374">Il protocollo di propagazione richiesto non è stato registrato come CRM.</span><span class="sxs-lookup"><span data-stu-id="65444-374">The requested propagation protocol was not registered as a CRM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERRORE di \_ transazione del \_ \_ buffer Marshall non valido \_**</span><span class="sxs-lookup"><span data-stu-id="65444-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR\_TRANSACTION\_INVALID\_MARSHALL\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-376">6713 (0x1A39)</span><span class="sxs-lookup"><span data-stu-id="65444-376">6713 (0x1A39)</span></span>
</dt> <dt>



<span data-ttu-id="65444-377">Il buffer passato a PushTransaction o PullTransaction non è in un formato valido.</span><span class="sxs-lookup"><span data-stu-id="65444-377">The buffer passed in to PushTransaction or PullTransaction is not in a valid format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERRORE \_ \_ transazione corrente \_ non \_ valida**</span><span class="sxs-lookup"><span data-stu-id="65444-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR\_CURRENT\_TRANSACTION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-379">6714 (0x1A3A)</span><span class="sxs-lookup"><span data-stu-id="65444-379">6714 (0x1A3A)</span></span>
</dt> <dt>



<span data-ttu-id="65444-380">Il contesto di transazione corrente associato al thread non è un handle valido per un oggetto transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-380">The current transaction context associated with the thread is not a valid handle to a transaction object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**transazione di errore \_ \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="65444-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**ERROR\_TRANSACTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-382">6715 (0x1A3B)</span><span class="sxs-lookup"><span data-stu-id="65444-382">6715 (0x1A3B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-383">Impossibile aprire l'oggetto transazione specificato perché non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="65444-383">The specified Transaction object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERRORE \_ RESOURCEMANAGER \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="65444-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR\_RESOURCEMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-385">6716 (0x1A3C)</span><span class="sxs-lookup"><span data-stu-id="65444-385">6716 (0x1A3C)</span></span>
</dt> <dt>



<span data-ttu-id="65444-386">Non è stato possibile aprire l'oggetto ResourceManager specificato perché non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="65444-386">The specified ResourceManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**\_ \_ Impossibile trovare l'elenco errori \_**</span><span class="sxs-lookup"><span data-stu-id="65444-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**ERROR\_ENLISTMENT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-388">6717 (0x1A3D)</span><span class="sxs-lookup"><span data-stu-id="65444-388">6717 (0x1A3D)</span></span>
</dt> <dt>



<span data-ttu-id="65444-389">Non è stato possibile aprire l'oggetto di integrazione specificato perché non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="65444-389">The specified Enlistment object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERRORE \_ TRANSACTIONMANAGER \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="65444-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-391">6718 (0x1A3E)</span><span class="sxs-lookup"><span data-stu-id="65444-391">6718 (0x1A3E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-392">Non è stato possibile aprire l'oggetto TransactionManager specificato perché non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="65444-392">The specified TransactionManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERRORE \_ TRANSACTIONMANAGER \_ non in \_ linea**</span><span class="sxs-lookup"><span data-stu-id="65444-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-394">6719 (0x1A3F)</span><span class="sxs-lookup"><span data-stu-id="65444-394">6719 (0x1A3F)</span></span>
</dt> <dt>



<span data-ttu-id="65444-395">Impossibile creare o aprire l'oggetto specificato perché il TransactionManager associato non è online.</span><span class="sxs-lookup"><span data-stu-id="65444-395">The object specified could not be created or opened, because its associated TransactionManager is not online.</span></span> <span data-ttu-id="65444-396">TransactionManager deve essere portato completamente online chiamando RecoverTransactionManager per il ripristino fino alla fine del relativo file di log prima di poter aprire gli oggetti nella relativa transazione o negli spazi dei nomi ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="65444-396">The TransactionManager must be brought fully Online by calling RecoverTransactionManager to recover to the end of its LogFile before objects in its Transaction or ResourceManager namespaces can be opened.</span></span> <span data-ttu-id="65444-397">Inoltre, gli errori di scrittura dei record nel file di log possono causare la disconnessione di un TransactionManager.</span><span class="sxs-lookup"><span data-stu-id="65444-397">In addition, errors in writing records to its LogFile can cause a TransactionManager to go offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERRORE \_ TRANSACTIONMANAGER il \_ ripristino del \_ nome \_**</span><span class="sxs-lookup"><span data-stu-id="65444-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR\_TRANSACTIONMANAGER\_RECOVERY\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-399">6720 (0x1A40)</span><span class="sxs-lookup"><span data-stu-id="65444-399">6720 (0x1A40)</span></span>
</dt> <dt>



<span data-ttu-id="65444-400">Il TransactionManager specificato non è riuscito a creare gli oggetti contenuti nel file di log nello spazio dei nomi ob.</span><span class="sxs-lookup"><span data-stu-id="65444-400">The specified TransactionManager was unable to create the objects contained in its logfile in the Ob namespace.</span></span> <span data-ttu-id="65444-401">Di conseguenza, TransactionManager non è stato in grado di recuperare.</span><span class="sxs-lookup"><span data-stu-id="65444-401">Therefore, the TransactionManager was unable to recover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**transazione di errore \_ \_ non \_ radice**</span><span class="sxs-lookup"><span data-stu-id="65444-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR\_TRANSACTION\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-403">6721 (0x1A41)</span><span class="sxs-lookup"><span data-stu-id="65444-403">6721 (0x1A41)</span></span>
</dt> <dt>



<span data-ttu-id="65444-404">Non è stato possibile completare la chiamata per creare un'integrazione superiore in questo oggetto transazione perché l'oggetto transazione specificato per l'integrazione è un ramo subordinato della transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-404">The call to create a superior Enlistment on this Transaction object could not be completed, because the Transaction object specified for the enlistment is a subordinate branch of the Transaction.</span></span> <span data-ttu-id="65444-405">Solo la radice della transazione può essere integrata come superiore.</span><span class="sxs-lookup"><span data-stu-id="65444-405">Only the root of the Transaction can be enlisted on as a superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**\_oggetto transazione \_ errore \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="65444-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERROR\_TRANSACTION\_OBJECT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-407">6722 (0x1A42)</span><span class="sxs-lookup"><span data-stu-id="65444-407">6722 (0x1A42)</span></span>
</dt> <dt>



<span data-ttu-id="65444-408">Poiché la gestione transazioni associata o Resource Manager è stato chiuso, l'handle non è più valido.</span><span class="sxs-lookup"><span data-stu-id="65444-408">Because the associated transaction manager or resource manager has been closed, the handle is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**\_risposta transazione di errore \_ \_ non \_ integrata**</span><span class="sxs-lookup"><span data-stu-id="65444-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERROR\_TRANSACTION\_RESPONSE\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-410">6723 (0x1A43)</span><span class="sxs-lookup"><span data-stu-id="65444-410">6723 (0x1A43)</span></span>
</dt> <dt>



<span data-ttu-id="65444-411">Non è stato possibile eseguire l'operazione specificata in questa integrazione superiore perché l'integrazione non è stata creata con la risposta di completamento corrispondente in NotificationMask.</span><span class="sxs-lookup"><span data-stu-id="65444-411">The specified operation could not be performed on this Superior enlistment, because the enlistment was not created with the corresponding completion response in the NotificationMask.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**\_record transazioni \_ errore \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="65444-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**ERROR\_TRANSACTION\_RECORD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-413">6724 (0x1A44)</span><span class="sxs-lookup"><span data-stu-id="65444-413">6724 (0x1A44)</span></span>
</dt> <dt>



<span data-ttu-id="65444-414">Non è stato possibile eseguire l'operazione specificata perché il record che verrebbe registrato era troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="65444-414">The specified operation could not be performed, because the record that would be logged was too long.</span></span> <span data-ttu-id="65444-415">Questo problema può verificarsi a causa di due condizioni: sono presenti troppe integrazioni in questa transazione o il RecoveryInformation combinato per conto di tali integrazioni è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="65444-415">This can occur because of two conditions: either there are too many Enlistments on this Transaction, or the combined RecoveryInformation being logged on behalf of those Enlistments is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**\_transazione implicita errore \_ \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="65444-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR\_IMPLICIT\_TRANSACTION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-417">6725 (0x1A45)</span><span class="sxs-lookup"><span data-stu-id="65444-417">6725 (0x1A45)</span></span>
</dt> <dt>



<span data-ttu-id="65444-418">Transazione implicita non supportata.</span><span class="sxs-lookup"><span data-stu-id="65444-418">Implicit transaction are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERRORE \_ di \_ integrità transazioni \_ violato**</span><span class="sxs-lookup"><span data-stu-id="65444-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR\_TRANSACTION\_INTEGRITY\_VIOLATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-420">6726 (0x1A46)</span><span class="sxs-lookup"><span data-stu-id="65444-420">6726 (0x1A46)</span></span>
</dt> <dt>



<span data-ttu-id="65444-421">Il gestore delle transazioni kernel ha dovuto interrompere o dimenticare la transazione perché blocca lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="65444-421">The kernel transaction manager had to abort or forget the transaction because it blocked forward progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERRORE \_ TRANSACTIONMANAGER \_ identità non \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="65444-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR\_TRANSACTIONMANAGER\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-423">6727 (0x1A47)</span><span class="sxs-lookup"><span data-stu-id="65444-423">6727 (0x1A47)</span></span>
</dt> <dt>



<span data-ttu-id="65444-424">L'identità TransactionManager fornita non corrisponde a quella registrata nel file di log di TransactionManager.</span><span class="sxs-lookup"><span data-stu-id="65444-424">The TransactionManager identity that was supplied did not match the one recorded in the TransactionManager's log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERRORE \_ RM \_ non può \_ essere \_ bloccato per lo \_ \_ snapshot**</span><span class="sxs-lookup"><span data-stu-id="65444-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERROR\_RM\_CANNOT\_BE\_FROZEN\_FOR\_SNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-426">6728 (0x1A48)</span><span class="sxs-lookup"><span data-stu-id="65444-426">6728 (0x1A48)</span></span>
</dt> <dt>



<span data-ttu-id="65444-427">Questa operazione di snapshot non può continuare perché un gestore di risorse transazionale non può essere bloccato nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="65444-427">This snapshot operation cannot continue because a transactional resource manager cannot be frozen in its current state.</span></span> <span data-ttu-id="65444-428">Riprova.</span><span class="sxs-lookup"><span data-stu-id="65444-428">Please try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**la \_ transazione di errore \_ deve \_ WRITETHROUGH**</span><span class="sxs-lookup"><span data-stu-id="65444-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR\_TRANSACTION\_MUST\_WRITETHROUGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-430">6729 (0x1A49)</span><span class="sxs-lookup"><span data-stu-id="65444-430">6729 (0x1A49)</span></span>
</dt> <dt>



<span data-ttu-id="65444-431">La transazione non può essere integrata con il EnlistmentMask specificato, perché la transazione ha già completato la fase di prepreparazione.</span><span class="sxs-lookup"><span data-stu-id="65444-431">The transaction cannot be enlisted on with the specified EnlistmentMask, because the transaction has already completed the PrePrepare phase.</span></span> <span data-ttu-id="65444-432">Per garantire la correttezza, ResourceManager deve passare a una modalità Write-through e interrompere la memorizzazione nella cache dei dati all'interno di questa transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-432">In order to ensure correctness, the ResourceManager must switch to a write- through mode and cease caching data within this transaction.</span></span> <span data-ttu-id="65444-433">L'integrazione solo per le fasi successive delle transazioni può comunque avere esito positivo.</span><span class="sxs-lookup"><span data-stu-id="65444-433">Enlisting for only subsequent transaction phases may still succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**transazione di errore \_ \_ non \_ superiore**</span><span class="sxs-lookup"><span data-stu-id="65444-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR\_TRANSACTION\_NO\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-435">6730 (0x1A4A)</span><span class="sxs-lookup"><span data-stu-id="65444-435">6730 (0x1A4A)</span></span>
</dt> <dt>



<span data-ttu-id="65444-436">La transazione non ha un elenco superiore.</span><span class="sxs-lookup"><span data-stu-id="65444-436">The transaction does not have a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERRORE \_ euristico di errore \_ \_ possibile**</span><span class="sxs-lookup"><span data-stu-id="65444-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERROR\_HEURISTIC\_DAMAGE\_POSSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-438">6731 (0x1A4B)</span><span class="sxs-lookup"><span data-stu-id="65444-438">6731 (0x1A4B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-439">Il tentativo di eseguire il commit della transazione è stato completato, ma è possibile che non sia stato eseguito il commit di una parte dell'albero delle transazioni a causa dell'euristica.</span><span class="sxs-lookup"><span data-stu-id="65444-439">The attempt to commit the Transaction completed, but it is possible that some portion of the transaction tree did not commit successfully due to heuristics.</span></span> <span data-ttu-id="65444-440">È pertanto possibile che alcuni dati modificati nella transazione non abbiano eseguito il commit, causando un'incoerenza transazionale.</span><span class="sxs-lookup"><span data-stu-id="65444-440">Therefore it is possible that some data modified in the transaction may not have committed, resulting in transactional inconsistency.</span></span> <span data-ttu-id="65444-441">Se possibile, verificare la coerenza dei dati associati.</span><span class="sxs-lookup"><span data-stu-id="65444-441">If possible, check the consistency of the associated data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERRORE di \_ transazione TRANSazionale \_**</span><span class="sxs-lookup"><span data-stu-id="65444-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR\_TRANSACTIONAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-443">6800 (0x1A90)</span><span class="sxs-lookup"><span data-stu-id="65444-443">6800 (0x1A90)</span></span>
</dt> <dt>



<span data-ttu-id="65444-444">La funzione ha tentato di utilizzare un nome riservato per l'utilizzo da parte di un'altra transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-444">The function attempted to use a name that is reserved for use by another transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERRORE \_ RM \_ non \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="65444-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR\_RM\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-446">6801 (0x1A91)</span><span class="sxs-lookup"><span data-stu-id="65444-446">6801 (0x1A91)</span></span>
</dt> <dt>



<span data-ttu-id="65444-447">Il supporto delle transazioni all'interno del gestore di risorse specificato non è stato avviato o è stato arrestato a causa di un errore.</span><span class="sxs-lookup"><span data-stu-id="65444-447">Transaction support within the specified resource manager is not started or was shut down due to an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERRORE \_ \_ dei metadati RM \_ danneggiati**</span><span class="sxs-lookup"><span data-stu-id="65444-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR\_RM\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-449">6802 (0x1A92)</span><span class="sxs-lookup"><span data-stu-id="65444-449">6802 (0x1A92)</span></span>
</dt> <dt>



<span data-ttu-id="65444-450">I metadati di RM sono stati danneggiati.</span><span class="sxs-lookup"><span data-stu-id="65444-450">The metadata of the RM has been corrupted.</span></span> <span data-ttu-id="65444-451">RM non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="65444-451">The RM will not function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**Directory degli errori \_ \_ non \_ RM**</span><span class="sxs-lookup"><span data-stu-id="65444-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR\_DIRECTORY\_NOT\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-453">6803 (0x1A93)</span><span class="sxs-lookup"><span data-stu-id="65444-453">6803 (0x1A93)</span></span>
</dt> <dt>



<span data-ttu-id="65444-454">La directory specificata non contiene un gestore di risorse.</span><span class="sxs-lookup"><span data-stu-id="65444-454">The specified directory does not contain a resource manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**transazioni di errore \_ \_ remote non supportate \_**</span><span class="sxs-lookup"><span data-stu-id="65444-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**ERROR\_TRANSACTIONS\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-456">6805 (0x1A95)</span><span class="sxs-lookup"><span data-stu-id="65444-456">6805 (0x1A95)</span></span>
</dt> <dt>



<span data-ttu-id="65444-457">Il server o la condivisione remota non supporta le operazioni di file transazionali.</span><span class="sxs-lookup"><span data-stu-id="65444-457">The remote server or share does not support transacted file operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**dimensioni del log degli errori \_ \_ \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="65444-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**ERROR\_LOG\_RESIZE\_INVALID\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-459">6806 (0x1A96)</span><span class="sxs-lookup"><span data-stu-id="65444-459">6806 (0x1A96)</span></span>
</dt> <dt>



<span data-ttu-id="65444-460">Dimensioni del log richieste non valide.</span><span class="sxs-lookup"><span data-stu-id="65444-460">The requested log size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**\_oggetto errore \_ non \_ più \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="65444-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**ERROR\_OBJECT\_NO\_LONGER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-462">6807 (0x1A97)</span><span class="sxs-lookup"><span data-stu-id="65444-462">6807 (0x1A97)</span></span>
</dt> <dt>



<span data-ttu-id="65444-463">L'oggetto (file, flusso, collegamento) corrispondente all'handle è stato eliminato da un rollback della transazione salvataggio.</span><span class="sxs-lookup"><span data-stu-id="65444-463">The object (file, stream, link) corresponding to the handle has been deleted by a Transaction Savepoint Rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**\_ \_ \_ Impossibile trovare il flusso di errore miniversione \_**</span><span class="sxs-lookup"><span data-stu-id="65444-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-465">6808 (0x1A98)</span><span class="sxs-lookup"><span data-stu-id="65444-465">6808 (0x1A98)</span></span>
</dt> <dt>



<span data-ttu-id="65444-466">Impossibile trovare il file specificato miniversione per il file transazionale aperto.</span><span class="sxs-lookup"><span data-stu-id="65444-466">The specified file miniversion was not found for this transacted file open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**il \_ flusso di errore \_ miniversione \_ non è \_ valido**</span><span class="sxs-lookup"><span data-stu-id="65444-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-468">6809 (0x1A99)</span><span class="sxs-lookup"><span data-stu-id="65444-468">6809 (0x1A99)</span></span>
</dt> <dt>



<span data-ttu-id="65444-469">Il file specificato miniversione è stato trovato ma è stato invalidato.</span><span class="sxs-lookup"><span data-stu-id="65444-469">The specified file miniversion was found but has been invalidated.</span></span> <span data-ttu-id="65444-470">La causa più probabile è il rollback della transazione salvataggio.</span><span class="sxs-lookup"><span data-stu-id="65444-470">Most likely cause is a transaction savepoint rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERRORE \_ miniversione \_ inaccessibile \_ dalla \_ \_ transazione specificata**</span><span class="sxs-lookup"><span data-stu-id="65444-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR\_MINIVERSION\_INACCESSIBLE\_FROM\_SPECIFIED\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-472">6810 (0x1A9A)</span><span class="sxs-lookup"><span data-stu-id="65444-472">6810 (0x1A9A)</span></span>
</dt> <dt>



<span data-ttu-id="65444-473">Un miniversione può essere aperto solo nel contesto della transazione che l'ha creata.</span><span class="sxs-lookup"><span data-stu-id="65444-473">A miniversion may only be opened in the context of the transaction that created it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**errore durante l' \_ \_ apertura \_ \_ di miniversione con \_ modifica \_ finalità**</span><span class="sxs-lookup"><span data-stu-id="65444-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR\_CANT\_OPEN\_MINIVERSION\_WITH\_MODIFY\_INTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-475">6811 (0x1A9B)</span><span class="sxs-lookup"><span data-stu-id="65444-475">6811 (0x1A9B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-476">Non è possibile aprire un miniversione con modifica accesso.</span><span class="sxs-lookup"><span data-stu-id="65444-476">It is not possible to open a miniversion with modify access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**errore durante la creazione di un \_ \_ \_ altro \_ flusso \_ miniversioni**</span><span class="sxs-lookup"><span data-stu-id="65444-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR\_CANT\_CREATE\_MORE\_STREAM\_MINIVERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-478">6812 (0x1A9C)</span><span class="sxs-lookup"><span data-stu-id="65444-478">6812 (0x1A9C)</span></span>
</dt> <dt>



<span data-ttu-id="65444-479">Non è possibile creare altri miniversioni per questo flusso.</span><span class="sxs-lookup"><span data-stu-id="65444-479">It is not possible to create any more miniversions for this stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERRORE \_ di \_ versione del file remoto non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="65444-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR\_REMOTE\_FILE\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-481">6814 (0x1A9E)</span><span class="sxs-lookup"><span data-stu-id="65444-481">6814 (0x1A9E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-482">Il server remoto ha inviato un numero di versione o un FID non corrispondente per un file aperto con le transazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-482">The remote server sent mismatching version number or Fid for a file opened with transactions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**HANDLE di errore \_ \_ non \_ più \_ valido**</span><span class="sxs-lookup"><span data-stu-id="65444-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**ERROR\_HANDLE\_NO\_LONGER\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-484">6815 (0x1A9F)</span><span class="sxs-lookup"><span data-stu-id="65444-484">6815 (0x1A9F)</span></span>
</dt> <dt>



<span data-ttu-id="65444-485">L'handle è stato invalidato da una transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-485">The handle has been invalidated by a transaction.</span></span> <span data-ttu-id="65444-486">La causa più probabile è la presenza di un mapping di memoria su un file o un handle aperto quando la transazione è terminata o ne è stato eseguito il rollback a salvataggio.</span><span class="sxs-lookup"><span data-stu-id="65444-486">The most likely cause is the presence of memory mapping on a file or an open handle when the transaction ended or rolled back to savepoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERRORE \_ nessun \_ \_ metadati TXF**</span><span class="sxs-lookup"><span data-stu-id="65444-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR\_NO\_TXF\_METADATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-488">6816 (0x1AA0)</span><span class="sxs-lookup"><span data-stu-id="65444-488">6816 (0x1AA0)</span></span>
</dt> <dt>



<span data-ttu-id="65444-489">Non sono presenti metadati di transazione per il file.</span><span class="sxs-lookup"><span data-stu-id="65444-489">There is no transaction metadata on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**\_ \_ rilevato danneggiamento del log degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="65444-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**ERROR\_LOG\_CORRUPTION\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-491">6817 (0x1AA1)</span><span class="sxs-lookup"><span data-stu-id="65444-491">6817 (0x1AA1)</span></span>
</dt> <dt>



<span data-ttu-id="65444-492">I dati del log sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="65444-492">The log data is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**errore durante il \_ \_ ripristino \_ con \_ handle \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="65444-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR\_CANT\_RECOVER\_WITH\_HANDLE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-494">6818 (0x1AA2)</span><span class="sxs-lookup"><span data-stu-id="65444-494">6818 (0x1AA2)</span></span>
</dt> <dt>



<span data-ttu-id="65444-495">Il file non può essere recuperato perché è ancora aperto un handle.</span><span class="sxs-lookup"><span data-stu-id="65444-495">The file can't be recovered because there is a handle still open on it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERRORE \_ RM \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="65444-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR\_RM\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-497">6819 (0x1AA3)</span><span class="sxs-lookup"><span data-stu-id="65444-497">6819 (0x1AA3)</span></span>
</dt> <dt>



<span data-ttu-id="65444-498">Il risultato della transazione non è disponibile perché il gestore di risorse è stato disconnesso.</span><span class="sxs-lookup"><span data-stu-id="65444-498">The transaction outcome is unavailable because the resource manager responsible for it has disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**\_Elenco errori \_ non \_ superiore**</span><span class="sxs-lookup"><span data-stu-id="65444-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**ERROR\_ENLISTMENT\_NOT\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-500">6820 (0x1AA4)</span><span class="sxs-lookup"><span data-stu-id="65444-500">6820 (0x1AA4)</span></span>
</dt> <dt>



<span data-ttu-id="65444-501">La richiesta è stata rifiutata perché l'integrazione in questione non è un elenco superiore.</span><span class="sxs-lookup"><span data-stu-id="65444-501">The request was rejected because the enlistment in question is not a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**\_Ripristino errori \_ non \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="65444-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**ERROR\_RECOVERY\_NOT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-503">6821 (0x1AA5)</span><span class="sxs-lookup"><span data-stu-id="65444-503">6821 (0x1AA5)</span></span>
</dt> <dt>



<span data-ttu-id="65444-504">Il gestore di risorse transazionale è già coerente.</span><span class="sxs-lookup"><span data-stu-id="65444-504">The transactional resource manager is already consistent.</span></span> <span data-ttu-id="65444-505">Il ripristino non è necessario.</span><span class="sxs-lookup"><span data-stu-id="65444-505">Recovery is not needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERRORE \_ RM \_ già \_ avviato**</span><span class="sxs-lookup"><span data-stu-id="65444-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR\_RM\_ALREADY\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-507">6822 (0x1AA6)</span><span class="sxs-lookup"><span data-stu-id="65444-507">6822 (0x1AA6)</span></span>
</dt> <dt>



<span data-ttu-id="65444-508">Il gestore di risorse transazionale è già stato avviato.</span><span class="sxs-lookup"><span data-stu-id="65444-508">The transactional resource manager has already been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**\_identità file di errore \_ \_ non \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="65444-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**ERROR\_FILE\_IDENTITY\_NOT\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-510">6823 (0x1AA7)</span><span class="sxs-lookup"><span data-stu-id="65444-510">6823 (0x1AA7)</span></span>
</dt> <dt>



<span data-ttu-id="65444-511">Il file non può essere aperto in modo transazionale, perché la relativa identità dipende dal risultato di una transazione non risolta.</span><span class="sxs-lookup"><span data-stu-id="65444-511">The file cannot be opened transactionally, because its identity depends on the outcome of an unresolved transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**errore durante la \_ \_ \_ dipendenza transazionale \_**</span><span class="sxs-lookup"><span data-stu-id="65444-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR\_CANT\_BREAK\_TRANSACTIONAL\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-513">6824 (0x1AA8)</span><span class="sxs-lookup"><span data-stu-id="65444-513">6824 (0x1AA8)</span></span>
</dt> <dt>



<span data-ttu-id="65444-514">Non è possibile eseguire l'operazione perché un'altra transazione dipende dal fatto che questa proprietà non verrà modificata.</span><span class="sxs-lookup"><span data-stu-id="65444-514">The operation cannot be performed because another transaction is depending on the fact that this property will not change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERRORE \_ di \_ limite incrociato tra \_ RM \_**</span><span class="sxs-lookup"><span data-stu-id="65444-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERROR\_CANT\_CROSS\_RM\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-516">6825 (0x1AA9)</span><span class="sxs-lookup"><span data-stu-id="65444-516">6825 (0x1AA9)</span></span>
</dt> <dt>



<span data-ttu-id="65444-517">L'operazione comporterebbe un singolo file con due gestori di risorse transazionali e pertanto non è consentito.</span><span class="sxs-lookup"><span data-stu-id="65444-517">The operation would involve a single file with two transactional resource managers and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERRORE \_ TXF \_ dir \_ non \_ vuoto**</span><span class="sxs-lookup"><span data-stu-id="65444-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR\_TXF\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-519">6826 (0x1AAA)</span><span class="sxs-lookup"><span data-stu-id="65444-519">6826 (0x1AAA)</span></span>
</dt> <dt>



<span data-ttu-id="65444-520">Per eseguire questa operazione, è necessario che la directory $Txf sia vuota.</span><span class="sxs-lookup"><span data-stu-id="65444-520">The $Txf directory must be empty for this operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**sono \_ presenti transazioni INdubbie sull'errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65444-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**ERROR\_INDOUBT\_TRANSACTIONS\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-522">6827 (0x1AAB)</span><span class="sxs-lookup"><span data-stu-id="65444-522">6827 (0x1AAB)</span></span>
</dt> <dt>



<span data-ttu-id="65444-523">L'operazione lascia un gestore di risorse transazionale in uno stato incoerente e pertanto non è consentito.</span><span class="sxs-lookup"><span data-stu-id="65444-523">The operation would leave a transactional resource manager in an inconsistent state and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERRORE \_ TM \_ volatile**</span><span class="sxs-lookup"><span data-stu-id="65444-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR\_TM\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-525">6828 (0x1AAC)</span><span class="sxs-lookup"><span data-stu-id="65444-525">6828 (0x1AAC)</span></span>
</dt> <dt>



<span data-ttu-id="65444-526">Non è stato possibile completare l'operazione perché la gestione transazioni non contiene un log.</span><span class="sxs-lookup"><span data-stu-id="65444-526">The operation could not be completed because the transaction manager does not have a log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERRORE di \_ rollback \_ timer \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="65444-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR\_ROLLBACK\_TIMER\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-528">6829 (0x1AAD)</span><span class="sxs-lookup"><span data-stu-id="65444-528">6829 (0x1AAD)</span></span>
</dt> <dt>



<span data-ttu-id="65444-529">Non è stato possibile pianificare un rollback perché un rollback pianificato in precedenza è già stato eseguito o è stato accodato per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="65444-529">A rollback could not be scheduled because a previously scheduled rollback has already executed or been queued for execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERRORE \_ TXF \_ attributo \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="65444-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERROR\_TXF\_ATTRIBUTE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-531">6830 (0x1AAE)</span><span class="sxs-lookup"><span data-stu-id="65444-531">6830 (0x1AAE)</span></span>
</dt> <dt>



<span data-ttu-id="65444-532">L'attributo transazionale dei metadati nel file o nella directory è danneggiato e illeggibile.</span><span class="sxs-lookup"><span data-stu-id="65444-532">The transactional metadata attribute on the file or directory is corrupt and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERRORE \_ EFS \_ non \_ consentito \_ nella \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="65444-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR\_EFS\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-534">6831 (0x1AAF)</span><span class="sxs-lookup"><span data-stu-id="65444-534">6831 (0x1AAF)</span></span>
</dt> <dt>



<span data-ttu-id="65444-535">Non è stato possibile completare l'operazione di crittografia perché è attiva una transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-535">The encryption operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERRORE di \_ apertura TRANSazionale \_ \_ non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="65444-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR\_TRANSACTIONAL\_OPEN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-537">6832 (0x1AB0)</span><span class="sxs-lookup"><span data-stu-id="65444-537">6832 (0x1AB0)</span></span>
</dt> <dt>



<span data-ttu-id="65444-538">Questo oggetto non può essere aperto in una transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-538">This object is not allowed to be opened in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**\_crescita log degli errori \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="65444-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**ERROR\_LOG\_GROWTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-540">6833 (0x1AB1)</span><span class="sxs-lookup"><span data-stu-id="65444-540">6833 (0x1AB1)</span></span>
</dt> <dt>



<span data-ttu-id="65444-541">Il tentativo di creare lo spazio nel log di Transactional Resource Manager non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="65444-541">An attempt to create space in the transactional resource manager's log failed.</span></span> <span data-ttu-id="65444-542">Lo stato di errore è stato registrato nel registro eventi.</span><span class="sxs-lookup"><span data-stu-id="65444-542">The failure status has been recorded in the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERRORE di \_ mapping transazionale non \_ \_ supportato \_**</span><span class="sxs-lookup"><span data-stu-id="65444-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR\_TRANSACTED\_MAPPING\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-544">6834 (0x1AB2)</span><span class="sxs-lookup"><span data-stu-id="65444-544">6834 (0x1AB2)</span></span>
</dt> <dt>



<span data-ttu-id="65444-545">Mapping di memoria (creazione di una sezione mappata) un file remoto in una transazione non è supportato.</span><span class="sxs-lookup"><span data-stu-id="65444-545">Memory mapping (creating a mapped section) a remote file under a transaction is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERRORE \_ TXF \_ metadati \_ già \_ presenti**</span><span class="sxs-lookup"><span data-stu-id="65444-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERROR\_TXF\_METADATA\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-547">6835 (0x1AB3)</span><span class="sxs-lookup"><span data-stu-id="65444-547">6835 (0x1AB3)</span></span>
</dt> <dt>



<span data-ttu-id="65444-548">I metadati della transazione sono già presenti nel file e non possono essere sostituiti.</span><span class="sxs-lookup"><span data-stu-id="65444-548">Transaction metadata is already present on this file and cannot be superseded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**callback dell'ambito della transazione di errore \_ \_ \_ \_ non \_ impostati**</span><span class="sxs-lookup"><span data-stu-id="65444-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR\_TRANSACTION\_SCOPE\_CALLBACKS\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-550">6836 (0x1AB4)</span><span class="sxs-lookup"><span data-stu-id="65444-550">6836 (0x1AB4)</span></span>
</dt> <dt>



<span data-ttu-id="65444-551">Impossibile immettere un ambito di transazione perché il gestore dell'ambito non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="65444-551">A transaction scope could not be entered because the scope handler has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**\_Promozione della transazione di errore \_ obbligatoria \_**</span><span class="sxs-lookup"><span data-stu-id="65444-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**ERROR\_TRANSACTION\_REQUIRED\_PROMOTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-553">6837 (0x1AB5)</span><span class="sxs-lookup"><span data-stu-id="65444-553">6837 (0x1AB5)</span></span>
</dt> <dt>



<span data-ttu-id="65444-554">La promozione è stata necessaria per consentire l'integrazione di Resource Manager, ma la transazione è stata impostata in modo da non consentirla.</span><span class="sxs-lookup"><span data-stu-id="65444-554">Promotion was required in order to allow the resource manager to enlist, but the transaction was set to disallow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERRORE \_ non è possibile \_ eseguire il \_ file \_ nella \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="65444-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR\_CANNOT\_EXECUTE\_FILE\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-556">6838 (0x1AB6)</span><span class="sxs-lookup"><span data-stu-id="65444-556">6838 (0x1AB6)</span></span>
</dt> <dt>



<span data-ttu-id="65444-557">Questo file è aperto per la modifica in una transazione non risolta e può essere aperto per l'esecuzione solo da un lettore transazionale.</span><span class="sxs-lookup"><span data-stu-id="65444-557">This file is open for modification in an unresolved transaction and may be opened for execute only by a transacted reader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**transazioni di errore \_ \_ non \_ bloccate**</span><span class="sxs-lookup"><span data-stu-id="65444-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ERROR\_TRANSACTIONS\_NOT\_FROZEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-559">6839 (0x1AB7)</span><span class="sxs-lookup"><span data-stu-id="65444-559">6839 (0x1AB7)</span></span>
</dt> <dt>



<span data-ttu-id="65444-560">La richiesta di scongelamento delle transazioni bloccate è stata ignorata perché le transazioni non erano state precedentemente bloccate.</span><span class="sxs-lookup"><span data-stu-id="65444-560">The request to thaw frozen transactions was ignored because transactions had not previously been frozen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERRORE \_ \_ blocco transazioni \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="65444-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR\_TRANSACTION\_FREEZE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-562">6840 (0x1AB8)</span><span class="sxs-lookup"><span data-stu-id="65444-562">6840 (0x1AB8)</span></span>
</dt> <dt>



<span data-ttu-id="65444-563">Le transazioni non possono essere bloccate perché è già in corso un blocco.</span><span class="sxs-lookup"><span data-stu-id="65444-563">Transactions cannot be frozen because a freeze is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERRORE \_ non \_ \_ volume snapshot**</span><span class="sxs-lookup"><span data-stu-id="65444-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR\_NOT\_SNAPSHOT\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-565">6841 (0x1AB9)</span><span class="sxs-lookup"><span data-stu-id="65444-565">6841 (0x1AB9)</span></span>
</dt> <dt>



<span data-ttu-id="65444-566">Il volume di destinazione non è un volume snapshot.</span><span class="sxs-lookup"><span data-stu-id="65444-566">The target volume is not a snapshot volume.</span></span> <span data-ttu-id="65444-567">Questa operazione è valida solo su un volume montato come snapshot.</span><span class="sxs-lookup"><span data-stu-id="65444-567">This operation is only valid on a volume mounted as a snapshot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERRORE \_ nessun \_ salvataggio \_ con \_ \_ file aperti**</span><span class="sxs-lookup"><span data-stu-id="65444-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR\_NO\_SAVEPOINT\_WITH\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-569">6842 (0x1ABA)</span><span class="sxs-lookup"><span data-stu-id="65444-569">6842 (0x1ABA)</span></span>
</dt> <dt>



<span data-ttu-id="65444-570">L'operazione salvataggio non è riuscita perché i file sono aperti nella transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-570">The savepoint operation failed because files are open on the transaction.</span></span> <span data-ttu-id="65444-571">Questa operazione non è consentita.</span><span class="sxs-lookup"><span data-stu-id="65444-571">This is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**\_ripristino dati di errore \_ perso \_**</span><span class="sxs-lookup"><span data-stu-id="65444-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERROR\_DATA\_LOST\_REPAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-573">6843 (0x1ABB)</span><span class="sxs-lookup"><span data-stu-id="65444-573">6843 (0x1ABB)</span></span>
</dt> <dt>



<span data-ttu-id="65444-574">Windows ha individuato un danneggiamento in un file e il file è stato ripristinato.</span><span class="sxs-lookup"><span data-stu-id="65444-574">Windows has discovered corruption in a file, and that file has since been repaired.</span></span> <span data-ttu-id="65444-575">Potrebbe essersi verificata una perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="65444-575">Data loss may have occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERRORE \_ sparse \_ non \_ consentito \_ nella \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="65444-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR\_SPARSE\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-577">6844 (0x1ABC)</span><span class="sxs-lookup"><span data-stu-id="65444-577">6844 (0x1ABC)</span></span>
</dt> <dt>



<span data-ttu-id="65444-578">Non è stato possibile completare l'operazione di tipo sparse perché una transazione è attiva sul file.</span><span class="sxs-lookup"><span data-stu-id="65444-578">The sparse operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERRORE \_ TM \_ identità non \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="65444-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR\_TM\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-580">6845 (0x1ABD)</span><span class="sxs-lookup"><span data-stu-id="65444-580">6845 (0x1ABD)</span></span>
</dt> <dt>



<span data-ttu-id="65444-581">La chiamata per la creazione di un oggetto TransactionManager non è riuscita perché l'identità TM archiviata nel file di log non corrisponde all'identità TM passata come argomento.</span><span class="sxs-lookup"><span data-stu-id="65444-581">The call to create a TransactionManager object failed because the Tm Identity stored in the logfile does not match the Tm Identity that was passed in as an argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**sezione con errore \_ Floated \_**</span><span class="sxs-lookup"><span data-stu-id="65444-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR\_FLOATED\_SECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-583">6846 (0x1ABE)</span><span class="sxs-lookup"><span data-stu-id="65444-583">6846 (0x1ABE)</span></span>
</dt> <dt>



<span data-ttu-id="65444-584">Si è tentato di eseguire operazioni di I/O su un oggetto Section che è stato spostato a causa di una transazione che termina.</span><span class="sxs-lookup"><span data-stu-id="65444-584">I/O was attempted on a section object that has been floated as a result of a transaction ending.</span></span> <span data-ttu-id="65444-585">Nessun dato valido.</span><span class="sxs-lookup"><span data-stu-id="65444-585">There is no valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERRORE \_ non può \_ accettare il \_ lavoro transazionale \_**</span><span class="sxs-lookup"><span data-stu-id="65444-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR\_CANNOT\_ACCEPT\_TRANSACTED\_WORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-587">6847 (0x1ABF)</span><span class="sxs-lookup"><span data-stu-id="65444-587">6847 (0x1ABF)</span></span>
</dt> <dt>



<span data-ttu-id="65444-588">Il gestore di risorse transazionale non è attualmente in grado di accettare il lavoro transazionale a causa di una condizione temporanea, ad esempio risorse insufficienti.</span><span class="sxs-lookup"><span data-stu-id="65444-588">The transactional resource manager cannot currently accept transacted work due to a transient condition such as low resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERRORE \_ non è possibile \_ interrompere \_ le transazioni**</span><span class="sxs-lookup"><span data-stu-id="65444-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR\_CANNOT\_ABORT\_TRANSACTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-590">6848 (0x1AC0)</span><span class="sxs-lookup"><span data-stu-id="65444-590">6848 (0x1AC0)</span></span>
</dt> <dt>



<span data-ttu-id="65444-591">Il gestore di risorse transazionale ha troppi transazioni in attesa che non possono essere interrotti.</span><span class="sxs-lookup"><span data-stu-id="65444-591">The transactional resource manager had too many tranactions outstanding that could not be aborted.</span></span> <span data-ttu-id="65444-592">Il gestore di risorse transazionale è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="65444-592">The transactional resource manger has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERRORI \_ di \_ cluster danneggiati**</span><span class="sxs-lookup"><span data-stu-id="65444-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR\_BAD\_CLUSTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-594">6849 (0x1AC1)</span><span class="sxs-lookup"><span data-stu-id="65444-594">6849 (0x1AC1)</span></span>
</dt> <dt>



<span data-ttu-id="65444-595">Non è stato possibile completare l'operazione a causa di cluster danneggiati sul disco.</span><span class="sxs-lookup"><span data-stu-id="65444-595">The operation could not be completed due to bad clusters on disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**compressione degli errori \_ \_ non \_ consentita \_ nella \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="65444-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**ERROR\_COMPRESSION\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-597">6850 (0x1AC2)</span><span class="sxs-lookup"><span data-stu-id="65444-597">6850 (0x1AC2)</span></span>
</dt> <dt>



<span data-ttu-id="65444-598">Non è stato possibile completare l'operazione di compressione perché nel file è attiva una transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-598">The compression operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**VOLUME di errore \_ \_ Dirty**</span><span class="sxs-lookup"><span data-stu-id="65444-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR\_VOLUME\_DIRTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-600">6851 (0x1AC3)</span><span class="sxs-lookup"><span data-stu-id="65444-600">6851 (0x1AC3)</span></span>
</dt> <dt>



<span data-ttu-id="65444-601">Non è stato possibile completare l'operazione perché il volume è modificato.</span><span class="sxs-lookup"><span data-stu-id="65444-601">The operation could not be completed because the volume is dirty.</span></span> <span data-ttu-id="65444-602">Eseguire CHKDSK e riprovare.</span><span class="sxs-lookup"><span data-stu-id="65444-602">Please run chkdsk and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERRORE \_ nessun \_ rilevamento dei collegamenti \_ \_ nella \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="65444-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR\_NO\_LINK\_TRACKING\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-604">6852 (0x1AC4)</span><span class="sxs-lookup"><span data-stu-id="65444-604">6852 (0x1AC4)</span></span>
</dt> <dt>



<span data-ttu-id="65444-605">Non è stato possibile completare l'operazione di rilevamento dei collegamenti perché è attiva una transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-605">The link tracking operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_operazione \_ di errore non \_ supportata \_ nella \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="65444-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**ERROR\_OPERATION\_NOT\_SUPPORTED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-607">6853 (0x1AC5)</span><span class="sxs-lookup"><span data-stu-id="65444-607">6853 (0x1AC5)</span></span>
</dt> <dt>



<span data-ttu-id="65444-608">Questa operazione non può essere eseguita in una transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-608">This operation cannot be performed in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**HANDLE di errore \_ scaduto \_**</span><span class="sxs-lookup"><span data-stu-id="65444-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERROR\_EXPIRED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-610">6854 (0x1AC6)</span><span class="sxs-lookup"><span data-stu-id="65444-610">6854 (0x1AC6)</span></span>
</dt> <dt>



<span data-ttu-id="65444-611">L'handle non è più associato correttamente alla relativa transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-611">The handle is no longer properly associated with its transaction.</span></span> <span data-ttu-id="65444-612">Potrebbe essere stata aperta in un gestore di risorse transazionale che in seguito è stato forzato a riavviare.</span><span class="sxs-lookup"><span data-stu-id="65444-612">It may have been opened in a transactional resource manager that was subsequently forced to restart.</span></span> <span data-ttu-id="65444-613">Chiudere l'handle e aprirne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="65444-613">Please close the handle and open a new one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**transazione di errore \_ \_ non \_ integrata**</span><span class="sxs-lookup"><span data-stu-id="65444-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ERROR\_TRANSACTION\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-615">6855 (0x1AC7)</span><span class="sxs-lookup"><span data-stu-id="65444-615">6855 (0x1AC7)</span></span>
</dt> <dt>



<span data-ttu-id="65444-616">Non è stato possibile eseguire l'operazione specificata perché Resource Manager non è integrato nella transazione.</span><span class="sxs-lookup"><span data-stu-id="65444-616">The specified operation could not be performed because the resource manager is not enlisted in the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERRORE \_ ctx \_ WINSTATION \_ nome \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR\_CTX\_WINSTATION\_NAME\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-618">7001 (0x1B59)</span><span class="sxs-lookup"><span data-stu-id="65444-618">7001 (0x1B59)</span></span>
</dt> <dt>



<span data-ttu-id="65444-619">Il nome della sessione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="65444-619">The specified session name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERRORE \_ ctx \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="65444-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR\_CTX\_INVALID\_PD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-621">7002 (0x1B5A)</span><span class="sxs-lookup"><span data-stu-id="65444-621">7002 (0x1B5A)</span></span>
</dt> <dt>



<span data-ttu-id="65444-622">Il driver di protocollo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="65444-622">The specified protocol driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERRORE \_ ctx \_ PD \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="65444-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR\_CTX\_PD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-624">7003 (0x1B5B)</span><span class="sxs-lookup"><span data-stu-id="65444-624">7003 (0x1B5B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-625">Il driver di protocollo specificato non è stato trovato nel percorso di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-625">The specified protocol driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERRORE \_ ctx \_ WD \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="65444-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR\_CTX\_WD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-627">7004 (0x1B5C)</span><span class="sxs-lookup"><span data-stu-id="65444-627">7004 (0x1B5C)</span></span>
</dt> <dt>



<span data-ttu-id="65444-628">Il driver della connessione terminal specificato non è stato trovato nel percorso di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-628">The specified terminal connection driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERRORE \_ ctx \_ Impossibile \_ creare la \_ voce del log eventi \_**</span><span class="sxs-lookup"><span data-stu-id="65444-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR\_CTX\_CANNOT\_MAKE\_EVENTLOG\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-630">7005 (0x1B5D)</span><span class="sxs-lookup"><span data-stu-id="65444-630">7005 (0x1B5D)</span></span>
</dt> <dt>



<span data-ttu-id="65444-631">Non è stato possibile creare una chiave del registro di sistema per la registrazione eventi per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="65444-631">A registry key for event logging could not be created for this session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERRORE \_ ctx \_ nome servizio in \_ \_ conflitto**</span><span class="sxs-lookup"><span data-stu-id="65444-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR\_CTX\_SERVICE\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-633">7006 (0x1B5E)</span><span class="sxs-lookup"><span data-stu-id="65444-633">7006 (0x1B5E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-634">Nel sistema esiste già un servizio con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="65444-634">A service with the same name already exists on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERRORE \_ ctx di \_ chiusura \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="65444-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR\_CTX\_CLOSE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-636">7007 (0x1B5F)</span><span class="sxs-lookup"><span data-stu-id="65444-636">7007 (0x1B5F)</span></span>
</dt> <dt>



<span data-ttu-id="65444-637">Operazione di chiusura in sospeso per la sessione.</span><span class="sxs-lookup"><span data-stu-id="65444-637">A close operation is pending on the session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERRORE \_ ctx \_ nessun \_ OUTBUF**</span><span class="sxs-lookup"><span data-stu-id="65444-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR\_CTX\_NO\_OUTBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-639">7008 (0x1B60)</span><span class="sxs-lookup"><span data-stu-id="65444-639">7008 (0x1B60)</span></span>
</dt> <dt>



<span data-ttu-id="65444-640">Non sono disponibili buffer di output gratuiti.</span><span class="sxs-lookup"><span data-stu-id="65444-640">There are no free output buffers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERRORE \_ ctx \_ modem \_ inf \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="65444-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR\_CTX\_MODEM\_INF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-642">7009 (0x1B61)</span><span class="sxs-lookup"><span data-stu-id="65444-642">7009 (0x1B61)</span></span>
</dt> <dt>



<span data-ttu-id="65444-643">MODEM. Il file INF non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="65444-643">The MODEM.INF file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERRORE \_ ctx \_ . \_ modem non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR\_CTX\_INVALID\_MODEMNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-645">7010 (0x1B62)</span><span class="sxs-lookup"><span data-stu-id="65444-645">7010 (0x1B62)</span></span>
</dt> <dt>



<span data-ttu-id="65444-646">Il nome del modem non è stato trovato in MODEM. INF.</span><span class="sxs-lookup"><span data-stu-id="65444-646">The modem name was not found in MODEM.INF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**errore \_ di \_ risposta del modem CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65444-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-648">7011 (0x1B63)</span><span class="sxs-lookup"><span data-stu-id="65444-648">7011 (0x1B63)</span></span>
</dt> <dt>



<span data-ttu-id="65444-649">Il modem non ha accettato il comando inviato.</span><span class="sxs-lookup"><span data-stu-id="65444-649">The modem did not accept the command sent to it.</span></span> <span data-ttu-id="65444-650">Verificare che il nome del modem configurato corrisponda al modem collegato.</span><span class="sxs-lookup"><span data-stu-id="65444-650">Verify that the configured modem name matches the attached modem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERRORE \_ ctx \_ \_ risposta modem \_ timeout**</span><span class="sxs-lookup"><span data-stu-id="65444-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-652">7012 (0x1B64)</span><span class="sxs-lookup"><span data-stu-id="65444-652">7012 (0x1B64)</span></span>
</dt> <dt>



<span data-ttu-id="65444-653">Il modem non ha risposto al comando inviato.</span><span class="sxs-lookup"><span data-stu-id="65444-653">The modem did not respond to the command sent to it.</span></span> <span data-ttu-id="65444-654">Verificare che il modem sia cablato e acceso correttamente.</span><span class="sxs-lookup"><span data-stu-id="65444-654">Verify that the modem is properly cabled and powered on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERRORE \_ di \_ risposta modem CTX \_ \_ senza \_ gestore**</span><span class="sxs-lookup"><span data-stu-id="65444-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_CARRIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-656">7013 (0x1B65)</span><span class="sxs-lookup"><span data-stu-id="65444-656">7013 (0x1B65)</span></span>
</dt> <dt>



<span data-ttu-id="65444-657">Il rilevamento del vettore non è riuscito o il vettore è stato eliminato a causa di una disconnessione.</span><span class="sxs-lookup"><span data-stu-id="65444-657">Carrier detect has failed or carrier has been dropped due to disconnect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERRORE \_ ctx \_ modem \_ risposta \_ senza \_ Dialtone**</span><span class="sxs-lookup"><span data-stu-id="65444-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-659">7014 (0x1B66)</span><span class="sxs-lookup"><span data-stu-id="65444-659">7014 (0x1B66)</span></span>
</dt> <dt>



<span data-ttu-id="65444-660">Il tono di connessione non è stato rilevato entro il tempo richiesto.</span><span class="sxs-lookup"><span data-stu-id="65444-660">Dial tone not detected within the required time.</span></span> <span data-ttu-id="65444-661">Verificare che il cavo telefonico sia correttamente collegato e funzionante.</span><span class="sxs-lookup"><span data-stu-id="65444-661">Verify that the phone cable is properly attached and functional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERRORE \_ ctx \_ \_ risposta modem \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="65444-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-663">7015 (0x1B67)</span><span class="sxs-lookup"><span data-stu-id="65444-663">7015 (0x1B67)</span></span>
</dt> <dt>



<span data-ttu-id="65444-664">Segnale occupato rilevato nel sito remoto sul callback.</span><span class="sxs-lookup"><span data-stu-id="65444-664">Busy signal detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERRORE \_ ctx \_ \_ risposta modem \_ voce**</span><span class="sxs-lookup"><span data-stu-id="65444-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-666">7016 (0x1B68)</span><span class="sxs-lookup"><span data-stu-id="65444-666">7016 (0x1B68)</span></span>
</dt> <dt>



<span data-ttu-id="65444-667">Voce rilevata nel sito remoto su callback.</span><span class="sxs-lookup"><span data-stu-id="65444-667">Voice detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**errore \_ ctx \_ TD \_**</span><span class="sxs-lookup"><span data-stu-id="65444-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERROR\_CTX\_TD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-669">7017 (0x1B69)</span><span class="sxs-lookup"><span data-stu-id="65444-669">7017 (0x1B69)</span></span>
</dt> <dt>



<span data-ttu-id="65444-670">Errore del driver di trasporto.</span><span class="sxs-lookup"><span data-stu-id="65444-670">Transport driver error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERRORE \_ ctx \_ WINSTATION \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="65444-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR\_CTX\_WINSTATION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-672">7022 (0x1B6E)</span><span class="sxs-lookup"><span data-stu-id="65444-672">7022 (0x1B6E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-673">Impossibile trovare la sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="65444-673">The specified session cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERRORE \_ ctx \_ WINSTATION \_ già \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="65444-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERROR\_CTX\_WINSTATION\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-675">7023 (0x1B6F)</span><span class="sxs-lookup"><span data-stu-id="65444-675">7023 (0x1B6F)</span></span>
</dt> <dt>



<span data-ttu-id="65444-676">Il nome della sessione specificato è già in uso.</span><span class="sxs-lookup"><span data-stu-id="65444-676">The specified session name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERRORE \_ ctx \_ WINSTATION \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="65444-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR\_CTX\_WINSTATION\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-678">7024 (0x1B70)</span><span class="sxs-lookup"><span data-stu-id="65444-678">7024 (0x1B70)</span></span>
</dt> <dt>



<span data-ttu-id="65444-679">Non è possibile completare l'attività che si sta tentando di eseguire perché Servizi Desktop remoto è attualmente occupata.</span><span class="sxs-lookup"><span data-stu-id="65444-679">The task you are trying to do can't be completed because Remote Desktop Services is currently busy.</span></span> <span data-ttu-id="65444-680">Riprovare tra alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="65444-680">Please try again in a few minutes.</span></span> <span data-ttu-id="65444-681">Gli altri utenti dovrebbero comunque essere in grado di accedere.</span><span class="sxs-lookup"><span data-stu-id="65444-681">Other users should still be able to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERRORE \_ ctx \_ \_ modalità video non valida \_**</span><span class="sxs-lookup"><span data-stu-id="65444-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR\_CTX\_BAD\_VIDEO\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-683">7025 (0x1B71)</span><span class="sxs-lookup"><span data-stu-id="65444-683">7025 (0x1B71)</span></span>
</dt> <dt>



<span data-ttu-id="65444-684">È stato effettuato un tentativo di connessione a una sessione la cui modalità video non è supportata dal client corrente.</span><span class="sxs-lookup"><span data-stu-id="65444-684">An attempt has been made to connect to a session whose video mode is not supported by the current client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERRORE \_ ctx \_ Graphics \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR\_CTX\_GRAPHICS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-686">7035 (0x1B7B)</span><span class="sxs-lookup"><span data-stu-id="65444-686">7035 (0x1B7B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-687">L'applicazione ha tentato di abilitare la modalità grafica DOS.</span><span class="sxs-lookup"><span data-stu-id="65444-687">The application attempted to enable DOS graphics mode.</span></span> <span data-ttu-id="65444-688">La modalità grafica DOS non è supportata.</span><span class="sxs-lookup"><span data-stu-id="65444-688">DOS graphics mode is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERRORE \_ ctx \_ Logon \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="65444-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR\_CTX\_LOGON\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-690">7037 (0x1B7D)</span><span class="sxs-lookup"><span data-stu-id="65444-690">7037 (0x1B7D)</span></span>
</dt> <dt>



<span data-ttu-id="65444-691">Il privilegio di accesso interattivo è stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="65444-691">Your interactive logon privilege has been disabled.</span></span> <span data-ttu-id="65444-692">Contatta l'amministratore.</span><span class="sxs-lookup"><span data-stu-id="65444-692">Please contact your administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERRORE \_ ctx \_ non \_ console**</span><span class="sxs-lookup"><span data-stu-id="65444-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR\_CTX\_NOT\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-694">7038 (0x1B7E)</span><span class="sxs-lookup"><span data-stu-id="65444-694">7038 (0x1B7E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-695">L'operazione richiesta può essere eseguita solo nella console di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-695">The requested operation can be performed only on the system console.</span></span> <span data-ttu-id="65444-696">Questo è spesso il risultato di un driver o di una DLL di sistema che richiede l'accesso diretto alla console.</span><span class="sxs-lookup"><span data-stu-id="65444-696">This is most often the result of a driver or system DLL requiring direct console access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERRORE \_ di \_ query client CTX \_ \_ timeout**</span><span class="sxs-lookup"><span data-stu-id="65444-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR\_CTX\_CLIENT\_QUERY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-698">7040 (0x1B80)</span><span class="sxs-lookup"><span data-stu-id="65444-698">7040 (0x1B80)</span></span>
</dt> <dt>



<span data-ttu-id="65444-699">Il client non è riuscito a rispondere al messaggio di connessione al server.</span><span class="sxs-lookup"><span data-stu-id="65444-699">The client failed to respond to the server connect message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**errore durante la \_ \_ disconnessione della console CTX \_**</span><span class="sxs-lookup"><span data-stu-id="65444-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR\_CTX\_CONSOLE\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-701">7041 (0x1B81)</span><span class="sxs-lookup"><span data-stu-id="65444-701">7041 (0x1B81)</span></span>
</dt> <dt>



<span data-ttu-id="65444-702">La disconnessione della sessione della console non è supportata.</span><span class="sxs-lookup"><span data-stu-id="65444-702">Disconnecting the console session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERRORE \_ di \_ connessione console CTX \_**</span><span class="sxs-lookup"><span data-stu-id="65444-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR\_CTX\_CONSOLE\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-704">7042 (0x1B82)</span><span class="sxs-lookup"><span data-stu-id="65444-704">7042 (0x1B82)</span></span>
</dt> <dt>



<span data-ttu-id="65444-705">La riconnessione di una sessione disconnessa alla console non è supportata.</span><span class="sxs-lookup"><span data-stu-id="65444-705">Reconnecting a disconnected session to the console is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERRORE \_ ctx \_ shadow \_ negato**</span><span class="sxs-lookup"><span data-stu-id="65444-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR\_CTX\_SHADOW\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-707">7044 (0x1B84)</span><span class="sxs-lookup"><span data-stu-id="65444-707">7044 (0x1B84)</span></span>
</dt> <dt>



<span data-ttu-id="65444-708">La richiesta di controllo di un'altra sessione in modalità remota è stata negata.</span><span class="sxs-lookup"><span data-stu-id="65444-708">The request to control another session remotely was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERRORE \_ ctx \_ WINSTATION \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="65444-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR\_CTX\_WINSTATION\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-710">7045 (0x1B85)</span><span class="sxs-lookup"><span data-stu-id="65444-710">7045 (0x1B85)</span></span>
</dt> <dt>



<span data-ttu-id="65444-711">L'accesso alla sessione richiesto è stato negato.</span><span class="sxs-lookup"><span data-stu-id="65444-711">The requested session access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERRORE \_ ctx \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="65444-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR\_CTX\_INVALID\_WD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-713">7049 (0x1B89)</span><span class="sxs-lookup"><span data-stu-id="65444-713">7049 (0x1B89)</span></span>
</dt> <dt>



<span data-ttu-id="65444-714">Il driver della connessione terminal specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="65444-714">The specified terminal connection driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERRORE \_ ctx \_ ombreggiatura \_ non valida**</span><span class="sxs-lookup"><span data-stu-id="65444-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR\_CTX\_SHADOW\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-716">7050 (0x1B8A)</span><span class="sxs-lookup"><span data-stu-id="65444-716">7050 (0x1B8A)</span></span>
</dt> <dt>



<span data-ttu-id="65444-717">La sessione richiesta non può essere controllata in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="65444-717">The requested session cannot be controlled remotely.</span></span> <span data-ttu-id="65444-718">Questo potrebbe essere dovuto al fatto che la sessione è disconnessa o che attualmente non dispone di un utente connesso.</span><span class="sxs-lookup"><span data-stu-id="65444-718">This may be because the session is disconnected or does not currently have a user logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERRORE \_ ctx \_ ombreggiato \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="65444-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR\_CTX\_SHADOW\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-720">7051 (0x1B8B)</span><span class="sxs-lookup"><span data-stu-id="65444-720">7051 (0x1B8B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-721">La sessione richiesta non è configurata per consentire il controllo remoto.</span><span class="sxs-lookup"><span data-stu-id="65444-721">The requested session is not configured to allow remote control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERRORE \_ ctx \_ client \_ License \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="65444-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-723">7052 (0x1B8C)</span><span class="sxs-lookup"><span data-stu-id="65444-723">7052 (0x1B8C)</span></span>
</dt> <dt>



<span data-ttu-id="65444-724">La richiesta di connessione a questo Terminal Server è stata rifiutata.</span><span class="sxs-lookup"><span data-stu-id="65444-724">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="65444-725">Il numero di licenza del client Terminal Server è attualmente in uso da parte di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="65444-725">Your Terminal Server client license number is currently being used by another user.</span></span> <span data-ttu-id="65444-726">Per ottenere un numero di licenza univoco, rivolgersi all'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-726">Please call your system administrator to obtain a unique license number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERRORE per la \_ \_ licenza client CTX \_ \_ non \_ impostata**</span><span class="sxs-lookup"><span data-stu-id="65444-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-728">7053 (0x1B8D)</span><span class="sxs-lookup"><span data-stu-id="65444-728">7053 (0x1B8D)</span></span>
</dt> <dt>



<span data-ttu-id="65444-729">La richiesta di connessione a questo Terminal Server è stata rifiutata.</span><span class="sxs-lookup"><span data-stu-id="65444-729">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="65444-730">Il numero di licenza del client Terminal Server non è stato immesso per questa copia del client Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="65444-730">Your Terminal Server client license number has not been entered for this copy of the Terminal Server client.</span></span> <span data-ttu-id="65444-731">Contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-731">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERRORE \_ ctx \_ licenza \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="65444-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR\_CTX\_LICENSE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-733">7054 (0x1B8E)</span><span class="sxs-lookup"><span data-stu-id="65444-733">7054 (0x1B8E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-734">Il numero di connessioni a questo computer è limitato e tutte le connessioni sono in uso al momento.</span><span class="sxs-lookup"><span data-stu-id="65444-734">The number of connections to this computer is limited and all connections are in use right now.</span></span> <span data-ttu-id="65444-735">Provare a connettersi in un secondo momento o contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-735">Try connecting later or contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERRORE \_ ctx \_ \_ client licenze \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="65444-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR\_CTX\_LICENSE\_CLIENT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-737">7055 (0x1B8F)</span><span class="sxs-lookup"><span data-stu-id="65444-737">7055 (0x1B8F)</span></span>
</dt> <dt>



<span data-ttu-id="65444-738">Il client in uso non dispone di una licenza per l'uso di questo sistema.</span><span class="sxs-lookup"><span data-stu-id="65444-738">The client you are using is not licensed to use this system.</span></span> <span data-ttu-id="65444-739">La richiesta di accesso è stata negata.</span><span class="sxs-lookup"><span data-stu-id="65444-739">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERRORE \_ ctx \_ licenza \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="65444-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR\_CTX\_LICENSE\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-741">7056 (0x1B90)</span><span class="sxs-lookup"><span data-stu-id="65444-741">7056 (0x1B90)</span></span>
</dt> <dt>



<span data-ttu-id="65444-742">La licenza di sistema è scaduta.</span><span class="sxs-lookup"><span data-stu-id="65444-742">The system license has expired.</span></span> <span data-ttu-id="65444-743">La richiesta di accesso è stata negata.</span><span class="sxs-lookup"><span data-stu-id="65444-743">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERRORE \_ dell' \_ ombreggiatura CTX \_ non \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="65444-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR\_CTX\_SHADOW\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-745">7057 (0x1B91)</span><span class="sxs-lookup"><span data-stu-id="65444-745">7057 (0x1B91)</span></span>
</dt> <dt>



<span data-ttu-id="65444-746">Non è stato possibile terminare il controllo remoto perché la sessione specificata non è attualmente controllata in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="65444-746">Remote control could not be terminated because the specified session is not currently being remotely controlled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERRORE \_ ctx \_ dell'ombreggiatura \_ terminata \_ in base alla \_ modalità \_**</span><span class="sxs-lookup"><span data-stu-id="65444-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR\_CTX\_SHADOW\_ENDED\_BY\_MODE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-748">7058 (0x1B92)</span><span class="sxs-lookup"><span data-stu-id="65444-748">7058 (0x1B92)</span></span>
</dt> <dt>



<span data-ttu-id="65444-749">Il controllo remoto della console è stato terminato perché la modalità di visualizzazione è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="65444-749">The remote control of the console was terminated because the display mode was changed.</span></span> <span data-ttu-id="65444-750">La modifica della modalità di visualizzazione in una sessione di controllo remoto non è supportata.</span><span class="sxs-lookup"><span data-stu-id="65444-750">Changing the display mode in a remote control session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**il \_ numero di attivazioni errori è stato \_ \_ superato**</span><span class="sxs-lookup"><span data-stu-id="65444-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**ERROR\_ACTIVATION\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-752">7059 (0x1B93)</span><span class="sxs-lookup"><span data-stu-id="65444-752">7059 (0x1B93)</span></span>
</dt> <dt>



<span data-ttu-id="65444-753">L'attivazione è già stata reimpostata per il numero massimo di volte per questa installazione.</span><span class="sxs-lookup"><span data-stu-id="65444-753">Activation has already been reset the maximum number of times for this installation.</span></span> <span data-ttu-id="65444-754">Il timer di attivazione non verrà cancellato.</span><span class="sxs-lookup"><span data-stu-id="65444-754">Your activation timer will not be cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERRORE \_ ctx \_ WINSTATIONS \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="65444-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR\_CTX\_WINSTATIONS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-756">7060 (0x1B94)</span><span class="sxs-lookup"><span data-stu-id="65444-756">7060 (0x1B94)</span></span>
</dt> <dt>



<span data-ttu-id="65444-757">Gli account di accesso remoto sono attualmente disabilitati.</span><span class="sxs-lookup"><span data-stu-id="65444-757">Remote logins are currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERRORE \_ ctx \_ livello di crittografia \_ \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="65444-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR\_CTX\_ENCRYPTION\_LEVEL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-759">7061 (0x1B95)</span><span class="sxs-lookup"><span data-stu-id="65444-759">7061 (0x1B95)</span></span>
</dt> <dt>



<span data-ttu-id="65444-760">Non si dispone del livello di crittografia appropriato per accedere a questa sessione.</span><span class="sxs-lookup"><span data-stu-id="65444-760">You do not have the proper encryption level to access this Session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERRORE \_ ctx \_ sessione \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="65444-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR\_CTX\_SESSION\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-762">7062 (0x1B96)</span><span class="sxs-lookup"><span data-stu-id="65444-762">7062 (0x1B96)</span></span>
</dt> <dt>



<span data-ttu-id="65444-763">L'utente% s \\ \\ % s è attualmente connesso al computer.</span><span class="sxs-lookup"><span data-stu-id="65444-763">The user %s\\\\%s is currently logged on to this computer.</span></span> <span data-ttu-id="65444-764">Solo l'utente corrente o un amministratore può accedere a questo computer.</span><span class="sxs-lookup"><span data-stu-id="65444-764">Only the current user or an administrator can log on to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERRORE \_ ctx \_ Nessuna \_ forza \_ disconnessione**</span><span class="sxs-lookup"><span data-stu-id="65444-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR\_CTX\_NO\_FORCE\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-766">7063 (0x1B97)</span><span class="sxs-lookup"><span data-stu-id="65444-766">7063 (0x1B97)</span></span>
</dt> <dt>



<span data-ttu-id="65444-767">L'utente% s \\ \\ % s è già connesso alla console di questo computer.</span><span class="sxs-lookup"><span data-stu-id="65444-767">The user %s\\\\%s is already logged on to the console of this computer.</span></span> <span data-ttu-id="65444-768">Non si è autorizzati ad accedere in questo momento.</span><span class="sxs-lookup"><span data-stu-id="65444-768">You do not have permission to log in at this time.</span></span> <span data-ttu-id="65444-769">Per risolvere il problema, contattare% s \\ \\ % s e disconnettersi.</span><span class="sxs-lookup"><span data-stu-id="65444-769">To resolve this issue, contact %s\\\\%s and have them log off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERRORE \_ di \_ restrizione dell'account CTX \_**</span><span class="sxs-lookup"><span data-stu-id="65444-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR\_CTX\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-771">7064 (0x1B98)</span><span class="sxs-lookup"><span data-stu-id="65444-771">7064 (0x1B98)</span></span>
</dt> <dt>



<span data-ttu-id="65444-772">Non è possibile eseguire l'accesso a causa di una restrizione dell'account.</span><span class="sxs-lookup"><span data-stu-id="65444-772">Unable to log you on because of an account restriction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**errore \_ del \_ protocollo RDP errore \_**</span><span class="sxs-lookup"><span data-stu-id="65444-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERROR\_RDP\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-774">7065 (0x1B99)</span><span class="sxs-lookup"><span data-stu-id="65444-774">7065 (0x1B99)</span></span>
</dt> <dt>



<span data-ttu-id="65444-775">Il componente protocollo RDP %2 ha rilevato un errore nel flusso del protocollo e ha disconnesso il client.</span><span class="sxs-lookup"><span data-stu-id="65444-775">The RDP protocol component %2 detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERRORE \_ ctx \_ CDM \_ Connect**</span><span class="sxs-lookup"><span data-stu-id="65444-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR\_CTX\_CDM\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-777">7066 (0x1B9A)</span><span class="sxs-lookup"><span data-stu-id="65444-777">7066 (0x1B9A)</span></span>
</dt> <dt>



<span data-ttu-id="65444-778">Il servizio Mapping unità client si è connesso alla connessione Terminal.</span><span class="sxs-lookup"><span data-stu-id="65444-778">The Client Drive Mapping Service Has Connected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERRORE \_ ctx \_ CDM \_ Disconnect**</span><span class="sxs-lookup"><span data-stu-id="65444-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR\_CTX\_CDM\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-780">7067 (0x1B9B)</span><span class="sxs-lookup"><span data-stu-id="65444-780">7067 (0x1B9B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-781">Il servizio Mapping unità client si è disconnesso sulla connessione Terminal.</span><span class="sxs-lookup"><span data-stu-id="65444-781">The Client Drive Mapping Service Has Disconnected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**errore \_ ctx \_ livello di sicurezza \_ \_ errore**</span><span class="sxs-lookup"><span data-stu-id="65444-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERROR\_CTX\_SECURITY\_LAYER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-783">7068 (0x1B9C)</span><span class="sxs-lookup"><span data-stu-id="65444-783">7068 (0x1B9C)</span></span>
</dt> <dt>



<span data-ttu-id="65444-784">Il livello di sicurezza Terminal Server ha rilevato un errore nel flusso del protocollo e ha disconnesso il client.</span><span class="sxs-lookup"><span data-stu-id="65444-784">The Terminal Server security layer detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**\_sessioni non \_ compatibili con errore TS \_**</span><span class="sxs-lookup"><span data-stu-id="65444-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR\_TS\_INCOMPATIBLE\_SESSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-786">7069 (0x1B9D)</span><span class="sxs-lookup"><span data-stu-id="65444-786">7069 (0x1B9D)</span></span>
</dt> <dt>



<span data-ttu-id="65444-787">La sessione di destinazione non è compatibile con la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="65444-787">The target session is incompatible with the current session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**errore \_ del \_ \_ sottosistema video \_ TS errore**</span><span class="sxs-lookup"><span data-stu-id="65444-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR\_TS\_VIDEO\_SUBSYSTEM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-789">7070 (0x1B9E)</span><span class="sxs-lookup"><span data-stu-id="65444-789">7070 (0x1B9E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-790">Windows non è in grado di connettersi alla sessione perché si è verificato un problema nel sottosistema video di Windows.</span><span class="sxs-lookup"><span data-stu-id="65444-790">Windows can't connect to your session because a problem occurred in the Windows video subsystem.</span></span> <span data-ttu-id="65444-791">Provare a connettersi di nuovo in un secondo momento oppure rivolgersi all'amministratore del server per assistenza.</span><span class="sxs-lookup"><span data-stu-id="65444-791">Try connecting again later, or contact the server administrator for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_ \_ sequenza API non valida FRS ERR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65444-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS\_ERR\_INVALID\_API\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-793">8001 (0x1F41)</span><span class="sxs-lookup"><span data-stu-id="65444-793">8001 (0x1F41)</span></span>
</dt> <dt>



<span data-ttu-id="65444-794">L'API del servizio Replica file è stata chiamata in modo errato.</span><span class="sxs-lookup"><span data-stu-id="65444-794">The file replication service API was called incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**servizio di avvio di FRS \_ Err \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65444-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS\_ERR\_STARTING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-796">8002 (0x1F42)</span><span class="sxs-lookup"><span data-stu-id="65444-796">8002 (0x1F42)</span></span>
</dt> <dt>



<span data-ttu-id="65444-797">Impossibile avviare il servizio Replica file.</span><span class="sxs-lookup"><span data-stu-id="65444-797">The file replication service cannot be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**\_servizio FRS ERR \_ Stop \_**</span><span class="sxs-lookup"><span data-stu-id="65444-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS\_ERR\_STOPPING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-799">8003 (0x1F43)</span><span class="sxs-lookup"><span data-stu-id="65444-799">8003 (0x1F43)</span></span>
</dt> <dt>



<span data-ttu-id="65444-800">Impossibile arrestare il servizio Replica file.</span><span class="sxs-lookup"><span data-stu-id="65444-800">The file replication service cannot be stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ API interna di FRS ERR \_**</span><span class="sxs-lookup"><span data-stu-id="65444-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS\_ERR\_INTERNAL\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-802">8004 (0x1F44)</span><span class="sxs-lookup"><span data-stu-id="65444-802">8004 (0x1F44)</span></span>
</dt> <dt>



<span data-ttu-id="65444-803">La richiesta è stata terminata dall'API del servizio Replica file.</span><span class="sxs-lookup"><span data-stu-id="65444-803">The file replication service API terminated the request.</span></span> <span data-ttu-id="65444-804">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-804">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ Err \_ interno**</span><span class="sxs-lookup"><span data-stu-id="65444-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS\_ERR\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-806">8005 (0x1F45)</span><span class="sxs-lookup"><span data-stu-id="65444-806">8005 (0x1F45)</span></span>
</dt> <dt>



<span data-ttu-id="65444-807">Il servizio Replica file ha terminato la richiesta.</span><span class="sxs-lookup"><span data-stu-id="65444-807">The file replication service terminated the request.</span></span> <span data-ttu-id="65444-808">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-808">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**\_comunicazione del \_ servizio FRS ERR \_**</span><span class="sxs-lookup"><span data-stu-id="65444-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS\_ERR\_SERVICE\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-810">8006 (0x1F46)</span><span class="sxs-lookup"><span data-stu-id="65444-810">8006 (0x1F46)</span></span>
</dt> <dt>



<span data-ttu-id="65444-811">Impossibile contattare il servizio Replica file.</span><span class="sxs-lookup"><span data-stu-id="65444-811">The file replication service cannot be contacted.</span></span> <span data-ttu-id="65444-812">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-812">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**\_ \_ priv sufficiente per FRS ERR \_**</span><span class="sxs-lookup"><span data-stu-id="65444-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS\_ERR\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-814">8007 (0x1F47)</span><span class="sxs-lookup"><span data-stu-id="65444-814">8007 (0x1F47)</span></span>
</dt> <dt>



<span data-ttu-id="65444-815">Il servizio Replica file non è in grado di soddisfare la richiesta perché l'utente non dispone di privilegi sufficienti.</span><span class="sxs-lookup"><span data-stu-id="65444-815">The file replication service cannot satisfy the request because the user has insufficient privileges.</span></span> <span data-ttu-id="65444-816">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-816">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**\_autenticazione FRS ERR \_**</span><span class="sxs-lookup"><span data-stu-id="65444-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS\_ERR\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-818">8008 (0x1F48)</span><span class="sxs-lookup"><span data-stu-id="65444-818">8008 (0x1F48)</span></span>
</dt> <dt>



<span data-ttu-id="65444-819">Il servizio Replica file non è in grado di soddisfare la richiesta perché la RPC autenticata non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="65444-819">The file replication service cannot satisfy the request because authenticated RPC is not available.</span></span> <span data-ttu-id="65444-820">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-820">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**\_priv di elemento padre di FRS ERR \_ \_ insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="65444-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS\_ERR\_PARENT\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-822">8009 (0x1F49)</span><span class="sxs-lookup"><span data-stu-id="65444-822">8009 (0x1F49)</span></span>
</dt> <dt>



<span data-ttu-id="65444-823">Il servizio Replica file non è in grado di soddisfare la richiesta perché l'utente non dispone di privilegi sufficienti per il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="65444-823">The file replication service cannot satisfy the request because the user has insufficient privileges on the domain controller.</span></span> <span data-ttu-id="65444-824">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-824">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_ \_ autenticazione padre ERR \_ FRS**</span><span class="sxs-lookup"><span data-stu-id="65444-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS\_ERR\_PARENT\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-826">8010 (0x1F4A)</span><span class="sxs-lookup"><span data-stu-id="65444-826">8010 (0x1F4A)</span></span>
</dt> <dt>



<span data-ttu-id="65444-827">Il servizio Replica file non è in grado di soddisfare la richiesta perché la RPC autenticata non è disponibile nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="65444-827">The file replication service cannot satisfy the request because authenticated RPC is not available on the domain controller.</span></span> <span data-ttu-id="65444-828">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-828">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**\_da FRS \_ Err \_ figlio \_ a \_ comunicazione padre**</span><span class="sxs-lookup"><span data-stu-id="65444-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS\_ERR\_CHILD\_TO\_PARENT\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-830">8011 (0x1F4B)</span><span class="sxs-lookup"><span data-stu-id="65444-830">8011 (0x1F4B)</span></span>
</dt> <dt>



<span data-ttu-id="65444-831">Il servizio Replica file non è in grado di comunicare con il servizio Replica file sul controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="65444-831">The file replication service cannot communicate with the file replication service on the domain controller.</span></span> <span data-ttu-id="65444-832">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-832">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**\_errore \_ di FRS \_ da padre a \_ \_ comm figlio**</span><span class="sxs-lookup"><span data-stu-id="65444-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS\_ERR\_PARENT\_TO\_CHILD\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-834">8012 (0x1F4C)</span><span class="sxs-lookup"><span data-stu-id="65444-834">8012 (0x1F4C)</span></span>
</dt> <dt>



<span data-ttu-id="65444-835">Il servizio Replica file del controller di dominio non è in grado di comunicare con il servizio Replica file di questo computer.</span><span class="sxs-lookup"><span data-stu-id="65444-835">The file replication service on the domain controller cannot communicate with the file replication service on this computer.</span></span> <span data-ttu-id="65444-836">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-836">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**\_popolamento di \_ SYSVOL Err ERR \_**</span><span class="sxs-lookup"><span data-stu-id="65444-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS\_ERR\_SYSVOL\_POPULATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-838">8013 (0x1F4D)</span><span class="sxs-lookup"><span data-stu-id="65444-838">8013 (0x1F4D)</span></span>
</dt> <dt>



<span data-ttu-id="65444-839">Il servizio Replica file non è in grado di popolare il volume di sistema a causa di un errore interno.</span><span class="sxs-lookup"><span data-stu-id="65444-839">The file replication service cannot populate the system volume because of an internal error.</span></span> <span data-ttu-id="65444-840">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-840">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_ \_ \_ timeout popolare SYSVOL ERR \_**</span><span class="sxs-lookup"><span data-stu-id="65444-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS\_ERR\_SYSVOL\_POPULATE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-842">8014 (0x1F4E)</span><span class="sxs-lookup"><span data-stu-id="65444-842">8014 (0x1F4E)</span></span>
</dt> <dt>



<span data-ttu-id="65444-843">Il servizio Replica file non è in grado di popolare il volume di sistema a causa di un timeout interno.</span><span class="sxs-lookup"><span data-stu-id="65444-843">The file replication service cannot populate the system volume because of an internal timeout.</span></span> <span data-ttu-id="65444-844">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-844">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**il servizio FRS \_ Err \_ SYSVOL \_ è \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="65444-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS\_ERR\_SYSVOL\_IS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-846">8015 (0x1F4F)</span><span class="sxs-lookup"><span data-stu-id="65444-846">8015 (0x1F4F)</span></span>
</dt> <dt>



<span data-ttu-id="65444-847">Il servizio Replica file non è in grado di elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="65444-847">The file replication service cannot process the request.</span></span> <span data-ttu-id="65444-848">Il volume di sistema è occupato con una richiesta precedente.</span><span class="sxs-lookup"><span data-stu-id="65444-848">The system volume is busy with a previous request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**abbassamento di volume \_ SYSVOL Err di FRS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65444-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS\_ERR\_SYSVOL\_DEMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-850">8016 (0x1F50)</span><span class="sxs-lookup"><span data-stu-id="65444-850">8016 (0x1F50)</span></span>
</dt> <dt>



<span data-ttu-id="65444-851">Il servizio Replica file non è in grado di arrestare la replica del volume di sistema a causa di un errore interno.</span><span class="sxs-lookup"><span data-stu-id="65444-851">The file replication service cannot stop replicating the system volume because of an internal error.</span></span> <span data-ttu-id="65444-852">È possibile che nel registro eventi siano disponibili ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="65444-852">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="65444-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_parametro servizio FRS ERR \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65444-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS\_ERR\_INVALID\_SERVICE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65444-854">8017 (0x1F51)</span><span class="sxs-lookup"><span data-stu-id="65444-854">8017 (0x1F51)</span></span>
</dt> <dt>



<span data-ttu-id="65444-855">Il servizio Replica file ha rilevato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="65444-855">The file replication service detected an invalid parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65444-856">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65444-856">Requirements</span></span>



| <span data-ttu-id="65444-857">Requisito</span><span class="sxs-lookup"><span data-stu-id="65444-857">Requirement</span></span> | <span data-ttu-id="65444-858">Valore</span><span class="sxs-lookup"><span data-stu-id="65444-858">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65444-859">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65444-859">Minimum supported client</span></span><br/> | <span data-ttu-id="65444-860">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="65444-860">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="65444-861">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65444-861">Minimum supported server</span></span><br/> | <span data-ttu-id="65444-862">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65444-862">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65444-863">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65444-863">Header</span></span><br/>                   | <dl> <span data-ttu-id="65444-864"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="65444-864"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65444-865">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65444-865">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65444-866">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="65444-866">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




