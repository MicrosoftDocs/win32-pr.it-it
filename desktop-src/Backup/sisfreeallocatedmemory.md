---
title: Funzione SisFreeAllocatedMemory (sisbkup. h)
description: Libera la memoria allocata dalle funzioni API SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Backup della funzione SisFreeAllocatedMemory
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873533"
---
# <a name="sisfreeallocatedmemory-function"></a><span data-ttu-id="25401-104">SisFreeAllocatedMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="25401-104">SisFreeAllocatedMemory function</span></span>

<span data-ttu-id="25401-105">La funzione **SisFreeAllocatedMemory** libera la memoria allocata dalle funzioni API SIS.</span><span class="sxs-lookup"><span data-stu-id="25401-105">The **SisFreeAllocatedMemory** function frees memory allocated by SIS API functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="25401-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25401-106">Syntax</span></span>


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a><span data-ttu-id="25401-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="25401-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25401-108">*allocatedSpace* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25401-108">*allocatedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25401-109">Puntatore alla memoria allocata dall'API SIS.</span><span class="sxs-lookup"><span data-stu-id="25401-109">Pointer to the memory allocated by the SIS API.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25401-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25401-110">Return value</span></span>

<span data-ttu-id="25401-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="25401-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25401-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="25401-112">Remarks</span></span>

<span data-ttu-id="25401-113">Al termine della chiamata a questa funzione, il chiamante potrebbe non accedere più alla memoria liberata.</span><span class="sxs-lookup"><span data-stu-id="25401-113">After the call to this function completes, the caller may no longer access the freed memory.</span></span>

<span data-ttu-id="25401-114">Questa chiamata deve essere utilizzata per deallocare la memoria allocata per le stringhe di parametri *commonStoreRootPathname* restituite da [**SisCreateBackupStructure**](siscreatebackupstructure.md) e [**SisCreateRestoreStructure**](siscreaterestorestructure.md)e la matrice di stringhe contenente i nomi di file di archivio comuni restituiti da **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** e [**SisRestoredLink**](sisrestoredlink.md).</span><span class="sxs-lookup"><span data-stu-id="25401-114">This call should be used to deallocate the memory allocated for the *commonStoreRootPathname* parameter strings returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md) and [**SisCreateRestoreStructure**](siscreaterestorestructure.md), and the array of strings containing common-store file names returned from **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure**, and [**SisRestoredLink**](sisrestoredlink.md).</span></span> <span data-ttu-id="25401-115">Nel secondo caso, la matrice deve anche essere liberata chiamando **SisFreeAllocatedMemory**.</span><span class="sxs-lookup"><span data-stu-id="25401-115">In the latter case, the array itself also must be freed by calling **SisFreeAllocatedMemory**.</span></span>

## <a name="requirements"></a><span data-ttu-id="25401-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25401-116">Requirements</span></span>



| <span data-ttu-id="25401-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="25401-117">Requirement</span></span> | <span data-ttu-id="25401-118">Valore</span><span class="sxs-lookup"><span data-stu-id="25401-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25401-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25401-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25401-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="25401-120">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="25401-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25401-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25401-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25401-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="25401-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25401-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="25401-124"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="25401-124"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="25401-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="25401-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="25401-126"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25401-126"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="25401-127">DLL</span><span class="sxs-lookup"><span data-stu-id="25401-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25401-128"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25401-128"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25401-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25401-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25401-130">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="25401-130">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="25401-131">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="25401-131">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="25401-132">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="25401-132">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="25401-133">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="25401-133">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

 





