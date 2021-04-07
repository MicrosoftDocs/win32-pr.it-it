---
title: Funzione CopyRepairInfo (Ndattributils. h)
description: Crea una copia di una struttura RepairInfo.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- CopyRepairInfo funzione NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964001"
---
# <a name="copyrepairinfo-function"></a><span data-ttu-id="ad128-104">CopyRepairInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="ad128-104">CopyRepairInfo function</span></span>

<span data-ttu-id="ad128-105">La funzione **CopyRepairInfo** crea una copia di una struttura [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="ad128-105">The **CopyRepairInfo** function creates a copy of a [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad128-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad128-106">Syntax</span></span>


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="ad128-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad128-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad128-108">*Dest* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ad128-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad128-109">Tipo: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="ad128-109">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="ad128-110">Struttura da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ad128-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="ad128-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad128-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad128-112">Tipo: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="ad128-112">Type: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="ad128-113">Struttura esistente da copiare.</span><span class="sxs-lookup"><span data-stu-id="ad128-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad128-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad128-114">Return value</span></span>

<span data-ttu-id="ad128-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ad128-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ad128-116">I valori restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="ad128-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="ad128-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ad128-117">Return code</span></span>                                                                                   | <span data-ttu-id="ad128-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad128-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad128-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ad128-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ad128-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="ad128-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="ad128-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ad128-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ad128-122">Uno o più parametri non sono stati specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="ad128-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="ad128-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ad128-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ad128-124">Memoria disponibile insufficiente per completare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="ad128-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad128-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad128-125">Requirements</span></span>



| <span data-ttu-id="ad128-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad128-126">Requirement</span></span> | <span data-ttu-id="ad128-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ad128-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad128-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad128-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ad128-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ad128-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ad128-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad128-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ad128-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ad128-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ad128-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad128-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad128-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad128-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad128-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad128-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad128-135">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="ad128-135">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





