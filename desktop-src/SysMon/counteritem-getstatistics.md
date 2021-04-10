---
title: Metodo CounterItem. GetStatistics
description: Recupera i valori medio, massimo e minimo per il contatore.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Metodo GetStatistics SysMon
- Metodo GetStatistics SysMon, classe CounterItem
- Classe CounterItem SysMon, Metodo GetStatistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964348"
---
# <a name="counteritemgetstatistics-method"></a><span data-ttu-id="edea4-106">Metodo CounterItem. GetStatistics</span><span class="sxs-lookup"><span data-stu-id="edea4-106">CounterItem.GetStatistics method</span></span>

<span data-ttu-id="edea4-107">Recupera i valori medio, massimo e minimo per il contatore.</span><span class="sxs-lookup"><span data-stu-id="edea4-107">Retrieves the average, maximum, and minimum values for the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="edea4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edea4-108">Syntax</span></span>


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="edea4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="edea4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edea4-110">*numero massimo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edea4-110">*max* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edea4-111">Valore massimo del contatore.</span><span class="sxs-lookup"><span data-stu-id="edea4-111">Maximum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="edea4-112">valore *minimo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edea4-112">*min* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edea4-113">Valore minimo del contatore.</span><span class="sxs-lookup"><span data-stu-id="edea4-113">Minimum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="edea4-114">*media* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edea4-114">*average* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edea4-115">Valore medio del contatore.</span><span class="sxs-lookup"><span data-stu-id="edea4-115">Average value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="edea4-116">*stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="edea4-116">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edea4-117">Indica se i valori sono validi.</span><span class="sxs-lookup"><span data-stu-id="edea4-117">Indicates if the values are valid.</span></span>



| <span data-ttu-id="edea4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="edea4-118">Value</span></span>                                                                                              | <span data-ttu-id="edea4-119">Significato</span><span class="sxs-lookup"><span data-stu-id="edea4-119">Meaning</span></span>                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="edea4-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="edea4-120"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="edea4-121">I valori sono validi.</span><span class="sxs-lookup"><span data-stu-id="edea4-121">The values are valid.</span></span><br/>     |
| <dl> <span data-ttu-id="edea4-122"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="edea4-122"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="edea4-123">I valori non sono validi.</span><span class="sxs-lookup"><span data-stu-id="edea4-123">The values are not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edea4-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edea4-124">Return value</span></span>

<span data-ttu-id="edea4-125">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="edea4-125">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edea4-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="edea4-126">Remarks</span></span>

<span data-ttu-id="edea4-127">Per calcolare i valori statistici vengono utilizzati solo i valori dei contatori visibili nella finestra Graph.</span><span class="sxs-lookup"><span data-stu-id="edea4-127">Only those counter values that are visible in the graph window are used to calculate the statistical values.</span></span>

## <a name="requirements"></a><span data-ttu-id="edea4-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edea4-128">Requirements</span></span>



| <span data-ttu-id="edea4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="edea4-129">Requirement</span></span> | <span data-ttu-id="edea4-130">Valore</span><span class="sxs-lookup"><span data-stu-id="edea4-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edea4-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edea4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="edea4-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="edea4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="edea4-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edea4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="edea4-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="edea4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edea4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="edea4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edea4-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="edea4-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edea4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edea4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edea4-138">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="edea4-138">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="edea4-139">**CounterItem.GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="edea4-139">**CounterItem.GetDataAt**</span></span>](counteritem-getdataat.md)
</dt> <dt>

[<span data-ttu-id="edea4-140">**CounterItem. GetValue**</span><span class="sxs-lookup"><span data-stu-id="edea4-140">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





