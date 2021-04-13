---
title: Funzione FreeConnections (NapUtil. h)
description: Libera una struttura dei dati delle connessioni.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- NAP funzione FreeConnections
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f840d02572af3e6382a06a1873573fc7a30420e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340393"
---
# <a name="freeconnections-function"></a><span data-ttu-id="2a594-104">FreeConnections (funzione)</span><span class="sxs-lookup"><span data-stu-id="2a594-104">FreeConnections function</span></span>

> [!Note]  
> <span data-ttu-id="2a594-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="2a594-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2a594-106">La funzione **FreeConnections** libera una struttura di dati [**Connections**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="2a594-106">The **FreeConnections** function frees a [**Connections**](connections-struct.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a594-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a594-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a><span data-ttu-id="2a594-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a594-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a594-109">*connessioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2a594-109">*connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a594-110">Puntatore alla struttura [**Connections**](connections-struct.md) da liberare.</span><span class="sxs-lookup"><span data-stu-id="2a594-110">A pointer to the [**Connections**](connections-struct.md) structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a594-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a594-111">Remarks</span></span>

<span data-ttu-id="2a594-112">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="2a594-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="2a594-113">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="2a594-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="2a594-114">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="2a594-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="2a594-115">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="2a594-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="2a594-116">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="2a594-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a594-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a594-117">Requirements</span></span>



| <span data-ttu-id="2a594-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a594-118">Requirement</span></span> | <span data-ttu-id="2a594-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2a594-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2a594-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a594-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a594-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a594-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2a594-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a594-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a594-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a594-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2a594-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a594-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a594-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a594-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="2a594-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2a594-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a594-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a594-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a594-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a594-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a594-129">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="2a594-129">**AllocConnections**</span></span>](allocconnections-func.md)
</dt> </dl>

 

 





