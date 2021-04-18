---
title: CounterItem. GetValue, metodo
description: Recupera l'ultimo valore del contatore.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- Metodo GetValue SysMon
- Metodo GetValue SysMon, classe CounterItem
- Classe CounterItem SysMon, metodo GetValue
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302250"
---
# <a name="counteritemgetvalue-method"></a><span data-ttu-id="a92b0-106">CounterItem. GetValue, metodo</span><span class="sxs-lookup"><span data-stu-id="a92b0-106">CounterItem.GetValue method</span></span>

<span data-ttu-id="a92b0-107">Recupera l'ultimo valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="a92b0-107">Retrieves the last value of the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92b0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a92b0-108">Syntax</span></span>


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="a92b0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a92b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92b0-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a92b0-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a92b0-111">Ultimo valore campionato del contatore.</span><span class="sxs-lookup"><span data-stu-id="a92b0-111">Last sampled value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="a92b0-112">*stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a92b0-112">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a92b0-113">Indica se il valore è valido.</span><span class="sxs-lookup"><span data-stu-id="a92b0-113">Indicates if the value is valid.</span></span>



| <span data-ttu-id="a92b0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a92b0-114">Value</span></span>                                                                                              | <span data-ttu-id="a92b0-115">Significato</span><span class="sxs-lookup"><span data-stu-id="a92b0-115">Meaning</span></span>                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="a92b0-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a92b0-116"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a92b0-117">Il valore è valido.</span><span class="sxs-lookup"><span data-stu-id="a92b0-117">The value is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="a92b0-118"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="a92b0-118"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="a92b0-119">Il valore non è valido.</span><span class="sxs-lookup"><span data-stu-id="a92b0-119">The value is not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a92b0-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a92b0-120">Return value</span></span>

<span data-ttu-id="a92b0-121">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a92b0-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a92b0-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a92b0-122">Remarks</span></span>

<span data-ttu-id="a92b0-123">Se l'origine dei dati del contatore è da un file di log, il valore è l'ultimo valore del contatore nel file di log.</span><span class="sxs-lookup"><span data-stu-id="a92b0-123">If the source of the counter data is from a log file, the value is the last counter value in the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a92b0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a92b0-124">Requirements</span></span>



| <span data-ttu-id="a92b0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a92b0-125">Requirement</span></span> | <span data-ttu-id="a92b0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a92b0-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a92b0-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a92b0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a92b0-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a92b0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a92b0-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a92b0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a92b0-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a92b0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a92b0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a92b0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a92b0-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a92b0-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a92b0-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a92b0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92b0-134">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="a92b0-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="a92b0-135">**CounterItem. GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="a92b0-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="a92b0-136">**CounterItem. Value**</span><span class="sxs-lookup"><span data-stu-id="a92b0-136">**CounterItem.Value**</span></span>](counteritem-value.md)
</dt> </dl>

 

 





