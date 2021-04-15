---
title: Funzione DsBackupPrepare (ntdsbcli. h)
description: Prepara la directory sul server specificato per il backup online e restituisce un handle del contesto di backup utilizzato nelle chiamate successive ad altre funzioni di backup.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupPrepare
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477134"
---
# <a name="dsbackupprepare-function"></a><span data-ttu-id="0333b-104">DsBackupPrepare (funzione)</span><span class="sxs-lookup"><span data-stu-id="0333b-104">DsBackupPrepare function</span></span>

<span data-ttu-id="0333b-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="0333b-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0333b-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="0333b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0333b-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="0333b-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="0333b-108">La funzione **DsBackupPrepare** prepara la directory sul server specificato per il backup online e restituisce un handle del contesto di backup utilizzato nelle chiamate successive ad altre funzioni di backup.</span><span class="sxs-lookup"><span data-stu-id="0333b-108">The **DsBackupPrepare** function prepares the directory on the specified server for the online backup and returns a backup context handle used in subsequent calls to other backup functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="0333b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0333b-109">Syntax</span></span>


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="0333b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0333b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0333b-111">*szBackupServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0333b-111">*szBackupServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0333b-112">Puntatore a una stringa con terminazione null che contiene il nome del server di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="0333b-112">Pointer to a null-terminated string that contains the name of the server to backup.</span></span> <span data-ttu-id="0333b-113">Le barre rovesciate precedenti sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="0333b-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="0333b-114">Il server deve essere lo stesso computer da cui viene chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="0333b-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="0333b-115">Il nome del server non può contenere un carattere di sottolineatura ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="0333b-115">The server name cannot contain an underscore (\_) character.</span></span> <span data-ttu-id="0333b-116">Un esempio di nome di server è " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="0333b-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="0333b-117">*grbit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0333b-117">*grbit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0333b-118">Determina se verrà eseguito il backup dei file di log.</span><span class="sxs-lookup"><span data-stu-id="0333b-118">Determines if the log files will be backed up.</span></span> <span data-ttu-id="0333b-119">Questo valore deve essere sempre 0 perché i backup incrementali non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="0333b-119">This value should always be 0 because incremental backups are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0333b-120">*btBackupType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0333b-120">*btBackupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0333b-121">Specifica il tipo di backup.</span><span class="sxs-lookup"><span data-stu-id="0333b-121">Specifies the type of backup.</span></span> <span data-ttu-id="0333b-122">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0333b-122">This can be one of the following values.</span></span>

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span data-ttu-id="0333b-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**tipo di BACKUP \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="0333b-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP\_TYPE\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="0333b-124">Specifica un backup completo.</span><span class="sxs-lookup"><span data-stu-id="0333b-124">Specifies a full backup.</span></span> <span data-ttu-id="0333b-125">Viene eseguito il backup della directory completa (DIT, file di log e file di aggiornamento).</span><span class="sxs-lookup"><span data-stu-id="0333b-125">The complete directory (DIT, log files, and update files) are backed up.</span></span> <span data-ttu-id="0333b-126">Viene eseguito il backup di tutti i dati e i file di log delle transazioni vengono troncati.</span><span class="sxs-lookup"><span data-stu-id="0333b-126">All data is backed up and transaction log files are truncated.</span></span> <span data-ttu-id="0333b-127">Sono supportati solo backup completi.</span><span class="sxs-lookup"><span data-stu-id="0333b-127">Only full backups are supported.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span data-ttu-id="0333b-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_ \_ solo log dei tipi di backup \_**</span><span class="sxs-lookup"><span data-stu-id="0333b-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**BACKUP\_TYPE\_LOGS\_ONLY**</span></span>


</dt> <dd>

<span data-ttu-id="0333b-129">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0333b-129">This value is not supported.</span></span> <span data-ttu-id="0333b-130">Specifica che verrà eseguito il backup solo dei log del database e non del database stesso.</span><span class="sxs-lookup"><span data-stu-id="0333b-130">Specifies that only the database logs, and not the database itself, will be backed up.</span></span> <span data-ttu-id="0333b-131">Questa operazione viene in genere utilizzata durante l'esecuzione di un backup differenziale o incrementale.</span><span class="sxs-lookup"><span data-stu-id="0333b-131">This is normally used when performing a differential or incremental backup.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span data-ttu-id="0333b-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**tipo di BACKUP \_ \_ incrementale**</span><span class="sxs-lookup"><span data-stu-id="0333b-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**BACKUP\_TYPE\_INCREMENTAL**</span></span>


</dt> <dd>

<span data-ttu-id="0333b-133">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0333b-133">This value is not supported.</span></span> <span data-ttu-id="0333b-134">**DsBackupPrepare** restituisce **l' \_ errore \_ parametro non valido**.</span><span class="sxs-lookup"><span data-stu-id="0333b-134">**DsBackupPrepare** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0333b-135">*ppvExpiryToken* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0333b-135">*ppvExpiryToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0333b-136">Puntatore a un valore **PVOID** che riceve un puntatore a un token di scadenza associato a questo backup.</span><span class="sxs-lookup"><span data-stu-id="0333b-136">Pointer to a **PVOID** value that receives a pointer to an expiry token associated with this backup.</span></span> <span data-ttu-id="0333b-137">*pcbExpiryTokenSize* riceve le dimensioni, in byte, di questi dati.</span><span class="sxs-lookup"><span data-stu-id="0333b-137">*pcbExpiryTokenSize* receives the size, in bytes, of this data.</span></span> <span data-ttu-id="0333b-138">Il chiamante deve salvare il contenuto di questo token con il backup perché il token deve essere passato a [**DsRestorePrepare**](dsrestoreprepare.md) durante il tentativo di ripristino dei dati.</span><span class="sxs-lookup"><span data-stu-id="0333b-138">The caller must save the contents of this token with the backup because the token must be passed to [**DsRestorePrepare**](dsrestoreprepare.md) when attempting to restore data.</span></span> <span data-ttu-id="0333b-139">Dopo che il token è stato archiviato e non è più necessario, il chiamante deve liberare la memoria allocata usando [**DsBackupFree**](dsbackupfree.md).</span><span class="sxs-lookup"><span data-stu-id="0333b-139">After the token has been stored and is no longer required, the caller should free the allocated memory using [**DsBackupFree**](dsbackupfree.md).</span></span>

