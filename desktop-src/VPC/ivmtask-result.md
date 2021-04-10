---
title: Proprietà Result di IVMTask (VPCCOMInterfaces. h)
description: Recupera il risultato dell'attività.
ms.assetid: 640279ef-94b8-4e8f-88f3-a97cec54c121
keywords:
- Proprietà risultato PC virtuale
- Proprietà Result Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, proprietà Result
topic_type:
- apiref
api_name:
- IVMTask.Result
- IVMTask.get_Result
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4dc36d1529633a850bc10e5c89e8c07147aea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964597"
---
# <a name="ivmtaskresult-property"></a><span data-ttu-id="89c04-106">Proprietà IVMTask:: result</span><span class="sxs-lookup"><span data-stu-id="89c04-106">IVMTask::Result property</span></span>

<span data-ttu-id="89c04-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="89c04-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="89c04-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="89c04-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="89c04-109">Recupera il risultato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="89c04-109">Retrieves the result of the task.</span></span>

<span data-ttu-id="89c04-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="89c04-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c04-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89c04-111">Syntax</span></span>


```C++
HRESULT get_Result(
  [out, retval] VMTaskResult *result
);
```



## <a name="property-value"></a><span data-ttu-id="89c04-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="89c04-112">Property value</span></span>

<span data-ttu-id="89c04-113">Risultato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="89c04-113">The result of the task.</span></span> <span data-ttu-id="89c04-114">Per un elenco di valori, vedere [**VMTaskResult**](vmtaskresult.md).</span><span class="sxs-lookup"><span data-stu-id="89c04-114">For a list of values, see [**VMTaskResult**](vmtaskresult.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="89c04-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="89c04-115">Error codes</span></span>



| <span data-ttu-id="89c04-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="89c04-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="89c04-117">Significato</span><span class="sxs-lookup"><span data-stu-id="89c04-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="89c04-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="89c04-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="89c04-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="89c04-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="89c04-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="89c04-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="89c04-121">Il valore del parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="89c04-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="89c04-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="89c04-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="89c04-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="89c04-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="89c04-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89c04-124">Requirements</span></span>



| <span data-ttu-id="89c04-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="89c04-125">Requirement</span></span> | <span data-ttu-id="89c04-126">Valore</span><span class="sxs-lookup"><span data-stu-id="89c04-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c04-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89c04-127">Minimum supported client</span></span><br/> | <span data-ttu-id="89c04-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="89c04-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89c04-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89c04-129">Minimum supported server</span></span><br/> | <span data-ttu-id="89c04-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="89c04-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="89c04-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="89c04-131">End of client support</span></span><br/>    | <span data-ttu-id="89c04-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89c04-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="89c04-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="89c04-133">Product</span></span><br/>                  | <span data-ttu-id="89c04-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="89c04-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="89c04-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89c04-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="89c04-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="89c04-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="89c04-137">IID</span><span class="sxs-lookup"><span data-stu-id="89c04-137">IID</span></span><br/>                      | <span data-ttu-id="89c04-138">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="89c04-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="89c04-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89c04-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c04-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="89c04-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

