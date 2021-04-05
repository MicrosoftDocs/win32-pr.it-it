---
title: Proprietà ID IVMTask (VPCCOMInterfaces. h)
description: Recupera un identificatore univoco per questa attività.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- ID proprietà PC virtuale
- ID proprietà Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, proprietà ID
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874373"
---
# <a name="ivmtaskid-property"></a><span data-ttu-id="a774a-106">Proprietà IVMTask:: ID</span><span class="sxs-lookup"><span data-stu-id="a774a-106">IVMTask::ID property</span></span>

<span data-ttu-id="a774a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a774a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a774a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a774a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a774a-109">Recupera un identificatore univoco per questa attività.</span><span class="sxs-lookup"><span data-stu-id="a774a-109">Retrieves a unique identifier for this task.</span></span>

<span data-ttu-id="a774a-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a774a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a774a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a774a-111">Syntax</span></span>


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a><span data-ttu-id="a774a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a774a-112">Property value</span></span>

<span data-ttu-id="a774a-113">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="a774a-113">The unique identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a774a-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a774a-114">Error codes</span></span>



| <span data-ttu-id="a774a-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="a774a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a774a-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a774a-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a774a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a774a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a774a-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a774a-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a774a-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a774a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a774a-120">Il valore del parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="a774a-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="a774a-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a774a-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a774a-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a774a-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a774a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a774a-123">Requirements</span></span>



| <span data-ttu-id="a774a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a774a-124">Requirement</span></span> | <span data-ttu-id="a774a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a774a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a774a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a774a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a774a-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a774a-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a774a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a774a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a774a-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a774a-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a774a-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a774a-130">End of client support</span></span><br/>    | <span data-ttu-id="a774a-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a774a-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a774a-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a774a-132">Product</span></span><br/>                  | <span data-ttu-id="a774a-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a774a-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a774a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a774a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a774a-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a774a-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a774a-136">IID</span><span class="sxs-lookup"><span data-stu-id="a774a-136">IID</span></span><br/>                      | <span data-ttu-id="a774a-137">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="a774a-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="a774a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a774a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a774a-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="a774a-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

