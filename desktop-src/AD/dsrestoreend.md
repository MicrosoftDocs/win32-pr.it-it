---
title: Funzione DsRestoreEnd (ntdsbcli. h)
description: Chiamato per terminare un'operazione di ripristino.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestoreEnd
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048271"
---
# <a name="dsrestoreend-function"></a><span data-ttu-id="1dc84-104">DsRestoreEnd (funzione)</span><span class="sxs-lookup"><span data-stu-id="1dc84-104">DsRestoreEnd function</span></span>

<span data-ttu-id="1dc84-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="1dc84-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1dc84-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="1dc84-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1dc84-107">In alternativa, usare [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="1dc84-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="1dc84-108">Per terminare un'operazione di ripristino viene chiamata la funzione **DsRestoreEnd** .</span><span class="sxs-lookup"><span data-stu-id="1dc84-108">The **DsRestoreEnd** function is called to terminate a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc84-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1dc84-109">Syntax</span></span>


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="1dc84-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1dc84-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dc84-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dc84-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc84-112">Contiene l'handle del contesto di ripristino ottenuto con la funzione [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc84-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dc84-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1dc84-113">Return value</span></span>

<span data-ttu-id="1dc84-114">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1dc84-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="1dc84-115">Nell'elenco seguente sono elencati i possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="1dc84-115">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="1dc84-116">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="1dc84-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="1dc84-117">*HBC* non è valido.</span><span class="sxs-lookup"><span data-stu-id="1dc84-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1dc84-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dc84-118">Remarks</span></span>

<span data-ttu-id="1dc84-119">La funzione **DsRestoreEnd** chiude gli handle di binding in attesa ed esegue un'operazione di pulizia dopo un tentativo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1dc84-119">The **DsRestoreEnd** function closes outstanding binding handles and performs a cleanup operation after a restore attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc84-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dc84-120">Requirements</span></span>



| <span data-ttu-id="1dc84-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc84-121">Requirement</span></span> | <span data-ttu-id="1dc84-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1dc84-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc84-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dc84-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc84-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1dc84-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1dc84-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dc84-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc84-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1dc84-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1dc84-127">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1dc84-127">End of client support</span></span><br/>    | <span data-ttu-id="1dc84-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1dc84-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1dc84-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1dc84-129">End of server support</span></span><br/>    | <span data-ttu-id="1dc84-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1dc84-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1dc84-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dc84-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dc84-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc84-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="1dc84-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="1dc84-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="1dc84-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dc84-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="1dc84-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc84-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc84-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dc84-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc84-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dc84-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc84-138">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="1dc84-138">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="1dc84-139">Ripristino di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="1dc84-139">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="1dc84-140">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="1dc84-140">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

