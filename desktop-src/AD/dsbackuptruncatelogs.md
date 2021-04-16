---
title: Funzione DsBackupTruncateLogs (ntdsbcli. h)
description: Tronca i log di backup letti in precedenza.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupTruncateLogs
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517667"
---
# <a name="dsbackuptruncatelogs-function"></a><span data-ttu-id="3863b-104">DsBackupTruncateLogs (funzione)</span><span class="sxs-lookup"><span data-stu-id="3863b-104">DsBackupTruncateLogs function</span></span>

<span data-ttu-id="3863b-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="3863b-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3863b-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="3863b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3863b-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="3863b-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="3863b-108">La funzione **DsBackupTruncateLogs** tronca i log di backup precedentemente letti.</span><span class="sxs-lookup"><span data-stu-id="3863b-108">The **DsBackupTruncateLogs** function truncates the previously read backup logs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3863b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3863b-109">Syntax</span></span>


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="3863b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3863b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3863b-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3863b-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3863b-112">Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="3863b-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3863b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3863b-113">Return value</span></span>

<span data-ttu-id="3863b-114">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3863b-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="3863b-115">Nell'elenco seguente sono elencati altri possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="3863b-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="3863b-116">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="3863b-116">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="3863b-117">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="3863b-117">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="3863b-118">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="3863b-118">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="3863b-119">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="3863b-119">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="3863b-120">*HBC* non è valido.</span><span class="sxs-lookup"><span data-stu-id="3863b-120">*hbc* is invalid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3863b-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3863b-121">Remarks</span></span>

<span data-ttu-id="3863b-122">Utilizzare la funzione **DsBackupTruncateLogs** quando un backup completo o incrementale è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="3863b-122">Use the **DsBackupTruncateLogs** function when a full or incremental backup has completed successfully.</span></span>

> [!Caution]  
> <span data-ttu-id="3863b-123">Se questa funzione viene chiamata dopo un backup differenziale, tutte le informazioni di backup incrementali andranno perse.</span><span class="sxs-lookup"><span data-stu-id="3863b-123">If this function is called after a differential backup, all of the incremental backup information will be lost.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3863b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3863b-124">Requirements</span></span>



| <span data-ttu-id="3863b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3863b-125">Requirement</span></span> | <span data-ttu-id="3863b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3863b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3863b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3863b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3863b-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3863b-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3863b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3863b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3863b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3863b-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3863b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3863b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3863b-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="3863b-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="3863b-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="3863b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="3863b-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3863b-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="3863b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3863b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3863b-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3863b-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3863b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3863b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3863b-138">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="3863b-138">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="3863b-139">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="3863b-139">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="3863b-140">**DsSetCurrentBackupLog**</span><span class="sxs-lookup"><span data-stu-id="3863b-140">**DsSetCurrentBackupLog**</span></span>](dssetcurrentbackuplog.md)
</dt> <dt>

[<span data-ttu-id="3863b-141">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="3863b-141">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="3863b-142">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="3863b-142">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

