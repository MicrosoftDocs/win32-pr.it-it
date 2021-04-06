---
title: Funzione DsBackupEnd (ntdsbcli. h)
description: Chiamato per terminare un'operazione di backup.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupEnd
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873678"
---
# <a name="dsbackupend-function"></a><span data-ttu-id="52de4-104">DsBackupEnd (funzione)</span><span class="sxs-lookup"><span data-stu-id="52de4-104">DsBackupEnd function</span></span>

<span data-ttu-id="52de4-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="52de4-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="52de4-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="52de4-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="52de4-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="52de4-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="52de4-108">Per terminare un'operazione di backup viene chiamata la funzione **DsBackupEnd** .</span><span class="sxs-lookup"><span data-stu-id="52de4-108">The **DsBackupEnd** function is called to terminate a backup operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="52de4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52de4-109">Syntax</span></span>


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="52de4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="52de4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52de4-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52de4-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52de4-112">Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="52de4-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52de4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52de4-113">Return value</span></span>

<span data-ttu-id="52de4-114">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="52de4-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="52de4-115">Nell'elenco seguente sono elencati altri possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="52de4-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="52de4-116">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="52de4-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="52de4-117">*HBC* non è valido.</span><span class="sxs-lookup"><span data-stu-id="52de4-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52de4-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="52de4-118">Remarks</span></span>

<span data-ttu-id="52de4-119">La funzione **DsBackupEnd** chiude gli handle di binding in attesa ed esegue una pulizia dopo un tentativo di backup con esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="52de4-119">The **DsBackupEnd** function closes outstanding binding handles and performs a cleanup after a successful or unsuccessful backup attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="52de4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52de4-120">Requirements</span></span>



| <span data-ttu-id="52de4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="52de4-121">Requirement</span></span> | <span data-ttu-id="52de4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="52de4-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52de4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52de4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="52de4-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52de4-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52de4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52de4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="52de4-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52de4-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52de4-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52de4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="52de4-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="52de4-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="52de4-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="52de4-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="52de4-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52de4-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="52de4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="52de4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52de4-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52de4-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52de4-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52de4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52de4-134">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="52de4-134">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="52de4-135">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="52de4-135">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="52de4-136">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="52de4-136">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

