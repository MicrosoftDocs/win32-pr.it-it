---
title: Funzione DsBackupGetBackupLogs (ntdsbcli. h)
description: Ottiene l'elenco dei file di log di cui è necessario eseguire il backup per il contesto di backup specificato.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupGetBackupLogs
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964340"
---
# <a name="dsbackupgetbackuplogs-function"></a><span data-ttu-id="6e598-104">DsBackupGetBackupLogs (funzione)</span><span class="sxs-lookup"><span data-stu-id="6e598-104">DsBackupGetBackupLogs function</span></span>

<span data-ttu-id="6e598-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="6e598-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6e598-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6e598-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6e598-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="6e598-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="6e598-108">La funzione **DsBackupGetBackupLogs** Ottiene l'elenco dei file di log di cui è necessario eseguire il backup per il contesto di backup specificato.</span><span class="sxs-lookup"><span data-stu-id="6e598-108">The **DsBackupGetBackupLogs** function obtains the list of log files that must be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e598-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e598-109">Syntax</span></span>


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="6e598-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e598-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e598-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e598-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e598-112">Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="6e598-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6e598-113">*pszBackupLogFiles* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e598-113">*pszBackupLogFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e598-114">Puntatore a un puntatore di stringa che riceve l'elenco dei nomi dei file di log come percorsi UNC.</span><span class="sxs-lookup"><span data-stu-id="6e598-114">Pointer to a string pointer that receives the list of log file names as UNC paths.</span></span> <span data-ttu-id="6e598-115">Inizializzare questo valore su **null** prima di chiamare **DsBackupGetBackupLogs**.</span><span class="sxs-lookup"><span data-stu-id="6e598-115">Initialize this value to **NULL** before calling **DsBackupGetBackupLogs**.</span></span>

<span data-ttu-id="6e598-116">Questo elenco riceve un doppio elenco con terminazione null di singole stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="6e598-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="6e598-117">Questo buffer viene allocato dalla funzione **DsBackupGetBackupLogs** e deve essere liberato quando non è più necessario chiamando la funzione [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="6e598-117">This buffer is allocated by the **DsBackupGetBackupLogs** function and must be freed when no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="6e598-118">Il primo carattere di ogni nome file contiene una delle [**costanti BFT**](bft-constants.md) che identificano il tipo di nome.</span><span class="sxs-lookup"><span data-stu-id="6e598-118">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span>

</dd> <dt>

<span data-ttu-id="6e598-119">*pcbSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e598-119">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e598-120">Puntatore al valore **DWORD** che riceve le dimensioni, in byte, del buffer *pszBackupLogFiles* .</span><span class="sxs-lookup"><span data-stu-id="6e598-120">Pointer to **DWORD** value that receives the size, in bytes, of the *pszBackupLogFiles* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e598-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e598-121">Return value</span></span>

<span data-ttu-id="6e598-122">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6e598-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="6e598-123">Nell'elenco seguente sono elencati altri possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="6e598-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="6e598-124">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="6e598-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="6e598-125">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="6e598-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="6e598-126">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="6e598-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="6e598-127">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6e598-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="6e598-128">*HBC*, *pszBackupLogFiles* o *pcbSize* non è valido.</span><span class="sxs-lookup"><span data-stu-id="6e598-128">*hbc*, *pszBackupLogFiles*, or *pcbSize* is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="6e598-129">**ERRORE \_ di \_ memoria insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="6e598-129">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="6e598-130">Si è verificato un errore di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="6e598-130">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e598-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e598-131">Remarks</span></span>

<span data-ttu-id="6e598-132">La funzione **DsBackupGetBackupLogs** fornisce un elenco dei file di log necessari per un backup.</span><span class="sxs-lookup"><span data-stu-id="6e598-132">The **DsBackupGetBackupLogs** function provides a list of the log files necessary for a backup.</span></span> <span data-ttu-id="6e598-133">Un backup completo è costituito dai file di database forniti dalla funzione [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) e dai file di log.</span><span class="sxs-lookup"><span data-stu-id="6e598-133">A full backup consists of the database files provided by the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function and the log files.</span></span> <span data-ttu-id="6e598-134">I backup incrementali dei server Active Directory non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="6e598-134">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e598-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e598-135">Requirements</span></span>



| <span data-ttu-id="6e598-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e598-136">Requirement</span></span> | <span data-ttu-id="6e598-137">Valore</span><span class="sxs-lookup"><span data-stu-id="6e598-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e598-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e598-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6e598-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e598-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e598-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e598-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6e598-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e598-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e598-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e598-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e598-143"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e598-143"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e598-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="6e598-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e598-145"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e598-145"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e598-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6e598-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e598-147"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e598-147"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e598-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6e598-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6e598-149">**DsBackupGetBackupLogsW** (Unicode) e **DsBackupGetBackupLogsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6e598-149">**DsBackupGetBackupLogsW** (Unicode) and **DsBackupGetBackupLogsA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="6e598-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e598-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e598-151">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="6e598-151">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="6e598-152">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="6e598-152">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="6e598-153">**Costanti BFT**</span><span class="sxs-lookup"><span data-stu-id="6e598-153">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="6e598-154">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="6e598-154">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="6e598-155">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="6e598-155">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

