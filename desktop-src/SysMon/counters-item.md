---
title: Proprietà Counters. Item
description: Recupera l'istanza di CounterItem specificata dalla raccolta.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Proprietà Item SysMon
- Proprietà Item SysMon, classe Counters
- Classe contatori SysMon, proprietà Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475826"
---
# <a name="countersitem-property"></a><span data-ttu-id="4341f-106">Proprietà Counters. Item</span><span class="sxs-lookup"><span data-stu-id="4341f-106">Counters.Item property</span></span>

<span data-ttu-id="4341f-107">Recupera l'istanza di [**CounterItem**](counteritem.md) specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4341f-107">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span>

<span data-ttu-id="4341f-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4341f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4341f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4341f-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a><span data-ttu-id="4341f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4341f-110">Property value</span></span>

<span data-ttu-id="4341f-111">Istanza di [**CounterItem**](counteritem.md) che corrisponde al valore di indice specificato.</span><span class="sxs-lookup"><span data-stu-id="4341f-111">[**CounterItem**](counteritem.md) instance that corresponds to the specified index value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="4341f-112">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="4341f-112">Exceptions</span></span>



| <span data-ttu-id="4341f-113">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="4341f-113">Exception type</span></span>                                  | <span data-ttu-id="4341f-114">Condizione</span><span class="sxs-lookup"><span data-stu-id="4341f-114">Condition</span></span>                         |
|-------------------------------------------------|-----------------------------------|
| <span data-ttu-id="4341f-115">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="4341f-115">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="4341f-116">L'indice specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="4341f-116">The specified index is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4341f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4341f-117">Remarks</span></span>

<span data-ttu-id="4341f-118">Si tratta della proprietà predefinita dell'oggetto [**contatori**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="4341f-118">This is the default property of the [**Counters**](counters.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4341f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4341f-119">Requirements</span></span>



| <span data-ttu-id="4341f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4341f-120">Requirement</span></span> | <span data-ttu-id="4341f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4341f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4341f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4341f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4341f-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4341f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4341f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4341f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4341f-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4341f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4341f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4341f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4341f-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4341f-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4341f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4341f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4341f-129">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="4341f-129">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="4341f-130">**Contatori**</span><span class="sxs-lookup"><span data-stu-id="4341f-130">**Counters**</span></span>](counters.md)
</dt> </dl>

 

 





