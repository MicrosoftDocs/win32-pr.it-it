---
title: Funzione FreeIsolationInfoEx (NapUtil. h)
description: Libera una struttura di dati IsolationInfoEx.
ms.assetid: 9ca0e5ae-aed9-43e9-b8f7-90f13d62ac16
keywords:
- NAP funzione FreeIsolationInfoEx
topic_type:
- apiref
api_name:
- FreeIsolationInfoEx
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cf3f13f38130fe86383fee5bebe3a536ea9aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120931"
---
# <a name="freeisolationinfoex-function"></a><span data-ttu-id="408c4-104">FreeIsolationInfoEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="408c4-104">FreeIsolationInfoEx function</span></span>

> [!Note]  
> <span data-ttu-id="408c4-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="408c4-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="408c4-106">La funzione **FreeIsolationInfoEx** libera una struttura di dati [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .</span><span class="sxs-lookup"><span data-stu-id="408c4-106">The **FreeIsolationInfoEx** function frees an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="408c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="408c4-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeIsolationInfoEx(
  _In_ IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="408c4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="408c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408c4-109">*isolationInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="408c4-109">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408c4-110">Puntatore alla struttura di dati [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) da liberare.</span><span class="sxs-lookup"><span data-stu-id="408c4-110">A pointer to the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="408c4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="408c4-111">Remarks</span></span>

<span data-ttu-id="408c4-112">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="408c4-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="408c4-113">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="408c4-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="408c4-114">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="408c4-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="408c4-115">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="408c4-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="408c4-116">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="408c4-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="408c4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="408c4-117">Requirements</span></span>



| <span data-ttu-id="408c4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="408c4-118">Requirement</span></span> | <span data-ttu-id="408c4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="408c4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="408c4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="408c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="408c4-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="408c4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="408c4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="408c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="408c4-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="408c4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="408c4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="408c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="408c4-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="408c4-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="408c4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="408c4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="408c4-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="408c4-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





