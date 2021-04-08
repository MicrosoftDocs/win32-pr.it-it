---
title: Proprietà IVMTask ErrorDescription (VPCCOMInterfaces. h)
description: Recupera la descrizione dell'errore localizzata registrata per questa attività.
ms.assetid: 85728775-14b6-4031-9ccd-4c4f8c410705
keywords:
- Proprietà ErrorDescription Virtual PC
- Proprietà ErrorDescription Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, Proprietà ErrorDescription
topic_type:
- apiref
api_name:
- IVMTask.ErrorDescription
- IVMTask.get_ErrorDescription
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5c95eac383d8e071832fdbf7843c01345278c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743098"
---
# <a name="ivmtaskerrordescription-property"></a><span data-ttu-id="cd44f-106">Proprietà IVMTask:: ErrorDescription</span><span class="sxs-lookup"><span data-stu-id="cd44f-106">IVMTask::ErrorDescription property</span></span>

<span data-ttu-id="cd44f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cd44f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cd44f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cd44f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cd44f-109">Recupera la descrizione dell'errore localizzata registrata per questa attività.</span><span class="sxs-lookup"><span data-stu-id="cd44f-109">Retrieves the localized error description recorded for this task.</span></span>

<span data-ttu-id="cd44f-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cd44f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd44f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd44f-111">Syntax</span></span>


```C++
HRESULT get_ErrorDescription(
  [out, retval] BSTR *outErrorDesc
);
```



## <a name="property-value"></a><span data-ttu-id="cd44f-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cd44f-112">Property value</span></span>

<span data-ttu-id="cd44f-113">Descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="cd44f-113">The error description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cd44f-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="cd44f-114">Error codes</span></span>



| <span data-ttu-id="cd44f-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="cd44f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cd44f-116">Significato</span><span class="sxs-lookup"><span data-stu-id="cd44f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cd44f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cd44f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cd44f-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cd44f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="cd44f-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cd44f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cd44f-120">Il valore del parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="cd44f-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="cd44f-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cd44f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cd44f-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="cd44f-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cd44f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd44f-123">Requirements</span></span>



| <span data-ttu-id="cd44f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd44f-124">Requirement</span></span> | <span data-ttu-id="cd44f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cd44f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd44f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd44f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cd44f-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cd44f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd44f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd44f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cd44f-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cd44f-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cd44f-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cd44f-130">End of client support</span></span><br/>    | <span data-ttu-id="cd44f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd44f-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cd44f-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="cd44f-132">Product</span></span><br/>                  | <span data-ttu-id="cd44f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cd44f-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cd44f-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd44f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd44f-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd44f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cd44f-136">IID</span><span class="sxs-lookup"><span data-stu-id="cd44f-136">IID</span></span><br/>                      | <span data-ttu-id="cd44f-137">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="cd44f-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="cd44f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd44f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd44f-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="cd44f-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

