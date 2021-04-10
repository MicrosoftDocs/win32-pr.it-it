---
title: Funzione CopyRootCauseInfo (Ndattributils. h)
description: Crea una copia di una struttura RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- CopyRootCauseInfo funzione NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964002"
---
# <a name="copyrootcauseinfo-function"></a><span data-ttu-id="461cd-104">CopyRootCauseInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="461cd-104">CopyRootCauseInfo function</span></span>

<span data-ttu-id="461cd-105">La funzione **CopyRootCauseInfo** crea una copia di una struttura [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="461cd-105">The **CopyRootCauseInfo** function creates a copy of a [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="461cd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="461cd-106">Syntax</span></span>


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="461cd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="461cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="461cd-108">*Dest* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="461cd-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="461cd-109">Tipo: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="461cd-109">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="461cd-110">Struttura da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="461cd-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="461cd-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="461cd-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="461cd-112">Tipo: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="461cd-112">Type: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="461cd-113">Struttura esistente da copiare.</span><span class="sxs-lookup"><span data-stu-id="461cd-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="461cd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="461cd-114">Return value</span></span>

<span data-ttu-id="461cd-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="461cd-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="461cd-116">I valori restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="461cd-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="461cd-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="461cd-117">Return code</span></span>                                                                                   | <span data-ttu-id="461cd-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="461cd-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="461cd-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="461cd-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="461cd-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="461cd-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="461cd-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="461cd-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="461cd-122">Uno o più parametri non sono stati specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="461cd-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="461cd-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="461cd-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="461cd-124">Memoria disponibile insufficiente per completare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="461cd-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="461cd-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="461cd-125">Requirements</span></span>



| <span data-ttu-id="461cd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="461cd-126">Requirement</span></span> | <span data-ttu-id="461cd-127">Valore</span><span class="sxs-lookup"><span data-stu-id="461cd-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="461cd-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="461cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="461cd-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="461cd-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="461cd-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="461cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="461cd-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="461cd-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="461cd-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="461cd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="461cd-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="461cd-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="461cd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="461cd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461cd-135">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="461cd-135">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





