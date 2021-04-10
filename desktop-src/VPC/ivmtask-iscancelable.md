---
title: Proprietà IVMTask annullabile (VPCCOMInterfaces. h)
description: Determina se l'attività può essere annullata.
ms.assetid: abb8a29a-7f5b-45ba-ae79-d422dfb2f39d
keywords:
- Proprietà annullabile Virtual PC
- Proprietà annullabile Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, proprietà annullabile
topic_type:
- apiref
api_name:
- IVMTask.IsCancelable
- IVMTask.get_IsCancelable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd06db3fc338277d7551233b0d609ceae03f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121095"
---
# <a name="ivmtaskiscancelable-property"></a><span data-ttu-id="c80fa-106">Proprietà IVMTask:: cancelable</span><span class="sxs-lookup"><span data-stu-id="c80fa-106">IVMTask::IsCancelable property</span></span>

<span data-ttu-id="c80fa-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c80fa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c80fa-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c80fa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c80fa-109">Determina se l'attività può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="c80fa-109">Determines whether the task can be canceled.</span></span>

<span data-ttu-id="c80fa-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c80fa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c80fa-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c80fa-111">Syntax</span></span>


```C++
HRESULT get_IsCancelable(
  [out, retval] VARIANT_BOOL *isCancelable
);
```



## <a name="property-value"></a><span data-ttu-id="c80fa-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c80fa-112">Property value</span></span>

<span data-ttu-id="c80fa-113">**True** se l'attività può essere annullata prima del completamento e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c80fa-113">**TRUE** if the task can be canceled before completion and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c80fa-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c80fa-114">Error codes</span></span>



| <span data-ttu-id="c80fa-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="c80fa-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c80fa-116">Significato</span><span class="sxs-lookup"><span data-stu-id="c80fa-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c80fa-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c80fa-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c80fa-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c80fa-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c80fa-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c80fa-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c80fa-120">Il valore del parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="c80fa-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="c80fa-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c80fa-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c80fa-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c80fa-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c80fa-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c80fa-123">Requirements</span></span>



| <span data-ttu-id="c80fa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c80fa-124">Requirement</span></span> | <span data-ttu-id="c80fa-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c80fa-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c80fa-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c80fa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c80fa-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c80fa-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c80fa-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c80fa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c80fa-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c80fa-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c80fa-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c80fa-130">End of client support</span></span><br/>    | <span data-ttu-id="c80fa-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c80fa-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c80fa-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c80fa-132">Product</span></span><br/>                  | <span data-ttu-id="c80fa-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c80fa-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c80fa-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c80fa-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c80fa-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c80fa-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c80fa-136">IID</span><span class="sxs-lookup"><span data-stu-id="c80fa-136">IID</span></span><br/>                      | <span data-ttu-id="c80fa-137">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="c80fa-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="c80fa-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c80fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c80fa-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="c80fa-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

