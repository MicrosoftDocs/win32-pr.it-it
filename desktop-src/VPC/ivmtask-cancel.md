---
title: Metodo Cancel IVMTask (VPCCOMInterfaces. h)
description: Annulla l'attività.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Annulla metodo Virtual PC
- Metodo Cancel Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, metodo Cancel
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341233"
---
# <a name="ivmtaskcancel-method"></a><span data-ttu-id="e8d09-106">Metodo IVMTask:: Cancel</span><span class="sxs-lookup"><span data-stu-id="e8d09-106">IVMTask::Cancel method</span></span>

<span data-ttu-id="e8d09-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8d09-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8d09-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e8d09-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8d09-109">Annulla l'attività.</span><span class="sxs-lookup"><span data-stu-id="e8d09-109">Cancels the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d09-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8d09-110">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="e8d09-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8d09-111">Parameters</span></span>

<span data-ttu-id="e8d09-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e8d09-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8d09-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8d09-113">Return value</span></span>

<span data-ttu-id="e8d09-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e8d09-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e8d09-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8d09-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="e8d09-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8d09-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e8d09-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e8d09-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e8d09-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e8d09-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e8d09-119"><dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="e8d09-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="e8d09-120">L'attività non può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="e8d09-120">The task cannot be canceled.</span></span><br/>      |
| <dl> <span data-ttu-id="e8d09-121"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e8d09-121"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e8d09-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e8d09-122">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8d09-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8d09-123">Requirements</span></span>



| <span data-ttu-id="e8d09-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8d09-124">Requirement</span></span> | <span data-ttu-id="e8d09-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e8d09-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d09-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8d09-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d09-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8d09-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8d09-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8d09-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d09-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e8d09-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8d09-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e8d09-130">End of client support</span></span><br/>    | <span data-ttu-id="e8d09-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8d09-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8d09-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e8d09-132">Product</span></span><br/>                  | <span data-ttu-id="e8d09-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8d09-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8d09-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8d09-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8d09-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8d09-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e8d09-136">IID</span><span class="sxs-lookup"><span data-stu-id="e8d09-136">IID</span></span><br/>                      | <span data-ttu-id="e8d09-137">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="e8d09-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="e8d09-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8d09-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8d09-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="e8d09-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

