---
title: Funzione FreeFixupInfo (NapUtil. h)
description: Libera una struttura di dati FixupInfo.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- NAP funzione FreeFixupInfo
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abf1fe07557ac786a9f0cb8e8e06a30408f6d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302262"
---
# <a name="freefixupinfo-function"></a><span data-ttu-id="33857-104">FreeFixupInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="33857-104">FreeFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="33857-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="33857-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="33857-106">La funzione **FreeFixupInfo** libera una struttura di dati [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) .</span><span class="sxs-lookup"><span data-stu-id="33857-106">The **FreeFixupInfo** function frees a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="33857-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33857-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="33857-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="33857-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33857-109">*fixupInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33857-109">*fixupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33857-110">Puntatore alla struttura di dati [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) da liberare.</span><span class="sxs-lookup"><span data-stu-id="33857-110">A pointer to the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33857-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="33857-111">Remarks</span></span>

<span data-ttu-id="33857-112">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="33857-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="33857-113">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="33857-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="33857-114">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="33857-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="33857-115">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="33857-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="33857-116">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="33857-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="33857-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33857-117">Requirements</span></span>



| <span data-ttu-id="33857-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="33857-118">Requirement</span></span> | <span data-ttu-id="33857-119">Valore</span><span class="sxs-lookup"><span data-stu-id="33857-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="33857-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33857-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33857-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33857-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="33857-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33857-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33857-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33857-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="33857-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33857-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33857-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="33857-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="33857-126">DLL</span><span class="sxs-lookup"><span data-stu-id="33857-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33857-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33857-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33857-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33857-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33857-129">**AllocFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="33857-129">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
</dt> </dl>

 

 





