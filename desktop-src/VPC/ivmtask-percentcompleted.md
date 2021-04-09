---
title: Proprietà IVMTask PercentCompleted (VPCCOMInterfaces. h)
description: Recupera la percentuale di completamento dell'attività.
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- Proprietà PercentCompleted Virtual PC
- Proprietà PercentCompleted Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, Proprietà PercentCompleted
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa820adbbde2fc68632da27a9b146bd0e8f40143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743095"
---
# <a name="ivmtaskpercentcompleted-property"></a><span data-ttu-id="fb4d5-106">IVMTask::P proprietà ercentCompleted</span><span class="sxs-lookup"><span data-stu-id="fb4d5-106">IVMTask::PercentCompleted property</span></span>

<span data-ttu-id="fb4d5-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fb4d5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fb4d5-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fb4d5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fb4d5-109">Recupera la percentuale di completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="fb4d5-109">Retrieves the completion percentage of the task.</span></span>

<span data-ttu-id="fb4d5-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fb4d5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4d5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb4d5-111">Syntax</span></span>


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a><span data-ttu-id="fb4d5-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fb4d5-112">Property value</span></span>

<span data-ttu-id="fb4d5-113">Percentuale di completamento corrente.</span><span class="sxs-lookup"><span data-stu-id="fb4d5-113">The current completion percentage.</span></span> <span data-ttu-id="fb4d5-114">Il valore è un numero compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="fb4d5-114">The value is a number between 0 and 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb4d5-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fb4d5-115">Error codes</span></span>



| <span data-ttu-id="fb4d5-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="fb4d5-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="fb4d5-117">Significato</span><span class="sxs-lookup"><span data-stu-id="fb4d5-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fb4d5-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb4d5-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="fb4d5-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fb4d5-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="fb4d5-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fb4d5-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="fb4d5-121">Il valore del parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="fb4d5-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="fb4d5-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fb4d5-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="fb4d5-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="fb4d5-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fb4d5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb4d5-124">Requirements</span></span>



| <span data-ttu-id="fb4d5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb4d5-125">Requirement</span></span> | <span data-ttu-id="fb4d5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fb4d5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4d5-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb4d5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4d5-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fb4d5-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb4d5-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb4d5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4d5-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fb4d5-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fb4d5-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fb4d5-131">End of client support</span></span><br/>    | <span data-ttu-id="fb4d5-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb4d5-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fb4d5-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="fb4d5-133">Product</span></span><br/>                  | <span data-ttu-id="fb4d5-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fb4d5-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fb4d5-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb4d5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb4d5-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb4d5-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fb4d5-137">IID</span><span class="sxs-lookup"><span data-stu-id="fb4d5-137">IID</span></span><br/>                      | <span data-ttu-id="fb4d5-138">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="fb4d5-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="fb4d5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb4d5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4d5-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="fb4d5-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

