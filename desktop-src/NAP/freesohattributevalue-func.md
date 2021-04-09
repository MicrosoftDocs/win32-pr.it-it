---
title: Funzione FreeSoHAttributeValue (NapUtil. h)
description: Libera una struttura di dati SoHAttributeValue.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- NAP funzione FreeSoHAttributeValue
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048692"
---
# <a name="freesohattributevalue-function"></a><span data-ttu-id="7470b-104">FreeSoHAttributeValue (funzione)</span><span class="sxs-lookup"><span data-stu-id="7470b-104">FreeSoHAttributeValue function</span></span>

> [!Note]  
> <span data-ttu-id="7470b-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="7470b-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7470b-106">La funzione **FreeSoHAttributeValue** libera una struttura di dati [**SoHAttributeValue**](sohattributevalue-union.md) .</span><span class="sxs-lookup"><span data-stu-id="7470b-106">The **FreeSoHAttributeValue** function frees an [**SoHAttributeValue**](sohattributevalue-union.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7470b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7470b-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="7470b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7470b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7470b-109">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7470b-109">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7470b-110">Valore [**SoHAttributeType**](sohattributetype-enum.md) che specifica il tipo di valore dell'attributo SOH da liberare.</span><span class="sxs-lookup"><span data-stu-id="7470b-110">A [**SoHAttributeType**](sohattributetype-enum.md) value that specifies the type of SoH attribute value to free.</span></span>

</dd> <dt>

<span data-ttu-id="7470b-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7470b-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7470b-112">Puntatore a [**SoHAttributeValue**](sohattributevalue-union.md) da liberare.</span><span class="sxs-lookup"><span data-stu-id="7470b-112">A pointer to the [**SoHAttributeValue**](sohattributevalue-union.md) to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7470b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7470b-113">Remarks</span></span>

<span data-ttu-id="7470b-114">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="7470b-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="7470b-115">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="7470b-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="7470b-116">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="7470b-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="7470b-117">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="7470b-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="7470b-118">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="7470b-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="7470b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7470b-119">Requirements</span></span>



| <span data-ttu-id="7470b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7470b-120">Requirement</span></span> | <span data-ttu-id="7470b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7470b-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7470b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7470b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7470b-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7470b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7470b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7470b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7470b-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7470b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7470b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7470b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7470b-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="7470b-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="7470b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7470b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7470b-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7470b-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





