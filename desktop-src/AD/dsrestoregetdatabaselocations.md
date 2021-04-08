---
title: Funzione DsRestoreGetDatabaseLocations (ntdsbcli. h)
description: Ottiene i percorsi in cui devono essere copiati i file di backup durante un'operazione di ripristino.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestoreGetDatabaseLocations
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874133"
---
# <a name="dsrestoregetdatabaselocations-function"></a><span data-ttu-id="b5fa6-104">DsRestoreGetDatabaseLocations (funzione)</span><span class="sxs-lookup"><span data-stu-id="b5fa6-104">DsRestoreGetDatabaseLocations function</span></span>

<span data-ttu-id="b5fa6-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b5fa6-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b5fa6-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="b5fa6-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="b5fa6-108">La funzione **DsRestoreGetDatabaseLocations** ottiene i percorsi in cui devono essere copiati i file di backup durante un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-108">The **DsRestoreGetDatabaseLocations** function obtains the locations where backup files should be copied during a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5fa6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5fa6-109">Syntax</span></span>


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="b5fa6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5fa6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5fa6-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5fa6-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5fa6-112">Contiene l'handle del contesto di ripristino ottenuto con la funzione [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="b5fa6-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b5fa6-113">*pszDatabaseLocationList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5fa6-113">*pszDatabaseLocationList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5fa6-114">Puntatore a un puntatore di stringa che riceve l'elenco dei percorsi di database come percorsi UNC.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-114">Pointer to a string pointer that receives the list of database locations as UNC paths.</span></span> <span data-ttu-id="b5fa6-115">Questo elenco riceve un doppio elenco con terminazione null di singole stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-115">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="b5fa6-116">Questo buffer viene allocato dalla funzione **DsRestoreGetDatabaseLocations** e deve essere liberato quando non è più necessario chiamando la funzione [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="b5fa6-116">This buffer is allocated by the **DsRestoreGetDatabaseLocations** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="b5fa6-117">Il primo carattere di ogni nome file contiene una delle [**costanti BFT**](bft-constants.md) che identificano il tipo di nome.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-117">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the name type.</span></span> <span data-ttu-id="b5fa6-118">La funzione **DsRestoreGetDatabaseLocations** fornisce solo i tipi di nomi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-118">The **DsRestoreGetDatabaseLocations** function only supplies the following name types.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="b5fa6-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_database NTDS \_ BFT**</span><span class="sxs-lookup"><span data-stu-id="b5fa6-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="b5fa6-120">Il file di database NTDS deve essere copiato in questo file.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-120">The NTDS database file should be copied to this file.</span></span> <span data-ttu-id="b5fa6-121">Si tratta del file che è stato identificato come **BFT \_ NTDS \_ database** durante l'esecuzione del backup.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-121">This is the file that was identified as **BFT\_NTDS\_DATABASE** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span data-ttu-id="b5fa6-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**\_dir BFT log \_**</span><span class="sxs-lookup"><span data-stu-id="b5fa6-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="b5fa6-123">Tutti i file di log vengono copiati in questa directory.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-123">All log files are copied to this directory.</span></span> <span data-ttu-id="b5fa6-124">I file di log sono stati identificati come **\_ log BFT** quando è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-124">The log files were identified as **BFT\_LOG** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span data-ttu-id="b5fa6-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**\_dir del checkpoint BFT \_**</span><span class="sxs-lookup"><span data-stu-id="b5fa6-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="b5fa6-126">Tutti i file di patch vengono copiati in questa directory.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-126">All patch files are copied to this directory.</span></span> <span data-ttu-id="b5fa6-127">I file della patch sono stati identificati come **\_ \_ file di patch BFT** quando è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-127">The patch files were identified as **BFT\_PATCH\_FILE** when the backup was performed.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b5fa6-128">*pcbSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5fa6-128">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5fa6-129">Puntatore al valore **DWORD** che riceve le dimensioni, in byte, del buffer *pszDatabaseLocationList* .</span><span class="sxs-lookup"><span data-stu-id="b5fa6-129">Pointer to **DWORD** value that receives the size, in bytes, of the *pszDatabaseLocationList* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5fa6-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5fa6-130">Return value</span></span>

<span data-ttu-id="b5fa6-131">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-131">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="b5fa6-132">Nell'elenco seguente sono elencati i possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-132">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="b5fa6-133">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="b5fa6-133">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="b5fa6-134">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-134">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="b5fa6-135">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-135">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="b5fa6-136">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="b5fa6-136">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="b5fa6-137">*HBC*, *pszDatabaseLocationList* o *pcbSize* non sono validi.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-137">*hbc*, *pszDatabaseLocationList*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="b5fa6-138">**ERRORE \_ di \_ memoria insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="b5fa6-138">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="b5fa6-139">Si è verificato un errore di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-139">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5fa6-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5fa6-140">Remarks</span></span>

<span data-ttu-id="b5fa6-141">La funzione **DsRestoreGetDatabaseLocations** può essere usata per ottenere le directory di ripristino senza accedere ai dati di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="b5fa6-141">The **DsRestoreGetDatabaseLocations** function can be used to obtain the restoration directories without access to the backed up data.</span></span> <span data-ttu-id="b5fa6-142">A tale scopo, chiamare [**DsRestorePrepare**](dsrestoreprepare.md) con **null** per il parametro *pvExpiryToken* .</span><span class="sxs-lookup"><span data-stu-id="b5fa6-142">To do this, call [**DsRestorePrepare**](dsrestoreprepare.md) with **NULL** for the *pvExpiryToken* parameter.</span></span> <span data-ttu-id="b5fa6-143">In questo modo **DsRestorePrepare** restituisce un handle di contesto limitato che può essere utilizzato solo con la funzione **DsRestoreGetDatabaseLocations** .</span><span class="sxs-lookup"><span data-stu-id="b5fa6-143">This causes **DsRestorePrepare** to return a restricted context handle which can only be used with the **DsRestoreGetDatabaseLocations** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5fa6-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5fa6-144">Requirements</span></span>



| <span data-ttu-id="b5fa6-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5fa6-145">Requirement</span></span> | <span data-ttu-id="b5fa6-146">Valore</span><span class="sxs-lookup"><span data-stu-id="b5fa6-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5fa6-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5fa6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b5fa6-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5fa6-148">Windows Vista</span></span><br/>                                                                              |
| <span data-ttu-id="b5fa6-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5fa6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b5fa6-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5fa6-150">Windows Server 2008</span></span><br/>                                                                        |
| <span data-ttu-id="b5fa6-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5fa6-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5fa6-152"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5fa6-152"><dt>Ntdsbcli.h</dt></span></span> </dl>                 |
| <span data-ttu-id="b5fa6-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5fa6-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5fa6-154"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5fa6-154"><dt>Ntdsbcli.lib</dt></span></span> </dl>               |
| <span data-ttu-id="b5fa6-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b5fa6-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5fa6-156"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5fa6-156"><dt>Ntdsbcli.dll</dt></span></span> </dl>               |
| <span data-ttu-id="b5fa6-157">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b5fa6-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b5fa6-158">**DsRestoreGetDatabaseLocationsW** (Unicode) e **DsRestoreGetDatabaseLocationsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b5fa6-158">**DsRestoreGetDatabaseLocationsW** (Unicode) and **DsRestoreGetDatabaseLocationsA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5fa6-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5fa6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5fa6-160">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="b5fa6-160">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="b5fa6-161">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="b5fa6-161">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="b5fa6-162">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="b5fa6-162">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="b5fa6-163">Ripristino di Active Directory</span><span class="sxs-lookup"><span data-stu-id="b5fa6-163">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> </dl>

 

