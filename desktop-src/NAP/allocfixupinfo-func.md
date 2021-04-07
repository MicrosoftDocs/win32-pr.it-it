---
title: Funzione AllocFixupInfo (NapUtil. h)
description: Alloca memoria per una struttura FixupInfo della dimensione specificata.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- NAP funzione AllocFixupInfo
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873413"
---
# <a name="allocfixupinfo-function"></a><span data-ttu-id="a75e4-104">AllocFixupInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="a75e4-104">AllocFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="a75e4-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="a75e4-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a75e4-106">La funzione **AllocFixupInfo** alloca memoria per una struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) della dimensione specificata.</span><span class="sxs-lookup"><span data-stu-id="a75e4-106">The **AllocFixupInfo** function allocates memory for a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure of the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="a75e4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a75e4-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a><span data-ttu-id="a75e4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a75e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75e4-109">*fixupInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a75e4-109">*fixupInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a75e4-110">Puntatore all'indirizzo di una struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) appena allocata.</span><span class="sxs-lookup"><span data-stu-id="a75e4-110">A pointer to the address of a newly allocated [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a75e4-111">*countResultCodes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a75e4-111">*countResultCodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a75e4-112">Numero di codici di risultato da allocare a *fixupInfo*.</span><span class="sxs-lookup"><span data-stu-id="a75e4-112">The number of result codes to allocate to *fixupInfo*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75e4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a75e4-113">Return value</span></span>



| <span data-ttu-id="a75e4-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a75e4-114">Return code</span></span>                                                                                   | <span data-ttu-id="a75e4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a75e4-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a75e4-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a75e4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a75e4-117">L'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a75e4-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="a75e4-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a75e4-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a75e4-119">È stato passato un argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="a75e4-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="a75e4-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a75e4-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a75e4-121">Memoria virtuale insufficiente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a75e4-121">The system is out of virtual memory.</span></span> <span data-ttu-id="a75e4-122">Operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="a75e4-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a75e4-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a75e4-123">Remarks</span></span>

<span data-ttu-id="a75e4-124">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="a75e4-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="a75e4-125">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="a75e4-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="a75e4-126">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="a75e4-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="a75e4-127">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="a75e4-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="a75e4-128">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="a75e4-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75e4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a75e4-129">Requirements</span></span>



| <span data-ttu-id="a75e4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a75e4-130">Requirement</span></span> | <span data-ttu-id="a75e4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a75e4-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a75e4-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a75e4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a75e4-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a75e4-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a75e4-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a75e4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a75e4-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a75e4-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a75e4-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a75e4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a75e4-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="a75e4-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="a75e4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a75e4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a75e4-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a75e4-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a75e4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a75e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a75e4-141">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="a75e4-141">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
</dt> </dl>

 

 





