---
title: Funzione CopyHelperAttribute (Ndattributils. h)
description: Crea una copia di una struttura dell' \_ attributo helper.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- CopyHelperAttribute funzione NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301362"
---
# <a name="copyhelperattribute-function"></a><span data-ttu-id="64a5d-104">CopyHelperAttribute (funzione)</span><span class="sxs-lookup"><span data-stu-id="64a5d-104">CopyHelperAttribute function</span></span>

<span data-ttu-id="64a5d-105">La funzione **CopyHelperAttribute** crea una copia di una struttura dell' [**\_ attributo Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="64a5d-105">The **CopyHelperAttribute** function creates a copy of a [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a5d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64a5d-106">Syntax</span></span>


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a><span data-ttu-id="64a5d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="64a5d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64a5d-108">*Dest* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="64a5d-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64a5d-109">Tipo: \**\* [**\_ attributo Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _</span><span class="sxs-lookup"><span data-stu-id="64a5d-109">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="64a5d-110">Struttura da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="64a5d-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="64a5d-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64a5d-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64a5d-112">Tipo: \**\* [**\_ attributo Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)const* _</span><span class="sxs-lookup"><span data-stu-id="64a5d-112">Type: \**const [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="64a5d-113">Struttura esistente da copiare.</span><span class="sxs-lookup"><span data-stu-id="64a5d-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64a5d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64a5d-114">Return value</span></span>

<span data-ttu-id="64a5d-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="64a5d-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="64a5d-116">I valori restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="64a5d-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="64a5d-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="64a5d-117">Return code</span></span>                                                                                   | <span data-ttu-id="64a5d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64a5d-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64a5d-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64a5d-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="64a5d-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="64a5d-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="64a5d-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="64a5d-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="64a5d-122">Uno o più parametri non sono stati specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="64a5d-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="64a5d-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="64a5d-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="64a5d-124">Memoria disponibile insufficiente per completare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="64a5d-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="64a5d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64a5d-125">Requirements</span></span>



| <span data-ttu-id="64a5d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="64a5d-126">Requirement</span></span> | <span data-ttu-id="64a5d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="64a5d-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="64a5d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64a5d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="64a5d-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="64a5d-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="64a5d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64a5d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="64a5d-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="64a5d-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="64a5d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64a5d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="64a5d-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="64a5d-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64a5d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64a5d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a5d-135">**Helper ( \_ attributo)**</span><span class="sxs-lookup"><span data-stu-id="64a5d-135">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