</dd> <dt>

<span data-ttu-id="0333b-140">*pcbExpiryTokenSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0333b-140">*pcbExpiryTokenSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0333b-141">Puntatore a un valore **DWORD** che riceve le dimensioni, in byte, del token in *ppvExpiryToken*.</span><span class="sxs-lookup"><span data-stu-id="0333b-141">Pointer to a **DWORD** value that receives the size, in bytes, of the token in *ppvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="0333b-142">*phbc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0333b-142">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0333b-143">Puntatore a un valore **HBC** che riceve l'handle per il backup.</span><span class="sxs-lookup"><span data-stu-id="0333b-143">Pointer to an **HBC** value that receives the handle for the backup.</span></span> <span data-ttu-id="0333b-144">Questo handle viene utilizzato per chiamare altre funzioni di backup del servizio directory, ad esempio [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsBackupEnd**](dsbackupend.md).</span><span class="sxs-lookup"><span data-stu-id="0333b-144">This handle is used when calling other Directory Service backup functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsBackupEnd**](dsbackupend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0333b-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0333b-145">Return value</span></span>

<span data-ttu-id="0333b-146">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="0333b-146">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="0333b-147">Nell'elenco seguente sono elencati altri possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="0333b-147">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="0333b-148">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="0333b-148">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="0333b-149">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="0333b-149">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="0333b-150">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="0333b-150">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="0333b-151">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0333b-151">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="0333b-152">*szBackupServer* o *phbcBackupContext* non sono validi.</span><span class="sxs-lookup"><span data-stu-id="0333b-152">*szBackupServer* or *phbcBackupContext* are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0333b-153">**ERRORE \_ di \_ memoria insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="0333b-153">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="0333b-154">Si è verificato un errore di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="0333b-154">A memory allocation failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0333b-155">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="0333b-155">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="0333b-156">Il server in *szBackupServer* non è stato trovato, non è un controller di dominio o *szBackupServer* non è formattato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0333b-156">The server in *szBackupServer* could not be found, is not a domain controller or *szBackupServer* is not formatted correctly.</span></span> <span data-ttu-id="0333b-157">Questo valore è definito in ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="0333b-157">This value is defined in ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="0333b-158">**hrInvalidParam**</span><span class="sxs-lookup"><span data-stu-id="0333b-158">**hrInvalidParam**</span></span>
</dt> <dd>

<span data-ttu-id="0333b-159">*ppvExpiryToken* e/o *pcbExpiryTokenSize* non sono validi.</span><span class="sxs-lookup"><span data-stu-id="0333b-159">*ppvExpiryToken* and/or *pcbExpiryTokenSize* are invalid.</span></span> <span data-ttu-id="0333b-160">Questo valore è definito in ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="0333b-160">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="0333b-161">**\_binding RPC S \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0333b-161">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="0333b-162">La funzione viene chiamata in modalità remota o il server in *szServerName* non è un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="0333b-162">The function is called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0333b-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="0333b-163">Remarks</span></span>

<span data-ttu-id="0333b-164">Questa funzione richiede che il chiamante disponga del **privilegio \_ \_ nome backup se** .</span><span class="sxs-lookup"><span data-stu-id="0333b-164">This function requires that the caller has the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="0333b-165">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per modificare il contesto di sicurezza in cui viene chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="0333b-165">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to change the security context under which this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="0333b-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0333b-166">Requirements</span></span>



| <span data-ttu-id="0333b-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="0333b-167">Requirement</span></span> | <span data-ttu-id="0333b-168">Valore</span><span class="sxs-lookup"><span data-stu-id="0333b-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0333b-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0333b-169">Minimum supported client</span></span><br/> | <span data-ttu-id="0333b-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0333b-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0333b-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0333b-171">Minimum supported server</span></span><br/> | <span data-ttu-id="0333b-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0333b-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0333b-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0333b-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="0333b-174"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="0333b-174"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="0333b-175">Libreria</span><span class="sxs-lookup"><span data-stu-id="0333b-175">Library</span></span><br/>                  | <dl> <span data-ttu-id="0333b-176"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0333b-176"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="0333b-177">DLL</span><span class="sxs-lookup"><span data-stu-id="0333b-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0333b-178"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0333b-178"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="0333b-179">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0333b-179">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0333b-180">**DsBackupPrepareW** (Unicode) e **DsBackupPrepareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0333b-180">**DsBackupPrepareW** (Unicode) and **DsBackupPrepareA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0333b-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0333b-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0333b-182">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="0333b-182">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="0333b-183">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="0333b-183">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="0333b-184">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="0333b-184">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="0333b-185">**DsBackupEnd**</span><span class="sxs-lookup"><span data-stu-id="0333b-185">**DsBackupEnd**</span></span>](dsbackupend.md)
</dt> <dt>

[<span data-ttu-id="0333b-186">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="0333b-186">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="0333b-187">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="0333b-187">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="0333b-188">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="0333b-188">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

