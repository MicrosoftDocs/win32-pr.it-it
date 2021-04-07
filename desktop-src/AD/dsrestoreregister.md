---
title: Funzione DsRestoreRegister (ntdsbcli. h)
description: Registra un'operazione di ripristino.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestoreRegister
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048483"
---
# <a name="dsrestoreregister-function"></a><span data-ttu-id="87aba-104">DsRestoreRegister (funzione)</span><span class="sxs-lookup"><span data-stu-id="87aba-104">DsRestoreRegister function</span></span>

<span data-ttu-id="87aba-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="87aba-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87aba-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="87aba-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="87aba-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="87aba-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="87aba-108">La funzione **DsRestoreRegister** registra un'operazione di ripristino. Questa funzione consente di bloccare tutte le successive operazioni di ripristino e impedisce l'avvio della destinazione di ripristino fino a quando non viene chiamata la funzione [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="87aba-108">The **DsRestoreRegister** function registers a restore operation.This function interlocks all subsequent restore operations and prevents the restore target from starting until the [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="87aba-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87aba-109">Syntax</span></span>


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a><span data-ttu-id="87aba-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="87aba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87aba-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87aba-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87aba-112">Contiene l'handle del contesto di ripristino ottenuto con la funzione [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="87aba-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-113">*szCheckPointFilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87aba-113">*szCheckPointFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87aba-114">Puntatore a una stringa con terminazione null che contiene il percorso del file del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="87aba-114">Pointer to a null-terminated string that contains the path to the checkpoint file.</span></span> <span data-ttu-id="87aba-115">Questo percorso viene fornito dalla funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e ha un valore **BFT** di **BFT \_ Checkpoint \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="87aba-115">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_CHECKPOINT\_DIR**.</span></span> <span data-ttu-id="87aba-116">Corrisponde in genere al percorso del database di sistema.</span><span class="sxs-lookup"><span data-stu-id="87aba-116">Typically this is the same as the system database path.</span></span> <span data-ttu-id="87aba-117">Questo percorso è necessario per la corretta funzione di ripristino del backup.</span><span class="sxs-lookup"><span data-stu-id="87aba-117">This path is required for proper backup restore function.</span></span> <span data-ttu-id="87aba-118">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="87aba-118">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="87aba-119">Il passaggio di un **valore null** in questo parametro causerà un errore durante il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="87aba-119">Passing **NULL** in this parameter will cause an error during the restore process.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-120">*szLogPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87aba-120">*szLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87aba-121">Puntatore a una stringa con terminazione null che contiene il percorso in cui verranno ripristinati i file di log.</span><span class="sxs-lookup"><span data-stu-id="87aba-121">Pointer to a null-terminated string that contains the path where the log files will be restored.</span></span> <span data-ttu-id="87aba-122">Questo percorso viene fornito dalla funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e ha un valore **BFT** di **BFT \_ log \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="87aba-122">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_LOG\_DIR**.</span></span> <span data-ttu-id="87aba-123">Se il percorso punta a una directory vuota, vengono creati nuovi file di log.</span><span class="sxs-lookup"><span data-stu-id="87aba-123">If the path points to an empty directory, new log files are created there.</span></span> <span data-ttu-id="87aba-124">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="87aba-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-125">*rgrstmap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87aba-125">*rgrstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87aba-126">Matrice di strutture [**\_ RSTMAP edb**](edb-rstmap.md) che contiene i percorsi vecchi e nuovi per ogni database.</span><span class="sxs-lookup"><span data-stu-id="87aba-126">An array of [**EDB\_RSTMAP**](edb-rstmap.md) structures that contains the old and new paths for each database.</span></span> <span data-ttu-id="87aba-127">Esiste una struttura per ogni database.</span><span class="sxs-lookup"><span data-stu-id="87aba-127">There is one structure for each database.</span></span> <span data-ttu-id="87aba-128">Per la directory, esiste una struttura per il database di sistema e un'altra struttura per il database di directory.</span><span class="sxs-lookup"><span data-stu-id="87aba-128">For the directory, there is a structure for the system database and another structure for the directory database.</span></span> <span data-ttu-id="87aba-129">L'ordine degli elementi nella matrice non è rilevante.</span><span class="sxs-lookup"><span data-stu-id="87aba-129">The order of the elements in the array does not matter.</span></span> <span data-ttu-id="87aba-130">Il parametro *crstmap* contiene il numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="87aba-130">The *crstmap* parameter contains the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-131">*crstmap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87aba-131">*crstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87aba-132">Contiene il numero di elementi nella matrice *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="87aba-132">Contains the number of elements in the *rgrstmap* array.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-133">*szBackupLogPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87aba-133">*szBackupLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87aba-134">Puntatore a una stringa con terminazione null che contiene il percorso in cui risiedono attualmente i file di log di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="87aba-134">Pointer to a null-terminated string that contains the path where the backed up log files currently reside.</span></span> <span data-ttu-id="87aba-135">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="87aba-135">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-136">*genLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87aba-136">*genLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87aba-137">Contiene il numero di log più basso da ripristinare in questa sessione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="87aba-137">Contains the lowest log number to restore in this restore session.</span></span> <span data-ttu-id="87aba-138">Si tratta di un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="87aba-138">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-139">*genHigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87aba-139">*genHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87aba-140">Contiene il numero massimo di log da ripristinare in questa sessione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="87aba-140">Contains the highest log number to restore in this restore session.</span></span> <span data-ttu-id="87aba-141">Si tratta di un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="87aba-141">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87aba-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87aba-142">Return value</span></span>

