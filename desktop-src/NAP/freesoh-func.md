---
title: Funzione FreeSoH (NapUtil. h)
description: Libera una struttura di dati di rapporto di integrità.
ms.assetid: 587acf64-31be-46c8-9d49-b5014c1a90ba
keywords:
- NAP funzione FreeSoH
topic_type:
- apiref
api_name:
- FreeSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28409c18bf9f673c78d6df2a224cb936223edddb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121382"
---
# <a name="freesoh-function"></a><span data-ttu-id="eba44-104">FreeSoH (funzione)</span><span class="sxs-lookup"><span data-stu-id="eba44-104">FreeSoH function</span></span>

> [!Note]  
> <span data-ttu-id="eba44-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="eba44-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="eba44-106">La funzione **FreeSoH** libera una struttura di dati **SOH** .</span><span class="sxs-lookup"><span data-stu-id="eba44-106">The **FreeSoH** function frees a **SoH** data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba44-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eba44-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoH(
  _In_ SoH *soh
);
```



## <a name="parameters"></a><span data-ttu-id="eba44-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eba44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eba44-109">rapporto di *integrità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba44-109">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba44-110">Puntatore alla struttura dei dati di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) da liberare.</span><span class="sxs-lookup"><span data-stu-id="eba44-110">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eba44-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="eba44-111">Remarks</span></span>

<span data-ttu-id="eba44-112">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="eba44-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="eba44-113">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="eba44-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="eba44-114">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="eba44-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="eba44-115">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="eba44-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="eba44-116">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="eba44-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="eba44-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eba44-117">Requirements</span></span>



| <span data-ttu-id="eba44-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eba44-118">Requirement</span></span> | <span data-ttu-id="eba44-119">Valore</span><span class="sxs-lookup"><span data-stu-id="eba44-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eba44-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eba44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eba44-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eba44-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="eba44-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eba44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eba44-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eba44-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eba44-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eba44-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eba44-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="eba44-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="eba44-126">DLL</span><span class="sxs-lookup"><span data-stu-id="eba44-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eba44-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eba44-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





