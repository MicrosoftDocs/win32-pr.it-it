---
title: Funzione DsBackupGetDatabaseNames (ntdsbcli. h)
description: Ottiene l'elenco dei file di database di cui eseguire il backup per il contesto di backup specificato.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupGetDatabaseNames
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477135"
---
# <a name="dsbackupgetdatabasenames-function"></a><span data-ttu-id="6d176-104">DsBackupGetDatabaseNames (funzione)</span><span class="sxs-lookup"><span data-stu-id="6d176-104">DsBackupGetDatabaseNames function</span></span>

<span data-ttu-id="6d176-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="6d176-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6d176-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6d176-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6d176-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="6d176-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="6d176-108">La funzione **DsBackupGetDatabaseNames** Ottiene l'elenco dei file di database di cui eseguire il backup per il contesto di backup specificato.</span><span class="sxs-lookup"><span data-stu-id="6d176-108">The **DsBackupGetDatabaseNames** function obtains the list of database files to be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d176-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d176-109">Syntax</span></span>


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="6d176-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d176-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d176-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d176-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d176-112">Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="6d176-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6d176-113">*pszAttachmentInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6d176-113">*pszAttachmentInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d176-114">Puntatore a un puntatore di stringa che riceve l'elenco dei nomi di file di database come percorsi UNC.</span><span class="sxs-lookup"><span data-stu-id="6d176-114">Pointer to a string pointer that receives the list of database file names as UNC paths.</span></span> <span data-ttu-id="6d176-115">Questo valore deve essere inizializzato su **null** prima di chiamare **DsBackupGetDatabaseNames**.</span><span class="sxs-lookup"><span data-stu-id="6d176-115">This value must be initialized to **NULL** prior to calling **DsBackupGetDatabaseNames**.</span></span>

<span data-ttu-id="6d176-116">Questo elenco riceve un doppio elenco con terminazione null di singole stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="6d176-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="6d176-117">Questo buffer viene allocato dalla funzione **DsBackupGetDatabaseNames** e deve essere liberato quando non è più necessario chiamando la funzione [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="6d176-117">This buffer is allocated by the **DsBackupGetDatabaseNames** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="6d176-118">Il primo carattere di ogni nome di file contiene una delle [**costanti BFT**](bft-constants.md) che identificano il tipo di nome.</span><span class="sxs-lookup"><span data-stu-id="6d176-118">The first character of each file name contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span> <span data-ttu-id="6d176-119">La funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) fornisce solo i tipi di nomi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6d176-119">The [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function only supplies the following types of names.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="6d176-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_database NTDS \_ BFT**</span><span class="sxs-lookup"><span data-stu-id="6d176-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="6d176-121">Il file è un file di database NTDS.</span><span class="sxs-lookup"><span data-stu-id="6d176-121">The file is an NTDS database file.</span></span> <span data-ttu-id="6d176-122">Questo file deve essere copiato nel file identificato come **BFT \_ NTDS \_ database** quando vengono ripristinati i dati.</span><span class="sxs-lookup"><span data-stu-id="6d176-122">This file should be copied to the file identified as **BFT\_NTDS\_DATABASE** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span data-ttu-id="6d176-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**\_log BFT**</span><span class="sxs-lookup"><span data-stu-id="6d176-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>


</dt> <dd>

<span data-ttu-id="6d176-124">Il file è un file di log.</span><span class="sxs-lookup"><span data-stu-id="6d176-124">The file is a log file.</span></span> <span data-ttu-id="6d176-125">Tutti i file di log vengono copiati nella directory identificata come directory di **\_ log \_ BFT** quando vengono ripristinati i dati.</span><span class="sxs-lookup"><span data-stu-id="6d176-125">All log files are copied to the directory identified as **BFT\_LOG\_DIR** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span data-ttu-id="6d176-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_file patch \_ BFT**</span><span class="sxs-lookup"><span data-stu-id="6d176-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>


</dt> <dd>

<span data-ttu-id="6d176-127">Il file è un file di patch.</span><span class="sxs-lookup"><span data-stu-id="6d176-127">The file is a patch file.</span></span> <span data-ttu-id="6d176-128">Tutti i file di patch vengono copiati nella directory identificata come **BFT \_ Checkpoint \_** quando i dati vengono ripristinati.</span><span class="sxs-lookup"><span data-stu-id="6d176-128">All patch files are copied to the directory identified as **BFT\_CHECKPOINT\_DIR** when the data is restored.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6d176-129">*pcbSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6d176-129">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d176-130">Puntatore al valore **DWORD** che riceve le dimensioni, in byte, del buffer *pszAttachmentInfo* .</span><span class="sxs-lookup"><span data-stu-id="6d176-130">Pointer to **DWORD** value that receives the size, in bytes, of the *pszAttachmentInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d176-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d176-131">Return value</span></span>

<span data-ttu-id="6d176-132">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6d176-132">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="6d176-133">Nell'elenco seguente sono elencati altri possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="6d176-133">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="6d176-134">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="6d176-134">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="6d176-135">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="6d176-135">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="6d176-136">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="6d176-136">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="6d176-137">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6d176-137">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="6d176-138">*HBC*, *pszAttachmentInfo* o *pcbSize* non sono validi.</span><span class="sxs-lookup"><span data-stu-id="6d176-138">*hbc*, *pszAttachmentInfo*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="6d176-139">**ERRORE \_ di \_ memoria insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="6d176-139">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="6d176-140">Si è verificato un errore di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="6d176-140">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d176-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d176-141">Remarks</span></span>

<span data-ttu-id="6d176-142">La funzione **DsBackupGetDatabaseNames** fornisce un elenco dei file di database necessari per un backup.</span><span class="sxs-lookup"><span data-stu-id="6d176-142">The **DsBackupGetDatabaseNames** function provides a list of the database files necessary for a backup.</span></span> <span data-ttu-id="6d176-143">Un backup completo è costituito dai file di database e dai file di log forniti dalla funzione [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) .</span><span class="sxs-lookup"><span data-stu-id="6d176-143">A full backup consists of the database files and the log files provided by the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function.</span></span> <span data-ttu-id="6d176-144">I backup incrementali dei server Active Directory non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="6d176-144">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d176-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d176-145">Requirements</span></span>



| <span data-ttu-id="6d176-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d176-146">Requirement</span></span> | <span data-ttu-id="6d176-147">Valore</span><span class="sxs-lookup"><span data-stu-id="6d176-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d176-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d176-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6d176-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d176-149">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="6d176-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d176-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6d176-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d176-151">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="6d176-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d176-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d176-153"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d176-153"><dt>Ntdsbcli.h</dt></span></span> </dl>       |
| <span data-ttu-id="6d176-154">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d176-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d176-155"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d176-155"><dt>Ntdsbcli.lib</dt></span></span> </dl>     |
| <span data-ttu-id="6d176-156">DLL</span><span class="sxs-lookup"><span data-stu-id="6d176-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d176-157"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d176-157"><dt>Ntdsbcli.dll</dt></span></span> </dl>     |
| <span data-ttu-id="6d176-158">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6d176-158">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6d176-159">**DsBackupGetDatabaseNamesW** (Unicode) e **DsBackupGetDatabaseNamesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6d176-159">**DsBackupGetDatabaseNamesW** (Unicode) and **DsBackupGetDatabaseNamesA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d176-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d176-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d176-161">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="6d176-161">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="6d176-162">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="6d176-162">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="6d176-163">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="6d176-163">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="6d176-164">**Costanti BFT**</span><span class="sxs-lookup"><span data-stu-id="6d176-164">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="6d176-165">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d176-165">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="6d176-166">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="6d176-166">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