<span data-ttu-id="87aba-143">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="87aba-143">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="87aba-144">Nell'elenco seguente sono elencati i possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="87aba-144">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="87aba-145">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="87aba-145">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="87aba-146">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="87aba-146">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="87aba-147">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="87aba-147">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-148">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="87aba-148">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="87aba-149">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="87aba-149">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="87aba-150">**hrMissingExpiryToken**</span><span class="sxs-lookup"><span data-stu-id="87aba-150">**hrMissingExpiryToken**</span></span>
</dt> <dd>

<span data-ttu-id="87aba-151">Il token di scadenza fornito a [**DsRestorePrepare**](dsrestoreprepare.md) non è valido.</span><span class="sxs-lookup"><span data-stu-id="87aba-151">The expiry token supplied to [**DsRestorePrepare**](dsrestoreprepare.md) was invalid.</span></span> <span data-ttu-id="87aba-152">Questo valore è definito in ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="87aba-152">This value is defined in Ntdsbmsg.h.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87aba-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87aba-153">Requirements</span></span>



| <span data-ttu-id="87aba-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="87aba-154">Requirement</span></span> | <span data-ttu-id="87aba-155">Valore</span><span class="sxs-lookup"><span data-stu-id="87aba-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87aba-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87aba-156">Minimum supported client</span></span><br/> | <span data-ttu-id="87aba-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87aba-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87aba-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87aba-158">Minimum supported server</span></span><br/> | <span data-ttu-id="87aba-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87aba-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87aba-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87aba-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="87aba-161"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="87aba-161"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="87aba-162">Libreria</span><span class="sxs-lookup"><span data-stu-id="87aba-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="87aba-163"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87aba-163"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="87aba-164">DLL</span><span class="sxs-lookup"><span data-stu-id="87aba-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87aba-165"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87aba-165"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="87aba-166">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="87aba-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="87aba-167">**DsRestoreRegisterW** (Unicode) e **DsRestoreRegisterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="87aba-167">**DsRestoreRegisterW** (Unicode) and **DsRestoreRegisterA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="87aba-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87aba-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87aba-169">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="87aba-169">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="87aba-170">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="87aba-170">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="87aba-171">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="87aba-171">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="87aba-172">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="87aba-172">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> <dt>

[<span data-ttu-id="87aba-173">**\_RSTMAP edb**</span><span class="sxs-lookup"><span data-stu-id="87aba-173">**EDB\_RSTMAP**</span></span>](edb-rstmap.md)
</dt> <dt>

[<span data-ttu-id="87aba-174">Ripristino di Active Directory</span><span class="sxs-lookup"><span data-stu-id="87aba-174">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="87aba-175">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="87aba-175">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

