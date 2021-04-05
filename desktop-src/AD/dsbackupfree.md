---
title: Funzione DsBackupFree (ntdsbcli. h)
description: Rilascia la memoria allocata dal Active Directory Domain Services funzioni di backup e ripristino.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupFree
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873677"
---
# <a name="dsbackupfree-function"></a><span data-ttu-id="709ca-104">DsBackupFree (funzione)</span><span class="sxs-lookup"><span data-stu-id="709ca-104">DsBackupFree function</span></span>

<span data-ttu-id="709ca-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="709ca-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="709ca-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="709ca-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="709ca-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="709ca-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="709ca-108">La funzione **DsBackupFree** rilascia la memoria allocata dal Active Directory Domain Services funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="709ca-108">The **DsBackupFree** function releases memory allocated by the Active Directory Domain Services backup and restore functions.</span></span> <span data-ttu-id="709ca-109">Le funzioni seguenti allocano memoria che deve essere rilasciata con la funzione **DsBackupFree** .</span><span class="sxs-lookup"><span data-stu-id="709ca-109">The following functions allocate memory that must be released with the **DsBackupFree** function.</span></span>

-   [<span data-ttu-id="709ca-110">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="709ca-110">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
-   [<span data-ttu-id="709ca-111">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="709ca-111">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
-   [<span data-ttu-id="709ca-112">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="709ca-112">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
-   [<span data-ttu-id="709ca-113">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="709ca-113">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a><span data-ttu-id="709ca-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="709ca-114">Syntax</span></span>


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="709ca-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="709ca-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="709ca-116">*pvBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="709ca-116">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="709ca-117">Puntatore al buffer di memoria da liberare.</span><span class="sxs-lookup"><span data-stu-id="709ca-117">Pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="709ca-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="709ca-118">Return value</span></span>

<span data-ttu-id="709ca-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="709ca-119">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="709ca-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="709ca-120">Requirements</span></span>



| <span data-ttu-id="709ca-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="709ca-121">Requirement</span></span> | <span data-ttu-id="709ca-122">Valore</span><span class="sxs-lookup"><span data-stu-id="709ca-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="709ca-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="709ca-123">Minimum supported client</span></span><br/> | <span data-ttu-id="709ca-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="709ca-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="709ca-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="709ca-125">Minimum supported server</span></span><br/> | <span data-ttu-id="709ca-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="709ca-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="709ca-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="709ca-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="709ca-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="709ca-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="709ca-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="709ca-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="709ca-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="709ca-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="709ca-131">DLL</span><span class="sxs-lookup"><span data-stu-id="709ca-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="709ca-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="709ca-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="709ca-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="709ca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709ca-134">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="709ca-134">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="709ca-135">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="709ca-135">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="709ca-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="709ca-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="709ca-137">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="709ca-137">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="709ca-138">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="709ca-138">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="709ca-139">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="709ca-139">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

