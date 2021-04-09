---
title: Funzione FreeNapComponentRegistrationInfoArray (NapUtil. h)
description: Libera un numero specificato di strutture di dati NapComponentRegistrationInfo da una matrice.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- NAP funzione FreeNapComponentRegistrationInfoArray
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df823ad8086c57a6ee193bd0d58678786cfe325b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120930"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a><span data-ttu-id="82797-104">FreeNapComponentRegistrationInfoArray (funzione)</span><span class="sxs-lookup"><span data-stu-id="82797-104">FreeNapComponentRegistrationInfoArray function</span></span>

> [!Note]  
> <span data-ttu-id="82797-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="82797-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="82797-106">La funzione **FreeNapComponentRegistrationInfoArray** libera un numero specificato di strutture di dati [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) da una matrice.</span><span class="sxs-lookup"><span data-stu-id="82797-106">The **FreeNapComponentRegistrationInfoArray** function frees a specified number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures from an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="82797-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82797-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="82797-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="82797-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82797-109">*numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="82797-109">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82797-110">Numero di strutture [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) in *info* da liberare.</span><span class="sxs-lookup"><span data-stu-id="82797-110">The number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures in *info* to free.</span></span>

</dd> <dt>

<span data-ttu-id="82797-111">*informazioni* \[ su in\]</span><span class="sxs-lookup"><span data-stu-id="82797-111">*info* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82797-112">Puntatore a una matrice di strutture di dati [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) da liberare.</span><span class="sxs-lookup"><span data-stu-id="82797-112">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82797-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="82797-113">Remarks</span></span>

<span data-ttu-id="82797-114">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="82797-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="82797-115">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="82797-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="82797-116">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="82797-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="82797-117">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="82797-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="82797-118">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="82797-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="82797-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82797-119">Requirements</span></span>



| <span data-ttu-id="82797-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="82797-120">Requirement</span></span> | <span data-ttu-id="82797-121">Valore</span><span class="sxs-lookup"><span data-stu-id="82797-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82797-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82797-122">Minimum supported client</span></span><br/> | <span data-ttu-id="82797-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82797-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="82797-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82797-124">Minimum supported server</span></span><br/> | <span data-ttu-id="82797-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82797-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="82797-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82797-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="82797-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="82797-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="82797-128">DLL</span><span class="sxs-lookup"><span data-stu-id="82797-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82797-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82797-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





