---
title: Funzione AllocCountedString (NapUtil. h)
description: Alloca memoria per una stringa con terminazione null e la restituisce in una struttura CountedString.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- NAP funzione AllocCountedString
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301072"
---
# <a name="alloccountedstring-function"></a><span data-ttu-id="30998-104">AllocCountedString (funzione)</span><span class="sxs-lookup"><span data-stu-id="30998-104">AllocCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="30998-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="30998-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="30998-106">La funzione **AllocCountedString** alloca memoria per una stringa con terminazione null e la restituisce in una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="30998-106">The **AllocCountedString** function allocates memory for a null-terminated string and returns it in a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="30998-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30998-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a><span data-ttu-id="30998-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="30998-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30998-109">*countedString* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="30998-109">*countedString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30998-110">Puntatore all'indirizzo di una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) appena allocata.</span><span class="sxs-lookup"><span data-stu-id="30998-110">A pointer to the address of a newly allocated [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30998-111">*stringa* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="30998-111">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30998-112">Puntatore alla stringa con terminazione null da restituire in *countedString*.</span><span class="sxs-lookup"><span data-stu-id="30998-112">A pointer to the null-terminated string that is to be returned in *countedString*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30998-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30998-113">Return value</span></span>



| <span data-ttu-id="30998-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="30998-114">Return code</span></span>                                                                                   | <span data-ttu-id="30998-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30998-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30998-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30998-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="30998-117">L'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="30998-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="30998-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="30998-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="30998-119">È stato passato un argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="30998-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="30998-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="30998-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="30998-121">Memoria virtuale insufficiente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="30998-121">The system is out of virtual memory.</span></span> <span data-ttu-id="30998-122">Operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="30998-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30998-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="30998-123">Remarks</span></span>

<span data-ttu-id="30998-124">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="30998-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="30998-125">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="30998-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="30998-126">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="30998-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="30998-127">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="30998-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="30998-128">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="30998-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="30998-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30998-129">Requirements</span></span>



| <span data-ttu-id="30998-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="30998-130">Requirement</span></span> | <span data-ttu-id="30998-131">Valore</span><span class="sxs-lookup"><span data-stu-id="30998-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30998-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30998-132">Minimum supported client</span></span><br/> | <span data-ttu-id="30998-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30998-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30998-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30998-134">Minimum supported server</span></span><br/> | <span data-ttu-id="30998-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30998-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30998-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30998-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="30998-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="30998-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="30998-138">DLL</span><span class="sxs-lookup"><span data-stu-id="30998-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30998-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30998-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30998-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30998-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30998-141">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="30998-141">**FreeCountedString**</span></span>](freecountedstring-func.md)
</dt> </dl>

 

 





