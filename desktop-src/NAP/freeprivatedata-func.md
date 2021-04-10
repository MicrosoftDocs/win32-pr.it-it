---
title: Funzione FreePrivateData (NapUtil. h)
description: Libera una struttura di dati PrivateData.
ms.assetid: 94b3618e-224f-4801-94f3-2faa1a298ec0
keywords:
- NAP funzione FreePrivateData
topic_type:
- apiref
api_name:
- FreePrivateData
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4629c264c91a4e0c6e18443cf27a9fd9d182164
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964719"
---
# <a name="freeprivatedata-function"></a><span data-ttu-id="c52b0-104">FreePrivateData (funzione)</span><span class="sxs-lookup"><span data-stu-id="c52b0-104">FreePrivateData function</span></span>

> [!Note]  
> <span data-ttu-id="c52b0-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="c52b0-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c52b0-106">La funzione **FreePrivateData** libera una struttura di dati [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .</span><span class="sxs-lookup"><span data-stu-id="c52b0-106">The **FreePrivateData** function frees a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c52b0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c52b0-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreePrivateData(
  _In_ PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="c52b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c52b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c52b0-109">*PrivateData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c52b0-109">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c52b0-110">Puntatore alla struttura di dati [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) da liberare.</span><span class="sxs-lookup"><span data-stu-id="c52b0-110">A pointer to the [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c52b0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c52b0-111">Remarks</span></span>

<span data-ttu-id="c52b0-112">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="c52b0-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="c52b0-113">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="c52b0-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="c52b0-114">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="c52b0-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="c52b0-115">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="c52b0-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="c52b0-116">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="c52b0-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="c52b0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c52b0-117">Requirements</span></span>



| <span data-ttu-id="c52b0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c52b0-118">Requirement</span></span> | <span data-ttu-id="c52b0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c52b0-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c52b0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c52b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c52b0-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c52b0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c52b0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c52b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c52b0-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c52b0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c52b0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c52b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c52b0-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="c52b0-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="c52b0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c52b0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c52b0-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c52b0-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





