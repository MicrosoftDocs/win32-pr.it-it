---
title: Funzione DsRestoreRegisterComplete (ntdsbcli. h)
description: Chiamata eseguita per sbloccare un server Active Directory al termine di un'operazione di ripristino.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestoreRegisterComplete
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048482"
---
# <a name="dsrestoreregistercomplete-function"></a><span data-ttu-id="150a6-104">DsRestoreRegisterComplete (funzione)</span><span class="sxs-lookup"><span data-stu-id="150a6-104">DsRestoreRegisterComplete function</span></span>

<span data-ttu-id="150a6-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="150a6-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="150a6-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="150a6-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="150a6-107">In alternativa, usare [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="150a6-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="150a6-108">La funzione **DsRestoreRegisterComplete** viene chiamata per sbloccare un server Active Directory al termine di un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="150a6-108">The **DsRestoreRegisterComplete** function is called to unlock an Active Directory server after a restore operation is complete.</span></span> <span data-ttu-id="150a6-109">Questa funzione è controparte della funzione [**DsRestoreRegister**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="150a6-109">This function is counterpart to the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="150a6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="150a6-110">Syntax</span></span>


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a><span data-ttu-id="150a6-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="150a6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="150a6-112">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="150a6-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="150a6-113">Contiene l'handle del contesto di ripristino ottenuto con la funzione [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="150a6-113">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="150a6-114">*hrRestoreState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="150a6-114">*hrRestoreState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="150a6-115">Contiene lo stato finale dell'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="150a6-115">Contains the final status of the restore operation.</span></span> <span data-ttu-id="150a6-116">Questo parametro deve contenere **S \_ OK** se l'operazione di ripristino è stata eseguita correttamente o un codice di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="150a6-116">This parameter should contain **S\_OK** if the restore operation was successful or an error code otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="150a6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="150a6-117">Return value</span></span>

<span data-ttu-id="150a6-118">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="150a6-118">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="150a6-119">Nell'elenco seguente sono elencati i possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="150a6-119">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="150a6-120">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="150a6-120">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="150a6-121">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="150a6-121">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="150a6-122">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="150a6-122">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="150a6-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="150a6-123">Remarks</span></span>

<span data-ttu-id="150a6-124">Prima di riavviare il controller di dominio, chiamare questa funzione per fornire lo stato dell'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="150a6-124">Before you restart the domain controller, call this function to provide the status of the restore operation.</span></span> <span data-ttu-id="150a6-125">Se lo stato ha esito negativo, il servizio directory non viene avviato fino a quando non viene ripristinato un database valido.</span><span class="sxs-lookup"><span data-stu-id="150a6-125">If the status is not successful, the directory service will not start until a valid database has been restored.</span></span> <span data-ttu-id="150a6-126">Questa funzione completa l'operazione di ripristino e consente l'avvio Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="150a6-126">This function completes the restore operation and allows Active Directory Domain Services to start.</span></span>

## <a name="requirements"></a><span data-ttu-id="150a6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="150a6-127">Requirements</span></span>



| <span data-ttu-id="150a6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="150a6-128">Requirement</span></span> | <span data-ttu-id="150a6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="150a6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="150a6-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="150a6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="150a6-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="150a6-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="150a6-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="150a6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="150a6-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="150a6-133">None supported</span></span><br/>                                                               |
| <span data-ttu-id="150a6-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="150a6-134">End of client support</span></span><br/>    | <span data-ttu-id="150a6-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="150a6-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="150a6-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="150a6-136">End of server support</span></span><br/>    | <span data-ttu-id="150a6-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="150a6-137">None supported</span></span><br/>                                                               |
| <span data-ttu-id="150a6-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="150a6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="150a6-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="150a6-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="150a6-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="150a6-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="150a6-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="150a6-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="150a6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="150a6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="150a6-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="150a6-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="150a6-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="150a6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="150a6-145">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="150a6-145">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="150a6-146">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="150a6-146">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="150a6-147">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="150a6-147">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="150a6-148">Ripristino di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="150a6-148">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="150a6-149">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="150a6-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

