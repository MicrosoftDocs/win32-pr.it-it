---
title: Funzione SisFreeRestoreStructure (sisbkup. h)
description: Libera la memoria allocata per la struttura di ripristino SIS specificata ed esegue attività che preparano il filtro SIS per impostare correttamente i collegamenti creati durante l'operazione di ripristino.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Backup della funzione SisFreeRestoreStructure
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478730"
---
# <a name="sisfreerestorestructure-function"></a><span data-ttu-id="03fca-104">SisFreeRestoreStructure (funzione)</span><span class="sxs-lookup"><span data-stu-id="03fca-104">SisFreeRestoreStructure function</span></span>

<span data-ttu-id="03fca-105">La funzione **SisFreeRestoreStructure** libera la memoria allocata per la struttura di ripristino SIS specificata ed esegue attività che preparano il filtro SIS per impostare correttamente i collegamenti creati durante l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="03fca-105">The **SisFreeRestoreStructure** function frees the memory allocated for the specified SIS restore structure, and performs tasks that prepare the SIS filter to properly set up the links created during the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="03fca-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03fca-106">Syntax</span></span>


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a><span data-ttu-id="03fca-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="03fca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03fca-108">*sisRestoreStructure* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03fca-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03fca-109">Puntatore a una struttura di ripristino SIS restituita da [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="03fca-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03fca-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03fca-110">Return value</span></span>

<span data-ttu-id="03fca-111">Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="03fca-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="03fca-112">Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="03fca-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="03fca-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="03fca-113">Remarks</span></span>

<span data-ttu-id="03fca-114">L'accesso ai collegamenti SIS prima del completamento della chiamata a questa funzione può comportare un controllo del volume o una lettura parziale del contenuto del collegamento.</span><span class="sxs-lookup"><span data-stu-id="03fca-114">Accessing the SIS links before the call to this function completes can result in a volume check or a partial read of the link's contents.</span></span>

<span data-ttu-id="03fca-115">Si noti che non è sicuro presupporre che questa operazione dealloca solo la memoria.</span><span class="sxs-lookup"><span data-stu-id="03fca-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="03fca-116">Questa funzione, ad esempio, può eseguire anche operazioni amministrative aggiuntive per l'architettura SIS.</span><span class="sxs-lookup"><span data-stu-id="03fca-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="03fca-117">Chiamare pertanto questa funzione anche se l'operazione di ripristino verrà chiusa immediatamente dopo.</span><span class="sxs-lookup"><span data-stu-id="03fca-117">Therefore, call this function even if your restore operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="03fca-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03fca-118">Requirements</span></span>



| <span data-ttu-id="03fca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="03fca-119">Requirement</span></span> | <span data-ttu-id="03fca-120">Valore</span><span class="sxs-lookup"><span data-stu-id="03fca-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03fca-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03fca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="03fca-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="03fca-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="03fca-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03fca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="03fca-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03fca-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="03fca-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03fca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="03fca-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="03fca-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="03fca-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="03fca-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="03fca-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03fca-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="03fca-129">DLL</span><span class="sxs-lookup"><span data-stu-id="03fca-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03fca-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03fca-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03fca-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03fca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03fca-132">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="03fca-132">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> </dl>

 

