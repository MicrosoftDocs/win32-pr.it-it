---
title: Counters. Remove (metodo)
description: Rimuove un'istanza di CounterItem dalla raccolta.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Rimuovere il metodo SysMon
- Metodo Remove SysMon, classe Counters
- Classe Counters SysMon, Remove (metodo)
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964089"
---
# <a name="countersremove-method"></a><span data-ttu-id="18eef-106">Counters. Remove (metodo)</span><span class="sxs-lookup"><span data-stu-id="18eef-106">Counters.Remove method</span></span>

<span data-ttu-id="18eef-107">Rimuove un'istanza di [**CounterItem**](counteritem.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="18eef-107">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="18eef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18eef-108">Syntax</span></span>


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="18eef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="18eef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18eef-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="18eef-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18eef-111">Indice dell'oggetto [**CounterItem**](counteritem.md) da rimuovere dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="18eef-111">Index of the [**CounterItem**](counteritem.md) object to remove from the collection.</span></span> <span data-ttu-id="18eef-112">L'indice è in base uno.</span><span class="sxs-lookup"><span data-stu-id="18eef-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18eef-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18eef-113">Return value</span></span>

<span data-ttu-id="18eef-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="18eef-114">This method does not return a value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="18eef-115">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="18eef-115">Exceptions</span></span>



| <span data-ttu-id="18eef-116">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="18eef-116">Exception type</span></span>                                  | <span data-ttu-id="18eef-117">Condizione</span><span class="sxs-lookup"><span data-stu-id="18eef-117">Condition</span></span>                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="18eef-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="18eef-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="18eef-119">L'indice specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="18eef-119">The specified index is not valid.</span></span> <span data-ttu-id="18eef-120">Il valore ERR. Number è???.</span><span class="sxs-lookup"><span data-stu-id="18eef-120">The Err.Number value is ???.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="18eef-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="18eef-121">Remarks</span></span>

<span data-ttu-id="18eef-122">Per rimuovere tutti i contatori dalla raccolta, è possibile chiamare [**SystemMonitor. Reset**](systemmonitor-reset.md).</span><span class="sxs-lookup"><span data-stu-id="18eef-122">To remove all counters from the collection, you can call [**SystemMonitor.Reset**](systemmonitor-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18eef-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18eef-123">Requirements</span></span>



| <span data-ttu-id="18eef-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="18eef-124">Requirement</span></span> | <span data-ttu-id="18eef-125">Valore</span><span class="sxs-lookup"><span data-stu-id="18eef-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18eef-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18eef-126">Minimum supported client</span></span><br/> | <span data-ttu-id="18eef-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18eef-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="18eef-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18eef-128">Minimum supported server</span></span><br/> | <span data-ttu-id="18eef-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18eef-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18eef-130">DLL</span><span class="sxs-lookup"><span data-stu-id="18eef-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18eef-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="18eef-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18eef-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18eef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18eef-133">**Contatori**</span><span class="sxs-lookup"><span data-stu-id="18eef-133">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="18eef-134">**SystemMonitor. Reset**</span><span class="sxs-lookup"><span data-stu-id="18eef-134">**SystemMonitor.Reset**</span></span>](systemmonitor-reset.md)
</dt> </dl>

 

 





