---
title: Funzione SisFreeBackupStructure (sisbkup. h)
description: Libera la struttura di backup SIS specificata.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Backup della funzione SisFreeBackupStructure
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740695"
---
# <a name="sisfreebackupstructure-function"></a><span data-ttu-id="13c48-104">SisFreeBackupStructure (funzione)</span><span class="sxs-lookup"><span data-stu-id="13c48-104">SisFreeBackupStructure function</span></span>

<span data-ttu-id="13c48-105">La funzione **SisFreeBackupStructure** libera la struttura di backup SIS specificata.</span><span class="sxs-lookup"><span data-stu-id="13c48-105">The **SisFreeBackupStructure** function frees the specified SIS backup structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c48-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13c48-106">Syntax</span></span>


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a><span data-ttu-id="13c48-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="13c48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c48-108">*sisBackupStructure* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13c48-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c48-109">Puntatore alla struttura di backup SIS restituita da [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="13c48-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13c48-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13c48-110">Return value</span></span>

<span data-ttu-id="13c48-111">Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="13c48-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="13c48-112">Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="13c48-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c48-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="13c48-113">Remarks</span></span>

<span data-ttu-id="13c48-114">Questa funzione deve essere chiamata dopo il completamento dell'operazione di backup per il volume identificato dal valore del parametro *sisBackupStructure* .</span><span class="sxs-lookup"><span data-stu-id="13c48-114">This function should be called after the backup operation is completed for the volume identified by the value of the *sisBackupStructure* parameter.</span></span>

<span data-ttu-id="13c48-115">Si noti che non è sicuro presupporre che questa operazione dealloca solo la memoria.</span><span class="sxs-lookup"><span data-stu-id="13c48-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="13c48-116">Questa funzione, ad esempio, può eseguire anche operazioni amministrative aggiuntive per l'architettura SIS.</span><span class="sxs-lookup"><span data-stu-id="13c48-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="13c48-117">Chiamare pertanto questa funzione anche se l'operazione di backup verrà chiusa immediatamente dopo.</span><span class="sxs-lookup"><span data-stu-id="13c48-117">Therefore, call this function even if your backup operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c48-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13c48-118">Requirements</span></span>



| <span data-ttu-id="13c48-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="13c48-119">Requirement</span></span> | <span data-ttu-id="13c48-120">Valore</span><span class="sxs-lookup"><span data-stu-id="13c48-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13c48-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13c48-121">Minimum supported client</span></span><br/> | <span data-ttu-id="13c48-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="13c48-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="13c48-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13c48-123">Minimum supported server</span></span><br/> | <span data-ttu-id="13c48-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13c48-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13c48-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13c48-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="13c48-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="13c48-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="13c48-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="13c48-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="13c48-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13c48-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="13c48-129">DLL</span><span class="sxs-lookup"><span data-stu-id="13c48-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13c48-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13c48-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c48-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13c48-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c48-132">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="13c48-132">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

